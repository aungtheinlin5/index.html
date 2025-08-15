<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sketchware Block Programming Course</title>
    <script src="https://cdn.jsdelivr.net/npm/react@18.2.0/umd/react.development.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/react-dom@18.2.0/umd/react-dom.development.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@babel/standalone@7.20.15/babel.min.js"></script>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @keyframes rgbBorderRun {
            0% {
                border-image: linear-gradient(to right, red, green, blue, red) 1;
            }
            25% {
                border-image: linear-gradient(to right, green, blue, red, green) 1;
            }
            50% {
                border-image: linear-gradient(to right, blue, red, green, blue) 1;
            }
            75% {
                border-image: linear-gradient(to right, red, green, blue, red) 1;
            }
            100% {
                border-image: linear-gradient(to right, green, blue, red, green) 1;
            }
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .animate-rgb-border-run {
            border: 5px solid transparent;
            border-image-slice: 1;
            animation: rgbBorderRun 4s linear infinite;
            border-radius: 12px;
        }
        .animate-fade-in {
            animation: fadeIn 1s ease-out;
        }
    </style>
</head>
<body>
    <div id="root"></div>
    <script type="text/babel">
        function ContactForm() {
            const [name, setName] = React.useState('');
            const [email, setEmail] = React.useState('');
            const [message, setMessage] = React.useState('');

            const handleSubmit = () => {
                const mailtoLink = `mailto:aungtheinlin34@gmail.com?subject=Course Inquiry from ${encodeURIComponent(name)}&body=${encodeURIComponent('Name: ' + name + '\nEmail: ' + email + '\nMessage: ' + message)}`;
                window.location.href = mailtoLink;
            };

            return (
                <div className="bg-white p-8 rounded-lg shadow-lg max-w-lg mx-auto">
                    <h3 className="text-xl font-semibold text-gray-800 mb-4">Send Us a Message</h3>
                    <p className="text-gray-600 mb-6">Fill out the form below to join our Sketchware Block Programming Course!</p>
                    <div className="space-y-4">
                        <input
                            type="text"
                            placeholder="Your Name"
                            value={name}
                            onChange={(e) => setName(e.target.value)}
                            className="w-full p-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-600"
                            required
                        />
                        <input
                            type="email"
                            placeholder="Your Email"
                            value={email}
                            onChange={(e) => setEmail(e.target.value)}
                            className="w-full p-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-600"
                            required
                        />
                        <textarea
                            placeholder="Your Message"
                            value={message}
                            onChange={(e) => setMessage(e.target.value)}
                            className="w-full p-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-600"
                            rows="5"
                            required
                        ></textarea>
                        <button
                            onClick={handleSubmit}
                            className="w-full bg-indigo-600 text-white px-6 py-3 rounded-full font-semibold hover:bg-indigo-700 transition"
                        >
                            Send Message
                        </button>
                    </div>
                    <p className="text-gray-600 mt-4 text-center">
                        Or email us directly at: <a href="mailto:aungtheinlin34@gmail.com" className="text-indigo-600 hover:underline">aungtheinlin34@gmail.com</a>
                    </p>
                </div>
            );
        }

        function App() {
            return (
                <div className="min-h-screen bg-gray-50 font-sans">
                    <header className="bg-gradient-to-r from-indigo-700 to-purple-600 text-white py-12 relative overflow-hidden">
                        <div className="max-w-7xl mx-auto px-4 text-center">
                            <h1 className="text-5xl md:text-6xl font-extrabold animate-fade-in">
                                Sketchware Block Programming
                            </h1>
                            <p className="mt-4 text-xl md:text-2xl animate-fade-in" style={{ animationDelay: '0.2s' }}>
                                Build Mobile Apps Without Coding! Starts August 16, 2025
                            </p>
                            <a
                                href="#contact"
                                className="mt-6 inline-block bg-yellow-400 text-gray-900 px-6 py-3 rounded-full font-semibold text-lg hover:bg-yellow-500 transition animate-fade-in"
                                style={{ animationDelay: '0.4s' }}
                            >
                                Join Now for 50,000 MMK
                            </a>
                        </div>
                    </header>

                    <nav className="bg-white shadow-md sticky top-0 z-10">
                        <div className="max-w-7xl mx-auto px-4 py-3">
                            <div className="flex space-x-6 justify-center">
                                <a href="#home" className="text-gray-700 hover:text-indigo-600 font-medium">Home</a>
                                <a href="#courses" className="text-gray-700 hover:text-indigo-600 font-medium">Course Details</a>
                                <a href="#about" className="text-gray-700 hover:text-indigo-600 font-medium">About</a>
                                <a href="#contact" className="text-gray-700 hover:text-indigo-600 font-medium">Contact</a>
                            </div>
                        </div>
                    </nav>

                    <main className="max-w-7xl mx-auto px-4 py-10">
                        <section id="courses" className="mb-12">
                            <h2 className="text-3xl font-semibold text-gray-800 mb-6 text-center">Sketchware Block Programming Course</h2>
                            <div className="bg-white p-6 rounded-lg shadow-lg hover:shadow-xl transition animate-rgb-border-run">
                                <h3 className="text-xl font-semibold text-gray-800">Class 1: Learn to Build Mobile Apps</h3>
                                <p className="mt-2 text-gray-600">Join our hands-on course to learn Sketchware Block Programming and create your own mobile apps without writing code!</p>
                                <ul className="mt-4 text-gray-600 list-disc list-inside">
                                    <li><strong>Start Date:</strong> August 16, 2025</li>
                                    <li><strong>End Date:</strong> August 23, 2025</li>
                                    <li><strong>Schedule:</strong> Daily, 9:00 AM - 11:00 AM (Please confirm exact timings)</li>
                                    <li><strong>Course Fee:</strong> 50,000 MMK</li>
                                </ul>
                                <a href="#contact" className="mt-4 inline-block bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700">Register Now</a>
                            </div>
                        </section>

                        <section id="about" className="mb-12">
                            <h2 className="text-3xl font-semibold text-gray-800 mb-6 text-center">About the Course</h2>
                            <p className="text-gray-600">This course is designed for beginners and enthusiasts who want to dive into mobile app development using Sketchware's intuitive block-based programming. Learn to create functional apps in just one week!</p>
                        </section>

                        <section id="contact" className="mb-12">
                            <h2 className="text-3xl font-semibold text-gray-800 mb-6 text-center">Contact Us</h2>
                            <ContactForm />
                        </section>
                    </main>

                    <footer className="bg-gray-800 text-white py-6">
                        <div className="max-w-7xl mx-auto px-4 text-center">
                            <p>&copy; 2025 Sketchware Block Programming Course. All rights reserved.</p>
                        </div>
                    </footer>
                </div>
            );
        }

        const root = ReactDOM.createRoot(document.getElementById('root'));
        root.render(<App />);
    </script>
</body>
</html>
