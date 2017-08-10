# takengo_documentation
Take n Go Documentation

Created By
1. Franky Gabriel Sanjaya s3642810
2. Kendrick Kesley s3642811
3. Nadya Safira s3642868
4. Veronica Ong s3642807
5. Yulita Putri Hartoyo s3642813

## Local Machine Configuration

#### Add this on your hosts file (`C:/Windows/System32/drivers/etc/hosts`)
```
127.0.0.1 takengo.dev
127.0.0.1 api.takengo.dev
127.0.0.1 admin.takengo.dev
52.65.96.152 takengo.io
52.65.96.152 api.takengo.io
52.65.96.152 admin.takengo.io
```
#### Add this on your xampp vhosts (`C:\xampp\apache\conf\extra\httpd-vhosts.conf`)
##### NOTE: You need to restart the xampp after applying these changes
```
<VirtualHost takengo.dev:80>
  DocumentRoot "C:\xampp\htdocs\takengo_frontend\public"
  ServerAdmin takengo.dev
  <Directory "C:\xampp\htdocs\takengo_frontend">
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
  </Directory>
</VirtualHost>

<VirtualHost admin.takengo.dev:80>
  DocumentRoot "C:\xampp\htdocs\takengo_admin\public"
  ServerAdmin admin.takengo.dev
  <Directory "C:\xampp\htdocs\takengo_admin">
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
  </Directory>
</VirtualHost>

<VirtualHost api.menudriven.dev:80>
  DocumentRoot "C:\xampp\htdocs\takengo_api\public"
  ServerAdmin api.takengo.dev
  <Directory "C:\xampp\htdocs\takengo_api">
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
  </Directory>
</VirtualHost>
```

  * The first configuration will redirect `takengo.dev`, `admin.takengo.dev`, and `api.takengo.dev` to localhost (`127.0.0.1`).

  * The second configuration will serve the project based on the requested address. Note that `DocumentRoot` and `Directory` must match the project directory. If you clone the project inside the htdocs folder, the above configuration should work. But if you don't use the default method, please change the configuration based on your local machine.
