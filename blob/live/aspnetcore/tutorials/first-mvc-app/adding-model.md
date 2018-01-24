---
title: "将模型添加到 ASP.NET Core MVC 应用"
author: rick-anderson
description: "将模型添加到简单的 ASP.NET Core 应用。"
ms.author: riande
manager: wpickett
ms.date: 12/8/2017
ms.topic: get-started-article
ms.technology: aspnet
ms.prod: asp.net-core
uid: tutorials/first-mvc-app/adding-model
ms.openlocfilehash: c2cd3cc81221c146dec70e487a17b33360eb6112
ms.sourcegitcommit: 3e303620a125325bb9abd4b2d315c106fb8c47fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2018
---
[!INCLUDE[adding-model](../../includes/mvc-intro/adding-model1.md)]

<span data-ttu-id="d14c0-103">请注意：ASP.NET Core 2.0 模板包含 Models 文件夹。</span><span class="sxs-lookup"><span data-stu-id="d14c0-103">Note: The ASP.NET Core 2.0 templates contain the *Models* folder.</span></span>

<span data-ttu-id="d14c0-104">右键单击 Models 文件夹，然后单击“添加” > “类”。</span><span class="sxs-lookup"><span data-stu-id="d14c0-104">Right-click the *Models* folder > **Add** > **Class**.</span></span> <span data-ttu-id="d14c0-105">将类命名为“Movie”，并添加以下属性：</span><span class="sxs-lookup"><span data-stu-id="d14c0-105">Name the class **Movie** and add the following properties:</span></span>

[!code-csharp[Main](../../tutorials/first-mvc-app/start-mvc/sample/MvcMovie/Models/MovieNoEF.cs?name=snippet_1)]

<span data-ttu-id="d14c0-106">数据库需要 `ID` 字段以获取主键。</span><span class="sxs-lookup"><span data-stu-id="d14c0-106">The `ID` field is required by the database for the primary key.</span></span> 

<span data-ttu-id="d14c0-107">生成项目以验证有没有任何错误存在。</span><span class="sxs-lookup"><span data-stu-id="d14c0-107">Build the project to verify you don't have any errors.</span></span> <span data-ttu-id="d14c0-108">现在 MVC 应用中已具有模型。</span><span class="sxs-lookup"><span data-stu-id="d14c0-108">You now have a **M**odel in your **M**VC app.</span></span>

## <a name="scaffolding-a-controller"></a><span data-ttu-id="d14c0-109">搭建控制器基架</span><span class="sxs-lookup"><span data-stu-id="d14c0-109">Scaffolding a controller</span></span>

<span data-ttu-id="d14c0-110">在“解决方案资源管理器”中，右键单击“控制器”文件夹，然后单击“添加”>“控制器”。</span><span class="sxs-lookup"><span data-stu-id="d14c0-110">In **Solution Explorer**, right-click the *Controllers* folder **> Add > Controller**.</span></span>

![上述步骤的视图](adding-model/_static/add_controller.png)

<span data-ttu-id="d14c0-112">如果出现“添加 MVC 依赖项”对话框：</span><span class="sxs-lookup"><span data-stu-id="d14c0-112">If the **Add MVC Dependencies** dialog appears:</span></span>

