---
title: "Muhammad Elsadany"
layout: default
---

<style>
  .container {
    max-width: 1000px;
    margin: 0 auto;
    padding: 20px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
  }
  
  .profile-header {
    text-align: center;
    margin-bottom: 50px;
    padding: 30px 0;
    border-bottom: 2px solid #f0f0f0;
  }
  
  .profile-img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 20px;
    border: 4px solid #2c3e50;
  }
  
  .profile-header h1 {
    margin: 0;
    font-size: 2.5em;
    color: #2c3e50;
  }
  
  .profile-header p {
    font-size: 1.3em;
    margin: 10px 0 20px;
    color: #7f8c8d;
  }
  
  .profile-links a {
    margin: 0 15px;
    text-decoration: none;
    color: #3498db;
    font-weight: 500;
    font-size: 1.1em;
  }
  
  .profile-links a:hover {
    color: #2980b9;
    text-decoration: underline;
  }
  
  .section {
    margin: 50px 0;
  }
  
  .section h2 {
    color: #2c3e50;
    border-bottom: 2px solid #3498db;
    padding-bottom: 10px;
    margin-bottom: 30px;
  }
  
  .talk, .project {
    background: #f8f9fa;
    padding: 25px;
    border-radius: 10px;
    margin: 30px 0;
    border-left: 4px solid #3498db;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  }
  
  .talk h3, .project h3 {
    margin-top: 0;
    color: #2c3e50;
  }
  
  .talk img, .project img {
    max-width: 100%;
    border-radius: 8px;
    margin: 15px 0;
    box-shadow: 0 3px 10px rgba(0,0,0,0.1);
  }
  
  .tools {
    background: #e8f4fc;
    padding: 10px 15px;
    border-radius: 5px;
    margin: 15px 0;
    font-style: italic;
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
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
  }
  
  .gallery-item:hover {
    transform: translateY(-5px);
  }
  
  .gallery-item img {
    width: 100%;
    height: 250px;
    object-fit: cover;
    display: block;
  }
  
  .quote {
    font-style: italic;
    text-align: center;
    color: #7f8c8d;
    border-left: 3px solid #3498db;
    padding-left: 20px;
    margin: 30px 0;
  }
</style>

<div class="container">
  <!-- Profile Header -->
  <div class="profile-header">
    <img src="assets/images/profile/headshot.jpg" alt="Muhammad Elsadany" class="profile-img">
    <h1>Muhammad Elsadany</h1>
    <p><strong>Computational Biologist | Neuroscience Researcher</strong></p>
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
      <h3><a href="projects/brain-stim.md">Gene Expression Signature of Human Brain Stimulation</a></h3>
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
      <h3><a href="projects/te.md">Exceptional Ability: A Multimodal Cognitive Study</a></h3>
      <img src="assets/images/te/overview-PS.jpg" alt="Exceptional Ability Overview">
      <img src="assets/images/te/dwi1.jpg" alt="DTI Analysis 1">
      <img src="assets/images/te/dwi2.jpg" alt="DTI Analysis 2">
      <ul>
        <li>Designed and implemented a multimodal analysis pipeline integrating NIH-Toolbox/IQ scores, a custom language task, acoustic feature extraction (audio), interview transcription (Whisper AI), facial landmarking (computer vision), and structural/functional/diffusion MRI.</li>
        <li>Developed a 10-minute language task that effectively captures cognitive performance, demonstrating potential as an efficient digital biomarker.</li>
      </ul>
      <div class="tools">
        <strong>Tools:</strong> WhisperAI, PWEsuite, GPT, Archetypes, lingmatch, ANTs, AFNI, FSL, freesurfer, DSI-studio
      </div>
    </div>

    <div class="project">
      <h3><a href="projects/drug-response.md">Polygenic Drug Response Signatures</a></h3>
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
      <h3><a href="projects/drug-maps.md">Mapping Brain-Wide Drug Effects using Deep Learning</a></h3>
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
      <h3><a href="projects/bp-reddit.md">Linguistic and Behavioral Patterns in Bipolar Disorder from Social Media</a></h3>
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
    <p>Explore my favorite data visualizations across all research projects. This gallery automatically loads images from my visualization collection.</p>
    
    <div id="gallery-container" class="gallery-grid">
      <!-- Gallery will be populated automatically by JavaScript -->
      <p>Loading visualizations...</p>
    </div>
  </div>
</div>

<script>
// Simple JavaScript to automatically load gallery images
document.addEventListener('DOMContentLoaded', function() {
  // Define your gallery images here - just update this array when you add new images
  const galleryImages = [
    'assets/images/brain-stim/overview.jpg',
    'assets/images/drug-maps/overview.jpg',
    'assets/images/drug-maps/overview2.jpg',
    'assets/images/drug-response/overview.jpg',
    'assets/images/te/overview-PS.jpg',
    'assets/images/te/dwi1.jpg',
    'assets/images/te/dwi2.jpg',
    'assets/images/bp-reddit/overview.jpg',
    'assets/images/INSAR/overview.jpg',
    'assets/images/MRI-pipeline/overview.jpg'
    // Add more image paths here as you create them
    // Format: 'assets/images/folder-name/filename.jpg'
  ];
  
  const galleryContainer = document.getElementById('gallery-container');
  
  if (galleryContainer && galleryImages.length > 0) {
    galleryContainer.innerHTML = ''; // Clear loading message
    
    galleryImages.forEach(imagePath => {
      const galleryItem = document.createElement('div');
      galleryItem.className = 'gallery-item';
      
      const img = document.createElement('img');
      img.src = imagePath;
      img.alt = 'Research Visualization';
      img.loading = 'lazy'; // For better performance
      
      galleryItem.appendChild(img);
      galleryContainer.appendChild(galleryItem);
    });
  }
});
</script>