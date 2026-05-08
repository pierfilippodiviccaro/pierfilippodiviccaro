import { useState } from "react";
import { Copy, Check } from "lucide-react";
import { Button } from "@/components/ui/button";

const readmeContent = `<div align="center">

# Hi there, I'm Pierfilippo Di Viccaro 👋

[![GitHub followers](https://img.shields.io/github/followers/pierfilippodiviccaro?label=Follow&style=social)](https://github.com/pierfilippodiviccaro)
[![Profile Views](https://komarev.com/ghpvc/?username=pierfilippodiviccaro&color=blueviolet&style=flat-square)](https://github.com/pierfilippodiviccaro)

</div>

---

## 🧑‍💻 About Me

I'm a **Software Engineer** passionate about building clean, efficient, and scalable web applications.  
I love crafting robust backends and polished user interfaces that deliver real value.

- 🔭 Currently working on exciting web projects
- 🌱 Always learning and improving my craft
- 💬 Ask me about **PHP, Laravel, JavaScript, or web development**
- 📫 Reach me on [GitHub](https://github.com/pierfilippodiviccaro)

---

## 🛠️ Tech Stack

### Backend
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

### Frontend
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)

### Tools & Workflow
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Composer](https://img.shields.io/badge/Composer-885630?style=for-the-badge&logo=composer&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)

---

## 📊 GitHub Stats

<div align="center">

![pierfilippodiviccaro's GitHub Stats](https://github-readme-stats.vercel.app/api?username=pierfilippodiviccaro&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=pierfilippodiviccaro&layout=compact&theme=tokyonight&hide_border=true)

![GitHub Streak](https://streak-stats.demolab.com?user=pierfilippodiviccaro&theme=tokyonight&hide_border=true)

</div>

---

## 🚀 Featured Projects

> 📌 Pin your best repositories on GitHub and they'll appear here. Here are some highlights:

| Project | Description | Stack |
|--------|-------------|-------|
| 🔧 *Your Project 1* | Short description of what it does | Laravel, MySQL |
| 🎨 *Your Project 2* | Short description of what it does | PHP, JS, TailwindCSS |
| 📦 *Your Project 3* | Short description of what it does | Laravel, Vue.js |

---

## 🤝 Connect With Me

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-pierfilippodiviccaro-181717?style=for-the-badge&logo=github)](https://github.com/pierfilippodiviccaro)

</div>

---

<div align="center">

*"First, solve the problem. Then, write the code."* — John Johnson

⭐️ Feel free to explore my repositories and leave a star if you find something useful!

</div>`;

export default function Readme() {
  const [copied, setCopied] = useState(false);

  const handleCopy = () => {
    navigator.clipboard.writeText(readmeContent);
    setCopied(true);
    setTimeout(() => setCopied(false), 2000);
  };

  return (
    <div className="min-h-screen bg-gray-950 text-gray-100 p-6">
      <div className="max-w-4xl mx-auto">
        <div className="flex items-center justify-between mb-6">
          <div>
            <h1 className="text-2xl font-bold text-white">GitHub Profile README</h1>
            <p className="text-gray-400 text-sm mt-1">Copy the raw markdown and paste it into your <code className="bg-gray-800 px-1 rounded text-purple-400">pierfilippodiviccaro/pierfilippodiviccaro</code> repo as <code className="bg-gray-800 px-1 rounded text-purple-400">README.md</code></p>
          </div>
          <Button
            onClick={handleCopy}
            className="flex items-center gap-2 bg-purple-600 hover:bg-purple-700 text-white"
          >
            {copied ? <Check className="w-4 h-4" /> : <Copy className="w-4 h-4" />}
            {copied ? "Copied!" : "Copy Markdown"}
          </Button>
        </div>

        <div className="bg-gray-900 border border-gray-700 rounded-xl overflow-hidden">
          <div className="flex items-center gap-2 px-4 py-3 bg-gray-800 border-b border-gray-700">
            <div className="w-3 h-3 rounded-full bg-red-500" />
            <div className="w-3 h-3 rounded-full bg-yellow-500" />
            <div className="w-3 h-3 rounded-full bg-green-500" />
            <span className="ml-2 text-gray-400 text-sm">README.md</span>
          </div>
          <pre className="p-6 text-sm text-gray-300 whitespace-pre-wrap font-mono leading-relaxed overflow-auto max-h-[70vh]">
            {readmeContent}
          </pre>
        </div>
      </div>
    </div>
  );
}
