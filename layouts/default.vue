<template>
  <Head>
    <Title>Design System</Title>
    <Meta name="description" content="Design System" />
  </Head>
  <LayoutsBase>
    <template #navigation>
      <NavsNav>
        <template #logo>
          <TitresLogo>Medusa Sanctuary</TitresLogo>
        </template>

        <template #links>
          <LinksNavLink to="/">Accueil</LinksNavLink>
          <LinksNavLink to="/docs">Documentation</LinksNavLink>
        </template>
      </NavsNav>
    </template>

    <template #content>
      <slot />
    </template>

    <template #footer>
      <FootersBasic />
    </template>
  </LayoutsBase>
</template>
