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
