# NuxtLink v-for typing issue

Simple reproduction to demonstrate typing items in a v-for spread with the `<NuxtLink>` component.

## Steps

1. Install dependencies
2. Run `nuxt typecheck`

The check will report two type errors related to the `sites` variable used within a v-for context, but not for the same usage in a `<p>` element