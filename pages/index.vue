<template>
  <div>
    <GitHub />
    <b-row>
      <b-col cols="2">
        <Photo />
      </b-col>
      <b-col cols="10">
        <Logo />
      </b-col>
      <b-col cols="12">
        <BuyMeACoffee />
      </b-col>
      <b-col cols="12">
        <Subtitle />
      </b-col>
      <b-col cols="12">
        <LineBreak />
      </b-col>
      <b-col cols="12">
        <ImageLink
          name="Medium"
          href="https://charliechamp616.medium.com"
          :img="require('~/assets/medium.png')"
        />
      </b-col>
      <b-col cols="12">
        <ImageLink
          name="Lazy Texts"
          href="https://lazytexts.com"
          :img="require('~/assets/lazytexts.png')"
        />
      </b-col>
    </b-row>
  </div>
</template>
