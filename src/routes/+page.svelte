<!-- mm svelte migration
<-- alright so i know what i just did im sorry i will be editing that in the future -->
<!-- 10/3 i am utterly confused, i do not know how to use svelte, no idea what to do next. -->
<!-- 10/3 please god help me i a -->

<!-- <h1>CURRENT INTERESTS!!!!!111!!!1!111!</h1>
<ul>
  <li>Umineko when they cry</li>
  <li>Sheena Ringo</li>
  <li>Danganronpa</li>
  <li>Persona 4 Golden</li>
  <li>Bomb Rush Cyberfunk (and all grind fiction to be exact)</li>
  <li>Pseudoregalia</li>
</ul>

<p>this will be deleted, or added in an easter egg via a secret button.</p>
<p>for measure i will be making a specific design for each page.</p>
<p>i need to find a way to integrate backend.</p>
<p>i need an inclusive design in the main page which will be a mix probably.</p>
<p>aaand i need to add fun mechanics via backend and js (it will be torture)</p>  -->
<!-- Typescript -->
<script lang="ts">
  let glitchMint = $state(false);
  function triggerMint() : void {
    glitchMint = true;
    setTimeout(() => glitchMint = false, 500);
  }
</script>


<!-- HTML-->
 <div class="snap-container">
      <!-- Section, Mint!!! -->
  <section class="snap-section min-h-screen bg-[#0a0a0a] flex flex-col items-center justify-center">
    <button onclick={() => triggerMint()}
    class="text-8xl font-black tracking-widest cursor-pointer select-none bg-transparent border-none {glitchMint ? 'glitching' : ''}"
    style="color: #00ffaa;"
    > 
    MINT
    </button>
    <p class="mt-4 text-[#00ffaa] opacity-50 text-sm tracking-widest"> Click me :D</p>
  </section>

  <!-- section, Introduction!!! -->
   <section class="snap-section min-h-screen bg-[#0a0a0a] flex flex-col items-center justify-center">
    <p class="text-[#00dffaa] text-2xl tracking-widest"> Introduction: to do!</p>
   </section>

   <!-- section, carding! for interests page and projects -->
    <section class="min-h-screen bg-[#0a0a0a] flex flex-col items-center justify-center">
      <p class="text-[#00ffaa] text-2xl tracking-widest"> the cards will be here! hehehehe</p>
    </section>
</div>
  
<!-- CSS -->
  <style>
  .glitching {
    animation: glitch 0.4s steps(8) forwards;
    position: relative;
  }

  .glitching::before,
  .glitching::after {
    content: "MINTY";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  .glitching::before {
    color: #ff00ff;
    animation: glitch-before 0.4s steps(8) forwards;
    clip-path: polygon(0 0, 100% 0, 100% 45%, 0 45%);
  }

  .glitching::after {
    color: #00ffff;
    animation: glitch-after 0.4s steps(8) forwards;
    clip-path: polygon(0 55%, 100% 55%, 100% 100%, 0 100%);
  }

  @keyframes glitch {
    0%   { transform: translate(0); filter: hue-rotate(0deg); }
    20%  { transform: translate(-6px, 3px); filter: hue-rotate(90deg); }
    40%  { transform: translate(6px, -3px); filter: hue-rotate(180deg); }
    60%  { transform: translate(-3px, 6px); filter: hue-rotate(270deg); }
    80%  { transform: translate(3px, -6px); filter: hue-rotate(360deg); }
    100% { transform: translate(0); filter: hue-rotate(0deg); }
  }

  @keyframes glitch-before {
    0%   { transform: translate(0); }
    25%  { transform: translate(-8px, 0); }
    50%  { transform: translate(8px, 0); }
    75%  { transform: translate(-4px, 0); }
    100% { transform: translate(0); }
  }

  @keyframes glitch-after {
    0%   { transform: translate(0); }
    25%  { transform: translate(8px, 0); }
    50%  { transform: translate(-8px, 0); }
    75%  { transform: translate(4px, 0); }
    100% { transform: translate(0); }
  }
  .snap-container {
    height: 100vh;
    overflow-y: scroll;
    scroll-snap-type: y proximity;
  }
  .snap-section{
    scroll-snap-align: start;
  }
</style>