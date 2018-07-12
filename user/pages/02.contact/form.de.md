---
title: Kontakt
form:
    name: kontakt
    fields:
        -
            name: name
            label: Name
            placeholder: 'Dein Name'
            autocomplete: 'on'
            type: text
            validate:
                required: true
        -
            name: email
            label: E-mail
            placeholder: 'Deine E-Mail Adresse'
            type: email
            validate:
                required: true
        -
            name: message
            label: Nachricht
            placeholder: 'Schreibe hier eine kurze Nachricht über dich'
            type: textarea
            validate:
                required: true
        -
            name: checkbox
            type: checkbox
            label: 'Ich akzeptiere, dass meine hier eingegeben Daten zur Kontaktaufnahme auf dem Server gespeichert werden. Mehr in der Datenschutzerklärung.'
            validate:
                required: true
    buttons:
        -
            type: submit
            value: Senden
            classes: btn-primary
    process:
        -
            save:
                fileprefix: contact-
                dateformat: Ymd-His-u
                extension: txt
                body: '{% include ''forms/data.txt.twig'' %}'
        -
            message: 'Vielen Dank für deine Nachricht!'
        -
            display: danke
---

