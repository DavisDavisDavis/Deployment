<img src="https://media4.giphy.com/media/yht1UwF4Bko92/giphy.gif" width="100%">

# 06 - Netlify, Vercel & One.com

Netlify and Vercel are cloud computing companies that offer hosting and serverless backend services for web applications and static websites.

:books: Documentation

- [Netlify](https://docs.netlify.com/site-deploys/create-deploys/)

- [Vercel](https://vercel.com/docs/git-integrations)

- [Github Pages](https://pages.github.com/)

- [Deployments](https://docs.netlify.com/site-deploys/overview/#deploy-summary)

- [Vercel Build Steps](https://vercel.com/docs/build-step)

:headphones: Videos

- [Deploy Websites In Seconds With Netlify](https://www.youtube.com/watch?v=bjVUqvcCnxM)

- [Deploying an application with Vercel](https://www.youtube.com/watch?v=6YRymPx1-4s)

## Excercises

### One.com
1. To host your site using [FTP](https://www.hostinger.com/tutorials/what-is-ftp) head over to your One.com dashboard and click on SSH & FTP under 'advanced settings'. Then make sure the "allow access to SSH & SFTP" box is checked, then press the send-button. Now you should have receieved an e-mail in which you can generate your SFTP password.

3. Download and isntall Filezilla-client. 
	- Mac: remember to place the Filezilla app inside your aplication folder.
	- Windows: just follow the installations. 

4. Enter the information from the SSH & FTP-page on one.com into the quickconnect-section in the Filezilla client.

5. Now let's create the website that we will deploy. To be able to see anything on our new site we need to create a basic HTML file. Remember that web servers are looking for [index](https://en.m.wikipedia.org/wiki/Webserver_directory_index) files if you're visiting the [root domain](https://raventools.com/marketing-glossary/root-domain/)? Start of by making a folder and name it `first-deploy`; open it in Visual Studio Code and create an `index.html` file paste in this code.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Hello world</title>
    <link
      rel="icon"
      href="https://i.pinimg.com/originals/85/7f/d7/857fd79dfd7bd025e4cbb2169cd46e03.png"
    />
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1 class="title">HELLO WORLD!</h1>
    <img src="https://media.tenor.com/2roX3uxz_68AAAAM/cat-space.gif" alt="" />
    <p>This is my first website on the internet!! 💖</p>
  </body>
</html>
```

6. Next create a `style.css` file and paste in the following code.

```css
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@500&family=VT323&family=Work+Sans&display=swap");

* {
  box-sizing: border-box;
}

body {
  display: flex;
  flex-direction: column;
  align-items: center;

  font-family: "Roboto", sans-serif;
  background: black;

  animation: animatedText 3s infinite;
  text-align: center;
}

h1 {
  font-size: 5rem;
}

p {
  color: white;
  font-size: 1.5rem;
}

img {
  width: 50%;
  max-width: 20rem;
}

.title {
  background-image: linear-gradient(
    to right,
    #ff0000,
    #d2f700,
    #d9ff00,
    #00ffdd
  );
  background-clip: text;
  color: transparent;

  background-size: 300%;
  background-position: -100%;

  animation: animatedText 3s infinite alternate-reverse;
}

@keyframes animatedText {
  to {
    background-position: 100%;
  }
}

```

7. Try out your local website first to see if everything works before deploying the website by using using [live server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).

5. Go back to Filezilla and find the `first_deploy` folder that we just made. To upload your files to the server simply drag and drop your folder from the "local site" space into the "remote site" space under the folder bearing your domain-name.

6. Hopefully the site should be live now. Enter your domain-name in your browser of choice and see if everything is working. Remember to follow the filepath in the URL. 
> Keep in mind that One.com can be slow to update so give it a 2-5 mins.

### Netlify
1. Create a new [repository](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-new-repository) on Github.

3. Copy your previous website over to your new Github repo. Add, commit and push your changes to GitHub.

4. Sign up on [Netlify](https://www.netlify.com/) with your Github account.

5. Click on “New site from Git” and add the repository you just created and deploy the site. Navigate to your new site to make sure everything is working.

6. Let's give your site a [cool name](https://media.giphy.com/media/3ohc10GA6j4XrLWzZK/giphy.mp4), see if you can figure out where to change the domain name.

7. Now it's time to personalize your web page by chaning the gif and text to something that you would enjoy. Feel free to tinker around with the css and set it to your liking. 

8. **Extra:** If you have time to spare, you can deploy your new page on [Vercel](https://vercel.com/) as well.
