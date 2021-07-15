<template>
    <div class="user-form">
        <div class="user-form__nav">
            <button class="user-form__nav-button" type="button">Параметры</button>
            <button class="user-form__nav-button" type="button">Вопросы</button>
            <button class="user-form__nav-button" type="button">Логика</button>
            <button class="user-form__nav-button" type="button">Условия</button>
            <button class="user-form__nav-button active-button" type="button">Респонденты</button>
        </div>
        <form class="user-form__main-form" action="">
            <h2>Добавить опрос</h2>
            <div id="c-1" class="condition">
                <div class="condition-top">
                    <p id="cn-1" class="condition-name">Условие 1</p>
                    <select name="condition-type-1" id="">
                        <option selected value="">Возраст респондента</option>
                        <option value="18">18</option>
                        <option value="21">21</option>
                    </select>
                </div>
                <div class="range">
                    <p class="range-name">Диапазон 1</p>
                    <div class="range-values">
                        <p>от</p>
                        <input name="range-since-1" min="0" type="number">
                        <p>до</p>
                        <input name="range-to-1" max="100" type="number">
                    </div>
                </div>
                <div class="range">
                    <div class="or-range">
                        <p id="orn-1" class="or-range-name">или</p>
                        <p class="range-name">Диапазон 2</p>
                    </div>
                    <div class="range-values">
                        <p>от</p>
                        <input name="range-since-2" min="0" type="number">
                        <p>до</p>
                        <input name="range-to-2" max="100" type="number">
                    </div>
                </div>
                <div class="btns-block">
                    <div></div>
                    <div class="btns-block__container">
                        <button class="add-button">
                            <div class="plus-block">
                                <div class="plus-block__item"></div>
                                <div class="plus-block__item"></div>
                            </div>
                            <p>Добавить диапазон</p>
                        </button>
                        <button class="trash-button">
                            <img class="trash" :src="trash" alt="">
                            <p>Удалить условие</p>
                        </button>
                    </div>
                </div>
                <p id="ce-1" class="connecting-element">И</p>
            </div>
            <div id="c-2" class="condition">
                <div class="condition-top">
                    <p id="cn-2" class="condition-name">Условие 2</p>
                    <select name="age-respondent-2" id="">
                        <option selected value="">Тип карты лояльности</option>
                        <option value="Карта 1">Карта 1</option>
                        <option value="Карта 2">Карта 2</option>
                    </select>
                </div>
                <div class="range">
                    <p class="range-name">Тип 1</p>
                    <select name="card-type" id="">
                        <option selected value="Gold">Gold</option>
                        <option value="Silver">Silver</option>
                    </select>
                </div>
                <div class="btns-block">
                    <div></div>
                    <div class="btns-block__container">
                        <button class="add-button">
                            <div class="plus-block">
                                <div class="plus-block__item"></div>
                                <div class="plus-block__item"></div>
                            </div>
                            <p>Добавить тип</p>
                        </button>
                        <button class="trash-button">
                            <img class="trash" :src="trash" alt="">
                            <p>Удалить условие</p>
                        </button>
                    </div>
                </div>
                <p id="ce-2" class="connecting-element">И</p>
            </div>
            <div id="c-3" class="condition">
                <div class="condition-top">
                    <p id="cn-3" class="condition-name">Условие 3</p>
                    <select name="condition-type-3" id="">
                        <option selected value="">Статус карты лояльности</option>
                        <option value="Статус 2">Статус 1</option>
                        <option value="Статус 3">Статус 2</option>
                    </select>
                </div>
                <div class="range">
                    <p class="range-name">Статус 1</p>
                    <select name="card-status" id="">
                        <option selected value="Активна">Активна</option>
                        <option value="Неактивна">Неактивна</option>
                    </select>
                </div>
                <div class="btns-block">
                    <div></div>
                    <div class="btns-block__container">
                        <button class="add-button">
                            <div class="plus-block">
                                <div class="plus-block__item"></div>
                                <div class="plus-block__item"></div>
                            </div>
                            <p>Добавить диапазон</p>
                        </button>
                        <button class="trash-button">
                            <img class="trash" :src="trash" alt="">
                            <p>Удалить условие</p>
                        </button>
                    </div>
                </div>
            </div>
            <div class="new-condition">
                <div class="condition-top">
                    <p class="condition-name">Условие 3</p>
                    <select name="condition-status" id="">
                        <option selected value="">Статус карты лояльности</option>
                        <option value="Статус 2">Статус 1</option>
                        <option value="Статус 3">Статус 2</option>
                    </select>
                </div>
                <div class="btns-block">
                    <div></div>
                    <div id="bbc-last" class="btns-block__container">
                        <button class="trash-button">
                            <img class="trash" :src="trash" alt="">
                            <p>Удалить условие</p>
                        </button>
                    </div>
                </div>
            </div>
            <div class="add-condition">
                <div class="add-container">
                    <div class="add-container__plus-block">
                        <div class="add-container__plus-block-item"></div>
                        <div class="add-container__plus-block-item"></div>
                    </div>
                    <p>Нажмите, чтобы добавить новое условие выборки. <br>Все условия связываются между собой логическим “И”</p>
                </div>
            </div>
            <div class="stage-result__block">
                <button class="test-button">Протестировать запрос</button>
                <button @click="fakeSend" class="next-button">
                    <p>Далее</p>
                    <img :src="arrow" alt="">
                </button>
            </div>
        </form>
    </div>
</template>

<script>

    import trash from '../assets/img/trash.svg'
    import arrow from '../assets/img/arrow.svg'


    export default {
        name: "userFrom",
        data(){
            return{
                trash, arrow
            }
        },
        methods:{
            fakeSend(){
                let form = document.querySelector('.user-form__main-form')
                form.onsubmit = async (e) => {
                    e.preventDefault();
                    let formData = new FormData(form)
                    let response = await fetch('http://test.com/api/request', {
                        method: 'POST',
                        body: formData
                    });
                    alert('stop')
                };
            }
        },
        mounted() {
        }
    }
</script>