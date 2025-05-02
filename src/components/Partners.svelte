<script>
    import { onMount } from 'svelte';
    import Swiper from 'swiper';
    import { Autoplay, Pagination } from 'swiper/modules'; // ✅ Correct source for named modules
    import 'swiper/css';
    import 'swiper/css/pagination';
  
    export let item;
  
    let swiperInstance;
  
    Swiper.use([Autoplay, Pagination]); // ✅ Register modules
  
    function highlightActiveSlides(swiper) {
      swiper.slides.forEach(slide => slide.classList.remove("is-active"));
      const start = swiper.activeIndex;
      swiper.slides[start]?.classList.add("is-active");
      swiper.slides[start + 1]?.classList.add("is-active");
    }
  
    onMount(() => {
      swiperInstance = new Swiper(".serviceSwiper1", {
        slidesPerView: 2,
        spaceBetween: 20,
        speed: 1000,
        autoplay: {
          delay: 5000,
          disableOnInteraction: false,
        },
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
        },
        breakpoints: {
          0: {
            slidesPerView: 1,
          },
          640: {
            slidesPerView: 2,
          },
          1024: {
            slidesPerView: 2,
          },
        },
        on: {
          init: function () {
            highlightActiveSlides(this);
          },
          slideChange: function () {
            highlightActiveSlides(this);
          }
        }
      });
    });

  
    $: facilitiesSafe = item.facilities ?? [];

// Dynamically set grid columns
$: gridClass = facilitiesSafe.length <= 12 ? 'md:grid-cols-2' : 'md:grid-cols-3';

// Chunking function
function chunkFacilities(facilities, size) {
  const chunks = [];
  for (let i = 0; i < facilities.length; i += size) {
    chunks.push(facilities.slice(i, i + size));
  }
  return chunks;
}

