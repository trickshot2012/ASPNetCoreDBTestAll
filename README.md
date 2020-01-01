# ASPNetCoreDBTestAll
ASP.NET Core example using 6 different Database-Provider
//SQL-Server
services.AddDbContext<Context>(options =>
    options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));

//SQLite
services.AddDbContext<Context>(options =>
    options.UseSqlite(Configuration.GetConnectionString("DefaultConnection")));

//MariaDB 
services.AddDbContext<Context>(options =>
  options.UseMySql(Configuration.GetConnectionString("DefaultConnection")));

//MySQL
services.AddDbContext<Context>(options =>
 options.UseMySql(Configuration.GetConnectionString("DefaultConnection")));

//Postgres
services.AddDbContext<Context>(options =>
options.UseNpgsql(Configuration.GetConnectionString("DefaultConnection")));

//MongoDB
services.Configure<BookstoreDatabaseSettings>(
Configuration.GetSection(nameof(BookstoreDatabaseSettings)));
