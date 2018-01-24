<span data-ttu-id="626f4-101">使用以下内容替换 Razor 视图文件 Views/HelloWorld/Index.cshtml 的内容：</span><span class="sxs-lookup"><span data-stu-id="626f4-101">Replace the contents of the *Views/HelloWorld/Index.cshtml* Razor view file with the following:</span></span>

[!code-HTML[Main](../../tutorials/first-mvc-app/start-mvc/sample/MvcMovie/Views/HelloWorld/Index.cshtml)]

<span data-ttu-id="626f4-102">导航到 `http://localhost:xxxx/HelloWorld`。</span><span class="sxs-lookup"><span data-stu-id="626f4-102">Navigate to `http://localhost:xxxx/HelloWorld`.</span></span> <span data-ttu-id="626f4-103">`HelloWorldController` 中的 `Index` 方法作用不大；它运行 `return View();` 语句，指定此方法应使用视图模板文件来呈现对浏览器的响应。</span><span class="sxs-lookup"><span data-stu-id="626f4-103">The `Index` method in the `HelloWorldController` didn't do much; it ran the statement `return View();`, which specified that the method should use a view template file to render a response to the browser.</span></span> <span data-ttu-id="626f4-104">因为没有显式指定视图模板文件的名称，所以 MVC 默认使用 /Views/HelloWorld 文件夹中的 Index.cshtml 视图文件。</span><span class="sxs-lookup"><span data-stu-id="626f4-104">Because you didn't explicitly specify the name of the view template file, MVC defaulted to using the *Index.cshtml* view file in the */Views/HelloWorld* folder.</span></span> <span data-ttu-id="626f4-105">下面图片显示了视图中硬编码的</span><span class="sxs-lookup"><span data-stu-id="626f4-105">The image below shows the string "Hello from our View Template!"</span></span> <span data-ttu-id="626f4-106">字符串“Hello from our View Template!”</span><span class="sxs-lookup"><span data-stu-id="626f4-106">hard-coded in the view.</span></span>

![浏览器窗口](../../tutorials/first-mvc-app/adding-view/_static/hell_template.png)

