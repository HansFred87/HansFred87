<h1 align="center">Hi 👋, I'm Hans</h1>
<h3 align="center">A passionate frontend developer from PH</h3>

<p align="left"> <img src="https://komarev.com/ghpvc/?username=hansel&label=Profile%20views&color=0e75b6&style=flat" alt="hansel" /> </p>

- 🔭 I’m currently working on **SCP**

- 🌱 I’m currently learning **Python**

- 👯 I’m looking to collaborate on **SCP**

- 🤝 I’m looking for help with **SCP**

- 📫 How to reach me **hansfredricafort@gmail.com**

- ⚡ Fun fact **I'm interested in game dev**

  # 📊GitHub Stats :
![](https://github-readme-stats.vercel.app/api?username=Hans&theme=radical&hide_border=false&include_all_commits=false&count_private=false)<br/>
![](https://github-readme-streak-stats.herokuapp.com/?user=Hans&theme=radical&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Hans&theme=radical&hide_border=false&include_all_commits=false&count_private=false&layout=compact)

---
[![](https://visitcount.itsvg.in/api?id=Hans&icon=0&color=0)](https://visitcount.itsvg.in)


<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://www.youtube.com/c/lastorviod" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/youtube.svg" alt="lastorviod" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://getbootstrap.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain-wordmark.svg" alt="bootstrap" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://www.java.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" width="40" height="40"/> </a> <a href="https://www.php.net" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="php" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> </p>

// Authorization token that must have been created previously. See : https://developer.spotify.com/documentation/web-api/concepts/authorization
const token = 'undefined';
async function fetchWebApi(endpoint, method, body) {
  const res = await fetch(`https://api.spotify.com/${endpoint}`, {
    headers: {
      Authorization: `Bearer ${token}`,
    },
    method,
    body:JSON.stringify(body)
  });
  return await res.json();
}

async function getTopTracks(){
  // Endpoint reference : https://developer.spotify.com/documentation/web-api/reference/get-users-top-artists-and-tracks
  return (await fetchWebApi(
    'v1/me/top/tracks?time_range=long_term&limit=5', 'GET'
  )).items;
}

const topTracks = await getTopTracks();
console.log(
  topTracks?.map(
    ({name, artists}) =>
      `${name} by ${artists.map(artist => artist.name).join(', ')}`
  )
);

<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=hansel&show_icons=true&locale=en&layout=compact" alt="hansel" /></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=hansel&show_icons=true&locale=en" alt="hansel" /></p>
