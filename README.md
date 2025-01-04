# AI Image Generator

A modern React application that allows users to generate images using AI, save them, and share them with the community.

![AI Image Generator](https://via.placeholder.com/800x400?text=AI+Image+Generator)

## Features

- 🎨 AI-powered image generation from text prompts
- 💡 Smart prompt enhancement suggestions
- 🔄 Real-time image preview
- 📝 Prompt history tracking
- 💾 Save and share generated images
- 🎯 Writing tips for better results
- 🌗 Responsive design
- ⚡ Modern UI with animations

## Tech Stack

- React.js
- Tailwind CSS
- Lucide Icons
- React Router
- Node.js/Express (Backend)

## Prerequisites

Before you begin, ensure you have met the following requirements:
- Node.js >= 14.x
- npm >= 6.x

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/ai-image-generator.git
```

2. Navigate to the project directory:
```bash
cd ai-image-generator
```

3. Install dependencies:
```bash
npm install
```

4. Create a `.env` file in the root directory and add your environment variables:
```env
REACT_APP_API_URL=your_api_url
```

5. Start the development server:
```bash
npm start
```

## Project Structure

```
src/
├── components/
│   ├── form/
│   │   └── GenerateImage.jsx
│   ├── Input/
│   │   └── TextInput.jsx
│   └── buttons/
│       └── button.jsx
├── api/
│   └── index.js
├── styles/
│   └── index.css
└── App.js
```

## Component Usage

### GenerateImage Component

```jsx
import GenerateImage from './components/form/GenerateImage';

function App() {
  return (
    <GenerateImage
      onGenerate={async (prompt) => {
        // Handle image generation
        const response = await generateImage(prompt);
        return response;
      }}
      onPost={async (post) => {
        // Handle post creation
        await createPost(post);
      }}
      suggestions={[
        "A cyberpunk city at sunset with flying cars",
        "A magical forest with glowing mushrooms",
        "An underwater temple with ancient artifacts"
      ]}
    />
  );
}
```

## Props

| Prop | Type | Description |
|------|------|-------------|
| onGenerate | function | Callback function for image generation |
| onPost | function | Callback function for post creation |
| initialPost | object | Initial state for the post |
| suggestions | array | Array of prompt suggestions |

## Features in Detail

### Image Generation
- Enter a detailed prompt describing the desired image
- Enhanced prompt suggestions for better results
- Real-time preview of generated images

### Post Creation
- Add author name
- Share generated images with the community
- Track post creation status

### History Tracking
- Keep track of previously used prompts
- Quick reuse of successful prompts
- View generation history

## API Integration

The component interfaces with two main API endpoints:

1. Generate Image API:
```javascript
const response = await GenerateImageFromPrompt({ prompt: "your prompt" });
```

2. Create Post API:
```javascript
const response = await CreatePost({ name, prompt, photo });
```

## Styling

The project uses Tailwind CSS for styling with:
- Responsive design
- Modern UI components
- Smooth animations
- Custom color schemes
- Glassmorphism effects

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Contact

Your Name - [@yourusername](https://twitter.com/yourusername)

Project Link: [https://github.com/yourusername/ai-image-generator](https://github.com/yourusername/ai-image-generator)

## Acknowledgments

- [React Documentation](https://reactjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Lucide Icons](https://lucide.dev/)
