---
layout: page
title: projects
permalink: /projects/
#description: A growing collection of your cool projects.
nav: true
nav_order: 2
display_categories: [work, fun]
horizontal: false
---
---

<h2 class="mt-4">Diffusion Based Planning</h2>

<div class="mb-3">
  <a href="https://github.com/donipologhimire/diffusion_based_planning" class="btn btn-sm btn-outline-primary" target="_blank">
    <i class="fab fa-github mr-1"></i> View on GitHub
  </a>
</div>

<div class="row mt-3">
  <div class="col-12">
    <p>This project implements a Denoising Diffusion Probabilistic Model (DDPM) to learn a prior distribution over smooth, collision-free robot trajectories from expert demonstrations. The system consists of three main components: expert trajectory generation, model training, and inference.</p>
    
    <h4>1. Expert Trajectory Generation</h4>
    <p>TWe create a dataset of expert trajectories using A* search algorithm on a grid-based map with obstacles. These trajectories serve as the ground truth for training the diffusion model.</p>
    
    <p>Key features:</p>
    <ul>
      <li>Creates a binary obstacle map with walls and barriers</li>
      <li>Generates start and goal points in free spaces</li>
      <li>Uses A* search to find optimal paths</li>
      <li>Normalizes and processes trajectories to a consistent format</li>
      <li>Saves the dataset with trajectories and their conditions (start, goal, obstacle map)</li>
    </ul>
    
    <div class="text-center">
      <figure style="margin: 0 auto;">
        <img src="{{ '/assets/img/diffusion_planning/expert_trajectory.png' | relative_url }}" 
            alt="Expert trajectory generation" 
            class="img-fluid rounded z-depth-1"
            style="width: 300px; height: 300px; margin: 0 auto;">
        <figcaption>Expert trajectory generation</figcaption>
      </figure>
    </div>
    
    <h4>2. Model Training</h4>
    <p>We implement a diffusion model training pipeline.</p>
    
    <p>Key components:</p>
    <ul>
      <li>We load the expert trajectories and their conditions</li>
      <li>Implements a conditional UNet architecture that takes trajectory state, time embedding, and environmental conditions</li>
      <li>Trains the model to denoise random Gaussian noise into expert trajectories</li>
      <li>Uses classifier-free guidance (CFG) for improved conditioning</li>
      <li>Saves model checkpoints during training</li>
    </ul>
    
    <h4>3. Inference</h4>
    <p>Key features:</p>
    <ul>
      <li>Loads trained model checkpoints</li>
      <li>Implements the reverse diffusion process with classifier-free guidance</li>
      <li>Generates smooth, collision-free trajectories between any valid start and goal</li>
      <li>Visualizes the results with the obstacle map</li>
    </ul>
    
    <div class="row">
      <div class="col-md-6">
        <div class="text-center">
          {% include figure.liquid 
             path="assets/img/diffusion_planning/best_generated_trajectory.png"
             title="Best generated trajectory" 
             tyle="width: 80%; max-width: 300px; height: auto;"
             class="img-fluid rounded z-depth-1"
          %}
        </div>
      </div>

      <div class="col-md-6">
      <div class="text-center">
        <figure>
          <img src="{{ '/assets/img/diffusion_planning/trajectory_evolution_best.gif' | relative_url }}" 
              alt="Trajectory evolution" 
              class="img-fluid rounded z-depth-1"
              style="width: 80%; max-width: 400px; height: auto;"
              loading="eager">
          <figcaption>Trajectory evolution animation</figcaption>
        </figure>
      </div>
    </div>
    </div>
    
    <h4>Denoising Process Visualization</h4>
    <p>The diffusion model works by gradually denoising a random Gaussian noise distribution into a coherent trajectory. The following visualization shows this process:</p>
    
    <div class="text-center">
      {% include figure.liquid 
         path="assets/img/diffusion_planning/denoising_trajectory.png"
         title="Denoising process visualization" 
         class="img-fluid rounded z-depth-1"
      %}
    </div>
  </div>
</div>

<!-- title -->
<h2 class="mt-4">Research Posters</h2>


<!-- Poster navigation buttons -->
<div class="d-flex justify-content-center mb-3">
  <button class="btn btn-sm btn-primary mx-1" onclick="showPoster('poster1')" id="btn-poster1">Poster 1</button>
  <button class="btn btn-sm btn-outline-primary mx-1" onclick="showPoster('poster2')" id="btn-poster2">Poster 2</button>
  <button class="btn btn-sm btn-outline-primary mx-1" onclick="showPoster('poster3')" id="btn-poster3">Poster 3</button>
</div>

<!-- Poster 1 (Shown by default) -->
<div id="poster1" class="poster-content">
  <div class="row mt-3">
    <div class="col-12">
      <p><strong>Poster 1:</strong> The proposed "Stein Coverage" algorithm improves multisensor deployment by optimally matching sensor locations to event distributions using Stein Variational Gradient Descent (SVGD). It introduces a repulsive term to reduce coverage overlap and interference, creates a utility map highlighting critical regions, and solves the deployment as a linear assignment using the Hungarian algorithm.</p>
      
      <div class="text-center">
        <iframe src="{{ '/assets/pdf/SteinPoster.pdf' | relative_url }}" 
                width="100%" 
                height="700px" 
                frameborder="0">
        </iframe>
      </div>
    </div>
  </div>
