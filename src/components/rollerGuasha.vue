<template>
<div>
    <buy-form ref="buyFormComponent"></buy-form>

    <div class="main-container">
        <div class="img-block-wrap">
            <img src="../static/img/logo/logo-white.svg" class="logo">

            <div class="img-block greeting-img"></div>

            <div class="greeting-text-wrap">
                <h2 class="greeting-text run-fade-in-up">МАССАЖЕРЫ ДЛЯ ЛИЦА</h2>
            </div>
            <div class="overlay"></div>
        </div>

        <div class="good-block">
            <div class="dot dot-roller-1 dot-blue"></div>
            <div class="dot dot-roller-2 dot-yellow"></div>
            <div class="dot dot-roller-3 dot-yellow"></div>
            <div class="dot dot-roller-4 dot-red"></div>

            <h2 class="roller-header fade-in-up-animation">РОЛЛЕРЫ</h2>

            <div class="roller-img"></div>

            <div class="roller-text fade-in-up-animation">
                На протяжении веков роллеры из натуральных камней были одним из любимых бьюти-инструментов среди представительниц китайской аристократии. Сегодня массажный роллер для лица доступен каждой женщине, которая стремится к сохранению естественной красоты и молодости.
            </div>

            <div class="w-100 d-flex justify-content-center">
                <button class="styled-btn catalog-btn fade-in-up-animation" @click="catalogBtnClick">КАТАЛОГ</button>
            </div>

            <div class="down-arrow fade-in-up-animation"><i class="fa fa-fw fa-chevron-down"></i></div>
        </div>

        <div class="img-block-wrap">
            <div class="img-block roller-massage-img"></div>

            <div class="greeting-text-wrap">
                <h2 class="greeting-text fade-in-up-animation">ЧЕМ ПОЛЕЗЕН МАССАЖ ЛИЦА?</h2>
            </div>
            <div class="overlay"></div>
        </div>

        <div class="list-wrap">
            <div class="list">
                <div class="dot dot-list-1-1 dot-red"></div>
                <div class="dot dot-list-1-2 dot-yellow"></div>
                <div class="dot dot-list-1-3 dot-blue"></div>
                <div class="dot dot-list-1-4 dot-red"></div>

                <div class="list-item fade-in-up-animation">
                    <div class="item-image plus-item-img"></div>
                    <div class="item-text-wrap">
                        <h3 class="item-text-header">Улучшает кровообращение</h3>
                        <div class="item-text">Приток крови делает кожу сияющей и упругой — визуально более здоровой и обновленной</div>
                    </div>
                </div>
                <div class="list-item fade-in-up-animation">
                    <div class="item-image plus-item-img"></div>
                    <div class="item-text-wrap">
                        <h3 class="item-text-header">Уменьшает отечность</h3>
                        <div class="item-text">Прокатывание роликов по лицу способно избавить от отеков и мешков под глазами и сделать контур более четким — это называется лимфодренаж, процедура, когда из лимфы выводится лишняя жидкость. Как результат — сокращается число морщин, а кожа становится здоровее</div>
                    </div>
                </div>
                <div class="list-item fade-in-up-animation">
                    <div class="item-image plus-item-img"></div>
                    <div class="item-text-wrap">
                        <h3 class="item-text-header">Успокаивает кожу и снимает напряжение</h3>
                        <div class="item-text">Особенно если перед процедурой подержать валик в холодильнике; весь день мы щуримся, глядя на крошечный экран смартфона, и сжимаем челюсти, находясь в стрессе, vc мышц — большой шагv в пользу упругости кожи</div>
                    </div>
                </div>
                <div class="list-item fade-in-up-animation">
                    <div class="item-image plus-item-img"></div>
                    <div class="item-text-wrap">
                        <h3 class="item-text-header">Помогает нанести косметическое средство</h3>
                        <div class="item-text">Иногда нефритовые и кварцевые валики используют в паре с увлажняющими кремами и маслами</div>
                    </div>
                </div>
                <div class="list-item fade-in-up-animation">
                    <div class="item-image plus-item-img"></div>
                    <div class="item-text-wrap">
                        <h3 class="item-text-header">Устраняет заложенности носовых пазух</h3>
                    </div>
                </div>
            </div>
        </div>

        <div class="good-block">
            <div class="dot dot-guasha-1 dot-yellow"></div>
            <div class="dot dot-guasha-2 dot-blue"></div>
            <div class="dot dot-guasha-3 dot-red"></div>

            <h2 class="guasha-header fade-in-up-animation">ГУАША</h2>

            <div class="guasha-img"></div>

            <div class="guasha-text fade-in-up-animation">
                Гуа-ша – древняя практика массажа тела и лица, пришедшая из традиционной китайской медицины. Сегодня техника и одноименный инструмент, созданный из натурального камня, известна и любима во всем мире за свою эффективность в поддержании молодости и красоты.
            </div>

            <div class="w-100 d-flex justify-content-center">
                <button class="styled-btn catalog-btn fade-in-up-animation" @click="catalogBtnClick">КАТАЛОГ</button>
            </div>

            <div class="down-arrow fade-in-up-animation"><i class="fa fa-fw fa-chevron-down"></i></div>
        </div>

        <div class="img-block-wrap">
            <div class="img-block guasha-massage-img"></div>

            <div class="greeting-text-wrap">
                <h2 class="greeting-text fade-in-up-animation">ЧЕГО ОЖИДАТЬ ОТ РАБОТЫ С МАССАЖЕРАМИ?</h2>
            </div>

            <div class="overlay"></div>
        </div>

        <div class="list-wrap">
            <div class="list">
                <div class="dot dot-list-2-1 dot-yellow"></div>
                <div class="dot dot-list-2-2 dot-red"></div>
                <div class="dot dot-list-2-3 dot-blue"></div>
                <div class="dot dot-list-2-4 dot-red"></div>

                <div class="list-item fade-in-up-animation">
                    <div class="item-image check-item-img"></div>
                    <div class="item-text-wrap">
                        <h3 class="item-text-header">Лимфодренажный массаж</h3>
                        <div class="item-text">Движение лимфы занимает центральное место в технике гуаша. За счет проработки лимфатических путей происходит восстановление водного баланса клеток. Отток лимфы и прилив крови также обеспечивают своевременное выведение токсинов из организма.</div>
                    </div>
                </div>
                <div class="list-item fade-in-up-animation">
                    <div class="item-image check-item-img"></div>
                    <div class="item-text-wrap">
                        <h3 class="item-text-header">Пластический массаж</h3>
                        <div class="item-text">Техника мягко воздействует на мышцы лица и шеи, позволяя расслаблять их и укреплять одновременно. Используя массажеры для лица можно поддерживать тонус кожи лица, добиться лифтинг эффекта и уменьшить проявления морщин естественным путем.
                        </div>
                    </div>
                </div>
                <div class="list-item fade-in-up-animation">
                    <div class="item-image check-item-img"></div>
                    <div class="item-text-wrap">
                        <h3 class="item-text-header">Рефлексотерапия</h3>
                        <div class="item-text">На лице расположены биологически активные точки, ответственные за работу внутренних органов и систем. Воздействуя на эти точки, массаж роллером, а также массаж гуаша позволяют влиять не только на кожу, но и на общее состояние организма.</div>
                    </div>
                </div>
            </div>
        </div>

        <div class="catalog">
            <h2 class="catalog-header fade-in-up-animation">У НАС ВЫ МОЖЕТЕ ПРИОБРЕСТИ</h2>

            <div class="good-to-buy-block fade-in-up-animation">
                <div class="buy-img buy-roller-img"></div>
                <div class="buy-header sub-header-text">РОЛЛЕР ИЗ РОЗОВОГО КВАРЦА</div>
                <div class="buy-price">990 РУБ</div>
                <div class="w-100 d-flex justify-content-center">
                    <button class="styled-btn buy-btn" @click="buyBtnClick">КУПИТЬ</button>
                </div>
            </div>

            <div class="good-to-buy-block fade-in-up-animation">
                <div class="buy-img buy-guasha-img"></div>
                <div class="buy-header sub-header-text">ГУАША ИЗ РОЗОВОГО КВАРЦА</div>
                <div class="buy-price">890 РУБ</div>
                <div class="w-100 d-flex justify-content-center">
                    <button class="styled-btn buy-btn" @click="buyBtnClick">КУПИТЬ</button>
                </div>
            </div>

            <div class="good-to-buy-block fade-in-up-animation">
                <div class="buy-img buy-box-img"></div>
                <div class="buy-header sub-header-text">КОМПЛЕКТ РОЛЛЕР + ГУАША</div>
                <div class="buy-price">1690 РУБ</div>
                <div class="w-100 d-flex justify-content-center">
                    <button class="styled-btn buy-btn" @click="buyBtnClick">КУПИТЬ</button>
                </div>
            </div>
        </div>
    </div>
