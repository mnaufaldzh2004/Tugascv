<template>
  <div class="container">
    <header>
     <a href="https://imgbb.com/"><img src="https://i.ibb.co.com/bdz2WTK/nopal-jpg.jpg" alt="nopal-jpg" border="0"></a>
      <h1>{{ name }}</h1>
      <p>{{ title }}</p>
    </header>

    <section class="about">
      <h2>About Me</h2>
      <p>{{ about }}</p>
    </section>

    <section class="experience">
      <h2>Experience</h2>
      <ul>
        <li v-for="job in experiences" :key="job.id">
          <h3>{{ job.title }}</h3>
          <p>{{ job.company }} - {{ job.duration }}</p>
          <p>{{ job.description }}</p>
        </li>
      </ul>
    </section>

    <section class="skills">
      <h2>Skills</h2>
      <ul>
        <li v-for="skill in skills" :key="skill">
          <font-awesome-icon :icon="['fas', 'code']" /> {{ skill }}
        </li>
      </ul>
    </section>

    <footer>
      <a href="https://github.com/username" target="_blank">
        <font-awesome-icon :icon="['fab', 'github']" />
      </a>
      <a href="https://linkedin.com/in/username" target="_blank">
        <font-awesome-icon :icon="['fab', 'linkedin']" />
      </a>
      <a href="mailto:email@example.com">
        <font-awesome-icon :icon="['fas', 'envelope']" />
      </a>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'M Naufal DZ H',
      title: 'Full Stack Developer',
      profileImage: '/profile.jpg',
      about: 'I am a passionate Full Stack Developer with extensive experience in building and maintaining web applications from conception to deployment. With a strong foundation in both front-end and back-end technologies, I thrive in creating seamless, user-friendly experiences that meet business goals. My expertise includes working with JavaScript frameworks like Vue.js and React for the front end, and Node.js or Express on the back end, along with database management using SQL and NoSQL solutions like MongoDB..',
      experiences: [
        { id: 1, title: 'Frontend Developer', company: 'Good Year', duration: 'Jan 2020 - Present', description: 'Developing modern user interfaces using Vue.js and Nuxt.js.' },
        { id: 2, title: 'Backend Developer', company: 'Samsung', duration: 'Feb 2018 - Dec 2019', description: 'Building RESTful APIs using Node.js and Express.' }
      ],
      skills: ['JavaScript', 'Vue.js', 'Nuxt.js', 'Node.js', 'CSS', 'HTML']
    }
  }
}
</script>

<style scoped>
.experience li {
  background-color: #f4f4f4;
  padding: 15px;
  border-radius: 6px;
  margin-bottom: 10px;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

.experience li:hover {
  background-color: #ffebd6;
  transform: scale(1.02);
}

.skills li {
  transition: transform 0.3s ease;
}

.skills li:hover {
  transform: translateY(-5px);
  cursor: pointer;
}

/* assets/css/main.css */
body {
  font-family: 'Poppins', sans-serif;
  background-color: #f9f9f9;
  color: #333;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 900px;
  margin: 0 auto;
  padding: 20px;
  background-color: #fff;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  margin-top: 50px;
}

header {
  text-align: center;
  border-bottom: 2px solid #eee;
  padding-bottom: 20px;
}

.profile-picture {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  margin-bottom: 15px;
  border: 3px solid #ff5722;
}

h1 {
  font-weight: 600;
  color: #333;
}

p {
  color: #666;
}

.about, .experience, .skills {
  margin-top: 30px;
}

.about h2, .experience h2, .skills h2 {
  color: #ff5722;
  font-size: 24px;
  margin-bottom: 15px;
}

.experience ul, .skills ul {
  list-style: none;
  padding: 0;
}

.experience li, .skills li {
  background-color: #f4f4f4;
  padding: 15px;
  border-radius: 6px;
  margin-bottom: 10px;
  transition: background-color 0.3s ease;
}

.experience li:hover, .skills li:hover {
  background-color: #ffebd6;
}

.skills li {
  display: inline-block;
  margin-right: 10px;
  padding: 10px;
}

.skills li:hover {
  cursor: pointer;
}

footer {
  margin-top: 30px;
  text-align: center;
}

footer a {
  margin-right: 15px;
  color: #ff5722;
  text-decoration: none;
  font-size: 20px;
}

footer a:hover {
  color: #ff7e47;
}

</style>
