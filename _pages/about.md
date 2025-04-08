---
layout: about
title: about
permalink: /
# subtitle: <a href='#'>UCI</a>
subtitle: PhD candidate, University of California Irvine

# profile:
#   align: right
#   image: profile_pic.jpg
#   image_circular: true # crops the image to make it circular
#   more_info: >
#     <style>
#       .profile img { width: 200px; height: auto; }
#     </style>
#   # more_info: >
#   #   <p>555 your office number</p>
#   #   <p>123 your address street</p>
#   #   <p>Your City, State 12345</p>

profile:
  align: left
  image: profile_pic.jpg
  image_circular: false  # change to false for square image
  more_info: >
    <style>
      .profile {
        width: 240px;
        height: 240px;
        margin-bottom: 55px;  /* Creates space between image and text */
        padding-right : 20px;
        
      }
      .profile img {
        width: 100%;
        height: 100%;
        object-fit: cover;    /* Ensures image fills square space */
      }
      # .clearfix {
      #   clear: bottom;         /* Prevents text wrapping around image */
      #   padding-top: 20px;   /* Adds space between image and text */
      #   padding-right: 30px;
      #   padding-left: 20 px;
      }
    </style>

selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

**Currently:**
- Ph.D. candidate in Mechanical and Aerospace Engineering at UC Irvine (since 2020)
- Working under the guidance of <a href= 'https://solmaz.eng.uci.edu/'> Prof. Solmaz Kia </a>

**Research:**
My research focuses on robotics and multi-agent systems, specifically:
- Developing algorithms for coverage and monitoring with collaborative multi-robot systems
- Integrating multiple disciplines: 
  -Computer vision, Optimization, Control theory, Probabilistic machine learning, Variational inference, Graph theory
- Designing advanced planning and deployment strategies for robotic cooperation


<br>
**Previously:**
- ***Summer 2024***: Research Intern at <a href='https://arl.devcom.army.mil/'>US DEVCOM Army Research Lab</a> 
  - Focus: Active source seeking and exploration algorithms for search-and-rescue mission.
- ***Fall 2022***: Visiting Researcher at <a href='https://www.jpl.nasa.gov/'>NASA Jet Propulsion Laboratory</a>
  - Focus: Perception and motion planning for robotic exploration.
- Master in Mechanical and Aerospace Engineering from UC Irvine (2022)
- BSc in Mechanical Engineering from Howard University (2019)



**Research Vision:** <span style="font-style: italic; font-weight: 100;">
Looking ahead, I am excited to explore the role of abstractions/representation in achieving efficient and robust autonomy in robotics. I believe that the "right" representations are paramount in enabling robots to understand complex environments and execute sophisticated tasks efficiently.
<span id="vision-more" style="display: none;">
I am particularly interested in two approaches. The first is a hierarchical architecture that involves a low-level control loop for basic movement execution (for example, moving from point A to B) and a higher-level system that operates at a slower duty cycle to break down missions into sub-goal. The second is an end-to-end learning architecture that directly maps sensor inputs to motor commands ("pixels to volts"). The hierarchical framework provides the benefit of interpretability and data efficiency, but the end-to-end framework provides more flexibility that learns complex mapping directly from data and leads to emergent behaviors that are difficult to engineer explicitly in a hierarchical system. Ultimately, I aim to and want to encourage the robotics community to develop a hybrid system that integrates structured reasoning with learned flexibility of end-to-end learning, bridging low-level perception and high-level task semantics for resilient and intelligent autonomy.
</span>
</span>
<a id="vision-toggle" onclick="toggleVision()" style="cursor: pointer; color: #4B9CD3; font-size: 0.9em;">[See more]</a>

<script>
function toggleVision() {
  var moreText = document.getElementById("vision-more");
  var toggleText = document.getElementById("vision-toggle");
  
  if (moreText.style.display === "none") {
    moreText.style.display = "inline";
    toggleText.innerHTML = "[See less]";
  } else {
    moreText.style.display = "none";
    toggleText.innerHTML = "[See more]";
  }
}
</script>

I enjoy maintaining an active lifestyle through:
- Hiking
- Climbing
- Listening to podcasts

