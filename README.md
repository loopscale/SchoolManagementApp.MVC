# SchoolManagementApp.MVC

Useful Commands
---------------
Dotnet watch
Dotnet run


Dotnet add package <package_name>

dotnet tool install --global dotnet-ef

Database first model
---------------------------------
dotnet-ef dbcontext scaffold "Data Source=localhost\SQLEXPRESS;Initial Catalog=SchoolManagementDb;Integrated Security=True;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SQLServer -o Data

Force flag
--------
dotnet-ef dbcontext scaffold "Data Source=localhost\SQLEXPRESS;Initial Catalog=SchoolManagementDb;Integrated Security=True;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SQLServer -o Data -f

Exclude connection username and password
------------------------------------------------------------
dotnet-ef dbcontext scaffold "Data Source=localhost\SQLEXPRESS;Initial Catalog=SchoolManagementDb;Integrated Security=True;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SQLServer -o Data -f ---no-onconfiguring


Scaffold Controller and Views
-------------------------------------
dotnet tool install -g dotnet-aspnet-codegenerator

dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design

FOR MAC/LINUX - export PATH=$HOME/.dotnet/tools:$PATH

dotnet aspnet-codegenerator controller -name CoursesController -m Course -dc SchoolManagementDbContext --relativeFolderPath Controllers --useDefaultLayout --referenceScriptLibraries -f  

dotnet aspnet-codegenerator controller -name LecturersController -m Lecturer -dc SchoolManagementDbContext --relativeFolderPath Controllers --useDefaultLayout --referenceScriptLibraries -f
