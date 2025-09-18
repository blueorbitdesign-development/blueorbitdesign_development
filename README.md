import { useState } from "react"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { motion } from "framer-motion"; import { Briefcase, Cpu, Palette, Laptop, Building2, X } from "lucide-react";

export default function HomePage() { const [selectedProject, setSelectedProject] = useState(null);

const projects = [ {title: "3D CAD Modeling", img: "https://via.placeholder.com/800x450?text=3D+Design", description: "Detailed 3D CAD models for industrial and product design using AutoCAD, Inventor, and SolidWorks."}, {title: "Logo & Branding", img: "https://via.placeholder.com/800x450?text=Brand+Design", description: "Creative logos, brand identities, and marketing materials designed to stand out."}, {title: "Web Development", img: "https://via.placeholder.com/800x450?text=Website+Project", description: "Responsive websites and web applications tailored for business growth."}, {title: "Product Prototyping", img: "https://via.placeholder.com/800x450?text=Prototype", description: "Prototyping services from concept to functional models for testing and validation."}, {title: "Interior Visualization", img: "https://via.placeholder.com/800x450?text=Interior+Design", description: "3D visualization and planning for residential and commercial interior projects."}, {title: "App UI/UX", img: "https://via.placeholder.com/800x450?text=App+Design", description: "User-friendly mobile and web app interface design focusing on smooth user experience."} ];

return ( <div className="min-h-screen bg-gray-50 text-gray-900"> {/* Header */} <header className="flex items-center justify-between px-8 py-4 bg-white shadow-md"> <h1 className="text-2xl font-bold text-blue-600">Design & Development</h1> <nav className="space-x-6 hidden md:flex"> <a href="#about" className="hover:text-blue-600">About</a> <a href="#services" className="hover:text-blue-600">Services</a> <a href="#portfolio" className="hover:text-blue-600">Portfolio</a> <a href="#contact" className="hover:text-blue-600">Contact</a> </nav> <Button className="bg-blue-600 text-white rounded-xl">Get a Quote</Button> </header>

{/* Hero Section */}
  <section className="relative flex flex-col items-center justify-center text-center py-32 bg-gradient-to-r from-blue-600 to-indigo-700 text-white">
    <motion.h2 
      initial={{ opacity: 0, y: 20 }} 
      animate={{ opacity: 1, y: 0 }} 
      transition={{ duration: 0.6 }}
      className="text-4xl md:text-6xl font-bold mb-4"
    >
      Turning Ideas Into Reality
    </motion.h2>
    <p className="text-lg md:text-xl mb-6">Product, Engineering, Web & Branding Solutions – All Under One Roof</p>
    <Button className="bg-white text-blue-600 rounded-xl font-semibold">Explore Services</Button>
  </section>

  {/* About Section */}
  <section id="about" className="px-8 py-16 max-w-5xl mx-auto text-center">
    <h3 className="text-3xl font-bold mb-4">About Us</h3>
    <p className="text-gray-600 mb-6">
      We deliver innovative design & development solutions across product design, engineering, branding, and digital platforms.
    </p>
    <Button className="bg-blue-600 text-white rounded-xl">Know More</Button>
  </section>

  {/* Services Section */}
  <section id="services" className="px-8 py-16 bg-gray-100">
    <h3 className="text-3xl font-bold text-center mb-12">Our Services</h3>
    <div className="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
      {[{icon: Briefcase, title: "Product & Industrial Design"},
        {icon: Cpu, title: "Mechanical Engineering"},
        {icon: Palette, title: "Graphic & Branding Design"},
        {icon: Laptop, title: "Web & App Development"},
        {icon: Building2, title: "Architectural & Interior Design"}].map((service, i) => (
        <Card key={i} className="shadow-lg rounded-2xl">
          <CardContent className="flex flex-col items-center py-8">
            <service.icon className="w-12 h-12 text-blue-600 mb-4" />
            <h4 className="text-xl font-semibold text-center">{service.title}</h4>
          </CardContent>
        </Card>
      ))}
    </div>
  </section>

  {/* Portfolio Section */}
  <section id="portfolio" className="px-8 py-16">
    <h3 className="text-3xl font-bold text-center mb-12">Our Portfolio</h3>
    <div className="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
      {projects.map((project, i) => (
        <Card 
          key={i} 
          className="shadow-lg rounded-2xl overflow-hidden cursor-pointer hover:shadow-xl transition" 
          onClick={() => setSelectedProject(project)}
        >
          <img src={project.img} alt={project.title} className="w-full h-48 object-cover" />
          <CardContent className="p-4">
            <h4 className="text-xl font-semibold">{project.title}</h4>
          </CardContent>
        </Card>
      ))}
    </div>
  </section>

  {/* Project Modal */}
  {selectedProject && (
    <div className="fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50">
      <div className="bg-white rounded-2xl max-w-2xl w-full p-6 relative">
        <button 
          className="absolute top-4 right-4 text-gray-600 hover:text-black" 
          onClick={() => setSelectedProject(null)}
        >
          <X className="w-6 h-6" />
        </button>
        <img src={selectedProject.img} alt={selectedProject.title} className="w-full h-64 object-cover rounded-xl mb-4" />
        <h4 className="text-2xl font-bold mb-2">{selectedProject.title}</h4>
        <p className="text-gray-700">{selectedProject.description}</p>
      </div>
    </div>
  )}

  {/* Why Choose Us */}
  <section className="px-8 py-16 max-w-5xl mx-auto text-center">
    <h3 className="text-3xl font-bold mb-6">Why Choose Us?</h3>
    <ul className="grid grid-cols-1 md:grid-cols-2 gap-6 text-lg text-gray-700">
      <li>✔️ One-stop solution for Design & Development</li>
      <li>✔️ Expert team with multi-industry experience</li>
      <li>✔️ Affordable & customized services</li>
      <li>✔️ End-to-end support from concept to execution</li>
    </ul>
  </section>

  {/* Call to Action */}
  <section className="py-20 bg-blue-600 text-white text-center">
    <h3 className="text-3xl font-bold mb-4">Have a project in mind? Let’s build it together.</h3>
    <Button className="bg-white text-blue-600 rounded-xl font-semibold">Get in Touch</Button>
  </section>

  {/* Contact Section */}
  <section id="contact" className="px-8 py-16 max-w-4xl mx-auto">
    <h3 className="text-3xl font-bold text-center mb-8">Contact Us</h3>
    <form className="grid gap-4">
      <input type="text" placeholder="Your Name" className="p-3 rounded-xl border" />
      <input type="email" placeholder="Your Email" className="p-3 rounded-xl border" />
      <textarea placeholder="Your Message" className="p-3 rounded-xl border h-32" />
      <Button className="bg-blue-600 text-white rounded-xl">Send Message</Button>
    </form>
  </section>

  {/* Footer */}
  <footer className="py-6 bg-gray-900 text-gray-300 text-center">
    <p>© {new Date().getFullYear()} Design & Development. All rights reserved.</p>
  </footer>
</div>

); }

