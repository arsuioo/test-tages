# Отправка комментария под фото профиля TAGES

##  1. Получение access токена и сбор информации для запроса
1. Перейдите на страницу ВК
2. Во вкладке network найти запрос account.getTogglesExternal
3. Скопировать access_token
4. Открывем необходимое фото https://vk.com/tagesru?z=photo-210981032_457240823%2Falbum-210981032_0%2Frev
5. Из URL извлекаем owner_id: "-210981032 и photo_id: 457240823

##  2. Составление и отправка запроса
1. В Postman создаем новый POST запрос со следующими данными:

  URL: https://api.vk.com/method/photos.createComment

  Body:

   {
       "owner_id": "-210981032",
       "photo_id": "457240823",
       "message": "Тест",
       "access_token": "vk1.a.CjtyyAOvFYq4qBY_DpPXy31SXwP-96xBX91tJFJLdLdcF20w9J_WLeBauCHBkaO8YW5iQY6Copmd9clHKQ_Idr3Szc2TEMoJG4300QV5uPVbk0llyG3DVpoKg2z5tZZhn3k8x146HJJXeBXQt2Hq91h_TUNKD9tlsefGmKW-10hQCiRQkqJ2U69Z_4T7W8Cl5pL9VDd24rJPjPfRX7quZQ",
       "v": "5.199"
   }
2. После отправки получаем ответ с id комментария:
    {
        "response": 184
    }
