<template>
    <header>
        <div class="container">
            <a href="">
                <h2><span class="highlited">Fentec</span> Algiria</h2>
            </a>
            <div class="centered_logo">
                <img src="/imgs/header-left-arrow-icon.svg">
                <div class="logo">
                    <div class="img">
                        <img src="/imgs/fentec_logo.png" alt="Fentec logo">
                    </div>
                    <div class="links">
                        <a href="">
                            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-info-circle-filled" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 2c5.523 0 10 4.477 10 10a10 10 0 0 1 -19.995 .324l-.005 -.324l.004 -.28c.148 -5.393 4.566 -9.72 9.996 -9.72zm0 9h-1l-.117 .007a1 1 0 0 0 0 1.986l.117 .007v3l.007 .117a1 1 0 0 0 .876 .876l.117 .007h1l.117 -.007a1 1 0 0 0 .876 -.876l.007 -.117l-.007 -.117a1 1 0 0 0 -.764 -.857l-.112 -.02l-.117 -.006v-3l-.007 -.117a1 1 0 0 0 -.876 -.876l-.117 -.007zm.01 -3l-.127 .007a1 1 0 0 0 0 1.986l.117 .007l.127 -.007a1 1 0 0 0 0 -1.986l-.117 -.007z" stroke-width="0" fill="currentColor" /></svg>
                            <span class="hint">More Info</span>
                        </a>
                        <a href=""><svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-message-question" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M8 9h8" /><path d="M8 13h6" /><path d="M14 18h-1l-5 3v-3h-2a3 3 0 0 1 -3 -3v-8a3 3 0 0 1 3 -3h12a3 3 0 0 1 3 3v4.5" /><path d="M19 22v.01" /><path d="M19 19a2.003 2.003 0 0 0 .914 -3.782a1.98 1.98 0 0 0 -2.414 .483" /></svg>
                            <div class="hint">Join Us</div>
                        </a>
                    </div>
                </div>
                <img src="/imgs/header-right-arrow-icon.svg">
            </div>
            <div class="more-mobile">
                <a href="">Download</a>
            </div>
            <div class="more">
                <div class="lang-slider">
                    <div class="radio-group">
                        <input type="radio" name="lang" id="lang_ar" v-model="lang" value="ar">
                        <label for="lang_ar">ع</label>
                    </div>
                    <div class="radio-group">
                        <input type="radio" name="lang" id="lang_en" v-model="lang" value="en">
                        <label for="lang_en">EN</label>
                    </div>
                </div>
                <a href="" class="button button-primary">
                    <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-download" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M4 17v2a2 2 0 0 0 2 2h12a2 2 0 0 0 2 -2v-2" /><path d="M7 11l5 5l5 -5" /><path d="M12 4l0 12" /></svg>
                </a>
            </div>
        </div>
    </header>
</template>

<script>

export default {
name: 'HeaderComponent',
data() {
    return {
        lang: "en"
    }
},
}
</script>
