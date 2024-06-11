<script>
    import Nav from "$lib/components/Nav.svelte"
    import Autoplay from "embla-carousel-autoplay"
    import * as Carousel from "$lib/components/ui/carousel/index"
    import * as Card from "$lib/components/ui/card/index"
</script>

<div class="h-screen">
    <Nav />
    <div class='flex m-4 p-4 lg:justify-between sm:items-center sm:justify-center'>
        <h1 class="text-4xl text-wrap font-black lg:w-1/3 sm:w-2/3 sm:text-center">Video Editing, 3D Modelling, Drawing... I do it all</h1>
        <div class="w-1/3">
            <Carousel.Root plugins={[
                Autoplay({
                  delay: 5000,
                }),
              ]}>
                <Carousel.Content>
                  {#each Array(5) as _, i (i)}
                    <Carousel.Item>
                        <Card.Root>
                            <Card.Content>
                                <Card.Title>
                                    <h2>Title</h2>
                                </Card.Title>
                                <Card.Description>
                                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
                                </Card.Description>
                            </Card.Content>
                        </Card.Root>
                    </Carousel.Item>
                  {/each}
                </Carousel.Content>
              </Carousel.Root>
        </div>
    </div>
</div>