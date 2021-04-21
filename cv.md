# Ekaterina Railian

*(Екатерина Райлян)*

## Summary:

I am a Javascript developer, currently focusing on React.js framework. I have experience in developing personal projects and I enjoy pushing myself to learn new thechnologies. It's more than a year ago that I begain practical work in the field of development. Currently I work at EPAM as Junior Software Engineer. My ultimate goal this year is to switch to iOS development and puruse a full on career in that field. My greatest inspiration would be my husband, who has been in iOS for over 10 years now. 

## Skills:

<img align="left" alt="Visual Studio Code" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/visual-studio-code/visual-studio-code.png" />
<img align="left" alt="HTML5" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/html/html.png" />
<img align="left" alt="CSS3" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/css/css.png" />
<img align="left" alt="Sass" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/sass/sass.png" />
<img align="left" alt="JavaScript" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/javascript/javascript.png" />
<img align="left" alt="React" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/react/react.png" />
<img align="left" alt="Node.js" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/nodejs/nodejs.png" />
<img align="left" alt="Git" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/git/git.png" />
<img align="left" alt="GitHub" width="26px" src="https://raw.githubusercontent.com/github/explore/78df643247d429f6cc873026c0622819ad797942/topics/github/github.png" />
<img align="left" alt="Terminal" width="26px" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/terminal/terminal.png" />
<br>

## Code example:

```jsx
export default class Key {
  constructor(code, value) {
    this.code = code;
    this.value = value;
    this.type = this.assignKeyType();
  }

  render() {
    const keyClasses =
      this.type === 'modifier'
        ? `keyboard__key ${this.code.toLowerCase()}`
        : 'keyboard__key';
    if (this.type === TYPE.nav) return this.navigationKeys();
    return createElement(
      'button',
      { class: keyClasses, type: this.type, code: this.code },
      this.handleKeyValues()
    );
  }

  assignKeyType() {
    if (modifierKeys.includes(this.code)) return TYPE.mod;
    if (this.code === 'Arrows') return TYPE.nav;
    if (this.value.length > 1) return TYPE.symbol;
    return TYPE.alpha;
  }

  navigationKeys() {
    const navigationKeys = keyboardLayout.navigation.map((row) =>
      row.map((arrow) => {
        this.code = arrow;
        return createElement(
          'button',
          {
            class: `keyboard__key ${this.code}`,
            type: this.type,
            code: this.code,
          },
          createElement('span', { class: 'key__value' }, '')
        );
      })
    );
    return createElement('div', { class: 'keyboard__nav' }, navigationKeys);
  }

  handleKeyValues() {
    const textValues = [];
    textValues.push(createElement('span', { class: 'key__value' }, this.value[STANDARD]));
    if (Number(this.value[SUPER]) === COMMAND) this.value[SUPER] = String.fromCharCode(Number(this.value[SUPER]));
    if (this.value.length > 1)
      textValues.push(createElement('span', { class: 'key__superscript' }, this.value[SUPER]));
    return textValues;
  }
}
```

## Education:

### Diplomas:

* Bachelor of Computer Science (Ongoing 2024) - University of the People

### Certificates:

* Node.js - The Rolling Scopes School (November 2020)

* Frontend - The Rolling Scopes School (September 2020)

## Languages:

**English:** C1+ Writing /C2 Speaking

**Spanish**: B2 Writing / B2+ Speaking

**Russian**: Native

## Contact Me:

+375 44 717 1337

katerina.railian@mail.ru

[<img align="left" alt="kotiknalune | Telegram" width="22px" src="https://cdn4.iconfinder.com/data/icons/logos-and-brands/512/335_Telegram_logo-512.png" />][telegram]
[<img align="left" alt="kotiknalune | LinkedIn" width="22px" src="https://cdn4.iconfinder.com/data/icons/social-messaging-ui-color-shapes-2-free/128/social-linkedin-circle-512.png" />][linkedin]
[<img align="left" alt="kotiknalune | Instagram" width="22px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Instagram_logo_2016.svg/1200px-Instagram_logo_2016.svg.png" />][instagram]

[telegram]: https://twitter.com/kotiknalune
[instagram]: https://instagram.com/kotik.na.lune
[linkedin]: https://www.linkedin.com/in/kotiknalune/