</div>

<!-- Poster 2 (Initially Hidden) -->
<div id="poster2" class="poster-content" style="display: none;">
  <div class="row mt-3">
    <div class="col-12">
      <p><strong>Poster 2:</strong> This poster and paper considers a multi-sensor service matching deployment problem over a set of discrete target points that populate a finite flat surface. The service can be event detection among targets using a vision sensor or an acoustic receiver, video surveillance for target monitoring, or providing wireless coverage to the targets. The quality-of-service (QoS) of the sensors is spatially nonuniform and can be anisotropic. The sensors are heterogeneous in the sense that their QoS distribution over their sensing footprint is not the same.</p>
      <p>The objective is to determine the sensor's best deployment position and orientation such that the collective multi-sensor QoS distribution matches the spread of the targets in the environment as closely as possible.</p>
      
      <div class="text-center">
        {% include figure.liquid 
           path="assets/img/ECC2023.jpg"
           title="Multi-sensor service matching deployment" 
           class="img-fluid rounded z-depth-1"
        %}
      </div>
    </div>
  </div>
</div>

<!-- Poster 3 (Initially Hidden) -->
<div id="poster3" class="poster-content" style="display: none;">
  <div class="row mt-3">
    <div class="col-12">
      <p><strong>Poster 3:</strong> This poster presents a pipeline and a framework for distributed deployment and path planning for multiple UAVs with the goal of surveying open surface minefields. We want to use UAVs to help us determine the deformation in the strata of the open surface minefields inorder to predict natural disasters like landslides from causing loss of human life and other resources.</p>
      
      <div class="text-center">
        {% include figure.liquid 
           path="assets/img/NSF_IIT_UCI.jpg"
           title="UAV path planning for minefield surveying" 
           class="img-fluid rounded z-depth-1"
        %}
      </div>
    </div>
  </div>
</div>

<!-- JavaScript to handle poster switching -->
<script>
  function showPoster(posterID) {
    // Hide all posters
    document.querySelectorAll('.poster-content').forEach(function(poster) {
      poster.style.display = 'none';
    });
    
    // Reset all buttons to outline style
    document.querySelectorAll('[id^="btn-poster"]').forEach(function(btn) {
      btn.className = 'btn btn-sm btn-outline-primary mx-1';
    });
    
    // Show selected poster
    document.getElementById(posterID).style.display = 'block';
    
    // Highlight current button
    document.getElementById('btn-' + posterID).className = 'btn btn-sm btn-primary mx-1';
  }
</script>






<h2 class="mt-4">Video Demos</h2>

<!-- Video Demo section -->
<div class="container mt-3">
  <div class="row">
    <!-- Video 1 -->
     <div class="col-md-6 mb-4">
      <div class="card">
        <div class="card-body">
          <h5 class="card-title">Robot Follower using YOLO</h5>
          <div class="embed-responsive embed-responsive-16by9">
            <iframe class="embed-responsive-item" 
                    src="https://www.youtube.com/embed/c7BVYvfMQGg" 
                    allowfullscreen>
            </iframe>
          </div>
          <p class="card-text mt-2">
            We used You only look once (YOLO), a real-time object detector for a tracking problem. The robot tracks the human and follows the human using a simple controller
          </p>
        </div>
      </div>
    </div>
    
    <!-- Video 2 -->
    <div class="col-md-6 mb-4">
  <div class="card">
    <div class="card-body">
      <h5 class="card-title">Robot Teleoperation using Hand Gestures : </h5>
      <div class="embed-responsive embed-responsive-16by9">
        <iframe class="embed-responsive-item" 
                src="https://www.youtube.com/embed/63KGr5Yohog" 
                allowfullscreen>
        </iframe>
      </div>
      <p class="card-text mt-2">
        We propose to classify simple Human Hand Gestures (Go, Right, Left) using Ultra-Wide Band(UWB) sensor data. This project integrates machine learning techniques for potential robotic applications
      </p>
    </div>
  </div>
</div>
  </div>

  <div class="row">
    <!-- Video 3 -->
    <div class="col-md-6 mb-4">
      <div class="card">
        <div class="card-body">
          <h5 class="card-title">YouTube Demo</h5>
          <div class="embed-responsive embed-responsive-16by9">
            <iframe class="embed-responsive-item" 
                    src="https://www.youtube.com/embed/DV956ZV1Nyk" 
                    allowfullscreen>
            </iframe>
          </div>
          <p class="card-text mt-2">
            YouTube demonstration of our research results.
          </p>
        </div>
      </div>
    </div>
    
    
  </div>
</div>

<div class="projects">





<div class="projects">

