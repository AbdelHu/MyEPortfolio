<script>
    export let buttonText = "Button";

    function rickRoll() {
        location.href = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ';
    }
</script>

<button on:click={rickRoll}>
    {buttonText}
</button>


<style>
    button {
        transition: border-color 0.075s, filter 0.2s, color 0.35s;

        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;

        border-radius: 8px;
        border: 1px solid black;
        padding: 0.6em 1.2em;
        font-size: 1em;
        font-weight: 500;
        font-family: inherit;
        background-color: #1a1a1a;
        cursor: pointer;

        border-color: #646cff;

        filter: drop-shadow(1px 1px 2px #8383ff);
    }
    button:hover {
        border-color: #646cff;
        text-decoration: underline;

        filter: drop-shadow(7px 7px 14px #8383ff);
    } button:active {
        background-color: #eeeeee;
        color: black;
    }
</style>