---
title: контакт
form:
    name: контакт
    fields:
        -
            name: name
            label: Имя
            placeholder: 'Твое имя'
            autocomplete: 'on'
            type: text
            validate:
                required: true
        -
            name: email
            label: E-mail
            placeholder: 'Ваш E-mail'
            type: email
            validate:
                required: true
        -
            name: message
            label: Cообщение
            placeholder: 'Напишите короткое сообщение о себе здесь'
            type: textarea
            validate:
                required: true
        -
            name: checkbox
            type: checkbox
            label: 'Я согласен с тем, что мои данные, введенные здесь, будут храниться на сервере, чтобы связаться со мной. Больше в политике конфиденциальности.'
            validate:
                required: true
    buttons:
        -
            type: submit
            value: послать
            classes: btn-primary
    process:
        -
            save:
                fileprefix: contact-
                dateformat: Ymd-His-u
                extension: txt
                body: '{% include ''forms/data.txt.twig'' %}'
        -
            message: 'Спасибо за ваше сообщение!'
        -
            display: spasibo
---

