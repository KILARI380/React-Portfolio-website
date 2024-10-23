# we need to create a create-react-app-my-portfolio on the terminal
# then we need to organize the components folder in src with required components for your website.
# then write the code for the following components.
# App.js
import './App.css';

import React from 'react';
import { motion } from 'framer-motion';
import Header from './components/Header';
import About from './components/About';
import Skills from './components/Skills';
import Projects from './components/Projects';
import Footer from './components/Footer';
import './App.css'; // Optional for styling

function App() {
  return (
    <div className="App">
      <Header />
      <motion.div 
        initial={{ opacity: 0 }} 
        animate={{ opacity: 1 }} 
        transition={{ duration: 1 }}
      >
        <About />
        <Skills />
        <Projects />
      </motion.div>
      <Footer />
    </div>
  );
}

export default App;

 # App.css
 body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f4f4f4;
}

header {
  background: #333;
  color: #fff;
  padding: 1rem;
  text-align: left;
}
h1{
  text-align: center;
  color: orange;
}

h2 {
  color: #333;
  text-align: center;
}

section {
  margin: 2rem;
  padding: 2rem;
  background: #fff;
  border-radius: 5px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.projects-container {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.project-card {
  background: #f8f8f8;
  border-radius: 5px;
  padding: 1rem;
  margin: 1rem;
  width: 300px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.project-card img {
  width: 100%;
  border-radius: 5px;
}

a {
  display: inline-block;
  margin-top: 0.5rem;
  text-decoration: none;
  color: #007bff;
}

Footer{
  text-align: center;
}
p{
  text-align: center;
}
# About.js
import React from 'react';
import { motion } from 'framer-motion';

const About = () => {
  return (
    <motion.section 
      initial={{ x: -100 }} 
      animate={{ x: 0 }} 
      transition={{ duration: 0.5 }}
    >
      <h2>About Me</h2>
      <p>I'm a web developer with a passion for building user-friendly applications. I love coding and continuously learning new technologies.</p>
    </motion.section>
  );
};

export default About;
# Footer.js
import React from 'react';

const Footer = () => {
  return (
    <footer>
      <p>© 2024 Kilari Murali Krishna</p>
    </footer>
  );
};

export default Footer;
# Header.js
import React from 'react';

const Header = () => {
  return (
    <header>
      <h1>KILARI MURALI KRISHNA</h1>
      <h2>Web Developer</h2>
      <nav>
        <ul>
          <li>About</li>
          <li>Skills</li>
          <li>Projects</li>
          <li>Contact</li>
        </ul>
      </nav>
    </header>
  );
};

export default Header;
# Projectcard.js
import React from 'react';
import { motion } from 'framer-motion';

const ProjectCard = ({ project }) => {
  return (
    <motion.div 
      className="project-card" 
      initial={{ scale: 0.9 }} 
      animate={{ scale: 1 }} 
      transition={{ duration: 0.3 }}
    >
      <img src={project.imageUrl} alt={`${project.title} screenshot`} />
      <h3>{project.title}</h3>
      <p>{project.description}</p>
      <a href={project.liveUrl} target="_blank" rel="noopener noreferrer">Live Demo</a>
      <a href={project.repoUrl} target="_blank" rel="noopener noreferrer">View Code</a>
    </motion.div>
  );
};

export default ProjectCard;
# Projects.js
import React from 'react';
import { motion } from 'framer-motion';
import ProjectCard from './ProjectCard';

const Projects = () => {
  const projectData = [
    {
      title: "Open Weather API Key",
      description: "This Weather App allows users to enter a city name and retrieve the current weather data. You can enhance this application further by adding features such as a 5-day forecast, saving favorite cities, or improving error handling.",
      liveUrl: "https://github.com/KILARI380/Open-Weather-API-kEY",
      
    },
    {
      title: "TO-DO List",
      description: "This To-Do list application allows you to add tasks, mark them as complete, and delete them. You can enhance this application further by adding features such as saving tasks in local storage or editing existing tasks.",
      liveUrl: "https://github.com/KILARI380/TO-DO-List",
    },
  ];

  return (
    <motion.section 
      initial={{ opacity: 0 }} 
      animate={{ opacity: 1 }} 
      transition={{ duration: 0.5 }}
    >
      <h2>Projects</h2>
      <div className="projects-container">
        {projectData.map((project, index) => (
          <ProjectCard key={index} project={project} />
        ))}
      </div>
    </motion.section>
  );
};

export default Projects;
# Skills.js
import React from 'react';
import { motion } from 'framer-motion';

const Skills = () => {
  const skills = ["JavaScript", "React", "CSS", "HTML", "Node.js"];

  return (
    <motion.section 
      initial={{ scale: 0 }} 
      animate={{ scale: 1 }} 
      transition={{ duration: 0.5 }}
    >
      <h2>Skills</h2>
      <ul>
        {skills.map((skill, index) => (
          <li key={index}>{skill}</li>
        ))}
      </ul>
    </motion.section>
  );
};

export default Skills;

# After writing code for every component we need check if react app works correctly or links works correctly or else re-check the code for errors.

# After checking if we find no errors we can type npm start to open Personal portfolio website.

# even we can write more in the code later for any further developments. and finally deploy it with Netlify or vercel.
# Thank you
