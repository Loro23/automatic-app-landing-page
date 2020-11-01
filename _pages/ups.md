---
layout: page
title: Ups
include_in_header: true
---


# Ups ein Fehler ist aufgetreten
Wir arbeiten aktuell an einer neuen technischen Umsetzung, weslhalb unsere App aktuell down ist. Wir suchen aktuell noch dringend nach neuen Testern für die Features, wie Swipe und Community Share. Bitte trage dich mit deiner E-Mail bei uns ein, wenn du Lust hast bereits vor Release unsere neusten Features zu testen. 
<br>

title: Contact Form

form:
    name: contact

    fields:
        name:
          label: Name
          placeholder: Enter your name
          autocomplete: on
          type: text
          validate:
            required: true

        email:
          label: Email
          placeholder: Enter your email address
          type: email
          validate:
            required: true

        message:
          label: Message
          placeholder: Enter your message
          type: textarea
          validate:
            required: true

        g-recaptcha-response:
          label: Captcha
          type: captcha
          recaptcha_not_validated: 'Captcha not valid!'

    buttons:
        submit:
          type: submit
          value: Submit
        reset:
          type: reset
          value: Reset

    process:
        captcha: true
        save:
            fileprefix: contact-
            dateformat: Ymd-His-u
            extension: txt
            body: "{% include 'forms/data.txt.twig' %}"
        email:
            subject: "[Site Contact Form] {{ form.value.name|e }}"
            body: "{% include 'forms/data.html.twig' %}"
        message: Thank you for getting in touch!
        display: thankyou





