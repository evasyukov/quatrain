<template>
  <div class="quatrain">
    <div class="quatrain-list"
      v-for="index in 4"
      :key="index"
      :class="{ hidden: !visibleStanzas[index - 1] }"
    >
      <div v-if="index === 1">
        <p>Out of the night that covers me,</p>
        <p>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Black as the pit from pole to
          pole,
        </p>
        <p>I thank whatever gods may be</p>
        <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;For my unconquerable soul.</p>
      </div>
      <div v-if="index === 2">
        <p>In the fell clutch of circumstance</p>
        <p>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I have not winced nor cried aloud.
        </p>
        <p>Under the bludgeonings of chance</p>
        <p>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;My head is bloody, but unbowed.
        </p>
      </div>
      <div v-if="index === 3">
        <p>Beyond this place of wrath and tears</p>
        <p>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Looms but the Horror of the
          shade,
        </p>
        <p>And yet the menace of the years</p>
        <p>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Finds and shall find me unafraid.
        </p>
      </div>
      <div v-if="index === 4">
        <p>It matters not how strait the gate,</p>
        <p>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; How charged with punishments the
          scroll,
        </p>
        <p>I am the master of my fate</p>
        <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I am the captain of my soul.</p>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  props: {
    visibleStanzas: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style>
.quatrain {
  font-size: 24px;
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
  min-width: 500px;

  & p {
    margin: 0;
  }

  & div {
    margin-bottom: 20px;
  }
}
.quatrain-list:nth-child(1){
  background-color: rgba(94, 202, 52, 0.274);
}
.quatrain-list:nth-child(2){
  background-color: rgba(160, 110, 110, 0.601);
}
.quatrain-list:nth-child(3){
  background-color: rgba(98, 102, 161, 0.417);
}
.quatrain-list:nth-child(4){
  background-color: rgba(180, 78, 156, 0.419);
}
.hidden {
  display: none;
}
</style>
