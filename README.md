# Social Links Profile

This project is a simple, responsive profile card featuring social links and a hover effect for interactive elements. It uses HTML, CSS, Bootstrap, and Go for the backend to create an appealing and user-friendly layout.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup](#setup)
- [How to Use](#how-to-use)
- [Customization](#customization)

---

## Overview

This project showcases a fictional user profile with social links. Each link is styled as a hoverable card that scales up when hovered, providing a visually interactive experience. The profile card is centrally aligned on the screen with responsive design principles.

The backend server, implemented in Go, serves the frontend files.

## Features

- A responsive and minimalist design.
- Interactive hover effects on social links and the profile image.
- Backend server built with Go to serve frontend files.
- Bootstrap integration for layout and styling.
- Google Fonts for custom typography.
- Fully customizable color scheme and layout.

## Technologies Used

- **HTML5**: For semantic structure and layout.
- **CSS3**: For custom styling and hover effects.
- **Bootstrap 4.5.2**: For responsive design and utility classes.
- **Google Fonts**: For typography (Inter font).
- **Go**: Backend server to serve static files.

## Setup

1. Clone the repository or download the source files.
2. Ensure the following dependencies are available:
   - A modern web browser (Chrome, Firefox, etc.)
   - Internet connection for loading external resources (Bootstrap CSS and Google Fonts).
3. Set up the Go environment for running the backend server.

### Running the Backend Server

1. Install Go if not already installed. Refer to the [official Go documentation](https://golang.org/doc/install) for setup instructions.
2. Run the Go server:
   ```bash
   go run main.go
   ```
3. The server should start on `localhost:8010` (or a configured port).

The provided `main.go` file:

```go
package main

import "github.com/gofiber/fiber/v2"

func main() {
    app := fiber.New()
    app.Static("/", "./Frontend")
    app.Listen(":8010")
}
```

## How to Use

1. Start the backend server using the instructions above.
2. Navigate to `http://localhost:8010` in your web browser.
3. Hover over the profile image and social link buttons to see the interactive effects.

## Customization

### 1. Profile Information
Update the profile information (e.g., name, location, and bio) by modifying the respective `<div>` elements inside the `<main>` tag.

### 2. Social Links
Modify the text of the social links (`<p>` tags) to reflect actual links. For example, replace "GitHub" with your GitHub username or add actual hyperlinks as needed.

Example:
```html
<p class="rounded p-2" style="min-width: 240px; background-color: hsl(0, 0%, 20%);">
  <a href="https://github.com/username" target="_blank" style="text-decoration: none; color: inherit;">GitHub</a>
</p>
```

### 3. Styles
Adjust the styles in the `<style>` block or link an external stylesheet for more complex customizations. For example, change the colors in hover effects or modify the font sizes.

### 4. Profile Picture
Replace the `src` attribute of the `<img>` tag with a link to your preferred image or upload a new image to the `assets/images` directory and update the path.

## Dependencies

- **Bootstrap CSS**: Included via CDN for grid and utility classes.
- **Google Fonts**: Included via CDN for the "Inter" font.
- **Go**: Backend server to serve static files.

## License

This project is for educational and personal use. Feel free to modify and distribute it as needed.

# Social-links-profile
