<a name="title" />
# One ASP.NET / Hybrid Site #

---
<a name="Overview" />
## Overview ##

Demonstrates the new One ASP.NET tooling in Visual Studio by adding MVC and API controllers to a Web Forms application.

In this demo you will:

1. Create a new site using the Web Forms template but including MVC and Web API references.
1. Demonstrate that Default.aspx works as expected
1. Create a new Person model (int ID, string Name, int Age)
1. Scaffold Web Forms pages with read / write actions (<http://www.asp.net/web-forms/tutorials/aspnet-45/aspnet-scaffolding-with-web-forms>) 
1. Scaffold a new MVC controller named MvcPerson (<http://www.asp.net/mvc/tutorials/mvc-5/introduction/accessing-your-models-data-from-a-controller>) 
1. Scaffold a new Web API controller ApiPerson (<http://www.asp.net/web-api/overview/web-api-routing-and-actions/create-a-rest-api-with-attribute-routing>) 
1. Start the site and browse to the Web Forms page and browse to /Person/ to demonstrate the web forms scaffolded pages.
1. Browse to /MvcPerson to show the MVC scaffolded pages

<a id="goals" />
### Goals ###
In this demo, you will see how to:

1. (TODO: Insert goal 1 here)
1. (TODO: Insert goal 2 here)
1. (TODO: Insert goal 3 here)

<a name="technologies" />
### Key Technologies ###

- {TODO: Include technology name here} [here][1]
- {TODO: Include technology name here}
- [{TODO: Include technology name here}][2]

[1]: http://insert_link_to_technology_1_here/
[2]: http://insert_link_to_technology_2_here/

<a name="Setup" />
### Setup and Configuration ###
In order to execute this demo you need to set up your environment.

1. Open Visual Studio 2013.

<a name="Demo" />
## Demo ##
This demo is composed of the following segments:

1. [Creating a new site](#segment1).
1. [Creating an MVC Controller using Scaffolding](#segment2).
1. [Creating a Web API using Scaffolding](#segment3).
1. [Running the site](#segment4).

<a name="Segment1" />
### Creating a new site ###

1. Open the **File / New Project** dialog and show the options in the **Visual C# / Web** section.

1. Name the application _MyHybridSite_ and click **OK**.

	![Creating a new ASP.NET Web Application project](images/creating-a-new-project.png?raw=true "Creating a new ASP.NET Web Application project")

	_Creating a new ASP.NET Web Application project_

1. Select the **Web Forms** template and check the **MVC** and **Web API** options.

	![Selecting the Web Forms template](images/selecting-web-forms-template.png?raw=true "Selecting the Web Forms template")

	_Selecting the Web Forms template_

1. Click **OK** to create the project.

1. Explore the generated solution in the **Solution Explorer**.

	![Exploring the generated solution](images/exploring-the-generated-solution.png?raw=true "Exploring the generated solution")

	_Exploring the generated solution_

1. Open the **Default.aspx** file and show the generated code.

1. Press **F5** to run the web site.

1. Navigate to **/default.aspx**.

	![Navigating to the default webform](images/navigating-to-default-aspx.png?raw=true "Navigating to the default webform")

	_Navigating to the default webform_

1. Close the browser.

1. Create a _Person_ model class. To do that, right-click the **Model** folder and expand the **Add** menu and select **Class**.

	![Adding a new model class](images/adding-a-new-class.png?raw=true "Adding a new model class")

	_Adding a new model class_

1. Name the file _Person.cs_ and click **Add**.

	![Creating the Person model class](images/creating-the-person-model-class.png?raw=true "Creating the Person model class")

	_Creating the Person model class_

1. Add the following code to the **Person** class.

	<!-- mark:3-7 -->
	````C#
	public class Person
	{
		public int Id { get; set; }

		public string Name { get; set; }

		public int Age { get; set; }
	}
````

1. Build the solution.

<a name="Segment2" />
### Creating an MVC Controller using Scaffolding ###

1. Create the controller and views for the _Person_ Model class using scaffolding. To do that, right-click the **Controllers** folder and expand the **Add** menu and select **New Scaffolded Item...**

	![Creating a new scaffolded Controller](images/adding-scaffolding-controller.png?raw=true "Creating a new Controller")

	_Creating a new scaffolded Controller_

1. Select the **MVC 5 Controller with views, using Entity Framework** option in the **Add Scaffold** dialog and click **Add**.

	![Selecting the MVC 5 Controller with views and Entity Framework](images/selecting-mvc5-controller.png?raw=true "Selecting the MVC 5 Controller with views and Entity Framework")

	_Selecting the MVC 5 Controller with views and Entity Framework_

1. Change the name of the controller to **PersonController**.

	![Changing the controller name](images/changing-the-controller-name.png?raw=true "Changing the controller name")

	_Changing the controller name_

1. Select **Person** from the **Model class** list.

	![Selecting the Person  model](images/selecting-the-model.png?raw=true "Selecting the Person  model")

	_Selecting the Person model_

1. Create a new data context named **PersonContext**.

	![Creating the new PersonContext](images/creating-a-new-context.png?raw=true "Creating the new PersonContext")

	_Creating the new PersonContext_

1. Check the **Use async controller actions** checkbox.

	![Checking the use async controller actions checkbox](images/checking-the-async-option.png?raw=true "Checking the use async controller actions checkbox")

	_Checking the use async controller actions checkbox_

1. Finally, click **Add** to create the views and the controller with the default actions.

	![Creating the MvcPerson Controller](images/creating-the-mvcperson-controller.png?raw=true "Creating the MvcPerson Controller")

	_Creating the MvcPerson Controller_

1. Expand to the **Controller** folder and show the **MvcPersonController.cs** file, which was just created.

1. Open the **MvcPersonController.cs** file to show the generated content.

1. Expand the **Views** folder and show the new views under the **MvcPerson** folder.

<a name="Segment3" />
### Creating a Web API using Scaffolding ###

1. Create the Web API controller for the _Person_ Model class using scaffolding. To do that, right-click the **Controllers** folder and expand the **Add** menu and select **New Scaffolded Item...**

	![Creating a new scaffolded Controller](images/adding-scaffolding-controller.png?raw=true "Creating a new Controller")

	_Creating a new scaffolded Controller_

1. Select the **Web API 2 Controller with actions, using Entity Framework** option in the **Add Scaffold** dialog and click **Add**.

	![Selecting the Web API 2 Controller with actions, using Entity Framework](images/creating-a-new-webapi.png?raw=true "Selecting the Web API 2 Controller with actions, using Entity Framework")

	_Selecting the Web API 2 Controller with actions, using Entity Framework_

1. Change the name of the Web API to **ApiPersonController**.

1. Select **Person** from the **Model class** list.

	![Selecting the Person  model](images/selecting-the-person-model-for-webapi.png?raw=true "Selecting the Person model")

	_Selecting the Person model_

1. Check the **Use async controller actions** checkbox.

1. Finally, click **Add** to create the API controller with the default actions.

	![Creating the ApiPerson Web API](images/creating-the-person-webapi.png?raw=true "Creating the ApiPerson Web API")

	_Creating the ApiPerson Web API_

1. Expand to the **Controller** folder and show the **ApiPersonController.cs** file, which was just created.

1. Open the **ApiPersonController.cs** file to show the generated content.

<a name="Segment4" />
### Running the site ###

1. Press **F5** to run the web site.

1. Navigate to **/MvcPerson**.

---

<a name="summary" />
## Summary ##

By completing this demo you should have:

 * Created a new site using the Web Forms template but including MVC and Web API references.
 * Created a new Person model (int ID, string Name, int Age)
 * Scaffolded Web Forms pages with read / write actions
 * Scaffolded a new MVC controller named MvcPerson
 * Scaffolded a new Web API controller ApiPerson
 * Started the site and browsed to all the generated pages.

---