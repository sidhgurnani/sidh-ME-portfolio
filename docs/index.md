#
<div style="display: flex; align-items: center; gap: 30px;">
  <img src="./assets/Headshot.jpeg" alt="Professional Headshot" style="width: 150px; height: auto; border-radius: 8px;">
  
  <div>
    <div style="font-size: 2.5rem; font-weight: bold;">Sidh Gurnani</div>
    <div style="font-size: 1rem;">B.S. Mechanical Engineering · Purdue University · May 2025</div>
  </div>
</div>

## **About Me**
Hello! I am a mechanical engineering graduate with a strong passion for learning, problem-solving, and developing innovative solutions. I am a dependable and self-motivated individual who actively seeks opportunities to expand my knowledge and skills while growing both professionally and personally. I’m excited to contribute to meaningful projects and to continuously improve through new challenges.

My experience includes working with various tools and programs that allow me to contribute to projects on all fronts, notably:

* **CAD & FEA:** Siemens NX, Creo Parametric, ANSYS  
* **Programming:** Arduino (C/C++), Python, MATLAB, Simulink, Java, HTML  
* **Other/Misc:** Computer Vision (YOLO), 3D Printing, Manual & CNC Machining, Microsoft Office, MkDocs Documentation

I enjoy tackling complex challenges that require a balance of creative thinking and technical precision. I have experience self-managing projects, coordinating tasks, and documenting work clearly, which allows me to apply a basic level of project management while leveraging AI and machine learning to drive projects forward. This approach enables me to deliver innovative and practical solutions across a variety of engineering fields, continuously learning and adapting as I grow in my career.

In addition, I have also passed the Fundamentals of Engineering Mechanical Exam. View my certificate [here](https://www.credly.com/badges/e26c9eab-09fa-4799-9187-35e7419987a9/linked_in_profile).

Outside of engineering, I enjoy exploring new interests and developing skills that broaden my perspective. I’m eager to collaborate with others and contribute to projects that drive meaningful results.

<div><br></div>

## **Education**
_B.S. Mechanical Engineering · Purdue University · Aug 2021 - May 2025_

**Coursework:**

* **Math:** Calculus I-III; Linear Algebra; Differential Equations
* **Controls:** Electrical Engineering Fundamentals I; Controls I; Controls II
* **Mechanics:** Statics; Dynamics; Mechanics of Materials; Machine Design; Structure and Properties of Materials
* **Programming:** Object Oriented Programming (in Java); Entry-Level Programming in Python; The Data Mine Seminar II; The Data Mine Corporate Partners IV
* **Energy:** Thermodynamics I; Fluid Mechanics; Fluid Mechanics Lab; Heat and Mass Transfer
* **Design:** Graphical Communication; Computer Aided Design & Prototyping (Toy Design); Tools, Methods, and Techniques for Rapid, Iterative Product Design and Analysis; Sophomore Design; Capstone Senior Design
* **Other Electives:** Electric Vehicle Design; Engineering Economics; Introduction to Finite Element Analysis; System Methods

**Involvement:**

* **Purdue Formula SAE:** Drivetrain Member (September 2022 to May 2024) &rarr; Drivetrain System Owner (June 2024 to May 2025)
* **The Data Mine:** Data Science Undergraduate Reasearcher (January 2025 to May 2025)
* **ME 290 Peer Mentor:** (August 2024 to May 2025)

**Certificates (Personal Enrichment):**

<div id="gallery" style="display: flex; flex-wrap: wrap; gap: 10px;"></div>

<!-- Lightbox overlay -->
<div id="lightbox" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%;
  background: rgba(0,0,0,0.8); justify-content:center; align-items:center; z-index:1000;">
  <button id="prevBtn" style="position:absolute; left:20px; color:white; font-size:2rem; background:none; border:none; cursor:pointer;">&#10094;</button>
  <img id="lightbox-img" style="max-width:90%; max-height:90%; border-radius:10px; box-shadow:0 4px 20px rgba(0,0,0,0.5);" />
  <button id="nextBtn" style="position:absolute; right:20px; color:white; font-size:2rem; background:none; border:none; cursor:pointer;">&#10095;</button>
</div>

<style>
  #gallery img.thumb {
    width: 100%;
    max-width: 200px;
    cursor: pointer;
    border-radius: 6px;
    transition: transform 0.2s;
  }

  #gallery img.thumb:hover {
    transform: scale(1.05);
  }

  @media (max-width: 600px) {
    #gallery img.thumb {
      max-width: 45%;
    }
  }

  #prevBtn, #nextBtn {
    user-select: none;
  }
</style>

