goit-разметка-hw-06

Домашнее задание #6

.modal .header { margin-bottom: 12px; font-weight: 900; font-size: 20px;
line-height: 1.15; }

.modal .form-fields { display: flex; flex-direction: column; height: 342px;
margin-bottom: 20px;

text-align: left; }

.modal .form-fields .field-name { margin-bottom: 4px;

font-size: 12px; line-height: 1.17;

color: var(--secondary-text-color); }

.modal .input-field { position: relative; margin-bottom: 10px; }

.modal .input-field .icon { position: absolute; top: 50%; left: 12px; transform:
translateY(-50%);

fill: var(--main-black-color); transition: fill var(--timing)
var(--timing-function); /_ Делаем иконки прозрачными для ховера в Chrome _/
pointer-events: none; }

.modal .input-field input:hover + .icon, .modal .input-field input:focus + .icon
{ fill: var(--accent-color); }

.modal .form-fields input, .modal .form-fields textarea { width: 100%;

font-size: 14px; line-height: 1.14; letter-spacing: 0.01em;

background-color: transparent; border: 1px solid
var(--modal-form-fields-bordrer-color); border-radius: 4px;

transition: color var(--timing) var(--timing-function), border var(--timing)
var(--timing-function); }

.modal .form-fields input { height: 40px; padding: 12px 16px 12px 42px; }

.modal .form-fields textarea { height: 120px; padding: 12px 16px; resize: none;
}

.modal .form-fields input:hover, .modal .form-fields input:focus, .modal
.form-fields input:focus-within, .modal .form-fields textarea:hover, .modal
.form-fields textarea:focus { border: 1px solid var(--accent-color); /_ Удаляем
стандартный аутлайн чтоб виден был свой в Chrome _/ outline: 0; }

.modal .check { margin-bottom: 30px; }

.modal .check label { display: flex; justify-content: center; align-items:
center; }

.modal .check .svg-check { display: flex; justify-content: center; align-items:
center;

width: 16px; height: 15px; margin-right: 7px; border-radius: 2px;

background-origin: border-box; border: 2px solid var(--primary-text-color);
background-color: transparent; fill: transparent;

transition: border-color var(--timing) var(--timing-function), background-color
var(--timing) var(--timing-function), fill var(--timing) var(--timing-function),
box-shadow var(--timing) var(--timing-function); }

.modal .check label:hover .svg-check, .modal .check input:focus + .svg-check {
box-shadow: 0 0 0 4px var(--accent-color-trasparent); }

.modal .check a { color: var(--accent-color); text-decoration: underline;
margin-left: 7px; }

.modal .check input:checked + .svg-check { border-color: var(--accent-color);
background-color: var(--accent-color); fill: var(--main-light-color); }

 <p class="header">Оставьте свои данные, мы вам перезвоним</p>
      <form>
        <div class="form-fields">
          <label>
            <div class="field-name">Имя</div>
            <div class="input-field">
              <input name="name" type="name"/>
              <svg class="icon" width="18" height="18">
                <use href="./images/sprite.svg#icon-person"></use>
              </svg>
            </div>
          </label>
          <label>
            <div class="field-name">Телефон</div>
            <div class="input-field">
              <input name="tel" type="tel"/>
              <svg class="icon" width="18" height="18">
                <use href="./images/sprite.svg#icon-tel"></use>
              </svg>
            </div>
          </label>
          <label>
            <div class="field-name">Почта</div>
            <div class="input-field">
              <input name="email" type="email"/>
              <svg class="icon" width="18" height="18">
                <use href="./images/sprite.svg#icon-email"></use>
              </svg>
            </div>
          </label>
          <label>
            <div class="field-name">Комментарий</div>
            <textarea name="comment" placeholder="Введите текст"></textarea>
          </label>
        </div>
        <div class="check">
          <label>
            <input class="visually-hidden" name="accept" type="checkbox">
            <span class="svg-check">
              <svg class="icon" width="16" height="15">
                <use href="./images/sprite.svg#icon-check"></use>
              </svg>
            </span>
            Соглашаюсь с рассылкой и принимаю
            <a href="">Условия договора</a>
          </label>
        </div>
        <button class="submit-button" type="submit">Отправить</button>
      </form>
