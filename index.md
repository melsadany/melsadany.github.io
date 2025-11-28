---
title: "Muhammad Elsadany"
layout: default
---

<style>
  /* Reset and base styles */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  body {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    background-attachment: fixed;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
    min-height: 100vh;
  }
  
  /* Hide the download buttons */
  .btn, .header-btn {
    display: none !important;
  }
  
  /* Remove any theme-specific header styles that might show buttons */
  .page-header {
    background: transparent !important;
    color: white !important;
    padding: 0 !important;
    text-align: center;
  }
  
  .container {
    max-width: 1000px;
    margin: 0 auto;
    padding: 40px 20px;
  }
  
  .main-content {
    background: white;
    border-radius: 15px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.1);
    overflow: hidden;
  }
  
  .profile-header {
    text-align: center;
    margin-bottom: 50px;
    padding: 50px 30px 30px;
    background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
    color: white;
  }
  
  .profile-img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 20px;
    border: 4px solid rgba(255,255,255,0.3);
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
  }
  
  .profile-header h1 {
    margin: 0;
    font-size: 2.5em;
    color: white;
    text-shadow: 0 2px 4px rgba(0,0,0,0.3);
  }
  
  .profile-header p {
    font-size: 1.3em;
    margin: 10px 0 20px;
    color: rgba(255,255,255,0.9);
  }
  
  .profile-links a {
    margin: 0 15px;
    text-decoration: none;
    color: white;
    font-weight: 500;
    font-size: 1.1em;
    padding: 8px 15px;
    background: rgba(255,255,255,0.2);
    border-radius: 25px;
    transition: all 0.3s ease;
  }
  
  .profile-links a:hover {
    background: rgba(255,255,255,0.3);
    transform: translateY(-2px);
  }
  
  .content-wrapper {
    padding: 0 30px 50px;
  }
  
  .section {
    margin: 50px 0;
  }
  
  .section h2 {
    color: #2c3e50;
    border-bottom: 3px solid #3498db;
    padding-bottom: 10px;
    margin-bottom: 30px;
    font-size: 2em;
  }
  
  .talk, .project {
    background: #f8f9fa;
    padding: 25px;
    border-radius: 10px;
    margin: 30px 0;
    border-left: 4px solid #3498db;
    box-shadow: 0 5px 15px rgba(0,0,0,0.08);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .talk:hover, .project:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 30px rgba(0,0,0,0.15);
  }
  
  .talk h3, .project h3 {
    margin-top: 0;
    color: #2c3e50;
    font-size: 1.4em;
  }
  
  .talk h3 a, .project h3 a {
    color: #2c3e50;
    text-decoration: none;
  }
  
  .talk h3 a:hover, .project h3 a:hover {
    color: #3498db;
  }
  
  .talk img, .project img {
    max-width: 100%;
    border-radius: 8px;
    margin: 15px 0;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  }
  
  .tools {
    background: #e8f4fc;
    padding: 12px 15px;
    border-radius: 8px;
    margin: 15px 0;
    font-style: italic;
    border-left: 3px solid #3498db;
  }
  
  .gallery-section {
  margin: 50px 0;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  margin: 30px 0;
}

.gallery-item {
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 8px 20px rgba(0,0,0,0.15);
  transition: all 0.3s ease;
  position: relative;
  cursor: pointer;
  background: #f8f9fa;
}

.gallery-item:hover {
  transform: translateY(-8px) scale(1.02);
  box-shadow: 0 20px 40px rgba(0,0,0,0.25);
}

.gallery-item img {
  width: 100%;
  height: 300px;
  object-fit: contain;
  display: block;
  transition: transform 0.3s ease;
  padding: 10px;
  background: white;
}

.gallery-item:hover img {
  transform: scale(1.05);
}

/* Lightbox Modal Styles */
.lightbox {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  animation: fadeIn 0.3s;
}

