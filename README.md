Download Link: https://assignmentchef.com/product/solved-web422-assignment-4
<br>
For this assignment, we will be working with a professionally designed Bootstrap 4 “Blog” theme from <a href="https://bootstrapious.com/">https://bootstrapious.com/</a><a href="https://bootstrapious.com/">.</a> (<strong>Important Note: </strong>we are using the “free” version of this template, which means we must keep the footer link back to Bootstrapious, ie: “Template By Bootstrapious” intact in the footer)

The goal of this assignment is to use our knowledge of Angular to begin development and prototyping of a useable and scalable Blogging system User Interface (UI).  We must use the provided HTML &amp; CSS to help guide our design decisions and develop custom components to work with and display data.  We will not have any “live” data for this blog, but we will have some test data that we can use to ensure that all of the components function properly.




Specification:

<h1>Step 1: Creating an Angular App &amp; Downloading the Files</h1>

To begin this project we must create a new Angular app using the @angular/cli command line tool: “ng”.  If you do not have it installed yet, you can pull it from npm using the command:




<h2>npm install -g @angular/cli</h2>




Once the Angular CLI has been installed, you should be able to kickstart a new Angular application with the following command (<strong>Note: </strong>The options here enable routing, skip testing and skip the initialization of a “git” repository, respectfully)




<h2>ng new web422-a4 –routing -S -g</h2>




With our app in place, we must now download the template files.  You will not have to download anything directly from “bootstrapious” – instead, we have provided you with the main files that you will need here:




<a href="https://ict.senecacollege.ca/~patrick.crawford/shared/winter-2020/web422/A4/static.zip">https://ict.senecacollege.ca/~patrick.crawford/shared/winter</a><a href="https://ict.senecacollege.ca/~patrick.crawford/shared/winter-2020/web422/A4/static.zip">–</a><a href="https://ict.senecacollege.ca/~patrick.crawford/shared/winter-2020/web422/A4/static.zip">2020/web422/A4/static.zip</a>




<h1>Step 2: Static Content &amp; Main “View” Components</h1>

Before we start adding the HTML &amp; CSS, we have to make a few updates to our index.html file, ie: Add the following HTML just before the closing &lt;head&gt; tag to the “<strong>index.html</strong>” file.  The paths won’t make any sense yet, but we’ll fix that in the next step:




<em>&lt;!– Bootstrap CSS–&gt;</em>

<strong>&lt;link</strong> rel=”stylesheet” href=”/assets/vendor/bootstrap/css/bootstrap.min.css”<strong>&gt;</strong>

<em>&lt;!– Font Awesome CSS–&gt;</em>

<strong>&lt;link</strong> rel=”stylesheet” href=”/assets/vendor/font-awesome/css/font-awesome.min.css”<strong>&gt;</strong> <em>&lt;!– Custom icon font–&gt;</em>

<strong>&lt;link</strong> rel=”stylesheet” href=”/assets/css/fontastic.css”<strong>&gt;</strong>

<em>&lt;!– Google fonts – Open Sans–&gt;</em>

<strong>&lt;link</strong> rel=”stylesheet” href=”https://fonts.googleapis.com/css?family=Open+Sans:300,400,700″<strong>&gt;</strong>




<em>&lt;!– theme stylesheet–&gt;</em>

<strong>&lt;link</strong> rel=”stylesheet” href=”/assets/css/style.default.css” id=”theme-stylesheet”<strong>&gt;</strong>

<em>&lt;!– Custom stylesheet – for your changes–&gt;</em>

<strong>&lt;link</strong> rel=”stylesheet” href=”/assets/css/custom.css”<strong>&gt;</strong> <em>&lt;!– Favicon–&gt;</em>

<strong>&lt;link</strong> rel=”shortcut icon” href=”/assets/img/favicon.ico”<strong>&gt;</strong>

<em>&lt;!– Tweaks for older IEs–&gt;&lt;!–[if lt IE 9]&gt; </em>

<em>    &lt;script src=”https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js”&gt;&lt;/script&gt; </em>

