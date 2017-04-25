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

## Post-Install:
Log into the admin console:

```
http://magento2.dev/admin_plastics
username: magento2
password: Adm1n1
```

The initial setup script will take a few minutes. Once the spiner goes away, dismiss the 'Enable Advanced Reporting' modal by clicking 'Remind me later'

You should be looking at the dashboard page. There will probably be an error message at the top like:

```
One or more indexers are invalid. Make sure your Magento cron job is running.
```

To fix this, on the command line in the magento2 directory, type ```php bin/magento indexer:reindex```

Refresh the Dashboard in the browser window. After a few seconds, you should see another error message at the top:

```
One or more of the Cache Types are invalidated: Page Cache. Please go to Cache Management and refresh cache types.
```

To fix this, on the command line in the magento2 directory, type ```php bin/magento cache:clean```

## Backend Development
When making a change to Magento2 backend code, in order to see your changes live, on the command line in the magento2 directory, type ```php bin/magento setup:di:compile``` which will take a few minutes (~15) to complete. Grab a tasty beverage.

