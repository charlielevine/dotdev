<template>
  <hr />
</template>

<style>
hr {
  overflow: visible;
  height: 30px;
  border-style: solid;
  border-color: white;
  border-width: 1px 0 0 0;
  border-radius: 20px;
  margin-top: 3rem;
}
hr:before {
  display: block;
  content: '';
  height: 30px;
  margin-top: -31px;
  border-style: solid;
  border-color: white;
  border-width: 0 0 1px 0;
  border-radius: 20px;
}
</style>
