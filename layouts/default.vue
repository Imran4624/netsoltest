<template>
  <nav class="navbar">
    <div class="menu-item">
      <a class="icon" href="/">NETSOL</a>
    </div>
    <div class="menu-item">
      <!-- <a href="/">REGIONS</a> -->
        <div class="dropdown">
            <button class="dropbtn">REGIONS</button>
            <div class="dropdown-content">
              <a @click="changeUrl('/en-us')">USA</a>
              <a @click="changeUrl('/en-uk')">UK</a>
              <a @click="changeUrl('/en-ch')">China</a>
              <a @click="changeUrl('/en-pk')">Pakistan</a>
              <!-- Add more dropdown items as needed -->
            </div>
          </div>
    </div>
  </nav>
        <!---- output the page content --->
    <slot :country = selectedUrl />
</template>

<script >
export default {
  data() {
    return {
        newProducts: []
    };
  },
  methods: {
    changeUrl(url) {
      this.newProducts = url == "/en-us" ? [
   {
          id: 1,
          imageUrl: "/img1.png",
          type: "News",
          title: "Leasing Life Conference & Awards",
          description:
            "Solving the world’s problems through technology wouldn’t be possible without our most important invention.",
        },
        {
          id: 2,
          imageUrl: "/img2.png",
          type: "Blog",
          title: "Auto Finance Summit 2023",
          description:
            "Solving the world’s problems through technology wouldn’t be possible without our most important invention.",
        },
        {
          id: 3,
          imageUrl: "/img3.png",
          type: "Blog",
          title: "Careers at Netsol",
          description:
            "Solving the world’s problems through technology wouldn’t be possible without our most important invention.",
        },
        {
          id: 4,
          imageUrl: "/img4.png",
          type: "News",
          title: "Leasing Life Conference & Awards",
          description:
            "Solving the world’s problems through technology wouldn’t be possible without our most important invention.",
        },
]:[

        {
          id: 3,
          imageUrl: "/img3.png",
          type: "Blog",
          title: "Careers at Netsol",
          description:
            "Solving the world’s problems through technology wouldn’t be possible without our most important invention.",
        },
        {
          id: 4,
          imageUrl: "/img4.png",
          type: "News",
          title: "Leasing Life Conference & Awards",
          description:
            "Solving the world’s problems through technology wouldn’t be possible without our most important invention.",
        },
];
window.history.pushState({}, '', url);
      // Optionally, you can perform any additional actions here
    }
  }
};

// const changeUrl = (path) => {
//   window.history.pushState({}, '', path);
// };

</script>

<style>
.navbar{
    display: flex;
    align-items: center;
    justify-content: space-between;
padding: 10px 20px 10px 20px;
}
.icon{
width: 90px;
height: 16px;
text-decoration: none;
color: #FFFF;
}
.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background: radial-gradient(163.75% 163.75% at 23.45% 140%, #0025CE 0%, rgba(9, 93, 230, 0.53) 100%);
  min-width: 177px;
border-radius: 20px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
border-radius: 20px;
  display: block;
}

.dropdown-content a:hover {
  background-color: #ddd;
}

.dropdown:hover .dropdown-content {
  display: block;
}

.dropbtn {
  background: radial-gradient(163.75% 163.75% at 23.45% 140%, #000ace 0%, rgba(9, 93, 230, 0.53) 100%);
  color: white;
width: 177px;
height: 40px;
border-radius: 100px;
  /* padding: 16px; */
  font-size: 16px;
  border: none;
  cursor: pointer;
}
html {
  background: radial-gradient(
  ellipse at 29.45% 150%, 
  #248b4f 0%,   /* First color */
  rgba(26, 102, 223, 0.53) 25%,   /* Second color */
  #020b1c 50%,  /* Third color */
  #0b0e4f 75%   /* Fourth color */
);

  /* Add any other background properties as needed */
}

</style>
