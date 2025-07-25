#change mysql verison as per your production into the program.cs file :

builder.Services.AddDbContext<InventoryContext>(options =>
    options.UseMySql(
        builder.Configuration.GetConnectionString("dbconn"),
        new MySqlServerVersion(new Version(8, 0, 42)) // <-- use Mysql version here
    ));

# change your user id and password, db host server ip to the appsettings.json file; 

{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft": "Warning",
      "Microsoft.Hosting.Lifetime": "Information"
    }
  },
    "ConnectionStrings": {
        "DbConn": "server=192.168.126.153;database=inventorydb;user=Tipu;password=Tipu@123;"
    },
    "AllowedHosts": "*"
  }
