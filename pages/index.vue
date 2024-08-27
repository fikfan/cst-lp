<template>
  <div>
    <header class="flex h-20 border-b border-rose-200 py-6">
      <div class="w-full container flex items-center justify-between bg-background px-4 md:px-6">
        <a href="#" class="flex items-center">
          <img :src="Logo" alt="" class="max-w-[160px] md:max-w-[205px]">
        </a>
        <nav class="hidden items-center gap-6 lg:flex">
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground">
            About
          </a>
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground">
            Products
          </a>
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground">
            Services
          </a>
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground">
            Clients
          </a>
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground">
            Careers
          </a>
        </nav>
        <Button class="inline-flex">Work with us</Button>
      </div>
    </header>

    <section class="w-full py-12 md:py-24 lg:py-28 bg-off-white">
      <div class="container mx-auto px-4 md:px-6">
        <div class="text-center">
          <div class="flex flex-col justify-center items-center space-y-4">
            <div class="space-y-2">
              <h1 class="text-3xl font-bold tracking-tighter sm:text-5xl xl:text-6xl/none">
                We build awesome <br class="block md:hidden"> <<VueTypewriterEffect :strings="['things', 'websites', 'mobile app', 'software']" />>
              </h1>
            </div>
            <p class="max-w-[600px] text-muted-foreground md:text-xl">
              Core System Technologies is engaged primarily in design and development of online/cloud system, website, offline system and mobile app.
            </p>
            <div class="flex flex-col gap-2 min-[400px]:flex-row">
              <Button class="px-8 rounded-md">Get Started</Button>
              <Button class="px-8 rounded-md" variant="outline">Learn More</Button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="w-full py-12 md:py-24 lg:py-28">
      <div class="container px-4 md:px-6">
        <div class="flex flex-col items-center justify-center space-y-4 text-center">
          <h2 class="text-3xl font-bold tracking-tighter sm:text-5xl">Products</h2>
          <p class="max-w-[900px] text-muted-foreground md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed">
            Acme Inc offers a wide range of products to meet the needs of our clients.
          </p>
        </div>
        <div class="mx-auto grid max-w-5xl items-center gap-6 py-12">
          <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <Card v-for="project in projects" :key="project.id">
              <CardContent class="p-6 grid gap-4 items-center">
                <img
                  :src="project.image"
                  width="300"
                  height="300"
                  alt="Logo"
                  class="aspect-[2/1] overflow-hidden rounded-lg object-contain object-center"
                />
                <h3 class="text-xl font-bold text-center">{{ project.name }}</h3>
                <p class="text-muted-foreground">
                  {{ project.desc }}
                </p>
                <Button variant="outline" class="bg-off-white">Learn More</Button>
              </CardContent>
            </Card>

          </div>
        </div>
      </div>
    </section>

    <section class="w-full py-12 md:py-24 lg:py-28">
      <div class="container px-4 md:px-6">
        <div class="flex flex-col items-center justify-center space-y-4 text-center">
          <h2 class="text-3xl font-bold tracking-tighter sm:text-5xl">Services</h2>
          <p class="max-w-[900px] text-muted-foreground md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed">
            Acme Inc offers a wide range of services to meet the needs of our clients.
          </p>
        </div>
        <div class="mx-auto grid max-w-5xl items-center gap-6 py-12 lg:grid-cols-3 lg:gap-8">
          <Card v-for="service in services" :key="service.id" class="min-h-auto lg:min-h-[345px]">
            <CardContent class="p-6">
              <div class="p-2 rounded-full bg-gray-300 w-fit">
                <component :is="service.icon" />
              </div>
              <div class="grid gap-4 mt-2">
                <h3 class="text-xl font-bold">{{service.name}}</h3>
                <p class="text-muted-foreground">
                  {{ service.desc }}
                </p>
              </div>
            </CardContent>          
          </Card>

        </div> 

        <div class="w-full flex justify-center">
          <Button class="w-fit">Work with us</Button>
        </div>
      </div>
    </section>

    <section class="w-full py-12 md:py-24 lg:py-28 bg-off-white">
      <div class="container px-4 md:px-6">
        <div class="flex flex-col items-center justify-center space-y-4 text-center">
          
          <h2 class="text-3xl font-bold tracking-tighter sm:text-5xl">Our Clients</h2>
          <p class="max-w-[900px] text-muted-foreground md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed">
            Core System Technologies is proud to work with a diverse range of clients across various industries.
          </p>
          
          <div class="flex items-center gap-2 text-4xl font-bold pt-6 pb-2">
            <span>60+ Clients</span>
          </div>

          <div class="flex items-center gap-2 text-4xl font-bold pb-6">
            <span>90+ Projects ongoing</span>
          </div>

          <MarqueeComponent />
        </div>
      </div>
    </section>

    <section class="w-full py-12 md:py-24 lg:py-28 bg-off-white">
        <div class="container px-4 md:px-6">
          <div class="flex flex-col items-center justify-center space-y-4 text-center">
            <div class="space-y-2">
              <h2 class="text-3xl font-bold tracking-tighter sm:text-5xl">About Us</h2>
              <p class="max-w-[900px] text-muted-foreground md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed py-4">
                Core System Technologies is a leading provider of innovative solutions for businesses of all sizes. Our team of experts
                is dedicated to helping our clients succeed.
              </p>
            </div>
          </div>
          <div class="mx-auto grid max-w-5xl items-center gap-6 py-12 lg:grid-cols-2 lg:gap-12">
            <img
              :src="AboutHero"
              width="550"
              height="310"
              alt="Image"
              class="mx-auto aspect-video overflow-hidden rounded-xl object-cover object-center sm:w-full lg:order-last"
            />
            <div class="flex flex-col text-center md:text-left justify-center space-y-4">
              <ul class="grid gap-6">
                <li>
                  <div class="grid gap-1">
                    <h3 class="text-xl font-bold">Our Mission</h3>
                    <p class="text-muted-foreground">
                      To revolutionize the IT industry in Sarawak, Malaysia, and potentially across Asia by adopting the latest Internet/Cloud technologies as the core of our products.
                    </p>
                  </div>
                </li>
                <li>
                  <div class="grid gap-1">
                    <h3 class="text-xl font-bold">Our Values</h3>
                    <p class="text-muted-foreground">Innovation in online/cloud systems, websites, offline systems, and mobile apps, while committing to cutting-edge technologies, dedicating ourselves to client support through cloud server management, and emphasizing knowledge sharing via technical training</p>
                  </div>
                </li>
                <li>
                  <div class="grid gap-1">
                    <h3 class="text-xl font-bold">Our Team</h3>
                    <p class="text-muted-foreground">Based in Kuching, Sarawak, our company comprises a dedicated workforce of 15 full-time and 5 part-time employees, all committed to driving technological innovation in Malaysia and beyond.</p>
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
    </section>

    <section class="w-full py-12 md:py-24 lg:py-28 bg-off-white">
        <div class="container px-4 md:px-6">
          <div class="flex flex-col items-center justify-center space-y-4 text-center">
            
            <h2 class="text-3xl font-bold tracking-tighter sm:text-5xl">Get in touch</h2>
            <div class="max-w-[900px] text-muted-foreground md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed">
              <a href="https://maps.app.goo.gl/iKRZ9ftpb4DDtLAZ9" target="_blank" class="text-red-500 underline">Visit us</a> or let's discuss how we can work together.
            </div>
          
            <div class="flex flex-row gap-2 min-[400px]:flex-row">
              <Dialog>
                <DialogTrigger>
                  <Button>Contact Us</Button>
                </DialogTrigger>
                <DialogContent>
                  <DialogHeader>
                    <DialogTitle>Find us or give us a call!</DialogTitle>
                    <DialogDescription>
                      <div class="p-2 flex items-center">
                        <MapPin class="w-6 h-6 mr-2"/> 
                        <p>
                          3rd Floor, Milan Square, Sublot 12, Lot 554, Block 11, Jalan Wan Alwi, 93150 Kuching, Sarawak.
                        </p>
                      </div>

                      <div class="p-2 flex items-center">
                        <Phone class="w-4 h-4 mr-2" />
                        <p>+60 16-800 7676</p>
                      </div>
                    </DialogDescription>
                  </DialogHeader>

                  <DialogFooter>
                    <DialogClose as-child>
                      <Button>Got it, thanks!</Button>
                    </DialogClose>
                    
                  </DialogFooter>
                </DialogContent>
              </Dialog>
              <Dialog>
                <DialogTrigger>
                  <Button variant="outline">Careers</Button>
                </DialogTrigger>
                <DialogContent>
                  <DialogHeader>
                    <DialogTitle>Interested in joining us?</DialogTitle>
                    <DialogDescription>
                      <p>We are always welcoming new talent to join our company.</p><br>
                      <p>Please view our current job opportunities list to find out what position we are available at the moment. If you are interested in any of the available jobs please send us your resume at <a href="mailto:talent@coresystemtech.com" class="text-red-500 underline">talent@coresystemtech.com</a></p>
                      
                    </DialogDescription>
                  </DialogHeader>

                  <DialogFooter>
                    <DialogClose as-child>
                      <Button>Got it, thanks!</Button>
                    </DialogClose>
                    
                  </DialogFooter>
                </DialogContent>
              </Dialog>
            </div>

            <h5 class="text-2xl font-bold tracking-tighter sm:text-4xl pt-4">Follow our socials</h5>

            <div class="flex gap-4">
              <a href="https://www.facebook.com/cstsb/" target="_blank">
                <Button><Facebook class="w-4 h-4 mr-2" />Facebook</Button>
              </a>
              <a href="https://www.linkedin.com/company/coresystemtech/" target="_blank">
                <Button><Linkedin class="w-4 h-4 mr-2" />LinkedIn</Button>
              </a>
              
            </div>

          </div>
        </div>
    </section>

    <footer class="w-full border-t border-rose-200 py-4 px-4 md:px-6">
      <div class="container mx-auto flex flex-col items-center text-center md:text-right justify-between gap-4 sm:flex-row">
        <p class="text-sm text-muted-foreground">&copy; {{ new Date().getFullYear() }} UNOFFICIAL CONCEPT REDESIGN - FOR JOB APPLICATION PURPOSES ONLY</p>
        <a href="https://github.com/fikfan/cst-lp" target="_blank" class="text-red-500 underline text-sm text-muted-foreground">Repository Link</a>
      </div>
      
    </footer>

  </div>
