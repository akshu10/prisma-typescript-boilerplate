## Create a Prisma Project

The command below does two things:

<ul>
<li> Creates a new directory called <strong>prisma</strong> that contains the Prisma schema with your database connection variable and schema models </li>
<li> Also Creates <strong> .env</strong> in the root directory of the project, which contains environment variables (ie database connection URL)</li>
</ul>

<br>

```
yarn prisma init
```

<br>

### Generate Prisma Artifact

```
yarn generate
```

<br>

### Browse data

Prisma provides a way to explore your data via a UI

```
yarn studio
```

### Pull the DB schema

Pull the schema from an existing database, updating the Prisma schema

```
yarn pull
```

### Push the Prisma schema state to the DB

```
yarn push
```

## Running Migrations

The process for running migrations is as follows:

<ol>
<li> Update the schema.prisma file with your changes to migrate
</li>
<li>
<!-- &lt;migration_name> -->
To create a migration file without applying it run <strong> yarn schema:make &lt;migration_name></strong>
</li>
<li>
Run <strong> yarn migrate:development</strong> to migrate the migration created above.
</li>
</ol>
Running prisma migrate will automatically run the SQL migration file againt the database.

##### Note: 
> Running yarn prisma migrate dev directly applies the migration immediately
