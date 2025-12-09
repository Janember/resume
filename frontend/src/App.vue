<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 text-white">
    <nav class="fixed top-0 left-0 right-0 z-50 bg-slate-900/80 backdrop-blur-lg border-b border-white/10">
      <div class="container mx-auto px-4">
        <div class="flex items-center justify-between h-16">
          <div class="text-xl bg-gradient-to-r from-pink-400 to-purple-400 bg-clip-text text-transparent cursor-pointer 
          transform transition-transform duration-300 ease-out hover:scale-105">
            JanePortfolio
          </div>
          <div class="hidden md:flex items-center gap-8">
            <button
              v-for="item in navItems"
              :key="item.id"
              @click="scrollToSection(item.id)"
              :class="[
                'cursor-pointer relative transition-colors text-gray-300 hover:text-pink-400',
                activeSection === item.id ? 'text-pink-400 font-semibold' : ''
              ]"
            >
              {{ item.label }}
              <div
                class="absolute -bottom-1 left-0 right-0 h-0.5 bg-gradient-to-r from-pink-400 to-purple-400 rounded-full 
                      transition-all duration-300 origin-left"
                :class="activeSection === item.id ? 'scale-x-100 opacity-100' : 'scale-x-0 opacity-0'"
              ></div>
              
            </button>
          </div>
        </div>
      </div>
    </nav>
    <main class="relative z-10">
      <section id="home">
        <div class="min-h-screen flex items-center justify-center relative overflow-hidden pt-16">
          <div class="absolute inset-0">
            <img 
              src="/profile_picture.png"
              class="w-full h-full object-cover opacity-20"
            >
            <div class="absolute inset-0 bg-gradient-to-b from-slate-900/50 via-purple-900/50 to-slate-900"></div>
          </div>
          <div class="container mx-auto px-4 relative z-10">
            <div class="max-w-4xl mx-auto text-center">
              <div class="mb-8">
                <div class="w-40 h-40 mx-auto rounded-full bg-gradient-to-br from-pink-500 via-purple-500 to-blue-500 p-1">
                  <div class="w-full h-full rounded-full overflow-hidden bg-slate-900 flex items-center justify-center">
                    <img
                      src="/profile_picture.png"
                      class="w-full h-full object-cover scale-130 translate-x-2"
                      alt="Profile Picture"
                    >
                  </div>
                </div>
              </div>
              <div style="opacity: 1; transform: none;">
                <h1
                  class="text-outline text-5xl md:text-7xl mb-4 font-bold
                        bg-gradient-to-r from-pink-400 via-purple-400 to-blue-400
                        bg-clip-text text-transparent
                        drop-shadow-[0_0_4px_rgba(255,255,255,0.8)]
                  "
                >
                  Jane
                </h1>
                <p class="text-2xl md:text-3xl text-gray-300 mb-6">
                  Full Stack Developer
                </p>
                <p class="text-lg text-gray-400 max-w-2xl mx-auto mb-8">
                  I'm someone who's passionate about gaming and learning the complex algorithms that games use. Also some web development
                </p>
              </div>
            </div>
            <div class="flex items-center justify-center gap-4 mb-12">
              <a 
                href="https://github.com/Janember" 
                target="_blank" 
                rel="noopener noreferrer"
                class="p-3 rounded-full bg-white/10 hover:bg-white/20 transition-colors border border-white/20 hover:border-pink-400"
              >
              <img src="/github.svg" class="w-6 h-6 invert">
              </a>
              <a 
                href="https://www.linkedin.com/in/jan-ember-462809198/" 
                target="_blank" 
                rel="noopener noreferrer"
                class="p-3 rounded-full bg-white/10 hover:bg-white/20 transition-colors border border-white/20 hover:border-pink-400"
              >
              <img src="/linkedin.svg" class="w-6 h-6 invert">
              </a>
              <a 
                href="mailto:janember516@gmail.com" 
                target="_blank" 
                rel="noopener noreferrer"
                class="p-3 rounded-full bg-white/10 hover:bg-white/20 transition-colors border border-white/20 hover:border-pink-400"
              >
              <Mail class="w-6 h-6 text-white"></Mail>
              </a>
            </div>
            <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
              <button class="text-white px-8 py-3 bg-gradient-to-r from-pink-500 to-purple-500 rounded-full hover:shadow-lg hover:shadow-pink-500/50 transition-all">
                View My Work
              </button>
              <button class="text-white px-8 py-3 border-2 border-white/20 rounded-full hover:bg-white/10 transition-all">
                Get In Touch
              </button>
            </div>
          </div>
          <button 
            class="absolute bottom-8 left-1/2 transform -translate-x-1/2 text-white/60 hover:text-white transition-colors float-animation"
            @click="scrollToSection('about')"
            >
            <ChevronDown></ChevronDown>
          </button>
        </div>
      </section>
      <section id="about">
        <div class="min-h-screen flex !py-20">
          <div class="container mx-auto px-4">
            <div class="text-center mb-16">
              <h2 class="text-4xl md:text-5xl mb-4 bg-gradient-to-r from-pink-400 to-purple-400 bg-clip-text text-transparent">
                About Me
              </h2>
              <div class="w-20 h-1 bg-gradient-to-r from-pink-500 to-purple-500 mx-auto"></div>
            </div>
            <div class="grid md:grid-cols-2 gap-12 items-center max-w-6xl mx-auto">
              <div class="relative">
                <div class="relative rounded-2xl overflow-hidden border-2 border-white/20 shadow-2xl">
                  <img class="h-96 w-full object-cover" src="/about_me.png">
                  <div class="absolute inset-0 bg-gradient-to-br from-purple-600/30 to-pink-600/30"></div>
                </div>
              </div>
              <div class="space-y-6">
                <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-8 border border-white/10">
                  <h3 class="text-2xl mb-4 text-pink-300">Who I Am</h3>
                  <p class="text-gray-300 leading-relaxed mb-4">
                    I’m someone who has always been curious about how things work behind the scenes. This curiosity initially led me into gaming, where I didn’t just play but also explored modding and scripting, trying to understand the mechanics and inner workings of the games I enjoyed. This passion for exploration naturally evolved into an interest in programming.                  
                  </p>
                  <p class="text-gray-300 leading-relaxed mb-4">
                    I began my programming journey with Python, experimenting with small projects and scripts that expanded my understanding of logic and problem-solving. From there, I explored C# and other languages, gradually building a foundation that allowed me to experiment with web development. This hands-on approach helped me gain practical experience and a deeper understanding of how software and web applications are built.                  
                  </p>
                  <p class="text-gray-300 leading-relaxed">
                    Eventually, my focus shifted toward web development, starting with the basics—HTML, CSS, JavaScript, and PHP—and later advancing into modern frameworks like React, Vue, and Tailwind. Through these experiences, I’ve had the opportunity to work on a few projects professionally, which strengthened both my technical skills and my ability to turn ideas into functioning applications.         
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section id="experience">
        <div class="min-h-screen flex !py-20">
          <div class="container mx-auto px-4">
            <div class="text-center mb-16">
              <h2 class="text-4xl md:text-5xl mb-4 bg-gradient-to-r from-pink-400 to-purple-400 bg-clip-text text-transparent">
                Work Experience
              </h2>
              <div class="w-20 h-1 bg-gradient-to-r from-pink-500 to-purple-500 mx-auto"></div>
            </div>
            <div class="max-w-4xl mx-auto">
              <div class="relative">
                <div class="absolute left-8 md:left-1/2 top-0 bottom-0 w-0.5 bg-gradient-to-b from-pink-500 via-purple-500 to-blue-500"></div>
                <div class="relative mb-12 md:pr-1/2">
                  <div class="absolute left-8 md:left-1/2 transform md:-translate-x-1/2 w-4 h-4 rounded-full bg-pink-500 ring-4 ring-pink-500/30"></div>
                  <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 hover:border-white/30 transition-all">
                    <div class="mb-4">
                      <div class="flex items-start justify-between gap-4 mb-2">
                        <div>
                          <h3 class="text-xl text-pink-300 mb-1">
                            Customer Service Representative
                          </h3>
                          <p class="text-lg text-white">
                            EHP Consulting Group
                          </p>
                        </div>
                        <span class="px-3 py-1 bg-gradient-to-r from-pink-500 to-purple-500 rounded-full text-xs shrink-0">
                          Current
                        </span>
                      </div>
                      <div class="flex flex-wrap gap-4 text-sm text-gray-400">
                        <div class="flex items-center gap-1 ">
                          <MapPin class="w-4 h-4"/>
                          <span>Tampa, FL</span>
                        </div>
                        <div class="flex items-center gap-1">
                          <Calendar class="w-4 h-4"/>
                          <span>2021-Present</span>
                        </div>
                      </div> 
                    </div>
                    <div class="space-y-2">
                      <div class="flex items-start gap-2 text-sm text-gray-300">
                        <BadgeCheck class="mt-0.5 w-4 h-4 text-green-400"/>
                        <span>Retained dissatisfied customers by offering quick resolutions</span>
                      </div>
                      <div class="flex items-start gap-2 text-sm text-gray-300">
                        <BadgeCheck class="mt-0.5 w-4 h-4 text-green-400"/>
                        <span>Helped train and mentor new staff to improve performance</span>
                      </div>
                      <div class="flex items-start gap-2 text-sm text-gray-300">
                        <BadgeCheck class="mt-0.5 w-4 h-4 text-green-400"/>
                        <span>Managed virtual machines in Amazon's AWS</span>
                      </div>
                      <div class="flex items-start gap-2 text-sm text-gray-300">
                        <BadgeCheck class="mt-0.5 w-4 h-4 text-green-400"/>
                        <span>Created SOPs to assist the whole department</span>
                      </div>
                    </div>
                  </div>
                  
                </div>
                <div class="relative mb-12 md:pr-1/2">
                  <div class="bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 hover:border-white/30 transition-all">
                    <div class="mb-4">
                      <div class="flex items-start justify-between gap-4 mb-2">
                        <div>
                          <h3 class="text-xl text-pink-300 mb-1">
                            On-the-Job Trainee
                          </h3>
                          <p class="text-lg text-white">
                            Custard Apple Outsourcing Inc.
                          </p>
                        </div>
                      </div>
                      <div class="flex flex-wrap gap-4 text-sm text-gray-400">
                        <div class="flex items-center gap-1 ">
                          <MapPin class="w-4 h-4"/>
                          <span>Gensan, PH</span>
                        </div>
                        <div class="flex items-center gap-1">
                          <Calendar class="w-4 h-4"/>
                          <span>2025</span>
                        </div>
                      </div> 
                    </div>
                    <div class="space-y-2">
                      <div class="flex items-start gap-2 text-sm text-gray-300">
                        <BadgeCheck class="mt-0.5 w-4 h-4 text-green-400"/>
                        <span>Edited 10+ short-form videos using tools like Adobe Premiere Pro, or CapCut</span>
                      </div>
                      <div class="flex items-start gap-2 text-sm text-gray-300">
                        <BadgeCheck class="mt-0.5 w-4 h-4 text-green-400"/>
                        <span>Successfully installed, updated, and configured a custom Linux distro.</span>
                      </div>
                      <div class="flex items-start gap-2 text-sm text-gray-300">
                        <BadgeCheck class="mt-0.5 w-4 h-4 text-green-400"/>
                        <span>Created documentation utilizing AI and other tools</span>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section id="skills">
        <div class="min-h-screen flex  !py-20">
          <div class="container mx-auto px-4">
            <div class="text-center mb-16">
              <h2 class="text-4xl md:text-5xl mb-4 bg-gradient-to-r from-pink-400 to-purple-400 bg-clip-text text-transparent">
                Skills & Technologies
              </h2>
              <div class="w-20 h-1 bg-gradient-to-r from-pink-500 to-purple-500 mx-auto"></div>
            </div>
            <div class="flex flex-wrap justify-center gap-3 mb-12">
              <Button
                v-for="cat in categories"
                :key="cat"
                @click="selectedCategory = cat"
                class="px-6 py-2 rounded-full transition-all bg-white/5 border border-white/10 hover:bg-white/10"
                :class="selectedCategory === cat ? 'bg-gradient-to-r from-pink-500 to-purple-500 shadow-lg shadow-pink-500/30' : ''"
              >
                {{ cat }}
              </Button>
            </div>
            <div class="max-w-6xl mx-auto">
              <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div
                  v-for="skill in filteredSkills"
                  :key="skill.name"
                  class="backdrop-blur-sm rounded-xl p-6 transition-all"
                  :class="[
                    `bg-gradient-to-br ${categoryColors[skill.type].from} ${categoryColors[skill.type].to}`,
                    categoryColors[skill.type].border,
                    'hover:border-white/30 border'
                  ]"
                >
                  <div class="flex items-center gap-3 mb-4">
                    <div class="text-3xl">
                      {{ skill.icon }}
                    </div>

                    <div class="flex-1">
                      <h3 class="text-lg text-white">{{ skill.name }}</h3>
                      <p class="text-xs text-gray-400">{{ skill.type }}</p>
                    </div>
                    <span class="text-sm text-gray-300">{{ skill.progress }}%</span>
                  </div>
                  <div class="relative h-2 bg-black/30 rounded-full overflow-hidden">
                    <div
                      class="absolute inset-y-0 left-0 rounded-full"
                      :class="`bg-gradient-to-r ${categoryColors[skill.type].barFrom} ${categoryColors[skill.type].barTo}`"
                      :style="{ width: skill.progress + '%' }"
                    ></div>
                    <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/20 to-transparent animate-pulse"></div>
                  </div>
                </div>
              </div>
              <div class="max-w-4xl mx-auto mt-12 bg-white/5 backdrop-blur-sm rounded-2xl p-8 border border-white/10">
                <h3 class="text-xl text-pink-300 mb-4">Additional Expertise</h3>
                <div class="flex flex-wrap gap-3">
                  <span 
                    v-for="exp in Expertises" 
                    :key="exp" 
                    class="px-4 py-2 bg-white/10 rounded-full text-sm text-gray-300 border border-white/20"
                  >
                    {{ exp }}
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section id="projects">
        <div class="min-h-screen flex  !py-20">
          <div class="container mx-auto px-4">
            <div class="text-center mb-16">
              <h2 class="text-4xl md:text-5xl mb-4 bg-gradient-to-r from-pink-400 to-purple-400 bg-clip-text text-transparent">
                Featured Projects
              </h2>
              <div class="w-20 h-1 bg-gradient-to-r from-pink-500 to-purple-500 mx-auto mb-4"></div>
              <p class="text-gray-400 max-w-2xl mx-auto">Here are some of my recent projects that showcase my skills and passion for programming and web development</p>
            </div>
            <div class="max-w-7xl mx-auto">
              <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div 
                  v-for="(project, index) in projects" 
                  :key="index"
                  class="group relative bg-white/5 backdrop-blur-sm rounded-2xl overflow-hidden border border-white/10 hover:border-white/30 transition-all md:col-span-2 lg:col-span-1"
                >
                  <div class="relative h-48 overflow-hidden">
                    <img :src="project.image" class="w-full h-full object-cover" />
                    <div class="absolute inset-0 bg-gradient-to-t from-slate-900 via-slate-900/50 to-transparent opacity-60"></div>
                    <div class="absolute inset-0 bg-gradient-to-br from-pink-600/80 to-purple-600/80 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center gap-4">
                      <a 
                        v-if="project.link"
                        :href="project.link"
                        target="_blank"
                        class="p-3 bg-white/20 backdrop-blur-sm rounded-full hover:bg-white/30 transition-colors"
                      >
                        <ExternalLink></ExternalLink>
                      </a>
                      <a 
                        v-if="project.github"
                        :href="project.github"
                        target="_blank"
                        class="p-3 bg-white/20 backdrop-blur-sm rounded-full hover:bg-white/30 transition-colors"
                      >
                        <img src="/github.svg" class="w-6 h-6 invert">
                      </a>
                    </div>
                  </div>
                  <div class="p-6">
                    <h3 class="text-xl text-pink-300 mb-2">
                      {{ project.name }}
                    </h3>
                    <p class="text-sm text-gray-400 mb-4 line-clamp-3">
                      {{ project.description }}
                    </p>
                    <div class="flex flex-wrap gap-2">
                      <span 
                        v-for="tag in project.tags" 
                        :key="tag"
                        class="px-3 py-1 bg-white/10 rounded-full text-xs text-gray-300 border border-white/20"
                      >
                        {{ tag }}
                      </span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section id="contact">
        <div class="min-h-screen flex  !py-20">
          <div class="container mx-auto px-4">
            <div class="text-center mb-16">
              <h2 class="text-4xl md:text-5xl mb-4 bg-gradient-to-r from-pink-400 to-purple-400 bg-clip-text text-transparent">
                Get In Touch
              </h2>
              <div class="w-20 h-1 bg-gradient-to-r from-pink-500 to-purple-500 mx-auto mb-4"></div>
              <p class="text-gray-400 max-w-2xl mx-auto">I'm always open to discussing new projects, creative ideas, or opportunities to be part of your vision.</p>
            </div>
            <div class="max-w-4xl mx-auto">
              <div >
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-12">
                  <a 
                    v-for="contact in contacts"
                    :key="contact" 
                    :href="contact.link" 
                    target="_blank" 
                    rel="noopener noreferrer"
                    class="group relative bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10 hover:border-white/30 transition-all overflow-hidden"
                  >
                    <div class="absolute inset-0 bg-gradient-to-br from-red-500 to-pink-500 opacity-0 group-hover:opacity-10 transition-opacity"></div>
                    <div class="relative flex items-center gap-4">
                      <div :class="contact.color" class="p-4 rounded-xl shadow-lg">
                      <img :src="contact.logo" class="w-7 h-7 invert"/>
                      </div>
                      <div class="flex-1 min-w-0">
                        <div class="text-sm text-gray-400 mb-1"> {{ contact.name }} </div>
                        <div class="text-white truncate group-hover:text-pink-300 transition-colors"> {{ contact.description }} </div>
                      </div>
                      <div class="text-gray-400 group-hover:text-pink-400 transition-colors">
                        →
                      </div>
                    </div>
                  </a>
                </div>
                <div class="mt-16 pt-8 border-t border-white/10 text-center">
                  <p class="text-gray-400 text-sm mb-4">
                    Built with VueJS, and Tailwind CSS
                  </p>
                  <p class="text-gray-500 text-sm">
                    © 2025 Jan Ember Quiamco. All rights reserved.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script setup>
  import { ref, onMounted, computed } from "vue";
  import { Mail, ChevronDown, MapPin, Calendar, BadgeCheck, ExternalLink } from "lucide-vue-next";

  const contacts = [
    {
      name: "Email",
      description: "janember516@gmail.com",
      link: "mailto:janember516@gmail.com",
      logo: "gmail.svg",
      color: "bg-gradient-to-br from-red-500 to-pink-500",
    },
    {
      name: "Github",
      description: "github.com/Janember",
      link: "https://github.com/Janember",
      logo: "github.svg",
      color: "bg-gradient-to-br from-gray-600 to-gray-800",
    },
    {
      name: "LinkedIn",
      description: "linkedin.com/in/jan-ember-462809198/",
      link: "https://www.linkedin.com/in/jan-ember-462809198/",
      logo: "linkedin.svg",
      color: "bg-gradient-to-br from-blue-600 to-blue-800",
    },
    {
      name: "X",
      description: "x.com/JaneQ516",
      link: "https://x.com/JaneQ516",
      logo: "x.svg",
      color: "bg-gradient-to-br from-gray-700 to-gray-900",
    }
  ]

  const projects = [
    {
      name: "Cosmogensan",
      description: "A service platform that allows users to browse chapel facilities, reserve memorial services online, and process secure digital payments.",
      tags: ["Vue", "PHP", "Tailwindcss"],
      image: "/cosmogensan.png",
      link: "https://cosmogensan.com/",
      github: "https://github.com/Janember/cosmogensan"
    },
  ]

  const Expertises = [ "Honey Select 2", "Koikatsu", "Testing", "Version Control", "Performance Optimization" ];

  const navItems = [
    { id: "home", label: "Home" },
    { id: "about", label: "About" },
    { id: "experience", label: "Experience" },
    { id: "skills", label: "Skills" },
    { id: "projects", label: "Projects" },
    { id: "contact", label: "Contacts" }
  ];

  const categoryColors = { 
    Frontend: { 
      from: "from-pink-500/20",
      to: "to-rose-500/20",
      border: "border-pink-500/30",
      barFrom: "from-pink-500",
      barTo: "to-rose-500",
    }, 
    Backend: { 
      from: "from-blue-500/20", 
      to: "to-cyan-500/20", 
      border: "border-blue-500/30", 
      barFrom: "from-blue-500", 
      barTo: "to-cyan-500",
    }, 
    DevOps: { 
      from: "from-purple-500/20", 
      to: "to-indigo-500/20", 
      border: "border-purple-500/30", 
      barFrom: "from-purple-500", 
      barTo: "to-indigo-500", 
    }, 
    GameDev: {
      from: "from-green-500/20", 
      to: "to-emerald-500/20", 
      border: "border-green-500/30", 
      barFrom: "from-green-500", 
      barTo: "to-emerald-500", 
    }
  };

  const selectedCategory = ref("All");

  const categories = ["All", "Frontend", "Backend", "GameDev", "DevOps"];

  const skills = [
    { name: "VueJS",        type: "Frontend", progress: "95", icon: "🟩" },
    { name: "ReactJS",      type: "Frontend", progress: "90", icon: "⚛️" },
    { name: "Tailwind CSS", type: "Frontend", progress: "90", icon: "💨" },
    { name: "HTML",         type: "Frontend", progress: "95", icon: "📄" },
    { name: "PHP",          type: "Backend",  progress: "90", icon: "🐘" },
    { name: "MySQL",        type: "Backend",  progress: "90", icon: "🛢️" },
    { name: "Python",       type: "Backend",  progress: "85", icon: "🐍" },
    { name: "Unity",        type: "GameDev",  progress: "90", icon: "🎮" },
    { name: "Godot",        type: "GameDev",  progress: "90", icon: "🤖" },
    { name: "RenPy",        type: "GameDev",  progress: "90", icon: "📘" },
    { name: "Git",          type: "DevOps",   progress: "90", icon: "🔧" },
  ];

  const filteredSkills = computed(() =>
  selectedCategory.value === "All"
      ? skills
      : skills.filter((s) => s.type === selectedCategory.value)
  );

  const activeSection = ref("home");

  const scrollToSection = (id) => {
    const el = document.getElementById(id);
    if (el) {
      el.scrollIntoView({ behavior: "smooth" });
    }
  };

  onMounted(() => {
    const sections = document.querySelectorAll("section");

    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            activeSection.value = entry.target.id;
          }
        });
      },
      { threshold: 0.6 }
    );

    sections.forEach((s) => observer.observe(s));
  });
</script>
<style scoped></style>
