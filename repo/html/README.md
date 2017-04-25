# Installing Magento2 from the GIT repo

Inside the Vagrant environment:

```
cd /var/www/html/
rm -rf magento2
git clone https://github.com/magento/magento2.git
cd magento2
composer install

```
Navigate to ```http://magento2.dev/setup``` to complete the Magento2 setup using the Web Wizard:

## Step 2: Add a Database

```
Database Server Host: localhost
Database Server Username: magento2
Database Server Password: 123
Database Name: magento2_magento
Table prefix: (optional) # Leave blank
```
## Step 3: Web Configuration

```
Your Store Address: http://magento2.dev/
Magento Admin Address: http://magento2.dev/admin_plastics
```

## Step 4: Customize Your Store

```
Store Default Time Zone: Central Standard Time (America/Chicago)
Store Default Currency: USD
Store Default Language: English (United States)
```
## Step 5: Create Admin Account

```
New Username: magento2
New Email: <your.email>@irishtitan.com
New Password: Adm1n1
Confirm Password: Adm1n1
```

## Step 6: Install
Click the `Install` button