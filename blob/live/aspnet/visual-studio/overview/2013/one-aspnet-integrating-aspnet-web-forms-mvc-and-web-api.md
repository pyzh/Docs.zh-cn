---
uid: visual-studio/overview/2013/one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api
title: "动手实验： 一个 ASP.NET： 集成 ASP.NET Web 窗体、 MVC 和 Web API |Microsoft 文档"
author: rick-anderson
description: "ASP.NET 是一个框架，用于生成 Web 站点、 应用程序和服务使用专用的技术，如 MVC、 Web API 及其他。 与 ASP.NET h 的扩展..."
ms.author: aspnetcontent
manager: wpickett
ms.date: 07/16/2014
ms.topic: article
ms.assetid: 4fe2558d-67cc-4d12-a5c1-6fb9f6f16137
ms.technology: 
ms.prod: .net-framework
msc.legacyurl: /visual-studio/overview/2013/one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api
msc.type: authoredcontent
ms.openlocfilehash: 55109723e566a9f7c66c1a59414377b05dbec760
ms.sourcegitcommit: 9a9483aceb34591c97451997036a9120c3fe2baf
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2017
---
<a name="hands-on-lab-one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api"></a><span data-ttu-id="ec86b-104">动手实验： 一个 ASP.NET： 将 ASP.NET Web 窗体、 MVC 和 Web API 集成</span><span class="sxs-lookup"><span data-stu-id="ec86b-104">Hands On Lab: One ASP.NET: Integrating ASP.NET Web Forms, MVC and Web API</span></span>
====================
<span data-ttu-id="ec86b-105">通过[Web 营地团队](https://twitter.com/webcamps)</span><span class="sxs-lookup"><span data-stu-id="ec86b-105">by [Web Camps Team](https://twitter.com/webcamps)</span></span>

[<span data-ttu-id="ec86b-106">下载 Web 营地培训工具包</span><span class="sxs-lookup"><span data-stu-id="ec86b-106">Download Web Camps Training Kit</span></span>](http://aka.ms/webcamps-training-kit)

> <span data-ttu-id="ec86b-107">ASP.NET 是一个框架，用于生成 Web 站点、 应用程序和服务使用专用的技术，如 MVC、 Web API 及其他。</span><span class="sxs-lookup"><span data-stu-id="ec86b-107">ASP.NET is a framework for building Web sites, apps and services using specialized technologies such as MVC, Web API and others.</span></span> <span data-ttu-id="ec86b-108">ASP.NET 其创建后看到与的扩展和表示需要具有集成这些技术，在向工作了新的工作**一个 ASP.NET**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-108">With the expansion ASP.NET has seen since its creation and the expressed need to have these technologies integrated, there have been recent efforts in working towards **One ASP.NET**.</span></span>
> 
> <span data-ttu-id="ec86b-109">Visual Studio 2013 引入了新的统一的项目系统，这样就可以生成应用程序，并使用一个项目中的所有 ASP.NET 技术。</span><span class="sxs-lookup"><span data-stu-id="ec86b-109">Visual Studio 2013 introduces a new unified project system which lets you build an application and use all the ASP.NET technologies in one project.</span></span> <span data-ttu-id="ec86b-110">此功能消除了需要在开始时的项目和它，坚持选择一种技术，并改为鼓励使用一个项目中的多个 ASP.NET 框架。</span><span class="sxs-lookup"><span data-stu-id="ec86b-110">This feature eliminates the need to pick one technology at the start of a project and stick with it, and instead encourages the use of multiple ASP.NET frameworks within one project.</span></span>
> 
> <span data-ttu-id="ec86b-111">在 Web 营地培训工具包中，在包括所有的示例代码和代码段[http://aka.ms/webcamps-training-kit](http://aka.ms/webcamps-training-kit)。</span><span class="sxs-lookup"><span data-stu-id="ec86b-111">All sample code and snippets are included in the Web Camps Training Kit, available at [http://aka.ms/webcamps-training-kit](http://aka.ms/webcamps-training-kit).</span></span>


<a id="Overview"></a>
## <a name="overview"></a><span data-ttu-id="ec86b-112">概述</span><span class="sxs-lookup"><span data-stu-id="ec86b-112">Overview</span></span>

<a id="Objectives"></a>
### <a name="objectives"></a><span data-ttu-id="ec86b-113">目标</span><span class="sxs-lookup"><span data-stu-id="ec86b-113">Objectives</span></span>

<span data-ttu-id="ec86b-114">在此动手实验中，你将了解如何：</span><span class="sxs-lookup"><span data-stu-id="ec86b-114">In this hands-on lab, you will learn how to:</span></span>

- <span data-ttu-id="ec86b-115">创建基于网站**一个 ASP.NET**项目类型</span><span class="sxs-lookup"><span data-stu-id="ec86b-115">Create a Web site based on the **One ASP.NET** project type</span></span>
- <span data-ttu-id="ec86b-116">使用不同**ASP.NET**框架喜欢**MVC**和**Web API**同一项目中</span><span class="sxs-lookup"><span data-stu-id="ec86b-116">Use different **ASP.NET** frameworks like **MVC** and **Web API** in the same project</span></span>
- <span data-ttu-id="ec86b-117">标识的主要组件**ASP.NET**应用程序</span><span class="sxs-lookup"><span data-stu-id="ec86b-117">Identify the main components of an **ASP.NET** application</span></span>
- <span data-ttu-id="ec86b-118">利用**ASP.NET 基架**framework 框架来自动创建控制器和视图，以执行 CRUD 操作根据模型类</span><span class="sxs-lookup"><span data-stu-id="ec86b-118">Take advantage of the **ASP.NET Scaffolding** framework to automatically create Controllers and Views to perform CRUD operations based on your model classes</span></span>
- <span data-ttu-id="ec86b-119">公开相同的信息的计算机和可读的格式为每个作业使用的正确工具集</span><span class="sxs-lookup"><span data-stu-id="ec86b-119">Expose the same set of information in machine- and human-readable formats using the right tool for each job</span></span>

<a id="Prerequisites"></a>
### <a name="prerequisites"></a><span data-ttu-id="ec86b-120">先决条件</span><span class="sxs-lookup"><span data-stu-id="ec86b-120">Prerequisites</span></span>

<span data-ttu-id="ec86b-121">完成本动手实验需要以下：</span><span class="sxs-lookup"><span data-stu-id="ec86b-121">The following is required to complete this hands-on lab:</span></span>

- <span data-ttu-id="ec86b-122">[Visual Studio Express 2013 for Web](https://www.microsoft.com/visualstudio/)或更高版本</span><span class="sxs-lookup"><span data-stu-id="ec86b-122">[Visual Studio Express 2013 for Web](https://www.microsoft.com/visualstudio/) or greater</span></span>
- [<span data-ttu-id="ec86b-123">Visual Studio 2013 Update 1</span><span class="sxs-lookup"><span data-stu-id="ec86b-123">Visual Studio 2013 Update 1</span></span>](https://go.microsoft.com/fwlink/?LinkId=301714)

<a id="Setup"></a>
### <a name="setup"></a><span data-ttu-id="ec86b-124">安装</span><span class="sxs-lookup"><span data-stu-id="ec86b-124">Setup</span></span>

<span data-ttu-id="ec86b-125">若要运行本动手实验中的练习，你将需要先设置你的环境。</span><span class="sxs-lookup"><span data-stu-id="ec86b-125">In order to run the exercises in this hands-on lab, you will need to set up your environment first.</span></span>

1. <span data-ttu-id="ec86b-126">打开 Windows 资源管理器并浏览到本实验的**源**文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec86b-126">Open Windows Explorer and browse to the lab's **Source** folder.</span></span>
2. <span data-ttu-id="ec86b-127">右键单击**Setup.cmd**和选择**以管理员身份运行**以启动安装过程将配置您的环境并安装本实验的 Visual Studio 代码段。</span><span class="sxs-lookup"><span data-stu-id="ec86b-127">Right-click on **Setup.cmd** and select **Run as administrator** to launch the setup process that will configure your environment and install the Visual Studio code snippets for this lab.</span></span>
3. <span data-ttu-id="ec86b-128">如果显示用户帐户控制对话框中，确认操作以继续。</span><span class="sxs-lookup"><span data-stu-id="ec86b-128">If the User Account Control dialog box is shown, confirm the action to proceed.</span></span>

> [!NOTE]
> <span data-ttu-id="ec86b-129">请确保您已在运行安装程序之前检查本实验的所有依赖项。</span><span class="sxs-lookup"><span data-stu-id="ec86b-129">Make sure you have checked all the dependencies for this lab before running the setup.</span></span>


<a id="CodeSnippets"></a>
### <a name="using-the-code-snippets"></a><span data-ttu-id="ec86b-130">使用代码片段</span><span class="sxs-lookup"><span data-stu-id="ec86b-130">Using the Code Snippets</span></span>

<span data-ttu-id="ec86b-131">在整个实验文档中，你将指示要插入代码块。</span><span class="sxs-lookup"><span data-stu-id="ec86b-131">Throughout the lab document, you will be instructed to insert code blocks.</span></span> <span data-ttu-id="ec86b-132">为方便起见，大多数的此代码提供作为 Visual Studio 代码段，你可以从访问在 Visual Studio 2013，为了避免必须手动添加它。</span><span class="sxs-lookup"><span data-stu-id="ec86b-132">For your convenience, most of this code is provided as Visual Studio Code Snippets, which you can access from within Visual Studio 2013 to avoid having to add it manually.</span></span>

> [!NOTE]
> <span data-ttu-id="ec86b-133">每个练习均附带的开始解决方案位于**开始**本练习，您可以完成相互独立地每个练习的文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec86b-133">Each exercise is accompanied by a starting solution located in the **Begin** folder of the exercise that allows you to follow each exercise independently of the others.</span></span> <span data-ttu-id="ec86b-134">请注意在练习过程中添加的代码段缺少这些开始解决方案中，并且可能不工作，直到完成练习。</span><span class="sxs-lookup"><span data-stu-id="ec86b-134">Please be aware that the code snippets that are added during an exercise are missing from these starting solutions and may not work until you have completed the exercise.</span></span> <span data-ttu-id="ec86b-135">在练习的源代码，你将找到**结束**包含具有完成相应练习中的步骤得到的代码的 Visual Studio 解决方案文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec86b-135">Inside the source code for an exercise, you will also find an **End** folder containing a Visual Studio solution with the code that results from completing the steps in the corresponding exercise.</span></span> <span data-ttu-id="ec86b-136">如果您在演练本动手实验需要其他帮助，你可以使用这些解决方案作为指南。</span><span class="sxs-lookup"><span data-stu-id="ec86b-136">You can use these solutions as guidance if you need additional help as you work through this hands-on lab.</span></span>


* * *

<a id="Exercises"></a>
## <a name="exercises"></a><span data-ttu-id="ec86b-137">练习</span><span class="sxs-lookup"><span data-stu-id="ec86b-137">Exercises</span></span>

<span data-ttu-id="ec86b-138">本动手实验包括以下练习：</span><span class="sxs-lookup"><span data-stu-id="ec86b-138">This hands-on lab includes the following exercises:</span></span>

1. [<span data-ttu-id="ec86b-139">创建一个新的 Web 窗体项目</span><span class="sxs-lookup"><span data-stu-id="ec86b-139">Creating a New Web Forms Project</span></span>](#Exercise1)
2. [<span data-ttu-id="ec86b-140">创建使用基架 MVC 控制器</span><span class="sxs-lookup"><span data-stu-id="ec86b-140">Creating an MVC Controller Using Scaffolding</span></span>](#Exercise2)
3. [<span data-ttu-id="ec86b-141">创建使用基架 Web API 控制器</span><span class="sxs-lookup"><span data-stu-id="ec86b-141">Creating a Web API Controller Using Scaffolding</span></span>](#Exercise3)

<span data-ttu-id="ec86b-142">估计时间来完成该实验： **60 分钟**</span><span class="sxs-lookup"><span data-stu-id="ec86b-142">Estimated time to complete this lab: **60 minutes**</span></span>

> [!NOTE]
> <span data-ttu-id="ec86b-143">当你首次启动 Visual Studio 时，你必须选择一个预定义的设置集合。</span><span class="sxs-lookup"><span data-stu-id="ec86b-143">When you first start Visual Studio, you must select one of the predefined settings collections.</span></span> <span data-ttu-id="ec86b-144">每个预定义的集合用于匹配特定的开发风格和确定窗口布局、 编辑器行为、 IntelliSense 代码段和对话框选项。</span><span class="sxs-lookup"><span data-stu-id="ec86b-144">Each predefined collection is designed to match a particular development style and determines window layouts, editor behavior, IntelliSense code snippets, and dialog box options.</span></span> <span data-ttu-id="ec86b-145">在本实验中的过程描述完成给定的任务 Visual Studio 中使用时所需的操作**常规开发设置**集合。</span><span class="sxs-lookup"><span data-stu-id="ec86b-145">The procedures in this lab describe the actions necessary to accomplish a given task in Visual Studio when using the **General Development Settings** collection.</span></span> <span data-ttu-id="ec86b-146">如果您为开发环境选择不同的设置集合，则表明可能存在你应考虑到帐户的步骤中的差异。</span><span class="sxs-lookup"><span data-stu-id="ec86b-146">If you choose a different settings collection for your development environment, there may be differences in the steps that you should take into account.</span></span>


<a id="Exercise1"></a>
### <a name="exercise-1-creating-a-new-web-forms-project"></a><span data-ttu-id="ec86b-147">练习 1： 创建新的 Web 窗体项目</span><span class="sxs-lookup"><span data-stu-id="ec86b-147">Exercise 1: Creating a New Web Forms Project</span></span>

<span data-ttu-id="ec86b-148">在本练习中，你将创建在 Visual Studio 2013 中使用新的 Web 窗体站点**一个 ASP.NET**统一项目体验，您便可轻松地集成在同一应用程序的 Web 窗体、 MVC 和 Web API 的组件。</span><span class="sxs-lookup"><span data-stu-id="ec86b-148">In this exercise you will create a new Web Forms site in Visual Studio 2013 using the **One ASP.NET** unified project experience, which will allow you to easily integrate Web Forms, MVC and Web API components in the same application.</span></span> <span data-ttu-id="ec86b-149">然后将浏览生成的解决方案，并识别其部分，你将在最后看到操作中的 Web 站点。</span><span class="sxs-lookup"><span data-stu-id="ec86b-149">You will then explore the generated solution and identify its parts, and finally you will see the Web site in action.</span></span>

<a id="Ex1Task1"></a>
#### <a name="task-1--creating-a-new-site-using-the-one-aspnet-experience"></a><span data-ttu-id="ec86b-150">任务 1 – 创建新站点使用一个 ASP.NET 体验</span><span class="sxs-lookup"><span data-stu-id="ec86b-150">Task 1 – Creating a New Site Using the One ASP.NET Experience</span></span>

<span data-ttu-id="ec86b-151">在此任务中，您将开始在 Visual Studio 中创建新的 Web 站点基于**一个 ASP.NET**项目类型。</span><span class="sxs-lookup"><span data-stu-id="ec86b-151">In this task you will start creating a new Web site in Visual Studio based on the **One ASP.NET** project type.</span></span> <span data-ttu-id="ec86b-152">**一个 ASP.NET**统一所有 ASP.NET 技术和为你提供混合并将根据需要对其进行匹配的选项。</span><span class="sxs-lookup"><span data-stu-id="ec86b-152">**One ASP.NET** unifies all ASP.NET technologies and gives you the option to mix and match them as desired.</span></span> <span data-ttu-id="ec86b-153">然后将应用程序中并排识别实时 Web 窗体、 MVC 和 Web API 的不同组件。</span><span class="sxs-lookup"><span data-stu-id="ec86b-153">You will then recognize the different components of Web Forms, MVC and Web API that live side by side within your application.</span></span>

1. <span data-ttu-id="ec86b-154">打开**Visual Studio Express 2013 for Web**和选择**文件 |新建项目...**启动一个新的解决方案。</span><span class="sxs-lookup"><span data-stu-id="ec86b-154">Open **Visual Studio Express 2013 for Web** and select **File | New Project...** to start a new solution.</span></span>

    ![创建新项目](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image1.png)

    <span data-ttu-id="ec86b-156">*创建新项目*</span><span class="sxs-lookup"><span data-stu-id="ec86b-156">*Creating a New Project*</span></span>
2. <span data-ttu-id="ec86b-157">在**新项目**对话框中，选择**ASP.NET Web 应用程序**下**Visual C# |Web**选项卡，并确保**.NET Framework 4.5**选择。</span><span class="sxs-lookup"><span data-stu-id="ec86b-157">In the **New Project** dialog box, select **ASP.NET Web Application** under the **Visual C# | Web** tab, and make sure **.NET Framework 4.5** is selected.</span></span> <span data-ttu-id="ec86b-158">将项目*MyHybridSite*，选择**位置**单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-158">Name the project *MyHybridSite*, choose a **Location** and click **OK**.</span></span>

    ![新的 ASP.NET Web 应用程序项目](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image2.png)

    <span data-ttu-id="ec86b-160">*创建新的 ASP.NET Web 应用程序项目*</span><span class="sxs-lookup"><span data-stu-id="ec86b-160">*Creating a new ASP.NET Web Application project*</span></span>
3. <span data-ttu-id="ec86b-161">在**新建 ASP.NET 项目**对话框中，选择**Web 窗体**模板，然后选择**MVC**和**Web API**选项。</span><span class="sxs-lookup"><span data-stu-id="ec86b-161">In the **New ASP.NET Project** dialog box, select the **Web Forms** template and select the **MVC** and **Web API** options.</span></span> <span data-ttu-id="ec86b-162">此外，请确保**身份验证**选项设置为**单个用户帐户**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-162">Also, make sure that the **Authentication** option is set to **Individual User Accounts**.</span></span> <span data-ttu-id="ec86b-163">单击“确定”  继续。</span><span class="sxs-lookup"><span data-stu-id="ec86b-163">Click **OK** to continue.</span></span>

    ![使用 Web 窗体模板，其中包括 Web API 和 MVC 组件创建新项目](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image3.png)

    <span data-ttu-id="ec86b-165">*使用 Web 窗体模板，其中包括 Web API 和 MVC 组件创建新项目*</span><span class="sxs-lookup"><span data-stu-id="ec86b-165">*Creating a new project with the Web Forms template, including Web API and MVC components*</span></span>
4. <span data-ttu-id="ec86b-166">你现在可以浏览生成解决方案的结构。</span><span class="sxs-lookup"><span data-stu-id="ec86b-166">You can now explore the structure of the generated solution.</span></span>

    ![浏览生成的解决方案](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image4.png)

    <span data-ttu-id="ec86b-168">*浏览生成的解决方案*</span><span class="sxs-lookup"><span data-stu-id="ec86b-168">*Exploring the generated solution*</span></span>

    1. <span data-ttu-id="ec86b-169">**帐户：**此文件夹包含要注册、 登录和管理应用程序的用户帐户的 Web 窗体页。</span><span class="sxs-lookup"><span data-stu-id="ec86b-169">**Account:** This folder contains the Web Form pages to register, log in to and manage the application's user accounts.</span></span> <span data-ttu-id="ec86b-170">此文件夹时添加**单个用户帐户**在 Web 窗体项目模板的配置过程中选择身份验证选项。</span><span class="sxs-lookup"><span data-stu-id="ec86b-170">This folder is added when the **Individual User Accounts** authentication option is selected during the configuration of the Web Forms project template.</span></span>
    2. <span data-ttu-id="ec86b-171">**模型：**此文件夹将包含表示应用程序数据的类。</span><span class="sxs-lookup"><span data-stu-id="ec86b-171">**Models:** This folder will contain the classes that represent your application data.</span></span>
    3. <span data-ttu-id="ec86b-172">**控制器**和**视图**： 这些文件夹所需的**ASP.NET MVC**和**ASP.NET Web API**组件。</span><span class="sxs-lookup"><span data-stu-id="ec86b-172">**Controllers** and **Views**: These folders are required for the **ASP.NET MVC** and **ASP.NET Web API** components.</span></span> <span data-ttu-id="ec86b-173">您将了解在下一步的练习中的 MVC 和 Web API 的技术。</span><span class="sxs-lookup"><span data-stu-id="ec86b-173">You will explore the MVC and Web API technologies in the next exercises.</span></span>
    4. <span data-ttu-id="ec86b-174">**Default.aspx**， **Contact.aspx**和**About.aspx**文件是预定义的 Web 窗体页面，其中你可以使用作为起始点构建特定于页你应用程序。</span><span class="sxs-lookup"><span data-stu-id="ec86b-174">The **Default.aspx**, **Contact.aspx** and **About.aspx** files are pre-defined Web Form pages that you can use as starting points to build the pages specific to your application.</span></span> <span data-ttu-id="ec86b-175">这些文件的编程逻辑驻留在单独的文件称为&quot;代码隐藏&quot;文件，该文件&quot;。 为&quot;或&quot;。 aspx.cs&quot;扩展 (具体取决于使用语言）。</span><span class="sxs-lookup"><span data-stu-id="ec86b-175">The programming logic of those files resides in a separate file referred to as the &quot;code-behind&quot; file, which has an &quot;.aspx.vb&quot; or &quot;.aspx.cs&quot; extension (depending on the language used).</span></span> <span data-ttu-id="ec86b-176">代码隐藏逻辑服务器上运行，并动态生成你的页面的 HTML 输出。</span><span class="sxs-lookup"><span data-stu-id="ec86b-176">The code-behind logic runs on the server and dynamically produces the HTML output for your page.</span></span>
    5. <span data-ttu-id="ec86b-177">**Site.Master**和**Site.Mobile.Master**页在应用程序中定义外观和感觉和所有的页面的标准行为。</span><span class="sxs-lookup"><span data-stu-id="ec86b-177">The **Site.Master** and **Site.Mobile.Master** pages define the look and feel and the standard behavior of all the pages in the application.</span></span>
5. <span data-ttu-id="ec86b-178">双击**Default.aspx**文件浏览页面的内容。</span><span class="sxs-lookup"><span data-stu-id="ec86b-178">Double-click the **Default.aspx** file to explore the content of the page.</span></span>

    ![浏览 Default.aspx 页](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image5.png)

    <span data-ttu-id="ec86b-180">*浏览 Default.aspx 页*</span><span class="sxs-lookup"><span data-stu-id="ec86b-180">*Exploring the Default.aspx page*</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec86b-181">**页**文件顶部的指令定义的 Web 窗体页的属性。</span><span class="sxs-lookup"><span data-stu-id="ec86b-181">The **Page** directive at the top of the file defines the attributes of the Web Forms page.</span></span> <span data-ttu-id="ec86b-182">例如， **MasterPageFile**特性指定为主路径页上的这种情况下， *Site.Master*页-和**Inherits**属性定义页后，可以继承的代码隐藏类。</span><span class="sxs-lookup"><span data-stu-id="ec86b-182">For example, the **MasterPageFile** attribute specifies the path to the master page -in this case, the *Site.Master* page- and the **Inherits** attribute defines the code-behind class for the page to inherit.</span></span> <span data-ttu-id="ec86b-183">此类位于由文件**代码隐藏**属性。</span><span class="sxs-lookup"><span data-stu-id="ec86b-183">This class is located in the file determined by the **CodeBehind** attribute.</span></span>
    > 
    > <span data-ttu-id="ec86b-184">**Asp： 内容**控件保持页面 （文本、 标记和控件） 的实际内容，并映射到**asp: ContentPlaceHolder**母版页上的控件。</span><span class="sxs-lookup"><span data-stu-id="ec86b-184">The **asp:Content** control holds the actual content of the page (text, markup and controls) and is mapped to a **asp:ContentPlaceHolder** control on the master page.</span></span> <span data-ttu-id="ec86b-185">在这种情况下，将内呈现页面内容*主内容*中定义的控件*Site.Master*页。</span><span class="sxs-lookup"><span data-stu-id="ec86b-185">In this case, the page content will be rendered inside the *MainContent* control defined in the *Site.Master* page.</span></span>
6. <span data-ttu-id="ec86b-186">展开**应用\_启动**文件夹，请注意**WebApiConfig.cs**文件。</span><span class="sxs-lookup"><span data-stu-id="ec86b-186">Expand the **App\_Start** folder and notice the **WebApiConfig.cs** file.</span></span> <span data-ttu-id="ec86b-187">由于使用一个 ASP.NET 模板配置你的项目时包括 Web API，因此，visual Studio 生成的解决方案中包含该文件。</span><span class="sxs-lookup"><span data-stu-id="ec86b-187">Visual Studio included that file in the generated solution because you included Web API when configuring your project with the One ASP.NET template.</span></span>
7. <span data-ttu-id="ec86b-188">打开**WebApiConfig.cs**文件。</span><span class="sxs-lookup"><span data-stu-id="ec86b-188">Open the **WebApiConfig.cs** file.</span></span> <span data-ttu-id="ec86b-189">在*WebApiConfig*类将查找映射 HTTP 与 Web API，配置将路由到**Web API 控制器**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-189">In the *WebApiConfig* class you will find the configuration associated with Web API, which maps HTTP routes to **Web API controllers**.</span></span>

    [!code-csharp[Main](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/samples/sample1.cs)]
8. <span data-ttu-id="ec86b-190">打开**RouteConfig.cs**文件。</span><span class="sxs-lookup"><span data-stu-id="ec86b-190">Open the **RouteConfig.cs** file.</span></span> <span data-ttu-id="ec86b-191">内部*RegisterRoutes*方法将查找与 MVC，映射到 HTTP 路由关联的配置**MVC 控制器**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-191">Inside the *RegisterRoutes* method you will find the configuration associated with MVC, which maps HTTP routes to **MVC controllers**.</span></span>

    [!code-csharp[Main](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/samples/sample2.cs)]

<a id="Ex1Task2"></a>
#### <a name="task-2--running-the-solution"></a><span data-ttu-id="ec86b-192">任务 2 – 运行解决方案</span><span class="sxs-lookup"><span data-stu-id="ec86b-192">Task 2 – Running the Solution</span></span>

<span data-ttu-id="ec86b-193">在此任务将运行生成的解决方案，浏览应用程序和它的某些功能，如 URL 重写和内置身份验证。</span><span class="sxs-lookup"><span data-stu-id="ec86b-193">In this task you will run the generated solution, explore the app and some of its features, like URL rewriting and built-in authentication.</span></span>

1. <span data-ttu-id="ec86b-194">若要运行解决方案，按**F5**或单击**启动**按钮位于工具栏上。</span><span class="sxs-lookup"><span data-stu-id="ec86b-194">To run the solution, press **F5** or click the **Start** button located on the toolbar.</span></span> <span data-ttu-id="ec86b-195">该应用程序主页应在浏览器中打开。</span><span class="sxs-lookup"><span data-stu-id="ec86b-195">The application home page should open in the browser.</span></span>

    ![运行解决方案](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image6.png)
2. <span data-ttu-id="ec86b-197">验证正在调用的 Web 窗体页。</span><span class="sxs-lookup"><span data-stu-id="ec86b-197">Verify that the Web Forms pages are being invoked.</span></span> <span data-ttu-id="ec86b-198">若要执行此操作，请追加**/contact.aspx**到地址栏，然后按 URL **Enter**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-198">To do this, append **/contact.aspx** to the URL in the address bar and press **Enter**.</span></span>

    ![友好 Url](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image7.png)

    <span data-ttu-id="ec86b-200">*友好 Url*</span><span class="sxs-lookup"><span data-stu-id="ec86b-200">*Friendly URLs*</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec86b-201">如你所见，URL 更改为**/请联系**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-201">As you can see, the URL changes to **/contact**.</span></span> <span data-ttu-id="ec86b-202">从开始**ASP.NET 4**，URL 路由功能已添加到 Web 窗体，因此你可以编写 Url 喜欢 *[http://www.mysite.com/products/software](http://www.mysite.com/products/software)* 而不是*[http://www.mysite.com/products.aspx?category=software](http://www.mysite.com/products.aspx?category=software)*。</span><span class="sxs-lookup"><span data-stu-id="ec86b-202">Starting from **ASP.NET 4**, URL routing capabilities were added to Web Forms, so you can write URLs like *[http://www.mysite.com/products/software](http://www.mysite.com/products/software)* instead of *[http://www.mysite.com/products.aspx?category=software](http://www.mysite.com/products.aspx?category=software)*.</span></span> <span data-ttu-id="ec86b-203">有关详细信息，请参阅[URL 路由](../../../web-forms/overview/getting-started/getting-started-with-aspnet-45-web-forms/url-routing.md)。</span><span class="sxs-lookup"><span data-stu-id="ec86b-203">For more information refer to [URL Routing](../../../web-forms/overview/getting-started/getting-started-with-aspnet-45-web-forms/url-routing.md).</span></span>
3. <span data-ttu-id="ec86b-204">现在，您将了解到应用程序集成的身份验证流。</span><span class="sxs-lookup"><span data-stu-id="ec86b-204">You will now explore the authentication flow integrated into the application.</span></span> <span data-ttu-id="ec86b-205">若要执行此操作，请单击**注册**页面的右上角。</span><span class="sxs-lookup"><span data-stu-id="ec86b-205">To do this, click **Register** in the upper-right corner of the page.</span></span>

    ![注册一个新用户](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image8.png)

    <span data-ttu-id="ec86b-207">*注册一个新用户*</span><span class="sxs-lookup"><span data-stu-id="ec86b-207">*Registering a new user*</span></span>
4. <span data-ttu-id="ec86b-208">在**注册**页上，输入**用户名**和**密码**，然后单击**注册**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-208">In the **Register** page, enter a **User name** and **Password**, and then click **Register**.</span></span>

    ![注册页](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image9.png)

    <span data-ttu-id="ec86b-210">*注册页*</span><span class="sxs-lookup"><span data-stu-id="ec86b-210">*Register page*</span></span>
5. <span data-ttu-id="ec86b-211">应用程序注册新帐户，并对用户身份验证。</span><span class="sxs-lookup"><span data-stu-id="ec86b-211">The application registers the new account, and the user is authenticated.</span></span>

    ![用户通过身份验证](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image10.png)

    <span data-ttu-id="ec86b-213">*用户通过身份验证*</span><span class="sxs-lookup"><span data-stu-id="ec86b-213">*User authenticated*</span></span>
6. <span data-ttu-id="ec86b-214">返回到 Visual Studio，然后按**SHIFT + F5**来停止调试。</span><span class="sxs-lookup"><span data-stu-id="ec86b-214">Go back to Visual Studio and press **SHIFT + F5** to stop debugging.</span></span>

<a id="Exercise2"></a>
### <a name="exercise-2-creating-an-mvc-controller-using-scaffolding"></a><span data-ttu-id="ec86b-215">练习 2： 创建使用基架 MVC 控制器</span><span class="sxs-lookup"><span data-stu-id="ec86b-215">Exercise 2: Creating an MVC Controller Using Scaffolding</span></span>

<span data-ttu-id="ec86b-216">在本练习中将利用 ASP.NET 基架框架提供的 Visual Studio 来创建 ASP.NET MVC 5 控制器操作与 Razor 视图可用于执行 CRUD 操作，而无需编写一行代码。</span><span class="sxs-lookup"><span data-stu-id="ec86b-216">In this exercise you will take advantage of the ASP.NET Scaffolding framework provided by Visual Studio to create an ASP.NET MVC 5 controller with actions and Razor views to perform CRUD operations, without writing a single line of code.</span></span> <span data-ttu-id="ec86b-217">基架过程将使用 Entity Framework Code First 在 SQL 数据库中生成的数据上下文和数据库架构。</span><span class="sxs-lookup"><span data-stu-id="ec86b-217">The scaffolding process will use Entity Framework Code First to generate the data context and the database schema in the SQL database.</span></span>

<span data-ttu-id="ec86b-218">**有关实体框架代码优先**</span><span class="sxs-lookup"><span data-stu-id="ec86b-218">**About Entity Framework Code First**</span></span>

<span data-ttu-id="ec86b-219">Entity Framework (EF) 是对象关系映射器 (ORM)，可用于创建数据访问应用程序使用而不是直接使用关系存储架构编程概念应用程序模型编程。</span><span class="sxs-lookup"><span data-stu-id="ec86b-219">Entity Framework (EF) is an object-relational mapper (ORM) that enables you to create data access applications by programming with a conceptual application model instead of programming directly using a relational storage schema.</span></span>

<span data-ttu-id="ec86b-220">Entity Framework Code First 建模工作流，可使用您自己的域类来表示在执行查询时，EF 依赖于该模型更改跟踪和更新函数。</span><span class="sxs-lookup"><span data-stu-id="ec86b-220">The Entity Framework Code First modeling workflow allows you to use your own domain classes to represent the model that EF relies on when performing querying, change-tracking and updating functions.</span></span> <span data-ttu-id="ec86b-221">使用 Code First 开发工作流，你不需要通过创建数据库或指定架构开始你的应用程序。</span><span class="sxs-lookup"><span data-stu-id="ec86b-221">Using the Code First development workflow, you do not need to begin your application by creating a database or specifying a schema.</span></span> <span data-ttu-id="ec86b-222">相反，你可以编写定义你的应用程序的最合适域模型对象的标准.NET 类，实体框架将为你创建数据库。</span><span class="sxs-lookup"><span data-stu-id="ec86b-222">Instead, you can write standard .NET classes that define the most appropriate domain model objects for your application, and Entity Framework will create the database for you.</span></span>

> [!NOTE]
> <span data-ttu-id="ec86b-223">你可以了解有关实体框架[此处](../../../entity-framework.md)。</span><span class="sxs-lookup"><span data-stu-id="ec86b-223">You can learn more about Entity Framework [here](../../../entity-framework.md).</span></span>


<a id="Ex2Task1"></a>
#### <a name="task-1--creating-a-new-model"></a><span data-ttu-id="ec86b-224">任务 1 – 创建新的模型</span><span class="sxs-lookup"><span data-stu-id="ec86b-224">Task 1 – Creating a New Model</span></span>

<span data-ttu-id="ec86b-225">现在，你将定义**人员**类，该类将基架过程用于创建 MVC 控制器和视图的模型。</span><span class="sxs-lookup"><span data-stu-id="ec86b-225">You will now define a **Person** class, which will be the model used by the scaffolding process to create the MVC controller and the views.</span></span> <span data-ttu-id="ec86b-226">首先，将通过创建**人员**模型类，在控制器中的 CRUD 操作将自动创建和使用基架功能。</span><span class="sxs-lookup"><span data-stu-id="ec86b-226">You will start by creating a **Person** model class, and the CRUD operations in the controller will be automatically created using scaffolding features.</span></span>

1. <span data-ttu-id="ec86b-227">打开**Visual Studio Express 2013 for Web**和**MyHybridSite.sln**解决方案位于**源/Ex2-MvcScaffolding/开始**文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec86b-227">Open **Visual Studio Express 2013 for Web** and the **MyHybridSite.sln** solution located in the **Source/Ex2-MvcScaffolding/Begin** folder.</span></span> <span data-ttu-id="ec86b-228">或者，继续与解决方案并在上一练习中获取。</span><span class="sxs-lookup"><span data-stu-id="ec86b-228">Alternatively, you can continue with the solution that you obtained in the previous exercise.</span></span>
2. <span data-ttu-id="ec86b-229">在**解决方案资源管理器**，右键单击**模型**文件夹**MyHybridSite**项目，然后选择**添加 |类...**.</span><span class="sxs-lookup"><span data-stu-id="ec86b-229">In **Solution Explorer**, right-click the **Models** folder of the **MyHybridSite** project and select **Add | Class...**.</span></span>

    ![添加人员模型类](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image11.png)

    <span data-ttu-id="ec86b-231">*添加人员模型类*</span><span class="sxs-lookup"><span data-stu-id="ec86b-231">*Adding the Person model class*</span></span>
3. <span data-ttu-id="ec86b-232">在**添加新项**对话框中，将文件*Person.cs*单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-232">In the **Add New Item** dialog box, name the file *Person.cs* and click **Add**.</span></span>

    ![创建个人模型类](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image12.png)

    <span data-ttu-id="ec86b-234">*创建个人模型类*</span><span class="sxs-lookup"><span data-stu-id="ec86b-234">*Creating the Person model class*</span></span>
4. <span data-ttu-id="ec86b-235">替换的内容**Person.cs**文件替换为以下代码。</span><span class="sxs-lookup"><span data-stu-id="ec86b-235">Replace the content of the **Person.cs** file with the following code.</span></span> <span data-ttu-id="ec86b-236">按**CTRL + S**以保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="ec86b-236">Press **CTRL + S** to save the changes.</span></span>

    <span data-ttu-id="ec86b-237">(代码段- *BringingTogetherOneAspNet-Ex2-PersonClass*)</span><span class="sxs-lookup"><span data-stu-id="ec86b-237">(Code Snippet - *BringingTogetherOneAspNet - Ex2 - PersonClass*)</span></span>

    [!code-csharp[Main](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/samples/sample3.cs)]
5. <span data-ttu-id="ec86b-238">在**解决方案资源管理器**，右键单击**MyHybridSite**项目，然后选择**生成**，或按**CTRL + SHIFT + B**以生成项目。</span><span class="sxs-lookup"><span data-stu-id="ec86b-238">In **Solution Explorer**, right-click the **MyHybridSite** project and select **Build**, or press **CTRL + SHIFT + B** to build the project.</span></span>

<a id="Ex2Task2"></a>
#### <a name="task-2--creating-an-mvc-controller"></a><span data-ttu-id="ec86b-239">任务 2 – 创建 MVC 控制器</span><span class="sxs-lookup"><span data-stu-id="ec86b-239">Task 2 – Creating an MVC Controller</span></span>

<span data-ttu-id="ec86b-240">现在，**人员**创建模型，将使用与实体框架的 ASP.NET MVC 基架创建的 CRUD 控制器操作和视图**人员**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-240">Now that the **Person** model is created, you will use ASP.NET MVC scaffolding with Entity Framework to create the CRUD controller actions and views for **Person**.</span></span>

1. <span data-ttu-id="ec86b-241">在**解决方案资源管理器**，右键单击**控制器**文件夹**MyHybridSite**项目，然后选择**添加 |新的基架的项...**.</span><span class="sxs-lookup"><span data-stu-id="ec86b-241">In **Solution Explorer**, right-click the **Controllers** folder of the **MyHybridSite** project and select **Add | New Scaffolded Item...**.</span></span>

    ![创建新的基架的控制器](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image13.png)

    <span data-ttu-id="ec86b-243">*创建新的基架控制器*</span><span class="sxs-lookup"><span data-stu-id="ec86b-243">*Creating a new Scaffolded Controller*</span></span>
2. <span data-ttu-id="ec86b-244">在**添加基架**对话框中，选择**数据与视图，MVC 5 控制器使用 Entity Framework** ，然后单击**添加。**</span><span class="sxs-lookup"><span data-stu-id="ec86b-244">In the **Add Scaffold** dialog box, select **MVC 5 Controller with views, using Entity Framework** and then click **Add.**</span></span>

    ![选择 MVC 5 控制器视图和实体框架](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image14.png)

    <span data-ttu-id="ec86b-246">*选择 MVC 5 控制器视图和实体框架*</span><span class="sxs-lookup"><span data-stu-id="ec86b-246">*Selecting MVC 5 Controller with views and Entity Framework*</span></span>
3. <span data-ttu-id="ec86b-247">设置*MvcPersonController*作为**控制器名称**，选择**使用异步控制器操作**选项并选择**人员 (MyHybridSite.Models)**作为**模型类**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-247">Set *MvcPersonController* as the **Controller name**, select the **Use async controller actions** option and select **Person (MyHybridSite.Models)** as the **Model class**.</span></span>

    ![添加基架 MVC 控制器](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image15.png)

    <span data-ttu-id="ec86b-249">*添加基架 MVC 控制器*</span><span class="sxs-lookup"><span data-stu-id="ec86b-249">*Adding an MVC controller with scaffolding*</span></span>
4. <span data-ttu-id="ec86b-250">下**数据上下文类**，单击**新建数据上下文...**.</span><span class="sxs-lookup"><span data-stu-id="ec86b-250">Under **Data context class**, click **New data context...**.</span></span>

    ![创建新的数据上下文](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image16.png)

    <span data-ttu-id="ec86b-252">*创建新的数据上下文*</span><span class="sxs-lookup"><span data-stu-id="ec86b-252">*Creating a new data context*</span></span>
5. <span data-ttu-id="ec86b-253">在**新建数据上下文**对话框中，名称的新的数据上下文*PersonContext*单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-253">In the **New Data Context** dialog box, name the new data context *PersonContext* and click **Add**.</span></span>

    ![创建新的 PersonContext](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image17.png)

    <span data-ttu-id="ec86b-255">*创建新的 PersonContext 类型*</span><span class="sxs-lookup"><span data-stu-id="ec86b-255">*Creating the new PersonContext type*</span></span>
6. <span data-ttu-id="ec86b-256">单击**添加**若要创建的新控制器**人员**使用基架。</span><span class="sxs-lookup"><span data-stu-id="ec86b-256">Click **Add** to create the new controller for **Person** with scaffolding.</span></span> <span data-ttu-id="ec86b-257">控制器操作、 Person 数据上下文和 Razor 视图，然后将生成 visual Studio。</span><span class="sxs-lookup"><span data-stu-id="ec86b-257">Visual Studio will then generate the controller actions, the Person data context and the Razor views.</span></span>

    ![之后使用基架创建 MVC 控制器](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image18.png)

    <span data-ttu-id="ec86b-259">*之后使用基架创建 MVC 控制器*</span><span class="sxs-lookup"><span data-stu-id="ec86b-259">*After creating the MVC controller with scaffolding*</span></span>
7. <span data-ttu-id="ec86b-260">打开**MvcPersonController.cs**文件中**控制器**文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec86b-260">Open the **MvcPersonController.cs** file in the **Controllers** folder.</span></span> <span data-ttu-id="ec86b-261">请注意自动生成的 CRUD 操作方法。</span><span class="sxs-lookup"><span data-stu-id="ec86b-261">Notice that the CRUD action methods have been generated automatically.</span></span>

    [!code-csharp[Main](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/samples/sample4.cs)]

    > [!NOTE]
    > <span data-ttu-id="ec86b-262">通过选择**使用异步控制器操作**从基架的复选框选项前面步骤中，Visual Studio 将生成对涉及到人员数据上下文的访问的所有操作的异步操作方法。</span><span class="sxs-lookup"><span data-stu-id="ec86b-262">By selecting the **Use async controller actions** check box from the scaffolding options in the previous steps, Visual Studio generates asynchronous action methods for all actions that involve access to the Person data context.</span></span> <span data-ttu-id="ec86b-263">建议的异步操作方法用于长时间运行、 非 CPU 绑定请求以避免阻止 Web 服务器在处理请求时执行工作。</span><span class="sxs-lookup"><span data-stu-id="ec86b-263">It is recommended that you use asynchronous action methods for long-running, non-CPU bound requests to avoid blocking the Web server from performing work while the request is being processed.</span></span>

<a id="Ex2Task3"></a>
#### <a name="task-3--running-the-solution"></a><span data-ttu-id="ec86b-264">任务 3 – 运行解决方案</span><span class="sxs-lookup"><span data-stu-id="ec86b-264">Task 3 – Running the Solution</span></span>

<span data-ttu-id="ec86b-265">在此任务中，你将运行以验证的解决方案的视图**人员**是否按预期工作。</span><span class="sxs-lookup"><span data-stu-id="ec86b-265">In this task, you will run the solution again to verify that the views for **Person** are working as expected.</span></span> <span data-ttu-id="ec86b-266">你将添加新的用户来验证已成功保存到数据库。</span><span class="sxs-lookup"><span data-stu-id="ec86b-266">You will add a new person to verify that it is successfully saved to the database.</span></span>

1. <span data-ttu-id="ec86b-267">按**F5**运行该解决方案。</span><span class="sxs-lookup"><span data-stu-id="ec86b-267">Press **F5** to run the solution.</span></span>
2. <span data-ttu-id="ec86b-268">导航到**/MvcPerson**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-268">Navigate to **/MvcPerson**.</span></span> <span data-ttu-id="ec86b-269">应显示的基架的视图显示的人员列表。</span><span class="sxs-lookup"><span data-stu-id="ec86b-269">The scaffolded view that shows the list of people should appear.</span></span>
3. <span data-ttu-id="ec86b-270">单击**新建**以添加新成员。</span><span class="sxs-lookup"><span data-stu-id="ec86b-270">Click **Create New** to add a new person.</span></span>

    ![导航到基架 MVC 视图](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image19.png)

    <span data-ttu-id="ec86b-272">*导航到基架 MVC 视图*</span><span class="sxs-lookup"><span data-stu-id="ec86b-272">*Navigating to the scaffolded MVC views*</span></span>
4. <span data-ttu-id="ec86b-273">在**创建**视图中，提供**名称**和**年龄**人猜出，然后单击**创建**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-273">In the **Create** view, provide a **Name** and an **Age** for the person, and click **Create**.</span></span>

    ![添加新的用户](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image20.png)

    <span data-ttu-id="ec86b-275">*添加新的用户*</span><span class="sxs-lookup"><span data-stu-id="ec86b-275">*Adding a new person*</span></span>
5. <span data-ttu-id="ec86b-276">新的用户添加到列表。</span><span class="sxs-lookup"><span data-stu-id="ec86b-276">The new person is added to the list.</span></span> <span data-ttu-id="ec86b-277">在元素列表中，单击**详细信息**若要显示的人员的详细信息视图。</span><span class="sxs-lookup"><span data-stu-id="ec86b-277">In the element list, click **Details** to display the person's details view.</span></span> <span data-ttu-id="ec86b-278">然后，在**详细信息**视图中，单击**回列表**回到列表视图。</span><span class="sxs-lookup"><span data-stu-id="ec86b-278">Then, in the **Details** view, click **Back to List** to go back to the list view.</span></span>

    ![人员的详细信息视图](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image21.png)

    <span data-ttu-id="ec86b-280">*人员的详细信息视图*</span><span class="sxs-lookup"><span data-stu-id="ec86b-280">*Person's details view*</span></span>
6. <span data-ttu-id="ec86b-281">单击**删除**链接以删除用户。</span><span class="sxs-lookup"><span data-stu-id="ec86b-281">Click the **Delete** link to delete the person.</span></span> <span data-ttu-id="ec86b-282">在**删除**视图中，单击**删除**以确认该操作。</span><span class="sxs-lookup"><span data-stu-id="ec86b-282">In the **Delete** view, click **Delete** to confirm the operation.</span></span>

    ![删除用户](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image22.png)

    <span data-ttu-id="ec86b-284">*删除用户*</span><span class="sxs-lookup"><span data-stu-id="ec86b-284">*Deleting a person*</span></span>
7. <span data-ttu-id="ec86b-285">返回到 Visual Studio，然后按**SHIFT + F5**来停止调试。</span><span class="sxs-lookup"><span data-stu-id="ec86b-285">Go back to Visual Studio and press **SHIFT + F5** to stop debugging.</span></span>

<a id="Exercise3"></a>
### <a name="exercise-3-creating-a-web-api-controller-using-scaffolding"></a><span data-ttu-id="ec86b-286">练习 3： 创建 Web API 控制器使用基架</span><span class="sxs-lookup"><span data-stu-id="ec86b-286">Exercise 3: Creating a Web API Controller Using Scaffolding</span></span>

<span data-ttu-id="ec86b-287">Web API 框架是 ASP.NET 堆栈的一部分，旨在使实现 HTTP 服务更容易，但通常发送和接收 JSON 或 XML 格式的数据，通过 RESTful API。</span><span class="sxs-lookup"><span data-stu-id="ec86b-287">The Web API framework is part of the ASP.NET Stack and designed to make implementing HTTP services easier, generally sending and receiving JSON- or XML-formatted data through a RESTful API.</span></span>

<span data-ttu-id="ec86b-288">在此练习中，您将再次使用 ASP.NET 基架以生成 Web API 控制器。</span><span class="sxs-lookup"><span data-stu-id="ec86b-288">In this exercise, you will use ASP.NET Scaffolding again to generate a Web API controller.</span></span> <span data-ttu-id="ec86b-289">你将使用相同**人员**和**PersonContext**从上一练习，以提供相同的个人数据以 JSON 格式的类。</span><span class="sxs-lookup"><span data-stu-id="ec86b-289">You will use the same **Person** and **PersonContext** classes from the previous exercise to provide the same person data in JSON format.</span></span> <span data-ttu-id="ec86b-290">你将看到相同的 ASP.NET 应用程序中以不同方式，你就可以公开相同的资源。</span><span class="sxs-lookup"><span data-stu-id="ec86b-290">You will see how you can expose the same resources in different ways within the same ASP.NET application.</span></span>

<a id="Ex3Task1"></a>
#### <a name="task-1--creating-a-web-api-controller"></a><span data-ttu-id="ec86b-291">任务 1 – 创建一个 Web API 控制器</span><span class="sxs-lookup"><span data-stu-id="ec86b-291">Task 1 – Creating a Web API Controller</span></span>

<span data-ttu-id="ec86b-292">在此任务将创建一个新**Web API 控制器**，将公开机耗材格式，如 JSON 中的个人数据。</span><span class="sxs-lookup"><span data-stu-id="ec86b-292">In this task you will create a new **Web API Controller** that will expose the person data in a machine-consumable format like JSON.</span></span>

1. <span data-ttu-id="ec86b-293">如果尚未打开，则打开**Visual Studio Express 2013 for Web**并打开**MyHybridSite.sln**解决方案位于**源/Ex3-WebAPI/开始**文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec86b-293">If not already opened, open **Visual Studio Express 2013 for Web** and open the **MyHybridSite.sln** solution located in the **Source/Ex3-WebAPI/Begin** folder.</span></span> <span data-ttu-id="ec86b-294">或者，继续与解决方案并在上一练习中获取。</span><span class="sxs-lookup"><span data-stu-id="ec86b-294">Alternatively, you can continue with the solution that you obtained in the previous exercise.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec86b-295">如果你从开始从练习 3 开始解决方案，按**CTRL + SHIFT + B**要生成解决方案。</span><span class="sxs-lookup"><span data-stu-id="ec86b-295">If you start with the Begin solution from Exercise 3, press **CTRL + SHIFT + B** to build the solution.</span></span>
2. <span data-ttu-id="ec86b-296">在**解决方案资源管理器**，右键单击**控制器**文件夹**MyHybridSite**项目，然后选择**添加 |新的基架的项...**.</span><span class="sxs-lookup"><span data-stu-id="ec86b-296">In **Solution Explorer**, right-click the **Controllers** folder of the **MyHybridSite** project and select **Add | New Scaffolded Item...**.</span></span>

    ![创建新的基架的控制器](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image23.png)

    <span data-ttu-id="ec86b-298">*创建新的基架的控制器*</span><span class="sxs-lookup"><span data-stu-id="ec86b-298">*Creating a new scaffolded Controller*</span></span>
3. <span data-ttu-id="ec86b-299">在**添加基架**对话框中，选择**Web API**的左窗格中，然后**Web API 2 Controller 其操作使用 Entity Framework**在中间窗格中，然后单击**添加。**</span><span class="sxs-lookup"><span data-stu-id="ec86b-299">In the **Add Scaffold** dialog box, select **Web API** in the left pane, then **Web API 2 Controller with actions, using Entity Framework** in the middle pane and then click **Add.**</span></span>

    <span data-ttu-id="ec86b-300">![选择包含操作和实体框架的 Web API 2 Controller](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image24.png "选择包含操作和实体框架 Web API 2 控制器")</span><span class="sxs-lookup"><span data-stu-id="ec86b-300">![Selecting Web API 2 Controller with actions and Entity Framework](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image24.png "Selecting Web API 2 Controller with actions and Entity Framework")</span></span>

    <span data-ttu-id="ec86b-301">*选择包含操作和实体框架的 Web API 2 控制器*</span><span class="sxs-lookup"><span data-stu-id="ec86b-301">*Selecting Web API 2 Controller with actions and Entity Framework*</span></span>
4. <span data-ttu-id="ec86b-302">设置*ApiPersonController*作为**控制器名称**，选择**使用异步控制器操作**选项并选择**人员 (MyHybridSite.Models)**和**PersonContext (MyHybridSite.Models)**作为**模型**和**数据上下文**分别类。</span><span class="sxs-lookup"><span data-stu-id="ec86b-302">Set *ApiPersonController* as the **Controller name**, select the **Use async controller actions** option and select **Person (MyHybridSite.Models)** and **PersonContext (MyHybridSite.Models)** as the **Model** and **Data context** classes respectively.</span></span> <span data-ttu-id="ec86b-303">然后单击 **“添加”**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-303">Then click **Add**.</span></span>

    <span data-ttu-id="ec86b-304">![添加基架使用一个 Web API 控制器](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image25.png "添加基架使用一个 Web API 控制器")</span><span class="sxs-lookup"><span data-stu-id="ec86b-304">![Adding a Web API Controller with scaffolding](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image25.png "Adding a Web API controller with scaffolding")</span></span>

    <span data-ttu-id="ec86b-305">*添加基架使用一个 Web API 控制器*</span><span class="sxs-lookup"><span data-stu-id="ec86b-305">*Adding a Web API controller with scaffolding*</span></span>
5. <span data-ttu-id="ec86b-306">然后，visual Studio 将生成**ApiPersonController**其四个的 CRUD 操作，可用于处理数据的类。</span><span class="sxs-lookup"><span data-stu-id="ec86b-306">Visual Studio will then generate the **ApiPersonController** class with the four CRUD actions to work with your data.</span></span>

    <span data-ttu-id="ec86b-307">![之后使用基架创建的 Web API 控制器](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image26.png "后使用基架创建的 Web API 控制器")</span><span class="sxs-lookup"><span data-stu-id="ec86b-307">![After creating the Web API controller with scaffolding](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image26.png "After creating the Web API controller with scaffolding")</span></span>

    <span data-ttu-id="ec86b-308">*之后使用基架创建的 Web API 控制器*</span><span class="sxs-lookup"><span data-stu-id="ec86b-308">*After creating the Web API controller with scaffolding*</span></span>
6. <span data-ttu-id="ec86b-309">打开**ApiPersonController.cs**文件并检查*GetPeople*操作方法。</span><span class="sxs-lookup"><span data-stu-id="ec86b-309">Open the **ApiPersonController.cs** file and inspect the *GetPeople* action method.</span></span> <span data-ttu-id="ec86b-310">此方法的查询的数据库字段**PersonContext**以获取数据的人员的类型。</span><span class="sxs-lookup"><span data-stu-id="ec86b-310">This method queries the db field of **PersonContext** type in order to get the people data.</span></span>

    [!code-csharp[Main](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/samples/sample5.cs)]
7. <span data-ttu-id="ec86b-311">请注意，上面的方法定义的注释。</span><span class="sxs-lookup"><span data-stu-id="ec86b-311">Now notice the comment above the method definition.</span></span> <span data-ttu-id="ec86b-312">它提供了公开此操作将在下一个任务中使用的 URI。</span><span class="sxs-lookup"><span data-stu-id="ec86b-312">It provides the URI that exposes this action which you will use in the next task.</span></span>

    [!code-csharp[Main](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/samples/sample6.cs)]

    > [!NOTE]
    > <span data-ttu-id="ec86b-313">默认情况下，Web API 配置为捕获到的查询*/api*路径，以避免与 MVC 控制器的冲突。</span><span class="sxs-lookup"><span data-stu-id="ec86b-313">By default, Web API is configured to catch the queries to the */api* path to avoid collisions with MVC controllers.</span></span> <span data-ttu-id="ec86b-314">如果你需要更改此设置，请参阅[路由在 ASP.NET Web API 中](../../../web-api/overview/web-api-routing-and-actions/routing-in-aspnet-web-api.md)。</span><span class="sxs-lookup"><span data-stu-id="ec86b-314">If you need to change this setting, refer to [Routing in ASP.NET Web API](../../../web-api/overview/web-api-routing-and-actions/routing-in-aspnet-web-api.md).</span></span>

<a id="Ex3Task2"></a>
#### <a name="task-2--running-the-solution"></a><span data-ttu-id="ec86b-315">任务 2 – 运行解决方案</span><span class="sxs-lookup"><span data-stu-id="ec86b-315">Task 2 – Running the Solution</span></span>

<span data-ttu-id="ec86b-316">在此任务将使用 Internet Explorer **F12 开发人员工具**检查来自 Web API 控制器的完整响应。</span><span class="sxs-lookup"><span data-stu-id="ec86b-316">In this task you will use the Internet Explorer **F12 developer tools** to inspect the full response from the Web API controller.</span></span> <span data-ttu-id="ec86b-317">你将看到如何可以捕获网络流量，以详细了解你的应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="ec86b-317">You will see how you can capture network traffic to get more insight into your application data.</span></span>

> [!NOTE]
> <span data-ttu-id="ec86b-318">请确保**Internet Explorer**中选择**启动**按钮位于 Visual Studio 工具栏上。</span><span class="sxs-lookup"><span data-stu-id="ec86b-318">Make sure that **Internet Explorer** is selected in the **Start** button located on the Visual Studio toolbar.</span></span>
> 
> ![Internet Explorer 选项](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image27.png)
> 
> <span data-ttu-id="ec86b-320">**F12 开发人员工具**具有一组范围广泛的此动手实验中未涉及的功能。</span><span class="sxs-lookup"><span data-stu-id="ec86b-320">The **F12 developer tools** have a wide set of functionality that is not covered in this hands-on-lab.</span></span> <span data-ttu-id="ec86b-321">如果你想要了解详细信息，请参阅[使用 F12 开发人员工具](https://msdn.microsoft.com/library/ie/bg182326(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ec86b-321">If you want to learn more about it, refer to [Using the F12 developer tools](https://msdn.microsoft.com/library/ie/bg182326(v=vs.85)).</span></span>


1. <span data-ttu-id="ec86b-322">按**F5**运行该解决方案。</span><span class="sxs-lookup"><span data-stu-id="ec86b-322">Press **F5** to run the solution.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec86b-323">为了正确执行此任务，你的应用程序需要具有的数据。</span><span class="sxs-lookup"><span data-stu-id="ec86b-323">In order to follow this task correctly, your application needs to have data.</span></span> <span data-ttu-id="ec86b-324">如果你的数据库为空，你可以返回在练习 2 中的任务 3，并按照如何创建新的用户使用 MVC 视图上的步骤。</span><span class="sxs-lookup"><span data-stu-id="ec86b-324">If your database is empty, you can go back to Task 3 in Exercise 2 and follow the steps on how to create a new person using the MVC views.</span></span>
2. <span data-ttu-id="ec86b-325">在浏览器中，按**F12**以打开**开发人员工具**面板。</span><span class="sxs-lookup"><span data-stu-id="ec86b-325">In the browser, press **F12** to open the **Developer Tools** panel.</span></span> <span data-ttu-id="ec86b-326">按**CTRL** + **4**或单击**网络**图标，，然后单击绿色箭头按钮，以开始捕获网络流量。</span><span class="sxs-lookup"><span data-stu-id="ec86b-326">Press **CTRL** + **4** or click the **Network** icon, and then click the green arrow button to begin capturing network traffic.</span></span>

    <span data-ttu-id="ec86b-327">![启动 Web API 网络捕获](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image28.png "启动 Web API 网络捕获")</span><span class="sxs-lookup"><span data-stu-id="ec86b-327">![Initiating Web API network capture](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image28.png "Initiating Web API network capture")</span></span>

    <span data-ttu-id="ec86b-328">*启动 Web API 网络捕获*</span><span class="sxs-lookup"><span data-stu-id="ec86b-328">*Initiating Web API network capture*</span></span>
3. <span data-ttu-id="ec86b-329">追加**api/ApiPerson**到浏览器的地址栏中的 URL。</span><span class="sxs-lookup"><span data-stu-id="ec86b-329">Append **api/ApiPerson** to the URL in the browser's address bar.</span></span> <span data-ttu-id="ec86b-330">现在将检查从响应的详细信息**ApiPersonController**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-330">You will now inspect the details of the response from the **ApiPersonController**.</span></span>

    <span data-ttu-id="ec86b-331">![检索通过 Web API 的人员数据](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image29.png "检索通过 Web API 的个人数据")</span><span class="sxs-lookup"><span data-stu-id="ec86b-331">![Retrieving person data through Web API](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image29.png "Retrieving person data through Web API")</span></span>

    <span data-ttu-id="ec86b-332">*通过 Web API 中检索用户数据*</span><span class="sxs-lookup"><span data-stu-id="ec86b-332">*Retrieving person data through Web API*</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec86b-333">下载完成后，系统将提示与下载的文件进行操作。</span><span class="sxs-lookup"><span data-stu-id="ec86b-333">Once the download finishes, you will be prompted to make an action with the downloaded file.</span></span> <span data-ttu-id="ec86b-334">使对话框保持打开状态，以能够查看响应内容通过开发人员工具窗口。</span><span class="sxs-lookup"><span data-stu-id="ec86b-334">Leave the dialog box open in order to be able to watch the response content through the Developers Tool window.</span></span>
4. <span data-ttu-id="ec86b-335">现在，你将检查响应的正文。</span><span class="sxs-lookup"><span data-stu-id="ec86b-335">Now you will inspect the body of the response.</span></span> <span data-ttu-id="ec86b-336">若要执行此操作，请单击**详细信息**选项卡，然后单击**响应正文**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-336">To do this, click the **Details** tab and then click **Response body**.</span></span> <span data-ttu-id="ec86b-337">你可以检查下载的数据是带有属性的对象列表**Id**，**名称**和**年龄**对应于这样的**人员**类。</span><span class="sxs-lookup"><span data-stu-id="ec86b-337">You can check that the downloaded data is a list of objects with the properties **Id**, **Name** and **Age** that correspond to the **Person** class.</span></span>

    <span data-ttu-id="ec86b-338">![查看 Web API 响应正文](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image30.png "查看 Web API 响应正文")</span><span class="sxs-lookup"><span data-stu-id="ec86b-338">![Viewing Web API Response Body](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image30.png "Viewing Web API Response Body")</span></span>

    <span data-ttu-id="ec86b-339">*查看 Web API 响应正文*</span><span class="sxs-lookup"><span data-stu-id="ec86b-339">*Viewing Web API Response Body*</span></span>

<a id="Ex3Task3"></a>
#### <a name="task-3--adding-web-api-help-pages"></a><span data-ttu-id="ec86b-340">任务 3 – 添加 Web API 帮助页</span><span class="sxs-lookup"><span data-stu-id="ec86b-340">Task 3 – Adding Web API Help Pages</span></span>

<span data-ttu-id="ec86b-341">当你创建一个 Web API 时，它可用于创建一个帮助页，以便其他开发人员知道如何调用你的 API。</span><span class="sxs-lookup"><span data-stu-id="ec86b-341">When you create a Web API, it is useful to create a help page so that other developers will know how to call your API.</span></span> <span data-ttu-id="ec86b-342">你可以创建并文档页手动更新，但最好将自动生成它们以避免维护工作。</span><span class="sxs-lookup"><span data-stu-id="ec86b-342">You could create and update the documentation pages manually, but it is better to auto-generate them to avoid having to do maintenance work.</span></span> <span data-ttu-id="ec86b-343">在此任务将使用 Nuget 包以自动生成到解决方案的 Web API 帮助页。</span><span class="sxs-lookup"><span data-stu-id="ec86b-343">In this task you will use a Nuget package to automatically generate Web API help pages to the solution.</span></span>

1. <span data-ttu-id="ec86b-344">从**工具**菜单在 Visual Studio 中，选择**库程序包管理器**，然后单击**程序包管理器控制台**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-344">From the **Tools** menu in Visual Studio, select **Library Package Manager**, and then click **Package Manager Console**.</span></span>
2. <span data-ttu-id="ec86b-345">在**程序包管理器控制台**窗口中，执行以下命令：</span><span class="sxs-lookup"><span data-stu-id="ec86b-345">In the **Package Manager Console** window, execute the following command:</span></span>

    [!code-powershell[Main](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/samples/sample7.ps1)]

    > [!NOTE]
    > <span data-ttu-id="ec86b-346">**Microsoft.AspNet.WebApi.HelpPage**程序包安装必需的程序集并添加下的帮助页的 MVC 视图**区域/HelpPage**文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec86b-346">The **Microsoft.AspNet.WebApi.HelpPage** package installs the necessary assemblies and adds MVC Views for the help pages under the **Areas/HelpPage** folder.</span></span>

    <span data-ttu-id="ec86b-347">![HelpPage 区域](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image31.png "HelpPage 区域")</span><span class="sxs-lookup"><span data-stu-id="ec86b-347">![HelpPage Area](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image31.png "HelpPage Area")</span></span>

    <span data-ttu-id="ec86b-348">*HelpPage 区域*</span><span class="sxs-lookup"><span data-stu-id="ec86b-348">*HelpPage Area*</span></span>
3. <span data-ttu-id="ec86b-349">默认情况下，帮助页具有文档的占位符字符串。</span><span class="sxs-lookup"><span data-stu-id="ec86b-349">By default, the help pages have placeholder strings for documentation.</span></span> <span data-ttu-id="ec86b-350">XML 文档注释可用于创建文档。</span><span class="sxs-lookup"><span data-stu-id="ec86b-350">You can use XML documentation comments to create the documentation.</span></span> <span data-ttu-id="ec86b-351">若要启用此功能，请打开**HelpPageConfig.cs**文件位于**应用程序区域/HelpPage\_启动**文件夹并取消注释以下行：</span><span class="sxs-lookup"><span data-stu-id="ec86b-351">To enable this feature, open the **HelpPageConfig.cs** file located in the **Areas/HelpPage/App\_Start** folder and uncomment the following line:</span></span>

    [!code-javascript[Main](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/samples/sample8.js)]
4. <span data-ttu-id="ec86b-352">在**解决方案资源管理器**，右键单击该项目**MyHybridSite**，选择**属性**单击**生成**选项卡。</span><span class="sxs-lookup"><span data-stu-id="ec86b-352">In **Solution Explorer**, right-click the project **MyHybridSite**, select **Properties** and click the **Build** tab.</span></span>

    <span data-ttu-id="ec86b-353">![生成选项卡](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image32.png "生成部分")</span><span class="sxs-lookup"><span data-stu-id="ec86b-353">![Build tab](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image32.png "Build section")</span></span>

    <span data-ttu-id="ec86b-354">*生成选项卡*</span><span class="sxs-lookup"><span data-stu-id="ec86b-354">*Build tab*</span></span>
5. <span data-ttu-id="ec86b-355">下**输出**，选择**XML 文档文件**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-355">Under **Output**, select **XML documentation file**.</span></span> <span data-ttu-id="ec86b-356">在编辑框中，键入**应用\_Data/XmlDocument.xml**。</span><span class="sxs-lookup"><span data-stu-id="ec86b-356">In the edit box, type **App\_Data/XmlDocument.xml**.</span></span>

    <span data-ttu-id="ec86b-357">![输出生成选项卡中的部分](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image33.png "输出生成选项卡中的部分")</span><span class="sxs-lookup"><span data-stu-id="ec86b-357">![Output section in Build tab](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image33.png "Output section in build tab")</span></span>

    <span data-ttu-id="ec86b-358">*生成选项卡中的输出部分*</span><span class="sxs-lookup"><span data-stu-id="ec86b-358">*Output section in Build tab*</span></span>
6. <span data-ttu-id="ec86b-359">按**CTRL** + **S**以保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="ec86b-359">Press **CTRL** + **S** to save the changes.</span></span>
7. <span data-ttu-id="ec86b-360">打开**ApiPersonController.cs**文件从**控制器**文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec86b-360">Open the **ApiPersonController.cs** file from the **Controllers** folder.</span></span>
8. <span data-ttu-id="ec86b-361">输入新行之间*GetPeople*方法签名和*/ / 获取 api/ApiPerson*注释，，然后键入三个正斜杠。</span><span class="sxs-lookup"><span data-stu-id="ec86b-361">Enter a new line between the *GetPeople* method signature and the *// GET api/ApiPerson* comment, and then type three forward slashes.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec86b-362">Visual Studio 会自动插入的 XML 元素定义的方法文档。</span><span class="sxs-lookup"><span data-stu-id="ec86b-362">Visual Studio automatically inserts the XML elements which define the method documentation.</span></span>
9. <span data-ttu-id="ec86b-363">添加摘要文本和的返回值*GetPeople*方法。</span><span class="sxs-lookup"><span data-stu-id="ec86b-363">Add a summary text and the return value for the *GetPeople* method.</span></span> <span data-ttu-id="ec86b-364">其外观应如下所示。</span><span class="sxs-lookup"><span data-stu-id="ec86b-364">It should look like the following.</span></span>

    [!code-csharp[Main](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/samples/sample9.cs)]
10. <span data-ttu-id="ec86b-365">按**F5**运行该解决方案。</span><span class="sxs-lookup"><span data-stu-id="ec86b-365">Press **F5** to run the solution.</span></span>
11. <span data-ttu-id="ec86b-366">追加**/帮助**到在地址栏中的该 URL 可浏览到帮助页。</span><span class="sxs-lookup"><span data-stu-id="ec86b-366">Append **/help** to the URL in the address bar to browse to the help page.</span></span>

    <span data-ttu-id="ec86b-367">![ASP.NET Web API 帮助页](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image34.png "ASP.NET Web API 帮助页")</span><span class="sxs-lookup"><span data-stu-id="ec86b-367">![ASP.NET Web API Help Page](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image34.png "ASP.NET Web API Help Page")</span></span>

    <span data-ttu-id="ec86b-368">*ASP.NET Web API 帮助页*</span><span class="sxs-lookup"><span data-stu-id="ec86b-368">*ASP.NET Web API Help Page*</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec86b-369">页面的主要内容是 Api，由控制器分组的表。</span><span class="sxs-lookup"><span data-stu-id="ec86b-369">The main content of the page is a table of APIs, grouped by controller.</span></span> <span data-ttu-id="ec86b-370">表条目动态生成的使用**IApiExplorer**接口。</span><span class="sxs-lookup"><span data-stu-id="ec86b-370">The table entries are generated dynamically, using the **IApiExplorer** interface.</span></span> <span data-ttu-id="ec86b-371">如果你添加或更新一个 API 控制器，表将自动更新生成应用程序的下一步时间。</span><span class="sxs-lookup"><span data-stu-id="ec86b-371">If you add or update an API controller, the table will be automatically updated the next time you build the application.</span></span>
    > 
    > <span data-ttu-id="ec86b-372">**API**列列出的 HTTP 方法和相对 URI。</span><span class="sxs-lookup"><span data-stu-id="ec86b-372">The **API** column lists the HTTP method and relative URI.</span></span> <span data-ttu-id="ec86b-373">**说明**列包含具有已从该方法的文档中提取的信息。</span><span class="sxs-lookup"><span data-stu-id="ec86b-373">The **Description** column contains information that has been extracted from the method's documentation.</span></span>
12. <span data-ttu-id="ec86b-374">请注意，在说明列显示您在前面的方法定义添加的说明。</span><span class="sxs-lookup"><span data-stu-id="ec86b-374">Note that the description you added above the method definition is displayed in the description column.</span></span>

    <span data-ttu-id="ec86b-375">![API 方法描述](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image35.png "API 方法描述")</span><span class="sxs-lookup"><span data-stu-id="ec86b-375">![API method description](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image35.png "API method description")</span></span>

    <span data-ttu-id="ec86b-376">*API 方法描述*</span><span class="sxs-lookup"><span data-stu-id="ec86b-376">*API method description*</span></span>
13. <span data-ttu-id="ec86b-377">单击其中一个 API 方法，以导航到具有更多详细信息，包括示例响应正文的页。</span><span class="sxs-lookup"><span data-stu-id="ec86b-377">Click one of the API methods to navigate to a page with more detailed information, including sample response bodies.</span></span>

    <span data-ttu-id="ec86b-378">![详细信息页](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image36.png "详细信息页")</span><span class="sxs-lookup"><span data-stu-id="ec86b-378">![Detail Information page](one-aspnet-integrating-aspnet-web-forms-mvc-and-web-api/_static/image36.png "Detail Information page")</span></span>

    <span data-ttu-id="ec86b-379">*详细的信息页*</span><span class="sxs-lookup"><span data-stu-id="ec86b-379">*Detailed information page*</span></span>

* * *

<a id="Summary"></a>
## <a name="summary"></a><span data-ttu-id="ec86b-380">摘要</span><span class="sxs-lookup"><span data-stu-id="ec86b-380">Summary</span></span>

<span data-ttu-id="ec86b-381">通过完成本动手实验你已学习如何：</span><span class="sxs-lookup"><span data-stu-id="ec86b-381">By completing this hands-on lab you have learned how to:</span></span>

- <span data-ttu-id="ec86b-382">创建新 Web 应用程序在 Visual Studio 2013 中使用一个 ASP.NET 体验</span><span class="sxs-lookup"><span data-stu-id="ec86b-382">Create a new Web application using the One ASP.NET Experience in Visual Studio 2013</span></span>
- <span data-ttu-id="ec86b-383">将多个 ASP.NET 技术集成到一个单个的项目</span><span class="sxs-lookup"><span data-stu-id="ec86b-383">Integrate multiple ASP.NET technologies into one single project</span></span>
- <span data-ttu-id="ec86b-384">从你使用 ASP.NET 基架的模型类生成 MVC 控制器和视图</span><span class="sxs-lookup"><span data-stu-id="ec86b-384">Generate MVC controllers and views from your model classes using ASP.NET Scaffolding</span></span>
- <span data-ttu-id="ec86b-385">生成 Web API 控制器，使用异步编程等通过 Entity Framework 数据访问的功能</span><span class="sxs-lookup"><span data-stu-id="ec86b-385">Generate Web API controllers, which use features such as Async Programming and data access through Entity Framework</span></span>
- <span data-ttu-id="ec86b-386">为你的控制器自动生成 Web API 帮助页</span><span class="sxs-lookup"><span data-stu-id="ec86b-386">Automatically generate Web API Help Pages for your controllers</span></span>