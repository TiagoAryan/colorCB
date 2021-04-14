<script>
  function slide(e) {
    const sliderPos = e.target.value;

    // Update the width of the foreground image
    document.getElementsByClassName("foreground-img")[0].style.width =
      sliderPos + "%";
    // Update the position of the slider button
    document.getElementsByClassName("slider-button")[0].style.left =
      "calc(" + sliderPos + "% - 18px)";
  }
</script>

<div class="container">
  <div class="img background-img" />
  <div class="img foreground-img" />
  <input
    type="range"
    min="1"
    max="100"
    value="50"
    class="slider"
    name="slider"
    id="slider"
    on:input={slide}
  />
  <div class="slider-button" />
</div>