</template>

<script setup>
import Logo from '@/assets/images/logo.png'
import AboutHero from '@/assets/images/man.jpg'
import VueTypewriterEffect from "vue-typewriter-effect";
import DatabaseLogo from '@/assets/icons/database.png'
import { Database, AppWindow, TabletSmartphone } from 'lucide-vue-next';
import { Facebook, Linkedin, MapPin, Phone } from 'lucide-vue-next';
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from '@/components/ui/card'

import {
  Dialog,
  DialogContent,
  DialogDescription,
  DialogFooter,
  DialogHeader,
  DialogTitle,
  DialogClose,
  DialogTrigger,
} from '@/components/ui/dialog'

const helloArray = ['hello', 'こんにちは', 'bonjour']


//projects card
const projects = ref([
  { id: 1, name: 'Project A', desc: 'Our flagship product, designed to streamline your business operations.', image: Logo },
  { id: 2, name: 'Project B', desc: 'Our flagship product, designed to streamline your business operations.', image: Logo },
  { id: 3, name: 'Project C', desc: 'Our flagship product, designed to streamline your business operations.', image: Logo }
])

const services = ref([
  { id:1, name: 'Website', desc: 'Expert web development team offering custom, affordable websites with responsive design, modern UI/UX, and full-stack proficiency in open-source technologies.', icon: Database },
  { id:2, name: 'Mobile App', desc: 'We employ structured frameworks and best practices, staying current with evolving tech trends to deliver optimal development solutions for our clients.', icon: AppWindow },
  { id:3, name: 'Online Application', desc: 'Our expert team delivers top-tier iOS and Android apps using cutting-edge tech and proven strategies. Proficient in Swift, Objective-C, Java, Kotlin, and cross-platform frameworks, we create feature-rich, user-centric mobile solutions that exceed client expectations', icon: TabletSmartphone }
])

</script>