.quote {
  font-style: italic;
  text-align: center;
  color: #7f8c8d;
  border-left: 3px solid #3498db;
  padding: 20px;
  margin: 30px 0;
  background: #f8f9fa;
  border-radius: 8px;
  font-size: 1.1em;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.lightbox-content {
  display: block;
  margin: auto;
  max-width: 90%;
  max-height: 90%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 8px;
  box-shadow: 0 0 40px rgba(0,0,0,0.5);
}

.close-lightbox {
  position: absolute;
  top: 20px;
  right: 30px;
  color: white;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
  z-index: 1001;
  transition: color 0.3s ease;
}

.close-lightbox:hover {
  color: #3498db;
}

.lightbox-nav {
  position: absolute;
  top: 50%;
  width: 100%;
  display: flex;
  justify-content: space-between;
  padding: 0 20px;
  transform: translateY(-50%);
}

.lightbox-nav button {
  background: rgba(255,255,255,0.2);
  border: none;
  color: white;
  font-size: 30px;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s ease;
}

.lightbox-nav button:hover {
  background: rgba(255,255,255,0.4);
}
  
  /* Responsive design */
  @media (max-width: 768px) {
    .container {
      padding: 20px 10px;
    }
    
    .content-wrapper {
      padding: 0 15px 30px;
    }
    
    .profile-header {
      padding: 30px 15px 20px;
    }
    
    .profile-img {
      width: 150px;
      height: 150px;
    }
    
    .profile-header h1 {
      font-size: 2em;
    }
    
    .profile-links a {
      display: block;
      margin: 10px auto;
      max-width: 200px;
    }
    
    .gallery-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="container">
  <!-- Profile Header -->
  <div class="profile-header">
    <img src="assets/images/profile/headshot.jpg" alt="Muhammad Elsadany" class="profile-img">
    <h1>Muhammad Elsadany</h1>
    <p><strong>Computational Biologist | Psychiatry Researcher</strong></p>
    <div class="profile-links">
      <a href="mailto:melsadany24@gmail.com">📧 Email</a>
      <a href="https://www.linkedin.com/in/melsadany/">💼 LinkedIn</a>
      <a href="https://github.com/melsadany">💻 GitHub</a>
      <a href="assets/docs/profile/Elsadany-resume_111625.pdf">📄 Resume</a>
      <a href="https://orcid.org/0000-0002-1019-3905">🔬 ORCiD</a>
    </div>
  </div>

  <!-- About Me Section -->
  <div class="section" id="about">
    <h2>About Me</h2>
    <p>My passion for genetics and mental health research stems from both personal experience and a deep curiosity about human behavior. As an autistic researcher, I bring a unique perspective to understanding neurodiversity—not just as a subject of study, but as a lived reality.</p>
    
    <p>My work focuses on decoding the complex relationships between genetics, cognition, and mental health through computational approaches. I integrate diverse data modalities—genetic, clinical, neuroimaging, audio, interview, and facial imagery—to uncover patterns that bridge scientific discovery with practical interventions.</p>
    
    <p>A central theme of my research is leveraging language as a powerful metric for understanding cognitive functions and mental health challenges. I'm particularly interested in developing accessible tools that can capture the nuances of human experience often missed by traditional assessments.</p>
    
    <p>My journey in the lab revealed how much I 'fit in' with the populations we study, leading to my own autism diagnosis at 25. This personal insight fuels my commitment to creating a more inclusive world where neurodiverse individuals are not just understood, but valued for their unique strengths.</p>
    
    <div class="quote">
      "I learn by going where I have to go." – Theodore Roethke
    </div>
    
    <p><em>Currently pursuing my PhD in Genetics at the University of Iowa, where I'm expanding my expertise in linguistics, computer vision, neuroimaging, and data science to better serve the neurodiversity community.</em></p>
  </div>

  <!-- Talks Section -->
  <div class="section" id="talks">
    <h2>Selected Talks & Presentations</h2>
    
    <div class="talk">
      <h3><a href="assets/docs/talks/INSAR.ppsx">Beyond Yes/No: A Multimodal Autism Propensity Score from Genes to Brain</a></h3>
      <p><strong>INSAR Conference 2025</strong> | <em>Oral Presentation</em></p>
      <img src="assets/images/INSAR/overview.jpg" alt="INSAR Presentation Preview">
      <p>Presented a novel deep learning framework that integrates multi-modal neuroimaging features—including fractional amplitude of low-frequency fluctuations (fALFF), structural morphometry, and diffusion tensor imaging (DTI) metrics—to generate a continuous autism likelihood score (0-1). This approach demonstrates the potential of combining multiple MRI modalities for improved neurophenotyping in autism spectrum disorder.</p>
      <div class="tools">
        <strong>Key Topics:</strong> Deep Learning, Multi-modal MRI Integration, fALFF, Structural MRI, DTI, Autism Biomarkers
      </div>
    </div>

    <div class="talk">
      <h3><a href="assets/docs/talks/INC.ppsx">Optimizing Structural MRI Processing Pipelines for 7T Data</a></h3>
      <p><strong>Iowa Neuroimaging Consortium, University of Iowa</strong> | <em>Invited Talk</em></p>
      <img src="assets/images/MRI-pipeline/overview.jpg" alt="MRI Pipeline Preview">
      <p>Comprehensive overview of structural MRI processing pipelines optimized for 7T scanner data, comparing various tools and approaches for cortical reconstruction, subcortical segmentation, and surface-based analysis. Provided practical guidance on pipeline selection based on specific research objectives and data characteristics.</p>
      <div class="tools">
        <strong>Key Topics:</strong> 7T MRI, Structural Processing Pipelines, Freesurfer, ANTs, FSL, Cortical Reconstruction, Quality Control
      </div>
    </div>
  </div>

  <!-- Projects Section -->
  <div class="section" id="projects">
    <h2>Featured Projects</h2>

    <div class="project">
      <h3>Gene Expression Signature of Human Brain Stimulation</h3>
      <img src="assets/images/brain-stim/overview.jpg" alt="Brain Stimulation Analysis">
      <ul>
        <li>Engineered an end-to-end computational pipeline for single-nuclei multi-omics (RNA+ATAC) data, implementing a bootstrapped pseudo-bulk strategy and mixed-effects models (lmmSeq) to identify cell-type-specific responses to electrical stimulation.</li>
        <li>Validated translational relevance through cross-species comparison (RRHO) with mouse models, identifying conserved gene sets.</li>
      </ul>
      <div class="tools">
        <strong>Tools:</strong> R, Seurat, lmmSeq, RRHO2, CellChat, scSeqComm, edgeR, DCA
      </div>
    </div>

    <div class="project">
      <h3>Exceptional Ability: A Multimodal Cognitive Study</h3>
      <img src="assets/images/te/overview-PS.jpg" alt="Exceptional Ability Overview">
      <ul>
        <li>Designed and implemented a multimodal analysis pipeline integrating NIH-Toolbox/IQ scores, a custom language task, acoustic feature extraction (audio), interview transcription (Whisper AI), facial landmarking (computer vision), and structural/functional/diffusion MRI.</li>
        <li>Developed a 10-minute language task that effectively captures cognitive performance, demonstrating potential as an efficient digital biomarker.</li>
      </ul>
      <div class="tools">
        <strong>Tools:</strong> WhisperAI, PWEsuite, GPT, Archetypes, lingmatch, ANTs, AFNI, FSL, freesurfer, DSI-studio
      </div>
    </div>

    <div class="project">
      <h3>Polygenic Drug Response Signatures</h3>
      <img src="assets/images/drug-response/overview.jpg" alt="Drug Response Analysis">
      <ul>
        <li>Developed a computational tool integrating genetic data (GWAS, eQTL, RNA-Seq) to generate personalized treatment recommendations for psychiatric disorders, with a focus on ADHD.</li>
        <li>Scaled the application to cohorts with 88,000+ participants (SPARK, ABCD) and validated predictions against behavioral scales (CBCL, BPM) and neuroimaging (fMRI) data.</li>
      </ul>
      <div class="tools">
        <strong>Tools:</strong> GWAS, eQTL, TWAS
      </div>
    </div>

    <div class="project">
      <h3>Mapping Brain-Wide Drug Effects using Deep Learning</h3>
      <img src="assets/images/drug-maps/overview2.jpg" alt="Drug Effects Brain Map">
      <ul>
        <li>Built a deep learning model that integrates brain-wide gene expression (Allen Institute) and fMRI trait maps with drug perturbation signatures (CMAP, LINCS) to predict functional brain activity changes for 838 compounds.</li>
        <li>Delivered insights through an interactive R Shiny application featuring 3D brain visualizations, linking compounds to phenotypic effects via Neurosynth and Neuromaps.</li>
      </ul>
      <div class="tools">
        <strong>Tools:</strong> DL, eQTL, TWAS, R Shiny
      </div>
    </div>

    <div class="project">
      <h3>Linguistic and Behavioral Patterns in Bipolar Disorder from Social Media</h3>
      <img src="assets/images/bp-reddit/overview.jpg" alt="Bipolar Reddit Analysis">
      <ul>
        <li>Analyzed 20 years of Reddit data to identify users self-identifying with bipolar disorder, extracting temporal patterns in activity, sleep cycles, emotional expression, and content preferences.</li>
        <li>Applied natural language processing to track linguistic markers of mood episodes, including sentiment analysis, topic modeling, and GPT-4 embeddings to quantify emotional volatility over time.</li>
        <li>Identified distinct behavioral signatures including disrupted sleep patterns (via posting times), content topic shifts, and cyclical emotional patterns corresponding to reported mood episodes.</li>
      </ul>
      <div class="tools">
        <strong>Tools:</strong> Python, NLP, GPT-4 Embeddings, Time-series Analysis, Sentiment Analysis, Topic Modeling
      </div>
    </div>
  </div>

  <!-- Automated Gallery Section -->
  <div class="gallery-section" id="gallery">
  <h2>Data Visualization Gallery</h2>
  <p>Explore my favorite data visualizations across all research projects. All figures are attached without any captions as they are not public yet. Click on any visualization to view it in full size. Navigate with arrow keys or swipe.</p>
    
    <div id="gallery-container" class="gallery-grid">
      <!-- Gallery will be populated automatically by JavaScript -->
      <p>Loading visualizations...</p>
    </div>
  </div>
</div>

<!-- Lightbox Modal -->
<div id="lightbox" class="lightbox">
  <span class="close-lightbox" onclick="closeLightbox()">&times;</span>
  <div class="lightbox-nav">
    <button onclick="changeImage(-1)">&#10094;</button>
    <button onclick="changeImage(1)">&#10095;</button>
  </div>
  <img class="lightbox-content" id="lightbox-img">
</div>

<script>
// Simplified gallery with lightbox functionality
document.addEventListener('DOMContentLoaded', function() {
  // Define your gallery images - just file paths, no titles/descriptions
  const galleryImages = [
    'assets/images/drug-maps/overview.jpg',
    'assets/images/te/overview-lang.jpg',
    'assets/gallery/arch-1.png',
    'assets/gallery/bar-1.png',
    'assets/gallery/bm-v1.jpg',
    'assets/gallery/cyto-1.jpg',
    'assets/gallery/den-1.png',
    'assets/gallery/den-2.png',
    'assets/gallery/den-3.png',
    'assets/gallery/dwi.jpg',
    'assets/gallery/euc-1.jpg',
    'assets/gallery/fALFF-1.png',
    'assets/gallery/forest-1.png',
    'assets/gallery/iq-2.jpg',
    'assets/gallery/jeo-1.png',
    'assets/gallery/loli-1.png',
    'assets/gallery/mo-1.png',
    'assets/gallery/mph-1.svg',
    'assets/gallery/nct-1.png',
    'assets/gallery/ne-1.jpg',
    'assets/gallery/net-1.png',
    'assets/gallery/net-2.png',
    'assets/gallery/peaks-1.jpg',
    'assets/gallery/rad-1.svg',
    'assets/gallery/scat-1.png',
    'assets/gallery/scat-2.png',
    'assets/gallery/scat-3.png',
    'assets/gallery/sel-1.jpg',
    'assets/gallery/sem-1.png',
    'assets/gallery/sem-2.jpg',
    'assets/gallery/st.png',
    'assets/gallery/time-1.gif',
    'assets/gallery/time-2.png',
    'assets/gallery/umap-1.jpg',
    'assets/gallery/upset-1.png',
    'assets/gallery/viol-1.png',
    'assets/gallery/wc-1.png'
    
    // Add more image paths here as you create them
    // Format: 'assets/images/folder-name/filename.jpg'
  ];
  
  const galleryContainer = document.getElementById('gallery-container');
  let currentImageIndex = 0;
  
  // Initialize gallery
  if (galleryContainer && galleryImages.length > 0) {
    galleryContainer.innerHTML = '';
    
    galleryImages.forEach((imageSrc, index) => {
      const galleryItem = document.createElement('div');
      galleryItem.className = 'gallery-item';
      galleryItem.onclick = () => openLightbox(index);
      
      const img = document.createElement('img');
      img.src = imageSrc;
      img.alt = 'Research Visualization';
      img.loading = 'lazy';
      
      galleryItem.appendChild(img);
      galleryContainer.appendChild(galleryItem);
    });
  }
  
  // Lightbox functions
  window.openLightbox = function(index) {
    currentImageIndex = index;
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    
    lightbox.style.display = 'block';
    lightboxImg.src = galleryImages[index];
    
    // Prevent body scroll when lightbox is open
    document.body.style.overflow = 'hidden';
  }
  
  window.closeLightbox = function() {
    document.getElementById('lightbox').style.display = 'none';
    document.body.style.overflow = 'auto';
  }
  
  window.changeImage = function(step) {
    currentImageIndex += step;
    
    // Loop around if at ends
    if (currentImageIndex >= galleryImages.length) {
      currentImageIndex = 0;
    } else if (currentImageIndex < 0) {
      currentImageIndex = galleryImages.length - 1;
    }
    
    openLightbox(currentImageIndex);
  }
  
  // Keyboard navigation
  document.addEventListener('keydown', function(e) {
    const lightbox = document.getElementById('lightbox');
    if (lightbox.style.display === 'block') {
      if (e.key === 'Escape') {
        closeLightbox();
      } else if (e.key === 'ArrowLeft') {
        changeImage(-1);
      } else if (e.key === 'ArrowRight') {
        changeImage(1);
      }
    }
  });
  
  // Close lightbox when clicking outside the image
  document.getElementById('lightbox').addEventListener('click', function(e) {
    if (e.target === this) {
      closeLightbox();
    }
  });
  
  // Touch swipe support for mobile
  let touchStartX = 0;
  let touchEndX = 0;
  
  document.getElementById('lightbox').addEventListener('touchstart', function(e) {
    touchStartX = e.changedTouches[0].screenX;
  });
  
  document.getElementById('lightbox').addEventListener('touchend', function(e) {
    touchEndX = e.changedTouches[0].screenX;
    handleSwipe();
  });
  
  function handleSwipe() {
    const swipeThreshold = 50;
    const diff = touchStartX - touchEndX;
    
    if (Math.abs(diff) > swipeThreshold) {
      if (diff > 0) {
        changeImage(1); // Swipe left - next image
      } else {
        changeImage(-1); // Swipe right - previous image
      }
    }
  }
});
</script>