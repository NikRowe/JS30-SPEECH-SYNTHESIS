# JS30 Speech Synthesis
Exercise 23 in WesBos' JavaScript30 tutorials. 

Another default browser object shown to us via the speechSynthesis interface! 
speechSynthesis takes a speechSynthesisUtterance (essentially what it will say) and then passes it to the objects speak() method. 
You then customize the speech via different voices, or rates, and pitches of the voice. 

For my bonus I chose to select voice from the imported browser voice list and set it as the default. Seeing as the &lt;select&gt; options aren't available in the HTML, I used a querySelector to grab the &lt;options&gt; elements upon loading and then match the value to the voice name I wanted as my default, finally adding a "selected" property to the element. 

    const voiceOptions = voicesDropdown.querySelectorAll('.option')
      voiceOptions.forEach(voice =>
        voice.value === 'Google UK English Male'
          ? voice.selected = 'selected'
          : ''
      )

<a href="https://nikrowedevjs30-speech-synthesis.netlify.app/">Demo</a>