Test M8A

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Audi Cars Slideshow</title>
  <style>
    .slideshow-container {
      position: relative;
      width: 100%;
      max-width: 600px;
      margin: auto;
    }

    .slide {
      display: none;
      position: absolute;
      width: 100%;
      height: auto;
    }

    .active {
      display: block;
    }
  </style>
</head>
<body>
  <div class="slideshow-container">
    <img src="https://mediaservice.audi.com/media/live/50710/fly1400x601n1/4spref/2023.png?imwidth=850" alt="Audi Car 1" class="slide active">
    <img src="https://cars.usnews.com/static/images/Auto/izmo/i31351528/2017_audi_r8_angularfront.jpg" alt="Audi Car 2" class="slide">
    <img src="https://mediaservice.audi.com/media/live/50710/fly1400x601n1/4nl5da/2023.png?imwidth=850" alt="Audi Car 3" class="slide">
  </div>

  <script>
    let slideIndex = 0;
    let slides = document.getElementsByClassName("slide");

    function showSlides() {
      for (let i = 0; i < slides.length; i++) {
        slides[i].classList.remove("active");
      }
      slideIndex++;
      if (slideIndex > slides.length) {
        slideIndex = 1;
      }
      slides[slideIndex - 1].classList.add("active");
      setTimeout(showSlides, 3000); // Change image every 3 seconds
    }

    showSlides();
  </script>
</body>
</html>
