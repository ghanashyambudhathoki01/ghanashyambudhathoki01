# 👋 Hi, I'm Ghanshyam Budhathoki
import React, { useEffect, useState } from "react"; import { Card, CardContent } from "@/components/ui/card"; import { motion } from "framer-motion";

export default function GitHubStatsCard() { const [stats, setStats] = useState(null);

useEffect(() => { async function fetchStats() { // Replace YOUR_USERNAME with your GitHub username const res = await fetch("https://api.github.com/users/YOUR_USERNAME"); const user = await res.json();

const reposRes = await fetch(user.repos_url);
  const repos = await reposRes.json();

  const totalStars = repos.reduce((sum, repo) => sum + repo.stargazers_count, 0);

  setStats({
    name: user.name,
    totalStars,
    totalRepos: user.public_repos,
    followers: user.followers,
    following: user.following,
  });
}
fetchStats();

}, []);

if (!stats) return <p className="text-center">Loading GitHub stats...</p>;

return ( <div className="max-w-2xl mx-auto p-4 grid gap-4"> {/* Top Stats Card */} <Card className="shadow-xl rounded-2xl p-4"> <CardContent className="space-y-2"> <h2 className="text-xl font-bold text-blue-600">{stats.name}'s GitHub Stats</h2> <p>⭐ Total Stars Earned: {stats.totalStars}</p> <p>📦 Public Repos: {stats.totalRepos}</p> <p>👥 Followers: {stats.followers}</p> <p>🔗 Following: {stats.following}</p> </CardContent> </Card>

{/* Contributions & Streak */}
  <Card className="shadow-xl rounded-2xl p-6 flex justify-between items-center">
    <motion.div whileHover={{ scale: 1.05 }} className="text-center">
      <p className="text-2xl font-bold">654</p>
      <p className="text-gray-500">Total Contributions</p>
    </motion.div>
    <motion.div whileHover={{ scale: 1.05 }} className="text-center">
      <p className="text-2xl font-bold">0</p>
      <p className="text-orange-500">Current Streak</p>
    </motion.div>
    <motion.div whileHover={{ scale: 1.05 }} className="text-center">
      <p className="text-2xl font-bold">60</p>
      <p className="text-gray-500">Longest Streak</p>
    </motion.div>
  </Card>
</div>

); }



<div style="display: flex; flex-wrap: wrap; gap: 5px; align-items: center;">

  <!-- Tech Stack -->
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB">

  <!-- Tools & Work -->
  <img src="https://img.shields.io/badge/VSCode-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white" alt="VSCode">
  <img src="https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/Git-GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="Git & GitHub">

  <!-- Productivity & Personality -->
  <img src="https://img.shields.io/badge/Productivity-20b2aa?style=for-the-badge&logo=notion&logoColor=white" alt="Productivity">
  <img src="https://img.shields.io/badge/Consistency-ff6347?style=for-the-badge&logo=clockify&logoColor=white" alt="Consistency">
  <img src="https://img.shields.io/badge/Hard_Working-ff8c00?style=for-the-badge&logo=zapier&logoColor=white" alt="Hard Working">
  <img src="https://img.shields.io/badge/Funny-ff69b4?style=for-the-badge&logo=messenger&logoColor=white" alt="Funny">
  <img src="https://img.shields.io/badge/Coffee-Love-6f4e37?style=for-the-badge&logo=coffeescript&logoColor=white" alt="Coffee Lover">

</div>
🎓 Learning Pharse of Full Stack Developer | 💻 Aspiring Full Stack Developer | 📚 Sharing My Learning Journey  
📍 Dolakha, Nepal | 🧠 Always learning and building projects

---

## 🚧 What I'm Working On
- 📘 Exploring full stack developer course and learning too
- 🎯 Building confidence
- 🧰 Documenting everything I learn in public

---

## 🧠 What I'm Learning
- Learning Full Stack Developer
- Using Git and GitHub to manage and publish code


---

## 📘 My Learning Journey
I began learning full stack developer with the goal of building a future in tech, even though I had no programming background.  
 Alongside full stack developer, I’ve explored tools like Git, GitHub, My focus right now is practicing consistently, building mini projects, and learning how real-world tools and code work together.

---


## 📈 My Goals
- Contribute to open-source beginner repositories
- Build a some mini projects
- Learn the full stack development

---

## 🔗 Connect with Me
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/ghanashyambudhathoki01)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=flat&logo=instagram&logoColor=white)](https://www.instagram.com/ghanashyam_072?igsh=dm9yZHZhYjJmcHZ6)
[![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=flat&logo=facebook&logoColor=white)](https://www.facebook.com/samraz.budathoki.1)
[![X](https://img.shields.io/badge/X-000000?style=flat&logo=x-twitter&logoColor=white)](https://x.com/ghanashyam_072?t=JBS2uJrcFMX2sKSo30KCnA&s=09)
<!---
ghanashyambudhathoki01/ghanashyambudhathoki01 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
