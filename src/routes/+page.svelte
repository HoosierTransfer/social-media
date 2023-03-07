<script>
</script>

<style>
    /* PLEASE USE BEM NAMING CONVENTION */
    :root {
        --color-green: #26de3b;
        --title-color: #26de3b;
        --navbar-top-color: #42414b;
        --search-bar-color: #111112;
        --search-bar-highlighted: #eeeeef;
        --search-bar-search-button-color: #232325;
        --search-bar-text-color: #f8f7ff;
        --search-bar-search-text-input-color: #39393f;
    }

    .nav-top-container {
        background: var(--navbar-top-color);
        display: grid;
        grid-template-columns: 100%;
        grid-template-rows: min-content min-content;
        gap: 0px 0px;
        grid-auto-flow: row;
        grid-template-areas:
            "."
            ".";
    }

    .nav-top {
        background: var(--navbar-top-color);
        height: 8vh;
        min-width: 100%;
        display: flex;
        gap: clamp(1px, 1vw, 20px);
        align-items: center;
        padding-left: clamp(1px, 1vw, 20px);
        font-weight: 600;
        font-size: 200%;
    }

    .nav-top-below {
        background: var(--navbar-top-color);
        height: 12vh;
        width: 100%;
        display: flex;
        gap: 10px;
        align-items: center;
        padding-left: 10px;
        font-weight: 600;
        font-size: 200%;
    }

    .nav-top__name {
        color: var(--title-color);
    }

    .nav-top-below__avatar {
        height: calc(100% - 20px);
        border-radius: 100%;
        aspect-ratio: 1;
        border: 3px solid var(--color-green);
    }

    @media only screen and (min-device-width: 480px) {
        .nav-top__search {
            height: calc(100% - calc(clamp(1px, 1vw, 20px)));
            /* dont know if 1000px is ok */
            /* but it works */
            border-radius: 1000px;
            width: 70%;
            background: var(--search-bar-color);
            display: flex;
        }

        .nav-top__search__search-button {
            color: var(--search-bar-text-color);
            font-size: 75%;
            /* again dont know if 1000px is ok */
            border-radius: 1000px 0px 0 1000px;
            flex-shrink: 1;
            border-top: 2px solid var(--search-bar-color);
            border-left: 2px solid var(--search-bar-color);
            border-bottom: 2px solid var(--search-bar-color);
            padding: 0 clamp(1px, 1vw, 20px) 0 clamp(1px, 1vw, 20px);
            background-color: var(--search-bar-search-button-color);
        }

        .nav-top__search__text-input {
            color: #f8f7ff;
            font-size: 75%;
            border-radius: 0 1000px 1000px 0;
            flex-grow: 1;
            padding-left: 10px;
            border: 2px solid var(--search-bar-color);
            background-color: var(--search-bar-search-text-input-color);
        }

        .nav-top__search__text-input:focus {
            border: 2px solid var(--search-bar-highlighted);
            outline: none;
        }
    }

    @media only screen and (max-device-width: 480px) {
        .nav-top {
            height: 5vh;
        }

        .nav-top__search {
            color: var(--search-bar-text-color);
            margin-left: auto;
            margin-right: clamp(1px, 1vw, 20px);
        }

        .nav-top__avatar {
            height: calc(100% - calc(clamp(1px, 2vw, 20px)));
            margin-right: clamp(1px, 2vw, 20px);
            object-fit: contain;
            border-radius: 100%;
        }

        .nav-top__icon {
            color: var(--search-bar-text-color);
            margin-right: clamp(1px, 1vw, 20px);
            margin-left: clamp(1px, 1vw, 20px);
        }
    }
</style>

<div class="nav-top-container">
    <div class="nav-top">
        <h1 class="nav-top__name">Among Us</h1>
        <i class="fa-solid fa-magnifying-glass nav-top__search" />
        <i class="fa-regular fa-bookmark nav-top__icon" />
        <img
            src="./profile images/profile.png"
            class="nav-top__avatar"
            alt="Profile"
        />
        <!-- <form class="nav-top__search">
        <button class="nav-top__search__search-button" type="submit">Search</button>
        <input type="text" class="nav-top__search__text-input" />
    </form> -->
    </div>
    <div class="nav-top-below">
        <img src="./profile images/profile.png" alt="Profile" class="nav-top-below__avatar" />
        <img src="./profile images/profile.png" alt="Profile" class="nav-top-below__avatar" />
        <img src="./profile images/profile.png" alt="Profile" class="nav-top-below__avatar" />

    </div>
</div>
