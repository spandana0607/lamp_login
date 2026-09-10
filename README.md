# 💡 Little Lamp — Animated Login & Signup

A cute and interactive **Login & Signup UI** designed around a little animated lamp.

The unique concept is simple:

> 💡 **Turn the lamp ON → Login**
> 🌙 **Turn the lamp OFF → Signup**

The entire experience is created using **HTML and CSS**, including the animated lamp, glowing effects, particles, 3D card flip, responsive layout, and UI animations.

## ✨ Live Demo

🔗 **Live Demo:** Add your deployed website link here

## 📸 Project Preview

**Little Lamp** creates a cozy night-room experience where the authentication screen changes depending on the lamp's state.

### 💡 Lamp ON

The room is bright and warm, and the **Login** card is displayed.

```text
💡 LIGHT IS ON

Welcome
back!

Your cozy little space is waiting for you.

[ Email address       ]
[ Password            ]

[ Remember me ]  Forgot password?

[ Enter My Space → ]

🌙 Turn off the lamp
   to create an account
```

### 🌙 Lamp OFF

The room becomes darker and the authentication card flips to the **Signup** side.

```text
🌙 LIGHT IS OFF

Create your
little space

A warm little corner made just for you.

[ Your name          ]
[ Email address       ]
[ Create password     ]

[ Create My Space ♡ ]

💡 Turn on the lamp
   to go back to login
```

## 🎯 Main Concept

The project uses a hidden checkbox as the lamp's state controller.

```html
<input
    type="checkbox"
    id="lamp-toggle"
    class="lamp-toggle"
>
```

The lamp's physical switch is connected to this checkbox through a `<label>`.

```html
<label
    for="lamp-toggle"
    class="lamp-switch"
    title="Turn lamp on/off"
>
    <span></span>
</label>
```

This allows the complete interaction to work without JavaScript.

## 🌟 Features

### 💡 Interactive Lamp

The lamp is completely created with HTML elements and CSS.

It includes:

* Lamp shade
* Shade rim
* Light glow
* Lamp arm
* Lamp neck
* Cute face
* Eyes
* Smile
* Lamp base
* Interactive switch

The lamp also gently floats and the face has an animated blinking effect.

### 🔄 3D Login/Signup Flip

The authentication card uses CSS 3D transforms.

When the lamp is turned off:

```css
.lamp-toggle:checked ~ .room .auth-card {
    transform: rotateY(180deg);
}
```

This creates the 3D card-flip effect between Login and Signup.

### 🌌 Dynamic Room

The room automatically changes from a warm bright environment to a darker nighttime environment when the lamp is switched off.

```css
.lamp-toggle:checked ~ .room {
    background:
        radial-gradient(
            circle at 27% 38%,
            #c9bbc6 0%,
            #9d899a 22%,
            #6d5d70 48%,
            #453c52 75%,
            #2b2939 100%
        );
}
```

### ✨ Animated Stars

The dark mode includes glowing stars that continuously twinkle.

```css
@keyframes starTwinkle {
    0%, 100% {
        opacity: .15;
        transform: scale(.6);
    }

    50% {
        opacity: 1;
        transform: scale(1.5);
    }
}
```

### ✨ Floating Light Particles

When the lamp is ON, small glowing particles float around the lamp.

When the lamp is OFF, they disappear.

```css
.lamp-toggle:checked ~ .room .particles {
    opacity: 0;
}
```

### 🌿 Cozy Table Scene

The lamp sits on a small animated-style table with:

* 🌱 Plant
* 🪴 Pot
* ☕ Coffee cup
* Coffee
* Cup handle
* Table top
* Table front
* Table legs

This gives the interface a cozy bedroom/workspace atmosphere.

## 🔐 Login Features

The Login screen contains:

* Email address
* Password
* Remember Me
* Forgot Password
* Enter My Space button

The Login state displays the message **"LIGHT IS ON"** and provides the instruction to turn off the lamp to create an account.

## 🆕 Signup Features

The Signup screen contains:

* Name
* Email address
* Create password
* Create My Space button

The Signup state displays **"LIGHT IS OFF"** and provides the instruction to turn the lamp back on to return to Login.

## 🎨 Animation Effects

The project contains several CSS animations:

* 💡 Lamp floating
* 👀 Eye blinking
* ✦ Sparkle animation
* ✨ Ambient glow pulse
* ⭐ Star twinkling
* 🔆 Light particles floating
* 💫 Authentication card 3D flip
* ✨ Button shine
* 🎯 Button hover animation
* 💡 Icon bounce
* 🌈 Background transitions

For example, the lamp continuously floats:

```css
@keyframes lampFloat {
    0%, 100% {
        transform: translateY(0) rotate(-1deg);
    }

    50% {
        transform: translateY(-9px) rotate(1.5deg);
    }
}
```

## 🛠️ Technologies Used

| Technology       | Purpose                  |
| ---------------- | ------------------------ |
| HTML5            | Structure                |
| CSS3             | Styling                  |
| CSS Animations   | Motion and effects       |
| CSS 3D Transform | Login/Signup card flip   |
| CSS Gradients    | Lighting and backgrounds |
| CSS Flexbox      | Layout                   |
| Responsive CSS   | Mobile support           |

## 🚫 No JavaScript

One of the interesting aspects of this project is that the main interaction does **not require JavaScript**.

The lamp state is controlled using:

```html
<input type="checkbox">
```

and CSS selectors such as:

```css
.lamp-toggle:checked ~ .room
```

This controls:

* Room lighting
* Lamp glow
* Light particles
* Lamp brightness
* Authentication card
* Login/Signup state
* Switch position

## 📂 Project Structure

```text
little-lamp/
│
├── index.html
├── style.css
└── README.md
```

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/little-lamp.git
```

### 2. Open the project

```bash
cd little-lamp
```

### 3. Launch

Open:

```text
index.html
```

in your browser.

You can also use **VS Code Live Server**.

## 📱 Responsive Design

The project includes responsive layouts for:

* 💻 Desktop
* 📱 Mobile
* 📲 Small mobile screens
* 💻 Tablet

On mobile devices, the lamp is positioned as a smaller background element while the authentication card remains the main focus.

## 🎨 Design Inspiration

The design combines:

**Cozy + Cute + 3D + Animation + Authentication UI**

instead of using a traditional Login/Signup screen.

The goal is to make a simple frontend project feel like an interactive mini experience.

## 💡 Future Improvements

Possible future additions:

* 🔐 Real authentication
* 💾 Backend integration
* 👤 User profiles
* 🔑 Password reset
* 📧 Email verification
* 🌙 Persistent lamp state
* 🔊 Lamp switch sound
* 🎵 Ambient background music
* 🌓 Theme customization
* 🏠 Personalized user dashboard

## ⚠️ Current Limitation

This is currently a **frontend UI project**.

The Login and Signup forms are interface demonstrations and are not connected to a real authentication backend.

## 🎯 Why This Project Is Unique

Most Login/Signup projects simply switch between two forms.

This project makes the **physical lamp itself the authentication switch**.

```text
             💡
          LAMP ON
             ↓
        ┌───────────┐
        │   LOGIN   │
        └───────────┘

             ↓

             🌙
         LAMP OFF
             ↓
        ┌───────────┐
        │  SIGNUP   │
        └───────────┘
```

## 📌 Instagram Project Idea

This project is especially suitable for showcasing on Instagram because the transformation can be demonstrated in a short video:

**"What if a lamp controlled your Login & Signup? 💡🌙"**

Suggested Reel flow:

```text
0–2 sec   → Dark room 🌙
2–4 sec   → Turn lamp ON 💡
4–6 sec   → 3D Login card appears
6–8 sec   → Turn lamp OFF
8–10 sec  → Card flips to Signup
10–12 sec → Final UI reveal ✨
```

## 👩‍💻 Author

**Yaganti Spandana**

Frontend Developer | HTML | CSS | JavaScript | React

## ⭐ Support

If you like this project, consider giving the repository a ⭐ on GitHub.

Follow for more creative **HTML, CSS, JavaScript and frontend projects**! 💡✨

---

### 🔖 Tags

```text
html
css
login-page
signup-page
login-signup
css-animation
3d-animation
3d-card
frontend
frontend-project
responsive-design
web-design
ui-design
cute-ui
lamp-ui
interactive-ui
creative-css
css-only
```