<em>    &lt;script src=”https://oss.maxcdn.com/respond/1.4.2/respond.min.js”&gt;&lt;/script&gt;&lt;![endif]–&gt;</em>




Next, we must copy the following folders (<strong>from</strong> our download in Step 1) <strong>into</strong> the “<strong>src/assets</strong>” folder within our newly created Angular application:




<ul>

 <li>css</li>

 <li>vendor</li>

 <li>img</li>

 <li>fonts</li>

</ul>




Finally, wipe out all of the content from <strong>app.component.html</strong> and replace it with <strong>&lt;p&gt;App Works!&lt;/p&gt;</strong> (just to render something for the time being).







<h1>Creating new “view” Components</h1>




Now that all of our styles are in place, we must create the primary components that will be rendered using client side routing.  These can be thought of as the “view” components.  Within most of these components, we will be creating smaller components.  However, before we do that, let’s get the boilerplate code for each “view” added in its own component:




For the next steps, use the Angular CLI (ng) to create the following components with boilerplate templates from the files provided (step 1)







<h2>HeaderComponent (header.component.ts)</h2>

<strong> </strong>

<ul>

 <li>Once you have created this component, copy the contents of the file “<strong>html</strong>” into the contents of “header.component.html” (replacing the automatically-generated paragraph element) and save the file.</li>

 <li>If you wish to test it at this time, you can add the <strong>&lt;app-header&gt;&lt;/app-header&gt;</strong> component to the <strong>component.html</strong> file</li>

</ul>




<h2>FooterComponent (footer.component.ts)</h2>

<strong> </strong>

<ul>

 <li>Once you have created this component, copy the contents of the file “<strong>html</strong>” into the contents of “footer.component.html” (replacing the automatically-generated paragraph element) and save the file.</li>

 <li>If you wish to test it at this time, you can add the <strong>&lt;app-footer&gt;&lt;/app-footer&gt;</strong> component to the <strong>component.html</strong> file</li>

</ul>

<strong> </strong>

<h2>HomeComponent (home.component.ts)</h2>

<strong> </strong>

<ul>

 <li>Once you have created this component, copy the contents of the file “<strong>html</strong>” into the contents of “home.component.html” (replacing the automatically-generated paragraph element) and save the file.</li>

 <li>If you wish to test it at this time, you can add the <strong>&lt;app-home&gt;&lt;/app-home&gt;</strong> component to the <strong>component.html</strong> file (ideally between the header and footer)</li>

</ul>

<strong> </strong>

<h2>BlogComponent (blog.component.ts)</h2>

<strong> </strong>

<ul>

 <li>Once you have created this component, copy the contents of the file “<strong>html</strong>” into the contents of “blog.component.html” (replacing the automatically-generated paragraph element) and save the file.</li>

 <li>If you wish to test it at this time, you can add the <strong>&lt;app-blog&gt;&lt;/app-blog&gt;</strong> component to the <strong>component.html</strong> file (ideally between the header and footer – you may want to comment out &lt;apphome&gt;&lt;/app-home&gt; if it was previously added)</li>

</ul>

<strong> </strong>

<h2>PostComponent (post.component.ts)</h2>

<strong> </strong>

<ul>

 <li>Once you have created this component, copy the contents of the file “<strong>html</strong>” into the contents of “post.component.html” (replacing the automatically-generated paragraph element) and save the file.</li>

 <li>If you wish to test it at this time, you can add the <strong>&lt;app-post&gt;&lt;/app-post&gt;</strong> component to the <strong>component.html</strong> file (ideally between the header and footer– you may want to comment out &lt;appblog&gt;&lt;/app-blog&gt; if it was previously added)</li>

</ul>

<strong> </strong>

<strong>PageNotFoundComponent (page-not-found.component.ts) </strong>

<strong> </strong>

<ul>

 <li>You are free to put whatever you like in this template – it’s the “404” view for our application</li>

</ul>

<h1>Step 3: Main Route Configuration</h1>