</div>
</template>


<script>
    new Vue({
        el: "#app",
        data: {
            elementsToAnimate: [],
            onePiecePrice: 0
        },
        created() {
            window.addEventListener('scroll', this.onScroll);
            this.onScroll();
        },
        mounted() {
            this.elementsToAnimate = this.$el.querySelectorAll('.fade-in-up-animation');
            this.elementsToAnimate.forEach(element => element.style.opacity = 0);
        },
        destroyed () {
            window.removeEventListener('scroll', this.onScroll);
        },
        methods: {
            onScroll() {
                this.elementsToAnimate.forEach(element => {
                    if (this.isInViewport(element)) {
                        if (!element.classList.contains("run-fade-in-up")) {
                            element.classList.add("run-fade-in-up");
                        }
                    } else {
                        element.classList.remove("run-fade-in-up");
                    }
                })
            },
            isInViewport(element) {
                var elementTop = $(element).offset().top;
                var viewportTop = $(window).scrollTop();
                var viewportBottom = viewportTop + $(window).height();

                return elementTop < viewportBottom;
            },
            catalogBtnClick(event) {
                event.preventDefault();

                document.getElementsByClassName("catalog").item(0).scrollIntoView({behavior: "smooth"})
            },
            buyBtnClick(event) {
                this.$refs.buyFormComponent.buyBtnClick(event);
            }
        }
    });
</script>

<link rel="stylesheet" href="/src/css/effect.css">
<link rel="stylesheet" href="/src/css/common.css">
<link rel="stylesheet" href="/src/css/roller-guasha.css">
