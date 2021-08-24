# Задания

## Сформулировать и написать тест-кейсы на поле ввода логина и пароля

### Данные кейсы проверяются для полей логина и пароля

<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">ID</th>
    <th class="tg-0pky">Название кейса</th>
    <th class="tg-0pky">Предусловие</th>
    <th class="tg-0pky">Данные для ввода</th>
    <th class="tg-0pky">Описание</th>
    <th class="tg-0pky">Ожидаемое значение</th>
    <th class="tg-0pky">Дополнительно</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">1</td>
    <td class="tg-c3ow" rowspan="9">Тестирование полей ввода.<br>Позитивные данные.</td>
    <td class="tg-c3ow" rowspan="17">Пользователь не авторизован в системе<br>и находится на странице /login.<br><br>Пользователь должен быть зарегистрирован в системе.</td>
    <td class="tg-0pky">qwerty</td>
    <td class="tg-0pky">Тестирование английских символов.</td>
    <td class="tg-0pky">Ошибки отсутствуют</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">2</td>
    <td class="tg-0pky">qwerty123</td>
    <td class="tg-0pky">Тестирование сочетания английских символов<br>и цифр.</td>
    <td class="tg-0pky">Ошибки отсутствуют</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">3</td>
    <td class="tg-0pky">q_werty</td>
    <td class="tg-0pky">Тестирование использования нижнего подчёркивания.</td>
    <td class="tg-0pky">Ошибки отсутствуют</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">4</td>
    <td class="tg-0pky">q.werty</td>
    <td class="tg-0pky">Тестирование использования точек.</td>
    <td class="tg-0pky">Ошибки отсутствуют</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">5</td>
    <td class="tg-0pky">q-werty</td>
    <td class="tg-0pky">Тестирование использование дефисов.</td>
    <td class="tg-0pky">Ошибки отсутствуют</td>
    <td class="tg-0pky">Ошибки возникают в зависимости от системы.</td>
  </tr>
  <tr>
    <td class="tg-0pky">6</td>
    <td class="tg-0pky">qwert</td>
    <td class="tg-0pky">Тестирование минимального количества символов в поле ввода.</td>
    <td class="tg-0pky">Ошибки отсутствуют</td>
    <td class="tg-0pky">Минимальное количество символов в данном случае - 5.</td>
  </tr>
  <tr>
    <td class="tg-0pky">7</td>
    <td class="tg-0pky">qwertyyuiopasdfg</td>
    <td class="tg-0pky">Тестирование максимального количества символов в поле ввода.</td>
    <td class="tg-0pky">Ошибки отсутствуют</td>
    <td class="tg-0pky">Максимальное количество символов в данном случае - 16.</td>
  </tr>
  <tr>
    <td class="tg-0pky">8</td>
    <td class="tg-0pky"> qwerty</td>
    <td class="tg-0pky">Тестирование ввода пробела в начале и конце <br>строки (должен игнорироваться).</td>
    <td class="tg-0pky">Ошибки отсутствуют</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">9</td>
    <td class="tg-0pky">q!w@e#r$t%y^</td>
    <td class="tg-0pky">Тестирование ввода специальных символов.</td>
    <td class="tg-0pky">Ошибки отсутствуют</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">10</td>
    <td class="tg-0pky" rowspan="8">Тестирование полей ввода.<br>Негативные данные.</td>
    <td class="tg-0pky">кириллица</td>
    <td class="tg-0pky">Тестирование использование кириллических символов<br>при авторизации.</td>
    <td class="tg-0pky">Ошибка: невозможно<br>использовать кириллицу</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">11</td>
    <td class="tg-0pky">1qwerty</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">Ошибка: цифры не могут </td>
    <td class="tg-0pky">Ошибки возникают в зависимости от системы.</td>
  </tr>
  <tr>
    <td class="tg-0pky">12</td>
    <td class="tg-0pky">&lt;h1&gt;some&lt;/h1&gt;</td>
    <td class="tg-0pky">Тестирование безопасности системы: XSS.</td>
    <td class="tg-0pky">Ошибка: html-теги не могут быть введены.</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">13</td>
    <td class="tg-0pky">```;;;SELECT * FROM table;</td>
    <td class="tg-0pky">Тестирование безопасности системы: SQL-injection.</td>
    <td class="tg-0pky">Ошибка: SQL-</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">14</td>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">Тестирование ввода пустой строки.</td>
    <td class="tg-0pky">Ошибка: пустая строка не может быть введена.</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">15</td>
    <td class="tg-0pky">q werty</td>
    <td class="tg-0pky">Тестирование пробелов в середине слова<br></td>
    <td class="tg-0pky">Ошибка: пробелы не могут быть в середине слова.</td>
    <td class="tg-0pky">-</td>
  </tr>
  <tr>
    <td class="tg-0pky">16</td>
    <td class="tg-0pky">qwer</td>
    <td class="tg-0pky">Тестирование меньше количества символов в поле, чем доступно.</td>
    <td class="tg-0pky">Ошибка: минимальное количество символов в поле - 5</td>
    <td class="tg-0pky">Минимальное количество символов в данном случае - 5.</td>
  </tr>
  <tr>
    <td class="tg-0pky">18</td>
    <td class="tg-0pky">qwertyyuiopasdfgq</td>
    <td class="tg-0pky">Тестирование большего количество символов в поле, чем доступно.</td>
    <td class="tg-0pky">Ошибка: максимальное количество символов в поле - 16</td>
    <td class="tg-0pky">Максимальное количество символов в данном случае - 16.</td>
  </tr>
</tbody>
</table>

## Сформулировать и написать тест-кейсы на кнопку входа

### Тестирование выполняется по шагам

<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">ID</th>
    <th class="tg-0pky">Название кейса</th>
    <th class="tg-0pky">Предусловие</th>
    <th class="tg-0pky">Шаги</th>
    <th class="tg-0pky">Ожидаемый результат<br></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">1</td>
    <td class="tg-0pky">Позитивное тестирование авторизации.</td>
    <td class="tg-0pky" rowspan="6">Пользователь не авторизован<br>и находится на странице /login.<br><br>Пользователь должен быть зарегистрирован<br>в системе.</td>
    <td class="tg-0pky">1) В поле логин ввести qwerty;<br>2) В поле пароль ввести qwerty1;<br>3) Нажать кнопку Войти</td>
    <td class="tg-0pky">Пользователь авторизуется.</td>
  </tr>
  <tr>
    <td class="tg-0pky">2</td>
    <td class="tg-0pky" rowspan="5">Негативное тестирование авторизации.<br></td>
    <td class="tg-0pky">1) Не заполнять поле логин;<br>2) В поле пароль ввести qwerty2;<br>3) Нажать кнопку Войти.</td>
    <td class="tg-0pky">Пользователь не авторизуется.<br>Ошибка: пустое поле ввода логина.</td>
  </tr>
  <tr>
    <td class="tg-0pky">3</td>
    <td class="tg-0pky">1) В поле логин ввести qwerty;<br>2) Не заполнять поле пароль;<br>3) Нажать кнопку Войти.</td>
    <td class="tg-0pky">Пользователь не авторизуется.<br>Ошибка: пустое поле ввода пароля.</td>
  </tr>
  <tr>
    <td class="tg-0pky">4</td>
    <td class="tg-0pky">1) Не заполнять поле логин;<br>2) Не заполнять поле пароль;<br>3) Нажать кнопку Войти.</td>
    <td class="tg-0pky">Пользователь не авторизуется.<br>Ошибка: пустые поля для ввода.</td>
  </tr>
  <tr>
    <td class="tg-0pky">5</td>
    <td class="tg-0pky">1) Ввести корректный логин;<br>2) Ввести некорректный пароль;<br>3) Нажать кнопку Войти.</td>
    <td class="tg-0pky">Пользователь не авторизуется.<br>Ошибка: некорректный пароль.</td>
  </tr>
  <tr>
    <td class="tg-0pky">6</td>
    <td class="tg-0pky">1) Ввести некорректный логин;<br>2) Ввести корректный пароль;<br>3) Нажать кнопку Войти.</td>
    <td class="tg-0pky">Пользователь не авторизуется.<br>Ошибка: несуществующий пользователь.</td>
  </tr>
</tbody>
</table>
