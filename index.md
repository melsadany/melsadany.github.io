---
title: "Muhammad Elsadany | Portfolio"
layout: default
---

<style>
  /* Reset and base styles */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  /* Your Custom Color Palette */
  :root {
    --primary: #4782b4;       /* Trustworthy blue */
    --primary-dark: #3C4856;  /* Deep navy */
    --accent: #ff4600;        /* Vibrant orange - attention */
    --secondary: #39C08F;     /* Fresh green - success */
    --tertiary: #00C0C5;      /* Teal - highlights */
    --warm: #C1624A;          /* Warm terracotta */
    --light: #88ADE1;         /* Light blue */
    --neutral: #627899;       /* Muted blue-gray */
    --pale: #F3B199;          /* Pale peach */
    --dark: #55433C;          /* Dark brown */
    --muted: #A6665F;         /* Muted red */
    --purple: #AE6885;        /* Soft purple */
    --deep-purple: #783753;   /* Deep plum */
  }
  
  body {
    background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
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
    background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary) 50%, var(--tertiary) 100%);
    color: white;
    position: relative;
    overflow: hidden;
  }
  
  .profile-header::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: 
      radial-gradient(circle at 20% 80%, var(--accent) 0%, transparent 50%),
      radial-gradient(circle at 80% 20%, var(--secondary) 0%, transparent 50%),
      radial-gradient(circle at 40% 40%, var(--purple) 0%, transparent 50%);
    opacity: 0.1;
    z-index: 1;
  }
  
  .profile-header > * {
    position: relative;
    z-index: 2;
  }
  
  .profile-img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 20px;
    border: 4px solid rgba(255,255,255,0.3);
    box-shadow: 
      0 10px 30px rgba(0,0,0,0.3),
      0 0 0 2px var(--accent);
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
  
  .profile-links {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    max-width: 800px;
    margin: 0 auto;
  }
  
  .profile-links a {
    text-decoration: none;
    color: white;
    font-weight: 500;
    font-size: 0.95em;
    padding: 6px 12px;
    background: rgba(255,255,255,0.2);
    border-radius: 20px;
    transition: all 0.3s ease;
    white-space: nowrap;
    border: 1px solid rgba(255,255,255,0.3);
  }
  
  .profile-links a:hover {
    background: var(--accent);
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(255, 70, 0, 0.3);
  }
  
  .content-wrapper {
    padding: 0 30px 50px;
  }
  
  .section {
    margin: 50px 0;
  }
  
  .section h2 {
    color: var(--primary-dark);
    border-bottom: 3px solid var(--accent);
    padding-bottom: 10px;
    margin-bottom: 30px;
    font-size: 2em;
  }
  
  .talk, .project {
    background: #f8f9fa;
    padding: 25px;
    border-radius: 10px;
    margin: 30px 0;
    border-left: 4px solid var(--accent);
    box-shadow: 0 5px 15px rgba(0,0,0,0.08);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }
  
  .talk::before, .project::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    width: 4px;
    background: linear-gradient(to bottom, var(--accent), var(--secondary));
  }
  
  .talk:hover, .project:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 30px rgba(0,0,0,0.15);
  }
  
  .talk h3, .project h3 {
    margin-top: 0;
    color: var(--primary-dark);
    font-size: 1.4em;
  }
  
  .talk h3 a, .project h3 a {
    color: var(--primary-dark);
    text-decoration: none;
  }
  
  .talk h3 a:hover, .project h3 a:hover {
    color: var(--accent);
  }
  
  .talk img, .project img {
    max-width: 100%;
    border-radius: 8px;
    margin: 15px 0;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    border: 2px solid var(--light);
  }
  
  .tools {
    background: linear-gradient(135deg, var(--light) 0%, var(--tertiary) 100%);
    color: white;
    padding: 12px 15px;
    border-radius: 8px;
    margin: 15px 0;
    font-style: italic;
    border-left: 3px solid var(--accent);
  }
  
  .quote {
    font-style: italic;
    text-align: center;
    color: var(--neutral);
    border-left: 3px solid var(--secondary);
    padding: 20px;
    margin: 30px 0;
    background: linear-gradient(135deg, #f8f9fa 0%, #e8f4fc 100%);
    border-radius: 8px;
    font-size: 1.1em;
    position: relative;
  }
  
  .quote::before {
    content: '"';
    font-size: 4em;
    color: var(--tertiary);
    position: absolute;
    top: -10px;
    left: 20px;
    opacity: 0.3;
    font-family: Georgia, serif;
  }
  
  /* Gallery Styles */
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
    border: 2px solid var(--light);
  }

  .gallery-item:hover {
    transform: translateY(-8px) scale(1.02);
    box-shadow: 
      0 20px 40px rgba(0,0,0,0.25),
      0 0 0 2px var(--accent);
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

  /* Show More Button */
  .show-more-button {
    background: linear-gradient(135deg, var(--accent) 0%, var(--warm) 100%);
    color: white;
    border: none;
    padding: 12px 30px;
    border-radius: 25px;
    font-size: 1.1em;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba(255, 70, 0, 0.3);
  }

  .show-more-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(255, 70, 0, 0.4);
    background: linear-gradient(135deg, var(--warm) 0%, var(--accent) 100%);
  }

  .gallery-count {
    text-align: center;
    color: var(--neutral);
    margin: 15px 0;
    font-style: italic;
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
    border: 2px solid var(--accent);
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
    background: var(--accent);
    width: 50px;
    height: 50px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
  }

  .close-lightbox:hover {
    color: white;
    background: var(--warm);
    transform: scale(1.1);
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
    background: var(--accent);
    border: none;
    color: white;
    font-size: 30px;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
  }

  .lightbox-nav button:hover {
    background: var(--warm);
    transform: scale(1.1);
  }
  
  /* Media & Links Section */
  .links-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 25px;
    margin: 30px 0;
  }

  .link-card {
    background: white;
    border-radius: 12px;
    padding: 25px;
    text-align: center;
    box-shadow: 0 5px 20px rgba(0,0,0,0.08);
    border: 2px solid var(--light);
    transition: all 0.3s ease;
    display: flex;
    flex-direction: column;
    height: 100%;
    position: relative;
    overflow: hidden;
  }

  .link-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--accent), var(--secondary), var(--tertiary));
  }

  .link-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 15px 35px rgba(0,0,0,0.15);
    border-color: var(--accent);
  }

  .link-icon {
    font-size: 2.5em;
    margin-bottom: 15px;
    background: linear-gradient(135deg, var(--primary), var(--tertiary));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .link-card h3 {
    color: var(--primary-dark);
    margin: 0 0 12px 0;
    font-size: 1.3em;
  }

  .link-card p {
    color: var(--neutral);
    margin: 0 0 20px 0;
    line-height: 1.5;
    flex-grow: 1;
  }

  .link-button {
    display: inline-block;
    background: linear-gradient(135deg, var(--primary) 0%, var(--tertiary) 100%);
    color: white;
    text-decoration: none;
    padding: 10px 20px;
    border-radius: 25px;
    font-weight: 500;
    transition: all 0.3s ease;
    border: none;
    cursor: pointer;
    margin-top: auto;
  }

  .link-button:hover {
    background: linear-gradient(135deg, var(--accent) 0%, var(--warm) 100%);
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(255, 70, 0, 0.3);
    color: white;
    text-decoration: none;
  }
  
  /* Video Section Styles */
  .video-container {
    max-width: 800px;
    margin: 30px auto;
    position: relative;
  }
  
  .video-protection-note {
    text-align: center;
    margin-top: 10px;
    color: #7f8c8d;
    font-style: italic;
  }
  
  /* Additional protection styles */
  video {
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }



  /* Color coding for different sections */
  .talk:nth-child(odd)::before {
    background: linear-gradient(to bottom, var(--accent), var(--warm));
  }
  
  .talk:nth-child(even)::before {
    background: linear-gradient(to bottom, var(--secondary), var(--tertiary));
  }
  
  .project:nth-child(4n+1)::before {
    background: linear-gradient(to bottom, var(--accent), var(--warm));
  }
  
  .project:nth-child(4n+2)::before {
    background: linear-gradient(to bottom, var(--secondary), var(--tertiary));
  }
  
  .project:nth-child(4n+3)::before {
    background: linear-gradient(to bottom, var(--purple), var(--deep-purple));
  }
  
  .project:nth-child(4n+4)::before {
    background: linear-gradient(to bottom, var(--primary), var(--light));
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
    
    .profile-header p {
      font-size: 1.1em;
    }
    
    .profile-links {
      gap: 8px;
    }
    
    .profile-links a {
      font-size: 0.85em;
      padding: 5px 10px;
      display: inline-block;
    }
    
    .gallery-grid {
      grid-template-columns: 1fr;
    }
    
    .links-grid {
      grid-template-columns: 1fr;
    }
  }

  /* For very small screens */
  @media (max-width: 480px) {
    .profile-links {
      flex-direction: column;
      align-items: center;
    }
    
    .profile-links a {
      width: 200px;
      text-align: center;
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

<!-- Video Summary Section -->
<div class="section" id="video-summary">
  <h2>Video Summary</h2>
  <p>For a quick overview of my research and background, watch this video summary created by NotebookLM:</p>
  
  <div class="video-container">
    <video 
      id="summaryVideo"
      controls
      controlsList="nodownload" 
      poster="assets/video/overview.png"
      oncontextmenu="return false;"
      style="width: 100%; border-radius: 10px; box-shadow: 0 10px 30px rgba(0,0,0,0.2);"
    >
      <source src="assets/video/vid-2.mp4" type="video/mp4">
      Your browser doesn't support the video tag. Please <a href="assets/video/vid-1.mp4">download the video</a> instead.
    </video>
    
    <div class="video-protection-note">
      <small>🔒 Video streaming only - download disabled for privacy</small>
    </div>
  </div>
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

<!-- Gallery Section -->
<div class="gallery-section" id="gallery">
  <h2>Data Visualization Gallery</h2>
  <p>Explore my favorite data visualizations across all research projects. Click on any visualization to view it in full size.</p>
  
  <div id="gallery-container" class="gallery-grid">
    <!-- Initial images will be loaded here -->
  </div>
  
  <div style="text-align: center; margin-top: 30px;">
    <button id="show-more-btn" class="show-more-button">Show More Visualizations</button>
    <button id="show-less-btn" class="show-more-button" style="display: none;">Show Less</button>
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
// Gallery with show more functionality
document.addEventListener('DOMContentLoaded', function() {
  // Define your gallery images - just file paths
  const galleryImages = [
    // first set
    'assets/gallery/arch-1.png',
    'assets/gallery/dwi.jpg',
    'assets/gallery/nct-1.png',
    'assets/gallery/rad-1.svg',
    'assets/gallery/ne-1.jpg',
    'assets/gallery/wc-1.png',
    
    // remaining images
    
    'assets/images/drug-maps/overview.jpg',
    'assets/images/te/overview-lang.jpg',
    'assets/gallery/bar-1.png',
    'assets/gallery/bm-v1.jpg',
    'assets/gallery/cyto-1.jpg',
    'assets/gallery/den-1.png',
    'assets/gallery/den-2.png',
    'assets/gallery/den-3.jpg',
    'assets/gallery/euc-1.jpg',
    'assets/gallery/fALFF-1.png',
    'assets/gallery/forest-1.png',
    'assets/gallery/iq-2.jpg',
    'assets/gallery/jeo-1.png',
    'assets/gallery/loli-1.png',
    'assets/gallery/mo-1.png',
    'assets/gallery/mph-1.svg',
    'assets/gallery/net-1.png',
    'assets/gallery/net-2.png',
    'assets/gallery/peaks-1.jpg',
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
    'assets/gallery/viol-1.png'
  ];
  
  const galleryContainer = document.getElementById('gallery-container');
  const showMoreBtn = document.getElementById('show-more-btn');
  const showLessBtn = document.getElementById('show-less-btn');
  let currentImageIndex = 0;
  let imagesPerLoad = 6; // Number of images to show initially and per "show more"
  let currentlyVisible = 0;
  
  // Initialize gallery
  if (galleryContainer && galleryImages.length > 0) {
    // Show initial set of images
    loadMoreImages();
    updateButtonVisibility();
  }
  
  // Load more images function
  function loadMoreImages() {
    const endIndex = Math.min(currentlyVisible + imagesPerLoad, galleryImages.length);
    
    for (let i = currentlyVisible; i < endIndex; i++) {
      const galleryItem = document.createElement('div');
      galleryItem.className = 'gallery-item';
      galleryItem.onclick = () => openLightbox(i);
      
      const img = document.createElement('img');
      img.src = galleryImages[i];
      img.alt = 'Research Visualization';
      img.loading = 'lazy';
      
      galleryItem.appendChild(img);
      galleryContainer.appendChild(galleryItem);
    }
    
    currentlyVisible = endIndex;
    updateButtonVisibility();
  }
  
  // Show less images function
  function showLessImages() {
    // Remove all gallery items
    galleryContainer.innerHTML = '';
    currentlyVisible = 0;
    
    // Reload only the initial set
    loadMoreImages();
  }
  
  // Update button visibility based on current state
  function updateButtonVisibility() {
    if (currentlyVisible >= galleryImages.length) {
      showMoreBtn.style.display = 'none';
      showLessBtn.style.display = 'inline-block';
    } else {
      showMoreBtn.style.display = 'inline-block';
      showLessBtn.style.display = 'none';
    }
    
    // Update gallery count display
    updateGalleryCount();
  }
  
  // Add gallery count display
  function updateGalleryCount() {
    // Remove existing count if any
    const existingCount = document.getElementById('gallery-count');
    if (existingCount) {
      existingCount.remove();
    }
    
    // Create new count display
    const countDiv = document.createElement('div');
    countDiv.id = 'gallery-count';
    countDiv.className = 'gallery-count';
    countDiv.textContent = `Showing ${currentlyVisible} of ${galleryImages.length} visualizations`;
    
    // Insert after gallery container
    galleryContainer.parentNode.insertBefore(countDiv, galleryContainer.nextSibling);
  }
  
  // Button event listeners
  showMoreBtn.addEventListener('click', loadMoreImages);
  showLessBtn.addEventListener('click', showLessImages);
  
  // Lightbox functions (keep your existing lightbox code)
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

// Video protection
document.addEventListener('DOMContentLoaded', function() {
  const video = document.getElementById('summaryVideo');
  
  if (video) {
    // Disable right-click on video
    video.addEventListener('contextmenu', function(e) {
      e.preventDefault();
      return false;
    });
    
    // Prevent video download via keyboard shortcuts
    document.addEventListener('keydown', function(e) {
      if (e.ctrlKey && (e.key === 's' || e.key === 'S')) {
        e.preventDefault();
        return false;
      }
    });
    
    // Additional protection - hide source on inspect (basic)
    video.addEventListener('loadstart', function() {
      // This makes it slightly harder to find the direct video URL
      const sources = video.getElementsByTagName('source');
      for (let source of sources) {
        source.setAttribute('data-src', source.src);
        source.src = '';
      }
      // Restore sources after a brief moment
      setTimeout(() => {
        for (let source of sources) {
          source.src = source.getAttribute('data-src');
        }
      }, 100);
    });
  }
});
</script>

<!-- Media & Links Section -->
<div class="section" id="media-links">
  <h2>Media & Additional Links</h2>
  <p>Explore more about my background, research environment, and contributions:</p>
  
  <div class="links-grid">
    <!-- Personal Story -->
    <div class="link-card">
      <div class="link-icon"></div>
      <h3>My Personal Journey</h3>
      <p>Read about my path into computational psychiatry and neurodiversity research</p>
      <a href="https://michaelson.lab.uiowa.edu/news/2025/02/ui-psychiatry-graduate-student-muhammad-elsadany-decodes-mental-health-data-and-his" class="link-button" target="_blank">Read Story</a>
    </div>

    <!-- Lab Profile -->
    <div class="link-card">
      <div class="link-icon"></div>
      <h3>Michaelson Lab</h3>
      <p>Learn about the research environment and team behind my PhD work</p>
      <a href="https://michaelson.lab.uiowa.edu/people/muhammad-elsadany" class="link-button" target="_blank">Visit Lab</a>
    </div>

    <!-- Program Profile -->
    <div class="link-card">
      <div class="link-icon"></div>
      <h3>IGP in Genetics</h3>
      <p>Explore the interdisciplinary genetics program at University of Iowa</p>
      <a href="https://genetics.grad.uiowa.edu/people/muhammad-elsadany" class="link-button" target="_blank">Program Info</a>
    </div>

    <!-- News Articles -->
    <div class="link-card">
      <div class="link-icon"></div>
      <h3>Research Features</h3>
      <p>News article about our research</p>
      <a href="https://medicineiowa.org/fall-2024/closer-exceptional-processing" class="link-button" target="_blank">View Articles</a>
    </div>

    <!-- Conference Materials -->
<div class="link-card">
  <div class="link-icon">🎤</div>
  <h3>INSAR 2025 Talk</h3>
  <p>Beyond Yes/No: A Multimodal Autism Propensity Score from Genes to Brain</p>
  <a href="https://view.officeapps.live.com/op/view.aspx?src=https://melsadany.github.io/assets/docs/talks/INSAR.ppsx" 
     class="link-button" target="_blank">View Presentation with Animations</a>
  <div class="download-note">
    <small><a href="assets/docs/talks/INSAR.ppsx" download>Download Original</a></small>
  </div>
</div>
    <div class="link-card">
      <div class="link-icon"></div>
      <h3>INC Talk</h3>
      <p>Slides from my presentation at INC</p>
      <a href="assets/docs/talks/INC.ppsx" class="link-button">Access Materials</a>
    </div>
    <div class="link-card">
      <div class="link-icon"></div>
      <h3>Seminar Talk</h3>
      <p>Slides from my lst presentation at the IGPG seminar series</p>
      <a href="assets/docs/talks/te-PS.ppsx" class="link-button">Access Materials</a>
    </div>


    </div>
  </div>
</div>