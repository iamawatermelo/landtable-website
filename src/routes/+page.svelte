<script>
  import Arrow from '$lib/icons/Arrow.svg?component';
  import Layer1 from '$lib/assets/herolayers/layer1.svg?component';
  import Layer2 from '$lib/assets/herolayers/layer2.svg?component';
  import Layer3 from '$lib/assets/herolayers/layer3.svg?component';
  import Layer4 from '$lib/assets/herolayers/layer4.svg?component';
</script>

<div class="hero">
  <div class="hero-left">
    <h1>Take back control<br /> of your data.</h1>
    <p class="hero-text">
      Migrate, update, visualise and automate your data with the Landtable Platform.
      Effortlessly.
    </p>
    
    <a href="https://github.com/iamawatermelo/landtable" class="hero-text">
      Keep up with development on GitHub <span class="arrow"><Arrow /></span>
    </a>
    
    <p>And, for Hack Clubbers, get a hosted Landtable instance for free. Launches mid-Feburary.</p>
  </div>
  <div class="hero-right" role="none">
    <div class="stack">
      <Layer1 />
      <Layer2 />
      <Layer3 />
      <Layer4 />
    </div>
  </div>
</div>

<style lang="scss">
  .hero {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    padding: 2em;
    background:
      url('$lib/assets/noise.svg'),
      linear-gradient(-35deg, #F8EEFF 0%, #BBBEFF 100%);
    border: 1em solid white;
    overflow: clip;
    gap: 4em;
    
    @media screen and (min-width: 32em) {
      border-width: 2em;
    }
    
    @media screen and (min-width: 64em) {
      font-size: 1.2em;
      padding-left: 4em;
    }
    
    @media screen and (min-width: 100em) {
      flex-direction: row;
    }
    
    @media screen and (min-width: 128em) {
      font-size: 1.5em;
    }
    
    .hero-left {
      display: flex;
      flex: 1 1 auto;
      flex-direction: column;
      justify-content: center;
      max-width: min-content;
      gap: 2em;
      
      br {
        display: none;
        
        @media screen and (min-width: 48em) {
          display: block;
        }
      }
      
      h1 {
        font-size: 2em;
        letter-spacing: .05rem;
        width: max-content;
        max-width: 100%;
      }
      
      .hero-text {
        font-size: 1.2em;
      }
      
      @media screen and (min-width: 32em) {
        h1 {
          font-size: 4em;
        }
        
        .hero-text {
          font-size: 1.5em;
        }
      }
    }
    
    .hero-right {
      flex: 1 1 auto;
      width: 100%;
      position: relative;
      height: 16em;
      
      @media screen and (min-width: 48em) {
        height: 32em;
      }
      
      @media screen and (min-width: 100em) {
        left: 4em;
        height: unset;
        --scale-factor: 2;
      }
      
      .stack {
        position: absolute;
        top: 50%;
        left: 2em;
        --scale-factor: 0.7;
        
        transform: rotate3d(0.7, 0.5, -0.3, 0.1turn) scale(var(--scale-factor)) translateY(calc(-50% + 128px));
        transform-style: preserve-3d;
        
        @media screen and (min-width: 48em) {
          --scale-factor: 1.2;
        }
        
        @media screen and (min-width: 100em) {
          left: 0;
          --scale-factor: 2;
        }
        
        :global(svg) {
          position: absolute;
          border-radius: 16px;
          
          &:nth-child(1) {
            transform: translateZ(2em) translateY(-50%);
            box-shadow: -8px 8px 16px 0px rgba(0,0,0,0.2);
          }
          
          &:nth-child(2) {
            transform: translateZ(4em) translateY(-50%);
            filter: drop-shadow(-8px 8px 16px rgba(0,0,0,0.1));
          }
          
          &:nth-child(3) {
            transform: translateZ(6em) translateY(-50%);
            filter: drop-shadow(-8px 8px 16px rgba(0,0,0,0.1));
          }
          
          &:nth-child(4) {
            transform: translateZ(8em) translateY(-50%);
            filter: drop-shadow(-8px 8px 16px rgba(0,0,0,0.1));
          }
        }
      }
    }
  } 
</style>