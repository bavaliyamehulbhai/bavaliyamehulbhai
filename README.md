import markdown

# Define user details
user_name = "Mehul Bavaliya"
user_handle = "@bavaliyamehulbhai"
user_role = "Software Engineer"
user_location = "Ahmedabad, India"
user_website = "mehulbavaliya.dev"
linkedin_url = "https://www.linkedin.com/in/mehul-bavaliya/" # Placeholders
twitter_url = "https://twitter.com/mehul_bavaliya"
instagram_url = "https://www.instagram.com/mehul_bavaliya/"

# Define about me text (verbatim)
about_me_text = "I'm a passionate Full Stack Developer who loves building scalable, user-friendly, and high-performance applications. I enjoy converting complex ideas into real-world products. Currently exploring System Design, Cloud Technologies, and AI."

# Define projects (verbatim data)
projects = [
    {
        "name": "StadiumOS AI",
        "description": "AI-powered Stadium Management Platform with incident detection, live tracking, seat navigation, analytics & more.",
        "tags": ["MERN", "AWS", "Socket.io", "Tailwind"],
        "image_url": "stadiumos_placeholder.png"
    },
    {
        "name": "LibraryOS",
        "description": "A complete Library Management SaaS with role-based access, book tracking, issue/return system & analytics.",
        "tags": ["MERN", "Express", "MongoDB", "JWT"],
        "image_url": "libraryos_placeholder.png"
    },
    {
        "name": "VolunteerHub",
        "description": "Volunteer Management System for organizations to manage volunteers, events, tasks & communications.",
        "tags": ["MERN", "Node.js", "Express", "Cloudinary"],
        "image_url": "volunteerhub_placeholder.png"
    },
    {
        "name": "BayFlow",
        "description": "Productivity & Time Management App with tasks, notes, pomodoro timer and habit tracking.",
        "tags": ["MERN", "Redux", "Tailwind", "Charts"],
        "image_url": "bayflow_placeholder.png"
    }
]

# Define Tech Stack Icons (using simpleicons.org with color)
tech_stack = [
    ("Java", "https://simpleicons.org/icons/java.svg", "ED8B00"),
    ("JavaScript", "https://simpleicons.org/icons/javascript.svg", "F7DF1E"),
    ("TypeScript", "https://simpleicons.org/icons/typescript.svg", "3178C6"),
    ("React", "https://simpleicons.org/icons/react.svg", "61DAFB"),
    ("Node.js", "https://simpleicons.org/icons/node-dot-js.svg", "339933"),
    ("Express", "https://simpleicons.org/icons/express.svg", "808080"), # (simple icons express is grey)
    ("MongoDB", "https://simpleicons.org/icons/mongodb.svg", "47A248"),
    ("MySQL", "https://simpleicons.org/icons/mysql.svg", "4479A1"),
    ("Tailwind", "https://simpleicons.org/icons/tailwindcss.svg", "06B6D4"),
    ("Redux", "https://simpleicons.org/icons/redux.svg", "764ABC"),
    ("Socket.io", "https://simpleicons.org/icons/socket-dot-io.svg", "010101"),
    ("Git", "https://simpleicons.org/icons/git.svg", "F05032"),
    ("Docker", "https://simpleicons.org/icons/docker.svg", "2496ED"),
    ("AWS", "https://simpleicons.org/icons/amazonwebservices.svg", "232F3E")
]

# Define Vercel API endpoints for stats
username_api = "bavaliyamehulbhai"
theme_api = "tokyonight" # Replicating the dark look

github_readme_stats_url = f"https://github-readme-stats.vercel.app/api?username={username_api}&show_icons=true&theme={theme_api}&hide_border=true&include_all_commits=true"
top_langs_stats_url = f"https://github-readme-stats.vercel.app/api/top-langs/?username={username_api}&layout=compact&theme={theme_api}&hide_border=true"
streak_stats_url = f"https://github-readme-streak-stats.herokuapp.com/?user={username_api}&theme={theme_api}&hide_border=true&background=0d1117"

