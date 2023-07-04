# Artikel 1
# Symfony from Campsapce

## Why this research about Symfony
Our very first weekly nerd was from Susan, who is a back-end developer in the company that runs Campspace. What started as a really interesting weekly nerd as she explained to us the importance of trying to understand how a back-end developer has to work with a front-end developer and likewise. However, I noticed that everything seemed cramped, and she was using Symfony. She also showcased some examples of filtering data using Elasticsearch, citing a server issue as the reason for using it instead of the usually reliable MySQL. Personally, I've worked with large amounts of data, and I believe it's more likely a server flaw than a problem with MySQL's performance.
I also observed that the class wasn't really paying attention, so I decided to ask her a question about why the company chose Symfony over a more robust framework called Laravel. Surprisingly, she responded by stating that Laravel is typically used for prototyping and "childish" projects, and it isn't widely used in production. I was taken aback by her response, but I didn't want to bore my classmates, so I chose not to engage in a discussion and simply accepted her statement. However, I would like to add that Laravel is the world's number one PHP framework for a reason, often referred to as "The PHP Framework for Web Artisans." While I acknowledge that Symfony is a powerful tool, it seems unfair to dismiss Laravel as suitable only for trivial projects. Both Symfony and Laravel can be used to build applications ranging from small to enterprise-level. So I thought how about a deeper dive into Symfony?

## Symfony the basics
Symfony is an open-source php framework, it uses a php version of 8.1+. It serves as a web application framework. Symfony provides a set of reusable components and tools for developing robust and scalable web applications using PHP. It follows the Model-View-Controller (MVC) architectural pattern, which helps separate the application logic from the presentation layer.

Symfony's primary role is to handle HTTP requests, route them to the appropriate controllers, and generate HTTP responses. It provides various features and functionalities for managing the application's configuration, handling database operations, managing forms, implementing security measures, and more.

In addition to serving as a web application framework, Symfony can also be used as a backend API framework, allowing developers to build RESTful APIs or microservices. It provides the necessary tools and components for handling API requests, data serialization, authentication, and authorization.

Overall, Symfony simplifies the development process by offering a standardized structure, extensive documentation, and a vibrant community. It is widely adopted by developers for building complex and high-performance PHP applications.

### Step 1 Installation
- PHP 8.1+
- composer install
```code
symfony new my_project_directory --version="6.3.*" --webapp
symfony new my_project_directory --version="6.3.*"
```

![afbeelding](https://github.com/SafouaneM/weekly-nerd/assets/31611670/ea97b9a7-ca47-4ff9-93fd-76b94b278379)
Reference: https://symfony.com/doc/current/setup.html

#### Step 2 Creating our first page
After installing everything we can create our first page, when we're creating a new page we need to create a new view and a new controller so that we can serve the content to the page.

#### Step 3 First creating a new route.yaml
```yaml
app_new_route:
    path: /new-route
    controller: App\Controller\NewRouteController::index
```
#### Step 4 Then afterwards create a NewRouteController:

```php
<?php

namespace App\Controller;

use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route;

class NewRouteController extends AbstractController
{
    /**
     * @Route("/new-route", name="app_new_route")
     */
    public function index(): Response
    {
        return $this->render('new_route/index.html.twig');
    }
}
```

#### Step 5 Create a new Twig template file we've kinda learned this in other lessons but then we used EJS, index.html.twig, in the templates/new_route directory. This file will be rendered by the controller's index method:
```html
{# templates/new_route/index.html.twig #}

<!DOCTYPE html>
<html>
<head>
    <title>New Route</title>
</head>
<body>
    <h1>Welcome to the new route page!</h1>
    <p>This is the content of the new route.</p>
</body>
</html>
```
Start the Symfony development server by running the following command in your project's root directory
```code
symfony serve
```

![afbeelding](https://github.com/SafouaneM/weekly-nerd/assets/31611670/6abc2058-1782-483b-8bf3-7686f845fc2d)


Now, you can access the new route by visiting http://localhost:8000/new-route in your web browser. The index.html.twig template will be rendered, displaying the content defined in the Twig file.

That's it! You have successfully created a new route, view, and page in Symfony. You can customize the route path, controller logic, and view template to suit your specific requirements.

### Conclusion

I still don't think I'd rather use Symfony instead of Laravel as installation and routing and other things seem complexer then they should be. But I respect people if they want to use Symfony if they can comfortably work with it. But I don't accept empty criticism like saying that a different framework is for childish projects only that shouldn't be acceptable. 

#### Sources
Reference: https://symfony.com/doc/current/setup.html




