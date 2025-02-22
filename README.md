# Starboy-store
On-line Store 
import React from "react";
import Image from "next/image";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function HomePage() {
  return (
    <div className="min-h-screen bg-white text-gray-900">
      <header className="bg-[#001F3F] text-white p-4">
        <div className="container mx-auto flex justify-between items-center">
          <h1 className="text-2xl font-bold">Star Boy</h1>
          <nav>
            <ul className="flex space-x-6">
              <li><a href="#inicio">Inicio</a></li>
              <li><a href="#tienda">Tienda</a></li>
              <li><a href="#sobre-nosotros">Sobre Nosotros</a></li>
              <li><a href="#testimonios">Testimonios</a></li>
              <li><a href="#contacto">Contacto</a></li>
            </ul>
          </nav>
        </div>
      </header>
      <section id="inicio" className="relative h-96">
        <div className="absolute inset-0">
          <Image
            src="/images/los-angeles-casual-banner.jpg"
            alt="Banner Los Angeles"
            fill
            className="object-cover"
            priority
          />
        </div>
        <div className="relative z-10 flex items-center justify-center h-full bg-black bg-opacity-50">
          <h2 className="text-4xl font-bold text-white">Moda Urbana con Elegancia</h2>
        </div>
      </section>
      <section id="tienda" className="py-10 container mx-auto">
        <h2 className="text-3xl font-bold text-center mb-8">Productos Destacados</h2>
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <Card className="overflow-hidden rounded-lg shadow-lg">
            <Image
              src="/images/chaqueta.jpg"
              alt="Chaqueta de lujo"
              width={600}
              height={800}
              className="object-cover"
            />
            <CardContent className="p-4">
              <h3 className="text-xl font-semibold">Chaqueta de Lujo</h3>
              <p className="text-gray-700">Chaqueta casual con estilo urbano.</p>
              <p className="mt-2 font-bold">$400,000 COP</p>
              <Button className="mt-4">Comprar</Button>
            </CardContent>
          </Card>
          <Card className="overflow-hidden rounded-lg shadow-lg">
            <Image
              src="/images/gorra.jpg"
              alt="Gorra casual"
              width={600}
              height={800}
              className="object-cover"
            />
            <CardContent className="p-4">
              <h3 className="text-xl font-semibold">Gorra Casual</h3>
              <p className="text-gray-700">Gorra con diseño exclusivo.</p>
              <p className="mt-2 font-bold">$150,000 COP</p>
              <Button className="mt-4">Comprar</Button>
            </CardContent>
          </Card>
        </div>
      </section>
      <section id="sobre-nosotros" className="py-10 bg-gray-100">
        <div className="container mx-auto">
          <h2 className="text-3xl font-bold text-center mb-8">Sobre Nosotros</h2>
          <p className="text-center text-gray-700 max-w-3xl mx-auto">
            En Star Boy, nos inspiramos en la sofisticación y el estilo casual de Los Ángeles. Combinamos lujo y autenticidad para ofrecer prendas exclusivas de alta calidad.
          </p>
        </div>
      </section>
      <section id="testimonios" className="py-10 container mx-auto">
        <h2 className="text-3xl font-bold text-center mb-8">Testimonios</h2>
        <div className="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div className="p-6 bg-white rounded-lg shadow-lg">
            <p className="text-gray-700">"Excelente calidad y diseño. Me encanta cómo se siente usar estas prendas, realmente marcan la diferencia."</p>
            <p className="mt-4 font-bold">- Juan Pérez</p>
          </div>
          <div className="p-6 bg-white rounded-lg shadow-lg">
            <p className="text-gray-700">"El servicio es inmejorable y los productos reflejan un alto nivel de sofisticación. ¡Altamente recomendado!"</p>
            <p className="mt-4 font-bold">- Carlos López</p>
          </div>
        </div>
      </section>
      <section id="contacto" className="py-10 bg-gray-50">
        <div className="container mx-auto">
          <h2 className="text-3xl font-bold text-center mb-8">Contacto</h2>
          <form className="max-w-xl mx-auto space-y-4">
            <input type="text" placeholder="Tu Nombre" className="w-full p-3 border rounded" required />
            <input type="email" placeholder="Tu Email" className="w-full p-3 border rounded" required />
            <textarea placeholder="Tu Mensaje" className="w-full p-3 border rounded" rows="4" required></textarea>
            <Button type="submit" className="w-full">Enviar Mensaje</Button>
          </form>
        </div>
      </section>
      <footer className="bg-[#001F3F] text-white p-6">
        <div className="container mx-auto text-center">
          <div className="mb-4">
            <h3 className="text-lg font-semibold">Métodos de Pago</h3>
            <div className="flex justify-center gap-4 mt-2">
              <Image src="/images/visa.png" alt="Visa" width={50} height={30} priority />
              <Image src="/images/mastercard.png" alt="MasterCard" width={50} height={30} priority />
              <Image src="/images/paypal.png" alt="PayPal" width={50} height={30} priority />
            </div>
          </div>
          <p>&copy; 2025 Star Boy. Todos los derechos reservados.</p>
        </div>
      </footer>
    </div>
  );
}

export default HomePage;