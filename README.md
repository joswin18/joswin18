## Hi there, I'm <span id="animated-name">joswin</span> 👋

<!-- Your introduction, tech stack, what you love, and let's connect sections here -->

### 🌄 A Favorite Quote

> <span id="animated-quote">"The only way to do great work is to love what you do." - Steve Jobs</span>

Thanks for stopping by! Let's create something amazing together. 😄

<!-- CSS and JavaScript for the name and quote animation -->
<style>
  /* CSS for the animated name */
  #animated-name {
    font-size: 32px;
    font-weight: bold;
    color: #333;
  }
  
  /* CSS for the animated quote */
  #animated-quote {
    font-size: 18px;
    font-style: italic;
    color: #777;
  }
  
  /* Animation keyframes */
  @keyframes type {
    from {
      width: 0;
    }
  }
  
  /* Apply animation to the name and quote */
  #animated-name::after,
  #animated-quote::after {
    content: "|";
    animation: type 0.5s infinite alternate;
  }
</style>

<!-- JavaScript to handle the animation -->
<script>
  // Function to handle the animation of the name and quote
  function animateText(elementId, text) {
    let index = 0;
    setInterval(() => {
      document.getElementById(elementId).textContent = text.slice(0, index);
      index = (index + 1) % (text.length + 1);
    }, 200); // Adjust the animation speed as needed
  }

  // Start the animations
  animateText("animated-name", "joswin");
  animateText("animated-quote", "\"The only way to do great work is to love what you do.\" - Steve Jobs");
</script>