# Special Integrated Contribution Graph Image (concept)
activity_graph_integrated_url = "activity_graph_integrated.png" # Need to create this and host.

# Badges (shields.io)
badges = [
    ("LinkedIn", f"https://img.shields.io/badge/-LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white&link={linkedin_url}", "https://simpleicons.org/icons/linkedin.svg"),
    ("Twitter", f"https://img.shields.io/badge/-Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white&link={twitter_url}", "https://simpleicons.org/icons/twitter.svg"),
    ("Instagram", f"https://img.shields.io/badge/-Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white&link={instagram_url}", "https://simpleicons.org/icons/instagram.svg")
]

# Generate project badges for tags
def generate_project_badges(tags):
    badges_html = ""
    for tag in tags:
        badges_html += f'<img src="https://img.shields.io/badge/-{tag}-blue?style=flat-square" alt="{tag}"> '
    return badges_html

# Construct README Markdown
readme_md = f"""
# <h1 align="center">Hi 👋, I'm Mehul Bavaliya</h1>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=bavaliyamehulbhai&repo=bavaliyamehulbhai&theme=tokyonight&hide_border=true" alt="Mehul's Pin" width="400">
</p>

## <p align="center"> A passionate Software Engineer from India</p>

<p align="center">
  <a href="{linkedin_url}" target="_blank">
    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="Mehul's LinkedIn" height="30" width="40" />
  </a>
  <a href="{twitter_url}" target="_blank">
    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/twitter.svg" alt="Mehul's Twitter" height="30" width="40" />
  </a>
</p>

<img align="right" alt="Coding" width="400" src="https://cdn.dribbble.com/users/1162077/screenshots/3848914/programmer.gif">

## About Me

{about_me_text}

---

## Featured Projects

| Project | Description | Stack |
| :--- | :--- | :--- |
{'\n'.join([f'| <img src="{p["image_url"]}" width="100" alt="{p["name"]}"><br><b>{p["name"]}</b> | {p["description"]} | {generate_project_badges(p["tags"])} |' for p in projects])}

---

## Tech Stack

<p align="center">
{'\n'.join([f'<img src="{icon_url}" alt="{name}" width="40" height="40" style="padding: 10px;" />' for name, icon_url, _ in tech_stack])}
</p>

---

## GitHub Stats

<p align="center">
  <img height="200" src="{github_readme_stats_url}" />
</p>
<p align="center">
  <img height="200" src="{streak_stats_url}" />
</p>
<p align="center">
  <img height="200" src="{top_langs_stats_url}" />
</p>

---

## Contribution Activity & Wired Data Flow

<p align="center">
  <img src="{activity_graph_integrated_url}" alt="Integrated Data Flow Contribution Graph" />
</p>
<p align="center">
<i>A live visualization where your GitHub contributions fuel real-time data flows to connected technologies and projects.</i>
</p>

---

### Achievements & Recognition

<p align="center">
  <img src="https://img.shields.io/badge/-AWS%20Certified-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white" alt="AWS Certified Badge">
  <img src="https://img.shields.io/badge/-Top%20Contributor-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="Top Contributor Badge">
  <img src="https://img.shields.io/badge/-Featured%20Dev-blue?style=for-the-badge" alt="Featured Dev Badge">
</p>

---

### Let's Connect!

<p align="center">
  <a href="https://www.linkedin.com/in/mehul-bavaliya/">
    <img src="https://img.shields.io/badge/-LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge">
  </a>
  <a href="https://twitter.com/mehul_bavaliya">
    <img src="https://img.shields.io/badge/-Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge">
  </a>
</p>

---

<p align="center">
Thanks for visiting! 👋
</p>
"""

# Define necessary filenames
readme_filename = "README.md"
cover_filename = "mehuls_cover.png"
graph_filename = "activity_graph_integrated.png"
proj_placeholders = [p['image_url'] for p in projects]

# Write to README.md file
with open(readme_filename, "w") as f:
    f.write(readme_md)

# Prepare to generate placeholder files and the integrated graph
print(f"Generated {readme_filename}. Now generating visual components:")
