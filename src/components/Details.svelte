<script>
    export let item;
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
                                            <span class="feature">KSUM Owned</span>
                                            <h2 class="title">{item.title}</h2>
                                            <ul class="flex-three list-wrap-heading">
                                                <li class="flex-three">
                                                    <i class="icon-18"></i>
                                                    <span>{item.address}</span>
                                                </li>
                                                <li class="flex-three text-[#00AEEF;] gap-3">
                                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                                                        <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75" />
                                                      </svg>
                                                      
                                                    <span class="text-black">{item.email}</span>
                                                </li>
                                                <li class="flex-three text-[#00AEEF;] gap-3">
                                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
                                                        <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 0 0 2.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 0 1-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 0 0-1.091-.852H4.5A2.25 2.25 0 0 0 2.25 4.5v2.25Z" />
                                                      </svg>
                                                      
                                                    <span class="text-black">{item.number}</span>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        
                            <div class="row pb-0 mb-0 hidden">
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
                            <section class="discount-h5 pb-20">
                                <div class="tf-container">
                                    <div class="description-wrap mb-4">
                                        <span class="description">Types of Space Available</span>
                                    </div>
                                    <div class="grid md:grid-cols-4 grid-cols-1 gap-4">
                                       
                                        {#if item.s1_type}
                                        <div class="">
                                            <div class="banner-part-item booking-style-2 relative bg-part-gray overflow-hidden">
                                                <p class="text-lg font-bold text-black hover:text-black pb-2">{item.s1_type}</p>
                                                <span class="text-sm font-bold">{item.s1_subsidy}% Subsidy</span>
                                                <span class="text-main sale-up pt-6 pb-4">{item.s1_rate}</span>
                                                <div class=" flex justify-between mb-6">
                                                    <p class="text-main   font-bold">Base Rate</p>
                                                    <p class="text-main  font-bold">{item.s1_base}/-</p>
                                                </div>
                                                <div class=" flex justify-between">
                                                    <p class="text-main   font-bold">After Subsidy</p>
                                                    <p class="text-main   font-bold">{item.s1_after}/-</p>
                                                </div>
                                            </div>
                                        </div>
                                        {/if}

                                        {#if item.s2_type}
                                        <div class="">
                                            <div class="banner-part-item booking-style-2 relative bg-part-gray overflow-hidden">
                                                <p class="text-lg font-bold text-black hover:text-black pb-2">{item.s2_type}</p>
                                                <span class="text-sm font-bold">{item.s2_subsidy}% Subsidy</span>
                                                <span class="text-main sale-up pt-6 pb-4">{item.s2_rate}</span>
                                                <div class=" flex justify-between mb-6">
                                                    <p class="text-main   font-bold">Base Rate</p>
                                                    <p class="text-main  font-bold">{item.s2_base}/-</p>
                                                </div>
                                                <div class=" flex justify-between">
                                                    <p class="text-main   font-bold">After Subsidy</p>
                                                    <p class="text-main   font-bold">{item.s2_after}/-</p>
                                                </div>
                                            </div>
                                        </div>
                                        {/if}

                                        {#if item.s3_type}
                                        <div class="">
                                            <div class="banner-part-item booking-style-2 relative bg-part-gray overflow-hidden">
                                                <p class="text-lg font-bold text-black hover:text-black pb-2">{item.s3_type}</p>
                                                <span class="text-sm font-bold">{item.s3_subsidy}% Subsidy</span>
                                                <span class="text-main sale-up pt-6 pb-4">{item.s3_rate}</span>
                                                <div class=" flex justify-between mb-6">
                                                    <p class="text-main   font-bold">Base Rate</p>
                                                    <p class="text-main  font-bold">{item.s3_base}/-</p>
                                                </div>
                                                <div class=" flex justify-between">
                                                    <p class="text-main   font-bold">After Subsidy</p>
                                                    <p class="text-main   font-bold">{item.s3_after}/-</p>
                                                </div>
                                            </div>
                                        </div>
                                        {/if}

                                        {#if item.s4_type}
                                        <div class="">
                                            <div class="banner-part-item booking-style-2 relative bg-part-gray overflow-hidden">
                                                <p class="text-lg font-bold text-black hover:text-black pb-2">{item.s4_type}</p>
                                                <span class="text-sm font-bold">{item.s4_subsidy}% Subsidy</span>
                                                <span class="text-main sale-up pt-6 pb-4">{item.s4_rate}</span>
                                                <div class=" flex justify-between mb-6">
                                                    <p class="text-main   font-bold">Base Rate</p>
                                                    <p class="text-main  font-bold">{item.s4_base}/-</p>
                                                </div>
                                                <div class=" flex justify-between">
                                                    <p class="text-main   font-bold">After Subsidy</p>
                                                    <p class="text-main   font-bold">{item.s4_after}/-</p>
                                                </div>
                                            </div>
                                        </div>
                                        {/if}
                                   
                                    </div>
                                </div>
                        
                            </section>
                            <div class="row mb-20 image-gallery-single">
                                {#if item.image}

                                <div class="col-12 col-sm-6">
                                    <img src={item.image} alt="image" class=" h-96 object-fill rounded-md">
                                </div>
                                {/if}
                                
                                <!-- {#if item.image1}
                                    <div class="col-6 col-sm-3">
                                        <img src={item.image1} alt="image" class="h-96 object-fill rounded-md">
                                    </div>
                                {/if}
                                
                                {#if item.image2}
                                    <div class="col-6 col-sm-3">
                                        <img src={item.image2} alt="image" class="h-96 object-fill rounded-md">
                                    </div>
                                {/if} -->

                                <div class=" col-6 col-sm-6">
                                    <div id="default-carousel" class="relative w-1/2" data-carousel="slide">
                                        <!-- Carousel wrapper -->
                                        <div class="relative h-56 overflow-hidden rounded-lg md:h-96">
                                             <!-- Item 1 -->
                                            <div class="hidden duration-700 ease-in-out" data-carousel-item>
                                                <img src="/leap/isc1.png" class="absolute block w-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                                            </div>
                                            <!-- Item 2 -->
                                            <div class="hidden duration-700 ease-in-out" data-carousel-item>
                                                <img src="/leap/isc1.png" class="absolute block w-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                                            </div>
                                            <!-- Item 3 -->
                                            <div class="hidden duration-700 ease-in-out" data-carousel-item>
                                                <img src="/leap/isc1.png" class="absolute block w-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                                            </div>
                                            <!-- Item 4 -->
                                            <div class="hidden duration-700 ease-in-out" data-carousel-item>
                                                <img src="/leap/isc1.png" class="absolute block w-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                                            </div>
                                            <!-- Item 5 -->
                                            <div class="hidden duration-700 ease-in-out" data-carousel-item>
                                                <img src="/leap/isc1.png" class="absolute block w-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                                            </div>
                                        </div>
                                        <!-- Slider indicators -->
                                        <div class="absolute z-30 flex -translate-x-1/2 bottom-5 left-1/2 space-x-3 rtl:space-x-reverse">
                                            <button type="button" class="w-3 h-3 rounded-full" aria-current="true" aria-label="Slide 1" data-carousel-slide-to="0"></button>
                                            <button type="button" class="w-3 h-3 rounded-full" aria-current="false" aria-label="Slide 2" data-carousel-slide-to="1"></button>
                                            <button type="button" class="w-3 h-3 rounded-full" aria-current="false" aria-label="Slide 3" data-carousel-slide-to="2"></button>
                                            <button type="button" class="w-3 h-3 rounded-full" aria-current="false" aria-label="Slide 4" data-carousel-slide-to="3"></button>
                                            <button type="button" class="w-3 h-3 rounded-full" aria-current="false" aria-label="Slide 5" data-carousel-slide-to="4"></button>
                                        </div>
                                        <!-- Slider controls -->
                                        <button type="button" class="absolute top-0 start-0 z-30 flex items-center justify-center h-full px-4 cursor-pointer group focus:outline-none" data-carousel-prev>
                                            <span class="inline-flex items-center justify-center w-10 h-10 rounded-full bg-white/30 dark:bg-gray-800/30 group-hover:bg-white/50 dark:group-hover:bg-gray-800/60 group-focus:ring-4 group-focus:ring-white dark:group-focus:ring-gray-800/70 group-focus:outline-none">
                                                <svg class="w-4 h-4 text-white dark:text-gray-800 rtl:rotate-180" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 6 10">
                                                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 1 1 5l4 4"/>
                                                </svg>
                                                <span class="sr-only">Previous</span>
                                            </span>
                                        </button>
                                        <button type="button" class="absolute top-0 end-0 z-30 flex items-center justify-center h-full px-4 cursor-pointer group focus:outline-none" data-carousel-next>
                                            <span class="inline-flex items-center justify-center w-10 h-10 rounded-full bg-white/30 dark:bg-gray-800/30 group-hover:bg-white/50 dark:group-hover:bg-gray-800/60 group-focus:ring-4 group-focus:ring-white dark:group-focus:ring-gray-800/70 group-focus:outline-none">
                                                <svg class="w-4 h-4 text-white dark:text-gray-800 rtl:rotate-180" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 6 10">
                                                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 9 4-4-4-4"/>
                                                </svg>
                                                <span class="sr-only">Next</span>
                                            </span>
                                        </button>
                                    </div>
                                </div>
    
                                
                                
                            </div>

                           





                            

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

  
  