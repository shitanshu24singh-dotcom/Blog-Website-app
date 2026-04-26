<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Blog Website App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f9;
      margin: 0;
      padding: 0;
    }
    header {
      background: #2196F3;
      color: white;
      padding: 15px;
      text-align: center;
    }
    nav {
      background: #1976D2;
      padding: 10px;
      text-align: center;
    }
    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
    }
    .container {
      display: flex;
      margin: 20px;
    }
    .content {
      flex: 3;
      margin-right: 20px;
    }
    .sidebar {
      flex: 1;
      background: #fff;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .post {
      background: #fff;
      padding: 20px;
      margin-bottom: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .post h2 {
      margin-top: 0;
    }
    footer {
      background: #2196F3;
      color: white;
      text-align: center;
      padding: 10px;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <header>
    <h1>My Blog</h1>
    <p>Sharing thoughts and ideas</p>
  </header>

  <nav>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
  </nav>

  <div class="container">
    <div class="content" id="blogContent">
      <!-- Blog posts will load here -->
    </div>

    <aside class="sidebar">
      <h3>About Me</h3>
      <p>Hi, I’m the author of this blog. I love coding and sharing knowledge.</p>
      <h3>Categories</h3>
      <ul>
        <li>Web Development</li>
        <li>Design</li>
        <li>Personal</li>
      </ul>
    </aside>
  </div>

  <footer>
    <p>&copy; 2026 My Blog. All rights reserved.</p>
  </footer>

  <script>
    const posts = [
      {
        title: "First Blog Post",
        date: "April 26, 2026",
        content: "Welcome to my blog! This is my first post. I’ll be sharing tutorials, thoughts, and updates here."
      },
      {
        title: "Second Blog Post",
        date: "April 25, 2026",
        content: "Here’s another entry. You can add as many posts as you like by updating the posts array."
      }
    ];

    const blogContent = document.getElementById("blogContent");

    function loadPosts() {
      posts.forEach(post => {
        const div = document.createElement("div");
        div.className = "post";
        div.innerHTML = `
          <h2>${post.title}</h2>
          <p><em>${post.date}</em></p>
          <p>${post.content}</p>
        `;
        blogContent.appendChild(div);
      });
    }

    loadPosts();
  </script>
</body>
</html>
