# Artikel 1
![afbeelding](https://github.com/SafouaneM/weekly-nerd/assets/31611670/97405d5d-2163-44d7-971c-cf90aa5a17dd)

## Introduction to Svelte
Our last weekly nerd session was about having a structured workflow and the differences between a personal project flow and a corporate project flow. She told us that she was an old student from the CMD course. And that she wanted to give us a quick rundown on how things are done in the corporate world. The company’s she has developed web applications for are famous companies in the netherlands like MaxVerstappen, citizen, ajas, NLZiet, en Heineken. But most interestingly she talked about a new framework on the block called *Svelte* and it’s even newer counterpart *SvelteKit*.

## Svelte 
Svelte is a modern JavaScript framework that focuses on creating efficient and performant web applications. It introduces a unique approach to building user interfaces by compiling components at build time instead of running them in the browser. This results in smaller bundle sizes and faster initial page loads compared to frameworks like React and Next.js.

Components in Svelte are reusable building blocks of a web application that consist of HTML, CSS, and JavaScript logic. They encapsulate specific functionality and can be easily composed and reused across different parts of an application. Svelte's component-based architecture promotes code reusability, modularity, and maintainability, allowing developers to build complex UIs with ease.

Since its official announcement on April 13, 2021, SvelteKit has emerged as a promising new contender in the web development landscape. It aims to provide a comprehensive framework for building server-rendered applications with features such as routing, code-splitting, and prefetching. With its focus on performance and developer experience, SvelteKit has gained attention as a potential replacement for React and Next.js, offering a more streamlined and less bloated alternative for web development projects.

### Positives of Svelte:

- Efficiency: Svelte's compilation approach leads to smaller bundle sizes and faster initial page loads compared to frameworks like React or Angular. This optimization enhances the overall performance of web applications.
- Developer Experience: Svelte's syntax is concise and intuitive, making it easier to learn and work with. Its component-based architecture promotes reusability, modularity, and maintainability, allowing developers to build complex UIs more efficiently.
- Framework Size: Svelte is lightweight and has a small footprint. It requires fewer dependencies and reduces the amount of boilerplate code needed, resulting in faster development cycles and improved project maintainability.

### Negatives of Svelte:

- Learning Curve: Despite its intuitive syntax, Svelte introduces a different paradigm and may require some adjustment for developers coming from traditional frameworks like React or Angular. This learning curve can be a challenge for newcomers to the Svelte ecosystem.
- Ecosystem Maturity: While Svelte is gaining popularity, its ecosystem is still growing and evolving. Compared to more established frameworks, the availability of third-party libraries, tools, and resources for Svelte might be relatively limited, requiring developers to be more self-reliant.
- Community Support: As a newer framework, Svelte may have a smaller community compared to frameworks like React or Vue.js. This could mean that finding answers to specific questions or troubleshooting issues may take longer, as there may be fewer community resources available.

## Svelte how to start?
![afbeelding](https://github.com/SafouaneM/weekly-nerd/assets/31611670/638c9a9d-e2a9-4a94-a424-93e5865352f2)
1. As we can see in the picture above we need to install the latest version of Node as we're using the npm package manager.
2. Afterwards as stated on the website we can see that SvelteKit will handle calling the Svelte compiler to convert your .svelte files into .js files that create the DOM and .css files that style it. It also provides all the other pieces you need to build a web application such as a development server, routing, deployment, and SSR support. SvelteKit uses Vite to build your code.
3. After having an empty svelte project we need to start with building our project, as we know in svelte we work component based so let's build our first hello world page and then afterwards build a button that we're going to use on our page.
4. We'll need to head to our src folder, we need to open that folder and then locate the App.Svelte file. This file is the main component of your application:

```svelte
<script>
  //js logic here
</script>

<main>
  <h1>Hello World!</h1>
</main>

<style>
* {
background: red;
color: white;
}
</style>
```

5. Now we can see our Hello World page but we don't have a working button yet let's fix that shall we?
6. Let's create a reusable button component that we can use on our page. Inside the src folder, create a new file called Button.svelte. Open the Button.svelte file and add the following code:
```svelte
<script>
  export let text;

  function handleClick() {
    const iframe = document.createElement('iframe');
    iframe.width = '560';
    iframe.height = '315';
    iframe.src = 'https://streamable.com/jupquu';
    iframe.frameborder = '0';
    iframe.allowfullscreen = 'true';
    document.body.appendChild(iframe);
  }
</script>

<button on:click={handleClick}>{text}</button>

<style>
  button {
    display: inline-block;
    padding: 12px 24px;
    font-size: 18px;
    color: #fff;
    background-color: #4CAF50;
    border: none;
    border-radius: 4px;
    transition: background-color 0.3s ease;
    text-decoration: none;
    cursor: pointer;
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.2);
  }

  button:hover {
    background-color: #45a049;
  }
</style>

```

7. Now let's head towards App.Svelte again and insert the following code:

```svelte
<script>
  import Button from './Button.svelte';</script>
</script>

<main>
  <h1>Hello World!</h1>
  <Button text="Click Me!" />
</main>


<style>
* {
background: red;
color: white;
}
</style>
```
8. Now we have a working Hello-World page that has a button component that links towards a website and we do that via the component instead of hardcoding it. Now the sky is the limit and it's on you how you want to expand this component.

9. Let's test it out https://svelte.dev/repl/00fe9166f40b400cb53d818814f0e5b8?version=4.0.3

After doing this research and after working with it for 5 weeks in the "Meesterproef" I've realised that svelte/kit is a really powerful tool and I'd love to work with it again when & if possible. I truly encourage you as the reader to complexify this example and make your own journey into Svelte. Thanks for reading and have a nice day.


Sources:
https://daily.dev/blog/building-with-svelte-all-you-need-to-know-before-you-start
https://svelte.dev/docs/introduction

