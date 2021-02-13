<template>
    <div class="buy-form-overlay">
        <form class="buy-form neomorphism animate__animated" method="post" action="/order">
            <a class="buy-form-close-icon" href="#" @click="buyFromCloseIconClick">&times;</a>

            <h3 class="buy-form-header">Ваш товар:</h3>

            <div class="buy-form-img neomorphism-light"></div>
            <input class="buy-form-input-img-address" type="hidden" name="imgAddress" value="1">

            <div class="sub-header-text buy-form-good-name">РОЛЛЕР</div>
            <input class="buy-form-input-good-name" type="hidden" name="goodName">

            <div class="buy-form-number-wrap">
                Количество: <span class="buy-form-number">1</span>&nbsp;шт.
                <button class="buy-form-plus-btn neomorphism-light" type="button" @click.prevent="buyFormPlusBtnClick">
                    <span class="plus">+</span>
                </button>
                <button class="buy-form-minus-btn neomorphism-light" type="button" @click.prevent="buyFormMinusBtnClick">
                    <span class="minus">-</span>
                </button>
                <input class="buy-form-input-number" type="hidden" name="number" value="1">
            </div>
            <div class="buy-form-price-wrap">
                Стоимость: <span class="buy-form-price"></span> <span>РУБ</span>
                <input class="buy-form-input-price" type="hidden" name="price">
            </div>

            <div class="buy-form-email-label">Укажите почтовый ящик для связи:<span style="color: rgb(251, 88, 88)">*</span></div>
            <div class="buy-form-email-input-wrap">
                <input class="buy-form-email-input neomorphism-inset"
                       name="email"
                       type="email"
                       placeholder="example@gmail.com"
                       required
                       @keyup="checkBuyForm" />
            </div>

            <div class="buy-form-phone-label">Телефон:</div>
            <div class="buy-form-phone-input-wrap">
                <input type="tel" class="buy-form-phone-input neomorphism-inset" name="phone"
                       pattern="^(\+7|7|8)?[\s\-]?\(?[489][0-9]{2}\)?[\s\-]?[0-9]{3}[\s\-]?[0-9]{2}[\s\-]?[0-9]{2}$"
                       placeholder="+7 (000) 000-00-00"/>
            </div>

            <button class="buy-form-button neomorphism-light" type="submit" @click="buyFormSubmitBtnClick">
                <span class="sub-header-text buy-form-btn-text">Заказать</span>
            </button>
        </form>
    </div>
</template>

<script>
export default({
    data() {
        return {
            onePiecePrice: 0
        }
    },
    methods: {
        buyFromCloseIconClick(event) {
            event.preventDefault();

            this.hideBuyForm();
        },
        hideBuyForm() {
            $(".buy-form-overlay")
                .css("opacity", "0");

            var makeOverlayInvisible = function () {
                $(".buy-form-overlay")
                    .css("visibility", "hidden");
            }

            $(".buy-form")
                .removeClass("animate__fadeInDown")
                .addClass("animate__fadeOutUp");

            setTimeout(makeOverlayInvisible, 500);
        },
        checkBuyForm() {
            var isValidEmail = document.getElementsByClassName("buy-form-email-input").item(0).checkValidity();

            if ($(".buy-form-email-input").val() === "") {
                document.getElementsByClassName("buy-form-button").item(0).disabled = true;
                emailField.css("background", "linear-gradient(to right, rgb(237, 238, 241), rgb(224, 225, 231))");

                return;
            }

            if (isValidEmail) {
                document.getElementsByClassName("buy-form-button").item(0).disabled = false;
                emailField.css("background", "linear-gradient(to right, rgb(237, 238, 241), rgb(224, 225, 231))");
            } else {
                document.getElementsByClassName("buy-form-button").item(0).disabled = true;
                emailField.css("background", "linear-gradient(to right, rgb(255, 226, 227), rgb(233, 207, 208))");
            }
        },
        buyFormSubmitBtnClick(event) {
            event.preventDefault();

            $(".buy-form").submit();
        },
        setBuyFormParameters(backgroundImg, goodName, price, backgroundSizeBehavior) {
            $(".buy-form-img")
                .css("background-image", backgroundImg)
                .css("background-size", backgroundSizeBehavior);
            $(".buy-form-good-name").text(goodName);
            $(".buy-form-input-good-name").val(goodName);

            $(".buy-form-price").text(price);
            $(".buy-form-input-price").val(price);

            $(".buy-form-input-img-address").val(backgroundImg);
        },
        buyFormPlusBtnClick() {
            let buyNumber = $(".buy-form-number");
            let number = parseInt(buyNumber.text()) + 1;

            buyNumber.text(number);
            $(".buy-form-input-number").val(number);

            this.refreshPrice(number);
        },
        buyFormMinusBtnClick() {
            let buyNumber = $(".buy-form-number");
            let number = parseInt(buyNumber.text());

            number = number <= 1 ? 1 : number - 1;

            buyNumber.text(number);
            $(".buy-form-input-number").val(number);

            this.refreshPrice(number);
        },
        refreshPrice(number) {
            let price = this.onePiecePrice * number;

            $(".buy-form-price").text(price);
            $(".buy-form-input-price").val(price);
        }
    }
})
</script>