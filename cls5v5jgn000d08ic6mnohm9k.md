---
title: "A Guide to Installing and Setting Up PostgreSQL on Red Hat"
seoTitle: "A Guide to Installing and Setting Up PostgreSQL on Red Hat"
seoDescription: "Step 1: Update the Package Manager
Step 2: Install PostgreSQL
Step 3: Initialize the Database Cluster
Step 4: Start PostgreSQL Service
Step 5: Enable PG.."
datePublished: Sat Feb 03 2024 09:20:08 GMT+0000 (Coordinated Universal Time)
cuid: cls5v5jgn000d08ic6mnohm9k
slug: a-guide-to-installing-and-setting-up-postgresql-on-red-hat
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1706951879018/2d4cc6e9-21f3-405e-96bc-0d3918b2af35.jpeg
tags: postgresql, databases, sql, redhat

---

PostgreSQL is a powerful and open-source relational database management system that is widely used for handling large-scale databases. In this guide, we will walk through the process of installing and setting up PostgreSQL on a Red Hat-based system, including the essential commands for configuration.

### Installing PostgreSQL on Red Hat:

#### Step 1: Update the Package Manager

Before installing PostgreSQL, it is good practice to ensure that your system is up-to-date. Run the following commands:

```bash
sudo yum update
```

#### Step 2: Install PostgreSQL

Use the following command to install PostgreSQL:

```bash
sudo yum install postgresql-server
```

### Initializing the PostgreSQL Database:

#### Step 3: Initialize the Database Cluster

After installing PostgreSQL, you need to initialize the database cluster. Execute the following command:

```bash
sudo postgresql-setup --initdb
```

#### Step 4: Start PostgreSQL Service

Start the PostgreSQL service with the following command:

```bash
sudo systemctl start postgresql
```

#### Step 5: Enable PostgreSQL to Start on Boot

Ensure PostgreSQL starts automatically on system boot:

```bash
sudo systemctl enable postgresql
```

### Configuring PostgreSQL:

#### Step 6: Edit `pg_hba.conf` for Authentication

Navigate to the PostgreSQL data directory:

```bash
cd /var/lib/pgsql/data
```

Open `pg_hba.conf` for editing:

```bash
nano pg_hba.conf
```

Add the following line to allow password authentication for connections from [localhost](http://localhost):

```bash
host    all             all             127.0.0.1/32            md5
```

Save the file and exit the editor.

#### Step 7: Restart PostgreSQL

To apply the changes made to the configuration, restart PostgreSQL:

```bash
sudo systemctl restart postgresql
```

### Testing the PostgreSQL Installation:

#### Step 8: Access the PostgreSQL Shell

You can now access the PostgreSQL shell to interact with the database:

```bash
sudo -u postgres psql
```

### Conclusion:

Congratulations! You have successfully installed and configured PostgreSQL on your Red Hat-based system. This guide covered the essential steps, from installation to setting up basic configuration files. PostgreSQL is now ready to handle your databases.

Remember that PostgreSQL is a robust and feature-rich database system, and this guide provides only a basic setup. Depending on your requirements, you may need to further configure PostgreSQL, create databases, and manage users. Always refer to the official PostgreSQL documentation for comprehensive information and best practices.