<span data-ttu-id="626f4-108">如果浏览器窗口较小（例如在移动设备上），则可能需要在右上角切换（点击）[Bootstrap 导航按钮](http://getbootstrap.com/components/#navbar)以查看“首页”、“关于”和“联系人”链接。</span><span class="sxs-lookup"><span data-stu-id="626f4-108">If your browser window is small (for example on a mobile device), you might need to toggle (tap) the [Bootstrap navigation button](http://getbootstrap.com/components/#navbar) in the upper right to see the **Home**, **About**, and **Contact** links.</span></span>

![突出显示 Bootstrap 导航按钮的浏览器窗口](../../tutorials/first-mvc-app/adding-view/_static/1.png)

## <a name="changing-views-and-layout-pages"></a><span data-ttu-id="626f4-110">更改视图和布局页面</span><span class="sxs-lookup"><span data-stu-id="626f4-110">Changing views and layout pages</span></span>

<span data-ttu-id="626f4-111">点击菜单链接（“MvcMovie”、“首页”、“关于”）。</span><span class="sxs-lookup"><span data-stu-id="626f4-111">Tap the menu links (**MvcMovie**, **Home**, **About**).</span></span> <span data-ttu-id="626f4-112">每页显示相同的菜单布局。</span><span class="sxs-lookup"><span data-stu-id="626f4-112">Each page shows the same menu layout.</span></span> <span data-ttu-id="626f4-113">菜单布局是在 Views/Shared/_Layout.cshtml 文件中实现的。</span><span class="sxs-lookup"><span data-stu-id="626f4-113">The menu layout is implemented in the *Views/Shared/_Layout.cshtml* file.</span></span> <span data-ttu-id="626f4-114">打开 Views/Shared/_Layout.cshtml 文件。</span><span class="sxs-lookup"><span data-stu-id="626f4-114">Open the *Views/Shared/_Layout.cshtml* file.</span></span>

<span data-ttu-id="626f4-115">[布局](xref:mvc/views/layout)模板使你能够在一个位置指定网站的 HTML 容器布局，然后将它应用到网站中的多个页面。</span><span class="sxs-lookup"><span data-stu-id="626f4-115">[Layout](xref:mvc/views/layout) templates allow you to specify the HTML container layout of your site in one place and then apply it across multiple pages in your site.</span></span> <span data-ttu-id="626f4-116">查找 `@RenderBody()` 行。</span><span class="sxs-lookup"><span data-stu-id="626f4-116">Find the `@RenderBody()` line.</span></span> <span data-ttu-id="626f4-117">`RenderBody` 是显示创建的所有特定于视图的页面的占位符，已包装在布局页面中。</span><span class="sxs-lookup"><span data-stu-id="626f4-117">`RenderBody` is a placeholder where all the view-specific pages you create show up, *wrapped* in the layout page.</span></span> <span data-ttu-id="626f4-118">例如，如果选择“关于”链接，Views/Home/About.cshtml 视图将在 `RenderBody` 方法中呈现。</span><span class="sxs-lookup"><span data-stu-id="626f4-118">For example, if you select the **About** link, the **Views/Home/About.cshtml** view is rendered inside the `RenderBody` method.</span></span>

## <a name="change-the-title-and-menu-link-in-the-layout-file"></a><span data-ttu-id="626f4-119">更改布局文件中的标题和菜单链接</span><span class="sxs-lookup"><span data-stu-id="626f4-119">Change the title and menu link in the layout file</span></span>

<span data-ttu-id="626f4-120">在标题元素中，将 `MvcMovie` 更改为 `Movie App`。</span><span class="sxs-lookup"><span data-stu-id="626f4-120">In the title element, change `MvcMovie` to `Movie App`.</span></span> <span data-ttu-id="626f4-121">将布局模板中的定位文本从 `MvcMovie` 更改为 `Mvc Movie`，并将控制器从 `Home` 更改为 `Movies`，如下所示：</span><span class="sxs-lookup"><span data-stu-id="626f4-121">Change the anchor text in the layout template from `MvcMovie` to `Mvc Movie` and the controller from `Home` to `Movies` as highlighted below:</span></span>

<span data-ttu-id="626f4-122">注意：ASP.NET Core 2.0 版本略有不同。</span><span class="sxs-lookup"><span data-stu-id="626f4-122">Note: The ASP.NET Core 2.0 version is slightly different.</span></span> <span data-ttu-id="626f4-123">它不包含 `@inject ApplicationInsights` 和 `@Html.Raw(JavaScriptSnippet.FullScript)`。</span><span class="sxs-lookup"><span data-stu-id="626f4-123">It doesn't contain `@inject ApplicationInsights` and `@Html.Raw(JavaScriptSnippet.FullScript)`.</span></span>

[!code-html[Main](../../tutorials/first-mvc-app/start-mvc/sample/MvcMovie/Views/Shared/_Layout.cshtml?highlight=7,31)]

>[!WARNING]
> <span data-ttu-id="626f4-124">我们尚未实现 `Movies` 控制器，所以如果单击此链接，将收到 404（未找到）错误。</span><span class="sxs-lookup"><span data-stu-id="626f4-124">We haven't implemented the `Movies` controller yet, so if you click on that link, you'll get a 404 (Not found) error.</span></span>

<span data-ttu-id="626f4-125">保存更改并点击“关于”链接。</span><span class="sxs-lookup"><span data-stu-id="626f4-125">Save your changes and tap the **About** link.</span></span> <span data-ttu-id="626f4-126">请注意浏览器选项卡上的标题现在显示的是**“关于 - 电影应用”**，而不是**“关于 - Mvc 电影”**:</span><span class="sxs-lookup"><span data-stu-id="626f4-126">Notice how the title on the browser tab now displays **About - Movie App** instead of **About - Mvc Movie**:</span></span> 

![关于标签](../../tutorials/first-mvc-app/adding-view/_static/about2.png)

<span data-ttu-id="626f4-128">点击“联系人”链接，请注意，标题和定位文本还会显示“电影应用”。</span><span class="sxs-lookup"><span data-stu-id="626f4-128">Tap the **Contact** link and notice that the title and anchor text also display **Movie App**.</span></span> <span data-ttu-id="626f4-129">我们能够在布局模板中进行一次更改，让网站上的所有页面都反映新的链接文本和新标题。</span><span class="sxs-lookup"><span data-stu-id="626f4-129">We were able to make the change once in the layout template and have all pages on the site reflect the new link text and new title.</span></span>

<span data-ttu-id="626f4-130">检查 Views/_ViewStart.cshtml 文件：</span><span class="sxs-lookup"><span data-stu-id="626f4-130">Examine the *Views/_ViewStart.cshtml* file:</span></span>


```HTML
@{
    Layout = "_Layout";
}
```

<span data-ttu-id="626f4-131">Views/_ViewStart.cshtml 文件将 Views/Shared/_Layout.cshtml 文件引入到每个视图中。</span><span class="sxs-lookup"><span data-stu-id="626f4-131">The *Views/_ViewStart.cshtml* file brings in the *Views/Shared/_Layout.cshtml* file to each view.</span></span> <span data-ttu-id="626f4-132">可以使用 `Layout` 属性设置不同的布局视图，或将它设置为 `null`，这样将不会使用任何布局文件。</span><span class="sxs-lookup"><span data-stu-id="626f4-132">You can use the `Layout` property to set a different layout view, or set it to `null` so no layout file will be used.</span></span>

<span data-ttu-id="626f4-133">更改 `Index` 视图的标题。</span><span class="sxs-lookup"><span data-stu-id="626f4-133">Change the title of the `Index` view.</span></span>

<span data-ttu-id="626f4-134">打开 Views/HelloWorld/Index.cshtml。</span><span class="sxs-lookup"><span data-stu-id="626f4-134">Open *Views/HelloWorld/Index.cshtml*.</span></span> <span data-ttu-id="626f4-135">有两处需要更改的地方：</span><span class="sxs-lookup"><span data-stu-id="626f4-135">There are two places to make a change:</span></span>

   * <span data-ttu-id="626f4-136">浏览器标题中显示的文字。</span><span class="sxs-lookup"><span data-stu-id="626f4-136">The text that appears in the title of the browser.</span></span>
   * <span data-ttu-id="626f4-137">辅助标题（`<h2>` 元素）。</span><span class="sxs-lookup"><span data-stu-id="626f4-137">The secondary header (`<h2>` element).</span></span>

<span data-ttu-id="626f4-138">稍稍对它们进行一些更改，这样可以看出哪一段代码更改了应用的哪部分。</span><span class="sxs-lookup"><span data-stu-id="626f4-138">You'll make them slightly different so you can see which bit of code changes which part of the app.</span></span>


```HTML
@{
    ViewData["Title"] = "Movie List";
}

<h2>My Movie List</h2>

<p>Hello from our View Template!</p>
```

<span data-ttu-id="626f4-139">上述代码中的 `ViewData["Title"] = "Movie List";` 将 `ViewData` 字典的 `Title` 属性设置为“Movie List”。</span><span class="sxs-lookup"><span data-stu-id="626f4-139">`ViewData["Title"] = "Movie List";` in the code above sets the `Title` property of the `ViewData` dictionary to "Movie List".</span></span> <span data-ttu-id="626f4-140">`Title` 属性在布局页面中的 `<title>` HTML 元素中使用：</span><span class="sxs-lookup"><span data-stu-id="626f4-140">The `Title` property is used in the `<title>` HTML element in the layout page:</span></span>


```HTML
<title>@ViewData["Title"] - Movie App</title>
   ```

<span data-ttu-id="626f4-141">保存更改并导航到 `http://localhost:xxxx/HelloWorld`。</span><span class="sxs-lookup"><span data-stu-id="626f4-141">Save your change and navigate to `http://localhost:xxxx/HelloWorld`.</span></span> <span data-ttu-id="626f4-142">请注意，浏览器标题、主标题和辅助标题已更改。</span><span class="sxs-lookup"><span data-stu-id="626f4-142">Notice that the browser title, the primary heading, and the secondary headings have changed.</span></span> <span data-ttu-id="626f4-143">（如果没有在浏览器中看到更改，则可能正在查看缓存的内容。</span><span class="sxs-lookup"><span data-stu-id="626f4-143">(If you don't see changes in the browser, you might be viewing cached content.</span></span> <span data-ttu-id="626f4-144">在浏览器中按 Ctrl + F5 强制加载来自服务器的响应。）浏览器标题是使用我们在 Index.cshtml 视图模板中设置的 `ViewData["Title"]` 以及在布局文件中添加的额外“ - Movie App”创建的。</span><span class="sxs-lookup"><span data-stu-id="626f4-144">Press Ctrl+F5 in your browser to force the response from the server to be loaded.) The browser title is created with `ViewData["Title"]` we set in the *Index.cshtml* view template and the additional "- Movie App" added in the layout file.</span></span>

<span data-ttu-id="626f4-145">还要注意，Index.cshtml 视图模板中的内容是如何与 Views/Shared/_Layout.cshtml 视图模板合并的，并且注意单个 HTML 响应被发送到了浏览器。</span><span class="sxs-lookup"><span data-stu-id="626f4-145">Also notice how the content in the *Index.cshtml* view template was merged with the *Views/Shared/_Layout.cshtml* view template and a single HTML response was sent to the browser.</span></span> <span data-ttu-id="626f4-146">凭借布局模板可以很容易地对应用程序中所有页面进行更改。</span><span class="sxs-lookup"><span data-stu-id="626f4-146">Layout templates make it really easy to make changes that apply across all of the pages in your application.</span></span> <span data-ttu-id="626f4-147">若要了解更多信息，请参阅[布局](../../mvc/views/layout.md)。</span><span class="sxs-lookup"><span data-stu-id="626f4-147">To learn more see [Layout](../../mvc/views/layout.md).</span></span>

![电影列表视图](../../tutorials/first-mvc-app/adding-view/_static/hell3.png)

<span data-ttu-id="626f4-149">但我们这一点点“数据”（在此示例中为“Hello from our View Template!”</span><span class="sxs-lookup"><span data-stu-id="626f4-149">Our little bit of "data" (in this case the "Hello from our View Template!"</span></span> <span data-ttu-id="626f4-150">消息）是硬编码的。</span><span class="sxs-lookup"><span data-stu-id="626f4-150">message) is hard-coded, though.</span></span> <span data-ttu-id="626f4-151">MVC 应用程序有一个“V”（视图），而你已有一个“C”（控制器），但还没有“M”（模型）。</span><span class="sxs-lookup"><span data-stu-id="626f4-151">The MVC application has a "V" (view) and you've got a "C" (controller), but no "M" (model) yet.</span></span>

## <a name="passing-data-from-the-controller-to-the-view"></a><span data-ttu-id="626f4-152">将数据从控制器传递给视图</span><span class="sxs-lookup"><span data-stu-id="626f4-152">Passing Data from the Controller to the View</span></span>

<span data-ttu-id="626f4-153">控制器操作会被调用以响应传入的 URL 请求。</span><span class="sxs-lookup"><span data-stu-id="626f4-153">Controller actions are invoked in response to an incoming URL request.</span></span> <span data-ttu-id="626f4-154">控制器类是编写处理传入浏览器请求的代码的地方。</span><span class="sxs-lookup"><span data-stu-id="626f4-154">A controller class is where you write the code that handles the incoming browser requests.</span></span> <span data-ttu-id="626f4-155">控制器从数据源检索数据，并决定将哪些类型的响应发送回浏览器。</span><span class="sxs-lookup"><span data-stu-id="626f4-155">The controller retrieves data from a data source and decides what type of response to send back to the browser.</span></span> <span data-ttu-id="626f4-156">可以从控制器使用视图模板来生成并格式化对浏览器的 HTML 响应。</span><span class="sxs-lookup"><span data-stu-id="626f4-156">View templates can be used from a controller to generate and format an HTML response to the browser.</span></span>

<span data-ttu-id="626f4-157">控制器负责提供所需的数据，使视图模板能够呈现响应。</span><span class="sxs-lookup"><span data-stu-id="626f4-157">Controllers are responsible for providing the data required in order for a view template to render a response.</span></span> <span data-ttu-id="626f4-158">最佳做法：视图模板不应该直接执行业务逻辑或与数据库进行交互。</span><span class="sxs-lookup"><span data-stu-id="626f4-158">A best practice: View templates should **not** perform business logic or interact with a database directly.</span></span> <span data-ttu-id="626f4-159">相反，视图模板应仅使用由控制器提供给它的数据。</span><span class="sxs-lookup"><span data-stu-id="626f4-159">Rather, a view template should work only with the data that's provided to it by the controller.</span></span> <span data-ttu-id="626f4-160">保持此“关注点分离”有助于保持代码干净、可测试性和可维护性。</span><span class="sxs-lookup"><span data-stu-id="626f4-160">Maintaining this "separation of concerns" helps keep your code clean, testable, and maintainable.</span></span>

<span data-ttu-id="626f4-161">目前，`HelloWorldController` 类中的 `Welcome` 方法采用 `name` 和 `ID` 参数，然后将值直接输出到浏览器。</span><span class="sxs-lookup"><span data-stu-id="626f4-161">Currently, the `Welcome` method in the `HelloWorldController` class takes a `name` and a `ID` parameter and then outputs the values directly to the browser.</span></span> <span data-ttu-id="626f4-162">与使控制器将此响应呈现为字符串相反，应将控制器更改为使用视图模板。</span><span class="sxs-lookup"><span data-stu-id="626f4-162">Rather than have the controller render this response as a string, let’s change the controller to use a view template instead.</span></span> <span data-ttu-id="626f4-163">视图模板将生成动态响应，这意味着你需要将适当的数据位从控制器传递给视图以生成响应。</span><span class="sxs-lookup"><span data-stu-id="626f4-163">The view template will generate a dynamic response, which means that you need to pass appropriate bits of data from the controller to the view in order to generate the response.</span></span> <span data-ttu-id="626f4-164">这可以通过让控制器将视图模板所需的动态数据（参数）放置在视图模板稍后可以访问的 `ViewData` 字典中来实现。</span><span class="sxs-lookup"><span data-stu-id="626f4-164">You can do this by having the controller put the dynamic data (parameters) that the view template needs in a `ViewData` dictionary that the view template can then access.</span></span>

<span data-ttu-id="626f4-165">返回到 HelloWorldController.cs 文件，并更改 `Welcome` 方法以将 `Message` 和 `NumTimes` 值添加到 `ViewData` 字典。</span><span class="sxs-lookup"><span data-stu-id="626f4-165">Return to the *HelloWorldController.cs* file and change the `Welcome` method to add a `Message` and `NumTimes` value to the `ViewData` dictionary.</span></span> <span data-ttu-id="626f4-166">`ViewData` 字典是一个动态对象，这意味着你可以将任何所需的内容放在其中；只有将内容放在其中后 `ViewData` 对象才具有定义的属性。</span><span class="sxs-lookup"><span data-stu-id="626f4-166">The `ViewData` dictionary is a dynamic object, which means you can put whatever you want in to it; the `ViewData` object has no defined properties until you put something inside it.</span></span> <span data-ttu-id="626f4-167">[MVC 模型绑定系统](xref:mvc/models/model-binding)自动将命名参数（`name` 和 `numTimes`）从地址栏中的查询字符串映射到方法中的参数。</span><span class="sxs-lookup"><span data-stu-id="626f4-167">The [MVC model binding system](xref:mvc/models/model-binding) automatically maps the named parameters (`name` and `numTimes`) from the query string in the address bar to parameters in your method.</span></span> <span data-ttu-id="626f4-168">完整的 HelloWorldController.cs 文件如下所示：</span><span class="sxs-lookup"><span data-stu-id="626f4-168">The complete *HelloWorldController.cs* file looks like this:</span></span>

[!code-csharp[Main](../../tutorials/first-mvc-app/start-mvc/sample/MvcMovie/Controllers/HelloWorldController.cs?name=snippet_5)]

<span data-ttu-id="626f4-169">`ViewData` 字典对象包含将传递给视图的数据。</span><span class="sxs-lookup"><span data-stu-id="626f4-169">The `ViewData` dictionary object contains data that will be passed to the view.</span></span> 

<span data-ttu-id="626f4-170">创建一个名为 Views/HelloWorld/Welcome.cshtml 的 Welcome 视图模板。</span><span class="sxs-lookup"><span data-stu-id="626f4-170">Create a Welcome view template named *Views/HelloWorld/Welcome.cshtml*.</span></span>

<span data-ttu-id="626f4-171">在 Welcome.cshtml 视图模板中创建一个循环，显示“Hello” `NumTimes`。</span><span class="sxs-lookup"><span data-stu-id="626f4-171">You'll create a loop in the *Welcome.cshtml* view template that displays "Hello" `NumTimes`.</span></span> <span data-ttu-id="626f4-172">使用以下内容替换 Views/HelloWorld/Welcome.cshtml 的内容：</span><span class="sxs-lookup"><span data-stu-id="626f4-172">Replace the contents of *Views/HelloWorld/Welcome.cshtml* with the following:</span></span>

[!code-html[Main](../../tutorials/first-mvc-app/start-mvc/sample/MvcMovie/Views/HelloWorld/Welcome.cshtml)]

<span data-ttu-id="626f4-173">保存更改并浏览到以下 URL：</span><span class="sxs-lookup"><span data-stu-id="626f4-173">Save your changes and browse to the following URL:</span></span>

`http://localhost:xxxx/HelloWorld/Welcome?name=Rick&numtimes=4`

<span data-ttu-id="626f4-174">数据取自 URL，并传递给使用 [MVC 模型绑定器](xref:mvc/models/model-binding)的控制器。</span><span class="sxs-lookup"><span data-stu-id="626f4-174">Data is taken from the URL and passed to the controller using the [MVC model binder](xref:mvc/models/model-binding) .</span></span> <span data-ttu-id="626f4-175">控制器将数据打包到 `ViewData` 字典中，并将该对象传递给视图。</span><span class="sxs-lookup"><span data-stu-id="626f4-175">The controller packages the data into a `ViewData` dictionary and passes that object to the view.</span></span> <span data-ttu-id="626f4-176">然后，视图将数据作为 HTML 呈现给浏览器。</span><span class="sxs-lookup"><span data-stu-id="626f4-176">The view then renders the data as HTML to the browser.</span></span>

![“关于”视图，显示了 Welcome 标签以及四个“Hello Rick”短语](../../tutorials/first-mvc-app/adding-view/_static/rick2.png)

<span data-ttu-id="626f4-178">在上面的示例中，我们使用 `ViewData` 字典将数据从控制器传递给视图。</span><span class="sxs-lookup"><span data-stu-id="626f4-178">In the sample above, we used the `ViewData` dictionary to pass data from the controller to a view.</span></span> <span data-ttu-id="626f4-179">稍后在本教程中，我们将使用视图模型将数据从控制器传递给视图。</span><span class="sxs-lookup"><span data-stu-id="626f4-179">Later in the tutorial, we will use a view model to pass data from a controller to a view.</span></span> <span data-ttu-id="626f4-180">传递数据的视图模型方法通常比 `ViewData` 字典方法更为优先。</span><span class="sxs-lookup"><span data-stu-id="626f4-180">The view model approach to passing data is generally much preferred over the `ViewData` dictionary approach.</span></span> <span data-ttu-id="626f4-181">有关详细信息，请参阅 [ViewModel vs ViewData vs ViewBag vs TempData vs Session in MVC](http://www.mytecbits.com/microsoft/dot-net/viewmodel-viewdata-viewbag-tempdata-mvc)（MVC 中 ViewModel、ViewData、ViewBag、TempData 和 Session 之间的比较）。</span><span class="sxs-lookup"><span data-stu-id="626f4-181">See [ViewModel vs ViewData vs ViewBag vs TempData vs Session in MVC](http://www.mytecbits.com/microsoft/dot-net/viewmodel-viewdata-viewbag-tempdata-mvc) for more information.</span></span>

<span data-ttu-id="626f4-182">当然，这是模型的一种“M”类型，而不是数据库类。</span><span class="sxs-lookup"><span data-stu-id="626f4-182">Well, that was a kind of an "M" for model, but not the database kind.</span></span> <span data-ttu-id="626f4-183">让我们用学到的内容来创建一个电影数据库。</span><span class="sxs-lookup"><span data-stu-id="626f4-183">Let's take what we've learned and create a database of movies.</span></span>