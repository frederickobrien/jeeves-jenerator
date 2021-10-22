<main>
  <div class="title-container">
    <h1><span id="jeeves">Jeeves</span> Jenerator</h1>
    <img src="./static/images/jeeves-and-wooster-illustration.jpg" alt="Ink illustration of Jeeves and Wooster" />
    <button on:click={randomStory}>New story</button>
</div>

<div class="jenerator">
    <p>The old bird Percy Wooster is rather in the soup because <span id="dilemma-text" class="random-text">...</span>. Usually Jeeves would take care of 
    it but relations have been icy since Wooster started wearing <span id="clothing-text" class="random-text">...</span>. 
    In attempting to resolve the issue himself Wooster makes it worse by <span id="mishap-text" class="random-text">...       
    </span>. Just when all seems lost Jeeves saves the day by <span id="solution-text" class="random-text">...</span>. 
    Unspeakably grateful for the help, Wooster gets rid of the offending item of clothing.</p>
</div>  
</main>


<style>
    main {
        font-family: Georgia, 'Times New Roman', Times, serif;
    }

    #jeeves, .random-text {
        color: #fe151b;
        font-weight: bold;
    }

    h1 {
        text-align: center;
    }

    img {
        width: 100%;
    }

    .title-container, .jenerator {
        width: 25%;
        margin: auto;
    }

    .jenerator {
        line-height: 1.5;
    }
</style>

<script>
    function randomStory() {
        document.getElementById("dilemma-text").innerHTML = dilemmas[Math.floor(Math.random() * dilemmas.length)];
        document.getElementById("clothing-text").innerHTML = clothing[Math.floor(Math.random() * clothing.length)];
        document.getElementById("mishap-text").innerHTML = mishaps[Math.floor(Math.random() * mishaps.length)];
        document.getElementById("solution-text").innerHTML = solutions[Math.floor(Math.random() * solutions.length)];
}

const dilemmas = [
  'the club is updating its membership requirements and he falls hopelessly short',
  'his pal Bingo is hopelessly in love with a woman all wrong for him',
  'Aunt Agatha has frozen his allowance again',
  'a chap at the club has nominated him to run for parliament',
  'a communist down the road is rather keen on removing his eyeballs'
];

const clothing = [
  'a kilt',
  'tan slacks',
  'velvet cravats',
  'feather-tipped shoes',
  'a burgundy top hat'
];

const mishaps = [
  'becoming the patron of several panda bears at London Zoo',
  'cutting loose a hot air balloon with Aunt Agatha inside it',
  'becoming engaged to three different women during one tea party',
  'getting himself placed on the international most wanted list',
  'burning down a wing of the Natural History Museum'
];

const solutions = [
  'passing the whole thing off as a practical joke',
  'fleeing with Wooster to Australia',
  'fleeing with Wooster to New York',
  'selling the story to a renowned author with writers block',
  'finding a doppelgänger to take the fall',
  'calling in a few favours to get a written pardon from the king',
  'staging a failed a coup to distract from Woosters misteps'
];

</script>