// Chunk only if valid
$: facilityChunks = chunkFacilities(facilitiesSafe, 3);
  </script>
  
  <div class="p-6 ">
   
    <section class="tour-single pt-24">
        <div class="tf-container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="tab-content" id="pills-tabContent">
                        <div class="tab-pane fade show active" id="pills-information" role="tabpanel"
                            aria-labelledby="pills-information-tab" tabindex="0">
                            <div class="row mb-50">
                                <div class="col-lg-12">
                                    <div class="inner-heading-wrap flex-two">
                                        <div class="inner-heading">
                                            <span class="feature">KSUM Partnered</span>
                                            <h2 class=" md:text-4xl text-3xl pb-4 font-bold">{item.title}</h2>
                                            <ul class="flex-three list-wrap-heading gap-3">
                                              <li class="flex-three">
                                                  <i class="icon-18"></i>
                                                  <span class="md:text-base text-[12px] text-black">{item.address}</span>
                                              </li>
                                              <li class="flex-three text-[#00AEEF;] gap-3">
                                                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                                                      <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
                                                    </svg>
                                                    
                                                  <span class="md:text-base text-[12px] text-black">{item.email}</span>
                                              </li>
                                              <li class="flex-three text-[#00AEEF;] gap-3">
                                                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                                                      <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 0 0 2.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 0 1-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 0 0-1.091-.852H4.5A2.25 2.25 0 0 0 2.25 4.5v2.25Z" />
                                                    </svg>
                                                    
                                                  <span class="md:text-base text-[12px] text-black">{item.number}</span>
                                              </li>
                                          </ul>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        
                            <div class="row pb-0 mb-10 hidden">
                                <div class="col-lg-12">
                                    <div class="information-content-tour">
                                       
                                        <div class="description-wrap mb-10">
                                            <p class="des text-justify">{item.desc}</p>
                                        </div>
                                       
                                    </div>
                                </div>
                                <!-- <div class="col-lg-4">
                                    <div class="side-bar-right">
                                      
                                        <div class="sidebar-widget bg-[#F4F6F8] p-8 rounded-md">
                                            <h6 class="block-heading">For assistance contact</h6>
                                            <ul class="category-confidence bg-[#F4F6F8] gap-2">
                                                <li class="flex-three text-[#00AEEF] gap-2">
                                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                                                        <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
                                                      </svg>
                                                      
                                                    <span>{item.email}</span>
                                                </li>
                                                <li class="flex-three text-[#00AEEF] gap-2">
                                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                                                        <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 0 0 2.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 0 1-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 0 0-1.091-.852H4.5A2.25 2.25 0 0 0 2.25 4.5v2.25Z" />
                                                      </svg>
                                                      
                                                    <span>{item.number}</span>
                                                </li>
                                            </ul>
                                        </div>
                                      
                                    </div>
                                </div> -->
                            </div>

                            <div class="flex md:flex-row flex-col md:mb-24 gap-4">
                              <div class="md:w-1/3 w-full h-64 object-cover md:mb-0 mb-4">
                                  <img src={item.image_main} alt="image" class=" h-full   rounded-md ">
                              </div>
                              <div class="md:w-2/3 w-full overflow-hidden">
                                  {#if item.images}
                                  <section class="md:container">
                                    <div class="swiper serviceSwiper1 overflow-hidden">
                                      <div class="swiper-wrapper">
                                        {#each item.images as image}
                                          <div class="swiper-slide h-auto flex flex-col">
                                            <div class="tf-widget-populer flex flex-col h-full">
                                              <div class="image relative">
                                                <img src="{image}" alt="Image" class="h-64 w-full" />
                                              </div>
                                            </div>
                                          </div>
                                        {/each}
                                      </div>
                                      <div class="swiper-pagination"></div>
                                    </div>
                                  </section>
                                {/if}
                              </div>
                          </div>


                            <div class="expect-wrap mb-24 md:pt-0 pt-10">
                                <h4 class="title pb-6 text-xl font-semibold">The facilities and offers available</h4>

                                <div class="grid grid-cols-1 gap-4 {gridClass}">
                                  {#each facilityChunks as chunk}
                                    <div>
                                      <ul class="listing-clude">
                                        {#each chunk as facility}
                                          <li class="flex-three">
                                            <i class="icon-Vector-7"></i>
                                            <p class="capitalize">{facility}</p>
                                          </li>
                                        {/each}
                                      </ul>
                                    </div>
                                  {/each}
                                </div>
                                
                                <!-- <div class="grid grid-cols-1 gap-4 {item.facilities.length <= 12 ? 'md:grid-cols-2' : 'md:grid-cols-3'}">
                                  <div>
                                    <ul class="listing-clude">
                                      {#each item.facilities.slice(0, 6) as facility}
                                        <li class="flex-three">
                                          <i class="icon-Vector-7"></i>
                                          <p class="capitalize">{facility}</p>
                                        </li>
                                      {/each}
                                    </ul>
                                  </div>
                                  
                                  <div>
                                    <ul class="listing-clude">
                                      {#each item.facilities.slice(6, 12) as facility}
                                        <li class="flex-three">
                                          <i class="icon-Vector-7"></i>
                                          <p>{facility}</p>
                                        </li>
                                      {/each}
                                    </ul>
                                  </div>
                                  
                                  {#if item.facilities.length > 12}
                                    <div>
                                      <ul class="listing-clude">
                                        {#each item.facilities.slice(12) as facility}
                                          <li class="flex-three">
                                            <i class="icon-Vector-7"></i>
                                            <p>{facility}</p>
                                          </li>
                                        {/each}
                                      </ul>
                                    </div>
                                  {/if}
                                  
                                </div> -->
                              </div>
                              
                            {#if item.images}
                            <section class="container mb-24 hidden">
                                <div class="">
                                    <div class="description-wrap mb-4">
                                        <span class="description">Facility Available</span>
                                    </div>
                                    <div class="row">
                                        <div class="col-lg-12 relative populer-activities-slide">
                                            <div class="swiper serviceSwiper populer-activities overflow-hidden">
                                                <div class="swiper-wrapper">
                                                    {#each item.images as image}
                                                        <div class="swiper-slide h-auto flex flex-col">
                                                            <div class="tf-widget-populer flex flex-col h-full">
                                                                <div class="image relative">
                                                                    <img src="{image}" alt="Image" class=" h-64">

                                                                </div>
                                                                
                                                            </div>
                                                        </div>
                                                    {/each}
                                                </div>
                                            </div>
                                            <!-- <div class="swiper-button-next"></div>
                                            <div class="swiper-button-prev"></div> -->
                                        </div>
                                    </div>
                                </div>
            
                            </section>
                            {/if}

                            <div class=" flex items-end justify-end w-full">
                                <a href="javascript:history.back()" class="text-blue-800 flex gap-2 text-xl font-semibold">
                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-3">
                                      <path stroke-linecap="round" stroke-linejoin="round" d="m18.75 4.5-7.5 7.5 7.5 7.5m-6-15L5.25 12l7.5 7.5" />
                                    </svg>
                                    Back
                                </a>
                            </div>

                        </div>
                    </div>
                </div>
            </div>

        </div>
    </section>

  
  
    
  </div>

  
  