Now that our main components are in place, it’s a good idea to get “routing” up and running to make it easier to test and develop each individual view.  To begin, configure the following routes in your  <strong>app-routing.module.ts</strong> file by adding the configurations to the <strong>Routes</strong> array:




<ul>

 <li><strong>Path: “home” – </strong>Shows the <strong>HomeComponent </strong></li>

 <li><strong>Path: “blog” – </strong>Shows the <strong>BlogComponent </strong></li>

 <li><strong>Path: “post” – </strong>Shows the <strong>PostComponent </strong></li>

 <li><strong>Path: “” – </strong>Redirects to the “/home” Route</li>

 <li><strong>No Route Found – </strong>Shows the <strong>PageNotFoundComponent </strong></li>

</ul>

<strong> </strong>

Once this is complete, place the “router outlet” component <strong>(&lt;router-outlet&gt;&lt;/router-outlet&gt;) </strong>between the &lt;app-header&gt;&lt;/app-header&gt; and &lt;app-footer&gt;&lt;/app-footer&gt; components in your <strong>app.component.html</strong> file.




As a final task before we start configuring our individual “views”, let’s make the “header” work with our Angular Routing components:




<ul>

 <li>Replace all 3 <strong>href</strong> properties with <strong>routerLink </strong>– this will ensure that whenever they are clicked, it will use our Angular routing instead of the default browser routing.</li>

 <li>Next, to ensure that our menu items are correctly <strong><u>highlighted</u></strong>, add the following “directive” to the <strong>same 3 anchor elements</strong>:</li>

</ul>

o <strong>routerLinkActive=”active” </strong>







<h1>Step 4: Mock “Blog” Data</h1>

Before we start dividing our views into reusable components (you probably have spotted all of the “widgets” in the side bar – these are perfect candidates), let’s add a few fake blog posts.




Since we’re using typescript, it makes sense for our data to be “typed” – ie: we must have a “class” to define the “shape” of each post.  To achieve this, add the following 2 files / content




<h2>Comment.ts</h2>

<strong> </strong>

<strong>export</strong> <strong>class</strong> Comment{

_id: string     author: string;     comment: string;

date: string;

}

<strong> </strong>

<h2>BlogPost.ts</h2>

<strong> </strong>

<strong>import</strong> { Comment } from “./Comment”;




<strong>export</strong> <strong>class</strong> BlogPost{

_id: string

title: string;     postDate: string;     featuredImage: string;

post: string;

postedBy: string;

comments: Array&lt;Comment&gt;;

category: string;     tags: Array&lt;string&gt;;     isPrivate: Boolean;

views: number;

}




Next, we must copy the <strong>blogData.json</strong> file (from our files included with the download in step 1) and place it within the “app” folder.  This will serve as our sample data for the blog.




Unfortunately, if we want to actually “import” this json file in any of our components, we must add a couple of

“compiler options” to our typescript configuration, ie: add the following two properties to the

<h3>“compilerOptions” property in the “tsconfig.base.json” file</h3>




<ul>

 <li>“resolveJsonModule”: true</li>

 <li>“esModuleInterop”: true</li>

</ul>




Now, if we want to ever pull in the data, we can add the following “import” lines in our component files:




<h3>import blogData from ‘../blogData.json’; import { BlogPost } from ‘../BlogPost’;</h3>

<strong> </strong>

In fact, since our “BlogComponent” will need the blog data, let’s proceed to add the above two “import” lines to the top of the <strong>blog.component.ts</strong> file now.




Inside the <strong>BlogComponent</strong> class, add the following property declaration:




<h3>blogPosts: Array&lt;BlogPost&gt; = blogData;</h3>

<strong> </strong>

This will ensure that our data is loaded as “blogPosts” before we start the next part of the assignment (in the future, this would come from a service which accesses a WEB API endpoint for data).







<h1>Step 5: “Blog” view components</h1>




