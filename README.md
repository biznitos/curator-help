# Curator Help
You can create quite complex web applications with Curator.
You can to create and manage:

* html pages
* forms
* create content from form submissions
* users
* leads
* files

## Web Pages
While its possible to create many standalone pages, it's better to create one or more layouts to prevent duplication of code.

### Layouts
In the template area create a new page of type "layout". When you do, you will get a sample layout that you can edit.

### Simple web pages
You can create the inner portion of a web page that gets inserted into the layout

### System Variables
Because we use Liquid under the hood, you have access to many system variables

#### System Variables
* {{site_url}}
* {{current_url}}
* {{path_info}}
* {{time}}
* {{year}}
* {{ip_address}}

##### Params from URL
When you make a request, the key and values of any parameters are available as follows
{{params.foo}} - example: https://mysite.com/help?foo=123

##### Environment Variables
The general environment of the person visiting your page is also available
* {{env.host}}
* {{env.method}} -- (GET, POST, PUT, etc)
* {{env.referer}}
* {{env.request_path}}
* {{env.path_info}}
* {{env.query_string}}
* {{env.segments}} -- the segments of a request split into an array

##### Cookies
Any cookies are also available as a map (hash) of keys and values
{{cookies.foo}} - will show the value of the cookie "foo"

##### Site Settings
Information about your site is also available to use:
* {{site.id}}
* {{site.cname}}
* {{site.cname_alt}}
* {{site.name}}
* {{site.description}}
* {{site.settings}}
* {{site.status}}
* {{site.phone}}
* {{site.address}}
* {{site.email}}
* {{site.logo}}