<script>
const galleryDiv = document.getElementById('gallery');
const lightbox = document.getElementById('lightbox');
const lightboxImg = document.getElementById('lightbox-img');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');

const images = [
  "certifications/7xy1ONQNmG1h6k8qFPYqmg.png",
  "certifications/8PGDc0DdpLxGIGom4GDFGg.png",
  "certifications/uH59YMFVLsP2IJ435OO8cQ.png",
  "certifications/Eyso7ypwAHqH18YXTjpg1g.png",
  "certifications/Python 101 for Data Science.jpg",
  "certifications/Data Visualization with Python.jpg",
  "certifications/Machine Learning with Python.jpg",
  "certifications/Customer Clustering with KMeans to Boost Business Strategy.jpg",
  "certifications/Precise Predictions Classification for Flower and Tumors.jpg",
  "certifications/Predictions Regression for Car Mileage and Diamond Price.jpg"
];

let currentIndex = 0;

// Load thumbnails
images.forEach((src, i) => {
  const thumb = document.createElement('img');
  thumb.src = src;
  thumb.className = 'thumb';

  thumb.onclick = () => openLightbox(i);

  galleryDiv.appendChild(thumb);
});

function openLightbox(index) {
  currentIndex = index;
  lightbox.style.display = "flex";
  lightboxImg.src = images[currentIndex];
}

function closeLightbox() {
  lightbox.style.display = "none";
}

function showNext() {
  currentIndex = (currentIndex + 1) % images.length;
  lightboxImg.src = images[currentIndex];
}

function showPrev() {
  currentIndex = (currentIndex - 1 + images.length) % images.length;
  lightboxImg.src = images[currentIndex];
}

// Navigation
nextBtn.onclick = (e) => { e.stopPropagation(); showNext(); };
prevBtn.onclick = (e) => { e.stopPropagation(); showPrev(); };

// Close on background click
lightbox.onclick = closeLightbox;

// Keyboard controls
document.addEventListener('keydown', (e) => {
  if (lightbox.style.display === "flex") {
    if (e.key === "ArrowRight") showNext();
    if (e.key === "ArrowLeft") showPrev();
    if (e.key === "Escape") closeLightbox();
  }
});
</script>

<div><br></div>

## **Projects**

<div class="grid cards" markdown>

-   __YOLO-Based Binary Object Sorting System__

    ---

    Binary object sorter using YOLO computer vision, with a custom Python app for object detection and an Arduino for physical object sorting.

    [:octicons-arrow-right-24: View more details](https://sidhgurnani.github.io/sidh-ME-portfolio/projects/#yolo-based-binary-object-sorting-system)

    [:octicons-arrow-right-24: View full technical documentation (opens new tab)](https://sidhgurnani.github.io/yolo-object-sorter-docs/){:target="_blank"}

-   __Purdue Formula SAE: PF25 Drivetrain__

    ---

    Responsible engineer tasked with designing and manufacturing drivetrain system on PF25 competition vehicle, helping secure 6th place.

    [:octicons-arrow-right-24: View more details](https://sidhgurnani.github.io/sidh-ME-portfolio/projects/#purdue-formula-sae-pf25-drivetrain)

-   __Data Science Undergraduate Reasearcher__

    ---

    Collaborated with Kautex to improve quality control in fuel tank manufacturing, with a focus on validating machine learning models with dimensional analysis methods.

    [:octicons-arrow-right-24: View more details](https://sidhgurnani.github.io/sidh-ME-portfolio/projects/#the-data-mine-data-science-undergraduate-reasearcher)

-   __ME 49601EVD Semester Projects__

    ---

    Series of projects focused on modelling acceleration of an electric vehicle and sourcing components for an electric go-kart based on design requirements.

    [:octicons-arrow-right-24: View more details](https://sidhgurnani.github.io/sidh-ME-portfolio/projects/#electric-vehicle-design-me-49601evd-semester-projects)

-   __ME 49601TMT Semester Project__

    ---

    Semester-long project focused on modelling an existing TRAXXAS RC Trophy Truck and re-engineering it for enhanced performance.

    [:octicons-arrow-right-24: View more details](https://sidhgurnani.github.io/sidh-ME-portfolio/projects/#tools-methods-and-techniques-for-rapid-iterative-product-design-and-analysis-me-49601tmt-semester-project)

-   __Technical Article - AEIS Internship Project__

    ---

    Self-guided research paper about a basic overview to what pistons are and ways that they can fail; written as my internship at AEIS.

    [:octicons-arrow-right-24: View more details](https://sidhgurnani.github.io/sidh-ME-portfolio/projects/#technical-article-aeis-internship-project)

</div>