

tescase 1

Name test: Проверка регистрация с валидными данными 
Pre-conditions: открыто приложение Postman 
Steps: 1. В приложении Postman в строку URL вводим:
          https://test-api.umarkets.com/registration/account?currentUrl=https%3A%2F%2Ftest-my.umarkets.com%2F%3Flang%3Den%23register
Steps: 2. В приложении Postman в вкладке "Body" ставим галку на "raw" и выбираем формат запроса "JSON" 
Steps: 3 В поле для ввода вести данные:
             {
               "Email": "leovacio2@gmail.com",
              "Password": "123useless"
              }
Steps: 5. Нажимаем "Send"
Expected Results: Status 200 ok
_________________________________________________________________________
tescase 2

Name test: Проверка регистрация с данными уже существующего пользователя 
Pre-conditions: открыто приложение Postman 
Steps: 1. В приложении Postman в строку URL вводим:
          https://test-api.umarkets.com/registration/account?currentUrl=https%3A%2F%2Ftest-my.umarkets.com%2F%3Flang%3Den%23register
Steps: 2. В приложении Postman в вкладке "Body" ставим галку на "raw" и выбираем формат запроса "JSON" 
Steps: 3 В поле для ввода вести данные: 
             {
               "Email": "leovacio2@gmail.com",
              "Password": "123useless"
              }
Steps: 4 Выбираем тип запроса "Post" 
Steps: 5. Нажимаем "Send"
Expected Results: Status 500 server ERROR
_________________________________________________________________________
tescase 3

Name test: Проверка Авторизации с данными существующего пользователя 
Pre-conditions: открыто приложение Postman 
Steps: 1. В приложении Postman в строку URL вводим:
        https://test-api.umarkets.com/account/logon?currentUrl=https%3A%2F%2Ftest-my.umarkets.com%2F%3Flang%3Den%23login
Steps: 2. В приложении Postman в вкладке "Body" ставим галку на "raw" и выбираем формат запроса "JSON" 
Steps: 3 В поле для ввода вести данные:
               {
               "Email": "leovacio2@gmail.com",
              "Password": "123useless"
              }
Steps: 4 Выбираем тип запроса "Post" 
Steps: 5. Нажимаем "Send"
Expected Results: Status 200
_________________________________________________________________________
tescase 4

Name test: Проверка Авторизации с не валидными данными 
Pre-conditions: открыто приложение Postman 
Steps: 1. В приложении Postman в строку URL вводим:
        https://test-api.umarkets.com/account/logon?currentUrl=https%3A%2F%2Ftest-my.umarkets.com%2F%3Flang%3Den%23login
Steps: 2. В приложении Postman в вкладке "Body" ставим галку на "raw" и выбираем формат запроса "JSON" 
Steps: 3 В поле для ввода вести данные: "Email": 
             { 
               "Email": "leovacio2@gmail.com",
              "Password": "123useless"
              }
Steps: 4 Выбираем тип запроса "Post" 
Steps: 5. Нажимаем "Send"
Expected Results: Status 401 Unauthorized
_________________________________________________________________________
tescase 5

Name test: Проверка востановления пароля
Pre-conditions: открыто приложение Postman 
Steps: 1. В приложении Postman в строку URL вводим:
      https://test-api.umarkets.com/account/forgot-password?currentUrl=https%3A%2F%2Ftest-my.umarkets.com%2F%3Flang%3Den%23forgotPassword
Steps: 2. В приложении Postman в вкладке "Body" ставим галку на "raw" и выбираем формат запроса "JSON" 
Steps: 3 В поле для ввода вести данные:
       {
       "culture": "en",
		     "Email": "leovacio2@gmail.com",
	     	"lang": null
	}
Steps: 4 Выбираем тип запроса "Post" 
Steps: 5. Нажимаем "Send"
Expected Results: 200
_________________________________________________________________________
tescase 6

Name test: Проверка востановления пароля с невалидным email
Pre-conditions: открыто приложение Postman 
Steps: 1. В приложении Postman в строку URL вводим:
      https://test-api.umarkets.com/account/forgot-password?currentUrl=https%3A%2F%2Ftest-my.umarkets.com%2F%3Flang%3Den%23forgotPassword
Steps: 2. В приложении Postman в вкладке "Body" ставим галку на "raw" и выбираем формат запроса "JSON" 
Steps: 3 В поле для ввода вести данные:
       {
       "culture": "en",
		     "Email": "vfjgfgcfgdrfjhdfghdfghgdf@gmail.com",
	     	"lang": null
	}
Steps: 4 Выбираем тип запроса "Post" 
Steps: 5. Нажимаем "Send"
Expected Results:  500 server ERROR
