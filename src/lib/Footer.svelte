<main>
    <h3 class="Effect-rainbow-text">Footer</h3>

    <section class="Section-main">
    
        <!-- Buttons linking my social media accounts (Intagram and Discord) -->
    
        <section class="Links">
            <div id="insta">
                <a href="https://www.instagram.com" target="_blank"><p>Instagram</p>
                <div class="Instagram"></div></a>
            </div>
            
        
            <div id="discord">
                <a href="https://discord.com" target="_blank"><p>Discord</p>
                <div class="Discord"></div></a>
            </div>
        </section>
    </section>
    
    <p>
        -- Made by Abdel Hussein
    </p>
    <p>
        --My old portfolio site was bad so i made this one
    </p>
</main>


<style>
    main {
        margin-bottom: 10%;
    }

    a {
        color: white;
    }

    .Section-main {
        display: flex;
        justify-content: center;
        font-weight: 1000;
    }

    div:hover {
        cursor: pointer;
        text-decoration: underline;
    }

    div a {
        transition: all 0.2s linear;
    }

    #insta:hover a {
        color: rgb(255, 138, 247);
    } #discord:hover a {
        color: rgb(167, 201, 255);
    }

    .Links {
        display: flex;;
        justify-content: space-between;
        width: 17.5%;
        margin-bottom: 10%;
    }

    .Instagram {
        width: 100px;
        height: 100px;
        border-radius: 50%;
        display: inline-block;
        position: relative;
        margin-top: 10px;

        background-color: rgb(255, 99, 125); /* alternate, in case bg image doesn't load... */
        background-image: url(./gwam.jpg);
        background-size: 100%;
        box-shadow: 0px 0px 8px 0px rgb(255, 99, 125);

        transition: all 0.3s ease-out;
    } .Instagram:hover, div:hover .Instagram {
        transform: translateY(-15px);
        box-shadow: 0px 0px 120px 0px rgb(255, 99, 125);
    }

    .Discord {
        width: 100px;
        height: 100px;
        border-radius: 50%;
        display: inline-block;
        margin-top: 10px;

        background-color: rgb(99, 154, 255); /* alternate, in case bg image doesn't load... */
        background-image: url(./discord.png);
        background-size: 100%;
        box-shadow: 0px 0px 8px 0px rgb(99, 154, 255);

        transition: all 0.3s ease-out;
    } .Discord:hover, div:hover .Discord {
        transform: translateY(-15px);
        box-shadow: 0px 0px 120px 0px rgb(99, 154, 255);
    }

    h3 {
        font-size: 250%;
    }
</style>