If you open your app to the “blog” route, you will notice that we have quite a few “containers” in the UI that manage data.  In the next part of this assignment, we will build out components for these containers <strong><u>PostCardComponent</u> </strong>










This component will be responsible for rendering the above chunk of UI (<strong>Hint</strong>: all the code <strong><em>inside</em></strong> &lt;div class=”post col-xl-6″&gt;…&lt;/div&gt;, so use that as your template starting point).




To get started, create the component using the <strong><em>ng g c</em></strong> (ng generate component) command, then proceed to implement the component according to the following specifications:




<ul>

 <li>It must receive a single property <strong>post</strong>. The type of this property will be <strong>BlogPost</strong> (therefore, { BlogPost } must be imported from ‘../BlogPost’ and the @Input() decorator must also be used.  Do not forget to import “Input” from @angular/core</li>

 <li>It must be rendered using the class property: “class=”post col-xl-6”, ie: “&lt;app-post-card class=”post col-xl-6″&gt;”</li>

 <li>Its “post-thumbnail” element must show the post’s “featuredImage”</li>

 <li>Its “date meta-last” element must show the post’s “postDate”</li>

 <li>Its “cateogory” element must show the post’s “category”</li>

 <li>Its “&lt;h3 class=”h4”&gt; element must show the post’s “title”</li>

 <li>Its ” &lt;p class=”text-muted”&gt; element must be changed to a &lt;div&gt; element instead (ie: “&lt;div class=”textmuted”&gt;…&lt;/div&gt;”. Also its “innerHtml” property must be set to the post’s “post”</li>

 <li>Its “avatar” image must be changed to “/assets/img/user.svg”</li>

 <li>Its “title” element must show the post’s “postedBy”</li>

 <li>Its “date” element (next to the clock) must show the post’s “postDate”</li>

 <li>Its “meta-last” element must show the number of comments, ie comments.length</li>

</ul>




Once this is done, use the new “app-post-card” in place of the existing elements in the “blog.component.html” template.  You should be able to show one app-post-card per “post” in the “blogPosts” array using *ngFor.




Using our sample data, your “blog” page should now look like the below screenshot:










<h2>SearchWidgetComponent</h2>










This component simply renders the “widget-search” element, so use that as your template starting point.




To get started, create the component using the <strong><em>ng g c</em></strong> (ng generate component) command.  We will use this to render the template only – we not be implementing any logic at this time.







<h2>LatestPostsComponent</h2>

<strong> </strong>







This component will be responsible for rendering the above chunk of UI (<strong>Hint</strong>: this is the &lt;div class=”widget latest-posts”&gt; element, so use that as your template starting point).




To get started, create the component using the <strong><em>ng g c</em></strong> (ng generate component) command, then proceed to implement the component according to the following specifications:




<ul>

 <li>It must receive a single property <strong>posts</strong>. The type of this property will be <strong>Array&lt;BlogPost&gt;</strong> (therefore,</li>

</ul>

{ BlogPost } must be imported from ‘../BlogPost’ and the @Input() decorator must also be used.  Do not forget to import “Input” from @angular/core

<ul>

 <li>Inside the template, you will notice three “item” elements, each nested inside an “&lt;a href=”#”&gt;” element. The idea is that we must render one “item” link for every “post” in the “posts” array according to the following:

  <ul>

   <li>Its “image” element must show the post’s “featuredImage”</li>

   <li>Its “title” element must show the post’s “title” o Its “views” element must show the post’s “views”</li>

   <li>Its “comments” element must show the number of comments, ie comments.length</li>

  </ul></li>

</ul>

Note: When you include the component, you can limit the number of “blogPosts” that you provide to the component using the code:




<h3>&lt;app-latest-posts [posts]=”blogPosts.slice(0,3)”&gt;&lt;/app-latest-posts&gt;</h3>




When complete, your component should look like:











































<h2>CategoriesComponent</h2>

<strong> </strong>







This component will be responsible for rendering the above chunk of UI (<strong>Hint</strong>: this is the &lt;div class=”widget categories”&gt; element, so use that as your template starting point).




To get started, create the component using the <strong><em>ng g c</em></strong> (ng generate component) command, then proceed to implement the component according to the following specifications:




<ul>

 <li>In the future, this component would have to worry about fetching the category data on its own. In the meantime, hardcode the following array as the component’s single property:</li>

</ul>




<strong>categories</strong>: Array&lt;<strong>any</strong>&gt; = [   {cat: “Crime”, num: 2},

{cat: “Comedy”, num: 1},

{cat: “Musical”, num: 1},

{cat: “Adventure”, num: 2},

{cat: “Drama”, num: 2},

{cat: “Action”, num: 2},

{cat: “Documentary”, num: 1},

{cat: “Thriller”, num: 1}

];




<ul>

 <li>In the template, you will notice that &lt;div class=”item d-flex justify-content-between”&gt;…&lt;/div&gt; is repeated once per category. We will use our “categories” array to accomplish the same output, ie: looping through the array and outputting one “item” per element.</li>

</ul>






















When complete, your component should look like:













<h2>TagsComponent</h2>










The <strong>TagsComponent</strong> functions very much like the CategoriesComponent in that it doesn’t accept any props and (for now) we will hardcode the existing tags into a “tags” array, ie:




tags: Array&lt;string&gt; =[

“#funny”,

“#dramatic”,

“#rental”,

“#seeagain”,

“#spooky”,

“#worththecost”,

“#lovedIt”,

“#scary”,

“#silly”,

“#good4kidz”

];

In the template, you will notice that &lt;li class=”list-inline-item”&gt;…&lt;/li&gt; is repeated once per category.  We will use our “tag” array to accomplish the same output, ie: looping through the array and outputting one “listinline-item” per element.




When complete, your component should look like:










<h1>Step 6: “Post” view components</h1>

Now that we have completed all of the “Blog” view components, we can move on to the “Post” view components.  The good news here is that that we can reuse most of the components from the “Blog” view




To get started, we will follow along with the same procedure as the “Blog” component, ie adding in the “blogPosts” array:




First, add the following “import” lines in our post.component.ts file:




<strong>import blogData from ‘../blogData.json’; import { BlogPost } from ‘../BlogPost’; </strong>




Next, inside the <strong>PostComponent</strong> class, add the following property declaration:




<h2>blogPosts: Array&lt;BlogPost&gt; = blogData;</h2>

<strong> </strong>

This will ensure that our data is loaded as “blogPosts” (once again – in the future, this would come from a service which accesses a WEB API endpoint for data).







<h2>Reusing the &lt;aside&gt; from blog.component.html</h2>




If you take a look at your completed blog.component.html, you should notice that your &lt;aside&gt; element is now much smaller than it used to be, ie:




&lt;aside class=”col-lg-4″&gt;

&lt;!– Widget [Search Bar Widget]–&gt;

&lt;app-search-widget&gt;&lt;/app-search-widget&gt;

&lt;!– Widget [Latest Posts Widget] –&gt;

&lt;app-latest-posts [posts]=”blogPosts.slice(0,3)”&gt;&lt;/app-latest-posts&gt;

&lt;!– Widget [Categories Widget]–&gt;

&lt;app-categories&gt;&lt;/app-categories&gt;

&lt;!– Widget [Tags Cloud Widget]–&gt;

&lt;app-tags&gt;&lt;/app-tags&gt;

&lt;/aside&gt;




You will also notice that we have the exact same &lt;aside&gt; element in our post.component.html file (starting at line 100).  For this next step, simply copy your full &lt;aside&gt; element from your blog.component.html and paste it in place of the existing &lt;aside&gt; within your post.component.html file!







<h2>PostDataComponent (The last one!)</h2>

<strong> </strong>

This Final Component is basically the entire “post single” div from the sample html, ie: “&lt;div class=”postsingle”&gt;…&lt;/div&gt;” (everything from line 6 to line 94 inclusive).  So, to get started wiring up this component, simply <u>cut</u> all of that HTML including the &lt;div class=”post-single”&gt;…&lt;/div&gt; container element, and <strong>paste</strong> it into your post-data.component.html.  Then, in its place add back:




<h3>&lt;app-post-data [post]=”blogPosts[0]”&gt;&lt;/app-post-data&gt;</h3>

<strong> </strong>

Note: We will simply be hard-coding the first blog post for now.




Next, once your html is in the right place (post-data.component.html) we can start working with the template according to the following specifications:




<ul>

 <li>It must receive a single property <strong>post</strong>. The type of this property will be <strong>BlogPost</strong> (therefore, { BlogPost } must be imported from ‘../BlogPost’ and the @Input() decorator must also be used.  Do not forget to import “Input” from @angular/core</li>

 <li>The “post-thumbnail” must show the post’s “featuredImage”</li>

 <li>The “category” must show the post’s “category”</li>

 <li>The &lt;h1&gt;…&lt;/h1&gt; element must show the post’s “title”</li>

 <li>The “avatar” must be changed to show “/assets/img/user.svg”</li>

 <li>The “title” (directly beneath avatar) must show the post’s “postedBy”</li>

 <li>The “date” element (next to the clock) must show the post’s “postDate”</li>

 <li>The “views” element (next to the eye) must show the post’s “views”</li>

 <li>The “comments” element must show the number of comments, ie comments.length</li>

 <li>The “post-body” innerHTML property must be set to the post’s “post”</li>

 <li>The “post-tags” must show one “&lt;a href=”#” class=”tag”&gt;…&lt;/a&gt; element for every tag in the post’s “tags” array such that the content of the &lt;a&gt; shows the value of a tag used in the post</li>

 <li>The “no-of-comments” must show the number of comments, ie comments.length</li>

</ul>

The last piece of this component implementation is the “comments” list.  To complete this, we must iterate over the “comments” array and display a &lt;div class=”comment”&gt;…&lt;/div&gt;” for every comment in the array.

This will involve updating the following “comment” related elements:




<ul>

 <li>The “title” should show the current comment’s “author”</li>

 <li>The “data” should show the current comment’s “date”</li>

 <li>The “comment body” innerHTML property must be set to the current comment’s “comment” Step 7:Updating Links and Testing</li>

</ul>




You will notice that there are a few things that are missing from our solution. Most notably the out of date, static blog posts on the Home page and in the footer.  If you require additional practice with components please feel free to use the knowledge gained from updating the “Blog” and “Post” views to refactor these views as well.




Also, you will notice that there’s a lot of “href” links still in the solution.  Unless the app requires the user to navigate away (ie: heading to twitter, etc.) then “href” should be replaced with “routerLink”, ie:




<ul>

 <li><strong>href=”#”</strong> should be replaced with <strong><u>routerLink</u></strong></li>

 <li><strong>href=”post.html”</strong> should be replaced with <strong>routerLink=”/post”</strong></li>

</ul>




Once this is complete, you should be ready to submit.  However have a look at the full-page screenshots of the app and compare your results with what you see.  Everyone is using the data, so it should look identical (unless you added some additional styling).




<ul>

 <li><a href="https://ict.senecacollege.ca/~patrick.crawford/shared/winter-2020/web422/A4/home.png">Home</a> <a href="https://ict.senecacollege.ca/~patrick.crawford/shared/winter-2020/web422/A4/home.png">View</a> (Sample)</li>

 <li><a href="https://ict.senecacollege.ca/~patrick.crawford/shared/winter-2020/web422/A4/blog.png">Blog View</a> (Sample)</li>

 <li><a href="https://ict.senecacollege.ca/~patrick.crawford/shared/winter-2020/web422/A4/post.png">Post View</a> (Sample)</li>

 <li><a href="https://ict.senecacollege.ca/~patrick.crawford/shared/winter-2020/web422/A4/404.png">404</a> <a href="https://ict.senecacollege.ca/~patrick.crawford/shared/winter-2020/web422/A4/404.png">View</a> (Sample)</li>

</ul>