* <span data-ttu-id="d14c0-113">[将 Visual Studio 更新到最新版本](https://www.visualstudio.com/downloads/)。</span><span class="sxs-lookup"><span data-stu-id="d14c0-113">[Update Visual Studio to the latest version](https://www.visualstudio.com/downloads/).</span></span> <span data-ttu-id="d14c0-114">15.5 之前的 Visual Studio 版本显示此对话框。</span><span class="sxs-lookup"><span data-stu-id="d14c0-114">Visual Studio versions prior to 15.5 show this dialog.</span></span>
* <span data-ttu-id="d14c0-115">如果无法更新，请选择“添加”，然后再次按照添加控制器步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d14c0-115">If you can't update, select **ADD**, and then follow the add controller steps again.</span></span>

<span data-ttu-id="d14c0-116">在“添加基架”对话框中，点击“包含视图的 MVC 控制器(使用 Entity Framework)”>“添加”。</span><span class="sxs-lookup"><span data-stu-id="d14c0-116">In the **Add Scaffold** dialog, tap **MVC Controller with views, using Entity Framework > Add**.</span></span>

![“添加基架”对话框](adding-model/_static/add_scaffold2.png)

<span data-ttu-id="d14c0-118">填写“添加控制器”对话框：</span><span class="sxs-lookup"><span data-stu-id="d14c0-118">Complete the **Add Controller** dialog:</span></span>

* <span data-ttu-id="d14c0-119">模型类：Movie（MvcMovie.Models）</span><span class="sxs-lookup"><span data-stu-id="d14c0-119">**Model class:** *Movie (MvcMovie.Models)*</span></span>
* <span data-ttu-id="d14c0-120">数据上下文类：选择 + 图标并添加默认的 MvcMovie.Models.MvcMovieContext </span><span class="sxs-lookup"><span data-stu-id="d14c0-120">**Data context class:** Select the **+** icon and add the default **MvcMovie.Models.MvcMovieContext**</span></span>

![“添加数据”上下文](adding-model/_static/dc.png)

* <span data-ttu-id="d14c0-122">视图：将每个选项保持为默认选中状态</span><span class="sxs-lookup"><span data-stu-id="d14c0-122">**Views:** Keep the default of each option checked</span></span>
* <span data-ttu-id="d14c0-123">控制器名称：保留默认的 MoviesController</span><span class="sxs-lookup"><span data-stu-id="d14c0-123">**Controller name:** Keep the default *MoviesController*</span></span>
* <span data-ttu-id="d14c0-124">点击“添加”</span><span class="sxs-lookup"><span data-stu-id="d14c0-124">Tap **Add**</span></span>

![“添加控制器”对话框](adding-model/_static/add_controller2.png)

<span data-ttu-id="d14c0-126">Visual Studio 将创建：</span><span class="sxs-lookup"><span data-stu-id="d14c0-126">Visual Studio creates:</span></span>

* <span data-ttu-id="d14c0-127">Entity Framework Core [数据库上下文类](xref:data/ef-mvc/intro#create-the-database-context) (Data/MvcMovieContext.cs)</span><span class="sxs-lookup"><span data-stu-id="d14c0-127">An Entity Framework Core [database context class](xref:data/ef-mvc/intro#create-the-database-context) (*Data/MvcMovieContext.cs*)</span></span>
* <span data-ttu-id="d14c0-128">电影控制器 (Controllers/MoviesController.cs)</span><span class="sxs-lookup"><span data-stu-id="d14c0-128">A movies controller (*Controllers/MoviesController.cs*)</span></span>
* <span data-ttu-id="d14c0-129">“创建”、“删除”、“详细信息”、“编辑”和“索引”页面的 Razor 视图文件 (Views/Movies/&ast;.cshtml)</span><span class="sxs-lookup"><span data-stu-id="d14c0-129">Razor view files for Create, Delete, Details, Edit, and Index pages (*Views/Movies/&ast;.cshtml*)</span></span>

<span data-ttu-id="d14c0-130">自动创建数据库上下文和 [CRUD](https://wikipedia.org/wiki/Create,_read,_update_and_delete)（创建、读取、更新和删除）操作方法和视图的过程称为“搭建基架”。</span><span class="sxs-lookup"><span data-stu-id="d14c0-130">The automatic creation of the database context and [CRUD](https://wikipedia.org/wiki/Create,_read,_update_and_delete) (create, read, update, and delete) action methods and views is known as *scaffolding*.</span></span> <span data-ttu-id="d14c0-131">你很快将具有功能完整的 Web 应用程序，可使用此应用程序管理电影数据库。</span><span class="sxs-lookup"><span data-stu-id="d14c0-131">You'll soon have a fully functional web application that lets you manage a movie database.</span></span>

<span data-ttu-id="d14c0-132">如果运行应用并单击“Mvc 电影”链接，则会出现以下类似的错误：</span><span class="sxs-lookup"><span data-stu-id="d14c0-132">If you run the app and click on the **Mvc Movie** link, you get an error similar to the following:</span></span>

```
An unhandled exception occurred while processing the request.

SqlException: Cannot open database "MvcMovieContext-<GUID removed>" requested by the login. The login failed.
Login failed for user 'Rick'.

System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString 
```

<span data-ttu-id="d14c0-133">你需要创建数据库，并且使用 EF Core [迁移](xref:data/ef-mvc/migrations)功能来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="d14c0-133">You need to create the database, and you'll use the EF Core [Migrations](xref:data/ef-mvc/migrations) feature to do that.</span></span> <span data-ttu-id="d14c0-134">通过迁移可创建与数据模型匹配的数据库，并在数据模型更改时更新数据库架构。</span><span class="sxs-lookup"><span data-stu-id="d14c0-134">Migrations lets you create a database that matches your data model and update the database schema when your data model changes.</span></span>

## <a name="add-ef-tooling-and-perform-initial-migration"></a><span data-ttu-id="d14c0-135">添加 EF 工具并执行初始迁移</span><span class="sxs-lookup"><span data-stu-id="d14c0-135">Add EF tooling and perform initial migration</span></span>

<span data-ttu-id="d14c0-136">在本部分中，将使用包管理器控制台 (PMC) 执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="d14c0-136">In this section you'll use the Package Manager Console (PMC) to:</span></span>

* <span data-ttu-id="d14c0-137">添加 Entity Framework Core 工具包。</span><span class="sxs-lookup"><span data-stu-id="d14c0-137">Add the Entity Framework Core Tools package.</span></span> <span data-ttu-id="d14c0-138">添加迁移并更新数据库需要此工具包。</span><span class="sxs-lookup"><span data-stu-id="d14c0-138">This package is required to add migrations and update the database.</span></span>
* <span data-ttu-id="d14c0-139">添加初始迁移。</span><span class="sxs-lookup"><span data-stu-id="d14c0-139">Add an initial migration.</span></span>
* <span data-ttu-id="d14c0-140">使用初始迁移来更新数据库。</span><span class="sxs-lookup"><span data-stu-id="d14c0-140">Update the database with the initial migration.</span></span>

<span data-ttu-id="d14c0-141">从“工具”菜单中，选择“NuGet 包管理器”>“程序包管理器控制台”。</span><span class="sxs-lookup"><span data-stu-id="d14c0-141">From the **Tools** menu, select **NuGet Package Manager > Package Manager Console**.</span></span>

<!-- following image shared with uid: tutorials/razor-pages/model -->
  ![PMC 菜单](adding-model/_static/pmc.png)

<span data-ttu-id="d14c0-143">在 PMC 中，输入以下命令：</span><span class="sxs-lookup"><span data-stu-id="d14c0-143">In the PMC, enter the following commands:</span></span>

``` PMC
Install-Package Microsoft.EntityFrameworkCore.Tools
Add-Migration Initial
Update-Database
```

<span data-ttu-id="d14c0-144">请注意：如果在使用 `Install-Package` 命令时收到错误，请打开 NuGet 包管理器并搜索 `Microsoft.EntityFrameworkCore.Tools` 包。</span><span class="sxs-lookup"><span data-stu-id="d14c0-144">**Note:** If you receive an error with the `Install-Package` command, open NuGet Package Manager and search for the `Microsoft.EntityFrameworkCore.Tools` package.</span></span> <span data-ttu-id="d14c0-145">通过此操作，可以安装包或检查是否已安装包。</span><span class="sxs-lookup"><span data-stu-id="d14c0-145">This allows you to install the package or check if it is already installed.</span></span> <span data-ttu-id="d14c0-146">或者，如果 PMC 存在任何问题，请参阅 [CLI 方法](#cli)。</span><span class="sxs-lookup"><span data-stu-id="d14c0-146">Alternatively, see the [CLI approach](#cli) if you have problems with the PMC.</span></span>

<span data-ttu-id="d14c0-147">`Add-Migration` 命令创建代码以创建初始数据库架构。</span><span class="sxs-lookup"><span data-stu-id="d14c0-147">The `Add-Migration` command creates code to create the initial database schema.</span></span> <span data-ttu-id="d14c0-148">此架构基于（Data/MvcMovieContext.cs 文件中的）`DbContext` 中指定的模型。</span><span class="sxs-lookup"><span data-stu-id="d14c0-148">The schema is based on the model specified in the `DbContext`(In the *Data/MvcMovieContext.cs* file).</span></span> <span data-ttu-id="d14c0-149">`Initial` 参数用于为迁移命名。</span><span class="sxs-lookup"><span data-stu-id="d14c0-149">The `Initial` argument is used to name the migrations.</span></span> <span data-ttu-id="d14c0-150">可以使用任意名称，但是按照惯例应选择描述迁移的名称。</span><span class="sxs-lookup"><span data-stu-id="d14c0-150">You can use any name, but by convention you choose a name that describes the migration.</span></span> <span data-ttu-id="d14c0-151">有关详细信息，请参阅[迁移简介](xref:data/ef-mvc/migrations#introduction-to-migrations)。</span><span class="sxs-lookup"><span data-stu-id="d14c0-151">See [Introduction to migrations](xref:data/ef-mvc/migrations#introduction-to-migrations) for more information.</span></span>

<span data-ttu-id="d14c0-152">`Update-Database` 命令在用于创建数据库的 Migrations/\<time-stamp>_Initial.cs 文件中运行 `Up` 方法。</span><span class="sxs-lookup"><span data-stu-id="d14c0-152">The `Update-Database` command runs the `Up` method in the *Migrations/\<time-stamp>_Initial.cs* file, which creates the database.</span></span>

<a name="cli"></a> <span data-ttu-id="d14c0-153">还可以使用命令行接口 (CLI) 来执行前面的步骤，而不使用 PMC：</span><span class="sxs-lookup"><span data-stu-id="d14c0-153">You can perform the preceeding steps using the command-line interface (CLI) rather than the PMC:</span></span>

* <span data-ttu-id="d14c0-154">将 [EF Core 工具](xref:data/ef-mvc/migrations#entity-framework-core-nuget-packages-for-migrations)添加到 .csproj 文件。</span><span class="sxs-lookup"><span data-stu-id="d14c0-154">Add [EF Core tooling](xref:data/ef-mvc/migrations#entity-framework-core-nuget-packages-for-migrations) to the *.csproj* file.</span></span>
* <span data-ttu-id="d14c0-155">从控制台（在项目目录中）运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="d14c0-155">Run the following commands from the console (in the project directory):</span></span>

  ```console
  dotnet ef migrations add Initial
  dotnet ef database update
  ```     
  

[!INCLUDE[adding-model](../../includes/mvc-intro/adding-model3.md)]

[!code-csharp[Main](../../tutorials/first-mvc-app/start-mvc/sample/MvcMovie/Startup.cs?name=ConfigureServices&highlight=6-7)]

[!INCLUDE[adding-model](../../includes/mvc-intro/adding-model4.md)]

![Model 项上的 Intellisense 上下文菜单，列出了 ID、价格、发布日期和标题的可用属性](adding-model/_static/ints.png)

## <a name="additional-resources"></a><span data-ttu-id="d14c0-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="d14c0-157">Additional resources</span></span>

* [<span data-ttu-id="d14c0-158">标记帮助程序</span><span class="sxs-lookup"><span data-stu-id="d14c0-158">Tag Helpers</span></span>](xref:mvc/views/tag-helpers/intro)
* [<span data-ttu-id="d14c0-159">全球化和本地化</span><span class="sxs-lookup"><span data-stu-id="d14c0-159">Globalization and localization</span></span>](xref:fundamentals/localization)

>[!div class="step-by-step"]
<span data-ttu-id="d14c0-160">[上一篇：添加视图](adding-view.md)
[下一篇：使用 SQL](working-with-sql.md)</span><span class="sxs-lookup"><span data-stu-id="d14c0-160">[Previous Adding a View](adding-view.md)
[Next Working with SQL](working-with-sql.md)</span></span>  