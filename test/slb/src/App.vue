


 <template>
  <ClientOnly>
    <CardContainer>
      <CardBody
        class="group/card relative size-auto rounded-xl border border-black/[0.1] bg-gray-50 p-6 sm:w-[30rem] dark:border-white/[0.2] dark:bg-black dark:hover:shadow-2xl dark:hover:shadow-emerald-500/[0.1]"
      >
        <CardItem
          :translate-z="50"
          class="text-xl font-bold text-neutral-600 dark:text-white"
        >
          Make things float in air
        </CardItem>
        <CardItem
          as="p"
          translate-z="60"
          class="mt-2 max-w-sm text-sm text-neutral-500 dark:text-neutral-300"
        >
          Hover over this card to unleash the power of CSS perspective
        </CardItem>
        <CardItem
          :translate-z="100"
          class="mt-4 w-full"
        >
          <img
            src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?q=80&w=2560&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
            height="1000"
            width="1000"
            class="h-60 w-full rounded-xl object-cover group-hover/card:shadow-xl"
            alt="thumbnail"
          />
        </CardItem>
        <div class="mt-20 flex items-center justify-between">
          <CardItem
            :translate-z="20"
            as="a"
            href="https://rahulv.dev"
            target="__blank"
            class="rounded-xl px-4 py-2 text-xs font-normal dark:text-white"
          >
            Visit →
          </CardItem>
          <CardItem
            :translate-z="20"
            as="button"
            class="rounded-xl bg-black px-4 py-2 text-xs font-bold text-white dark:bg-white dark:text-black"
          >
            Get Started
          </CardItem>
        </div>
      </CardBody>
    </CardContainer>
  </ClientOnly>
</template>

<script setup lang="ts">
import { CardContainer, CardBody, CardItem } from "@/components/ui/card-3d";
</script>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
