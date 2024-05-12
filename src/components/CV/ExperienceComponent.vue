<script>
export default {
  name: 'ExperienceComponent',
  props: {
    iconSrc: String,
    date: String,
    title: String,
    employer: String,
    description: String
  }
};
</script>

<template>
  <div id="container">
    <div id="main">
      <div id="icon">
        <img :src="iconSrc" alt="Company Icon" />
      </div>
      <div id="meta-info">
        <div id="date">
          {{ date }}
        </div>
        <div id="title">
          {{ title }}
        </div>
        <div id="employer">
          {{ employer }}
        </div>
      </div>
    </div>
    <div id="description">
      {{ description }}
    </div>
  </div>
</template>

<style scoped>
#container {
  display: flex;
  flex-direction: column;
  background-color: #f8f9fa;
  border: 1px solid #dee2e6;
  border-radius: 5px;
  padding: 20px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
}

#main {
	display: flex;
	flex-direction: row;
}

#icon {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 10px;
  width: 80px;
  height: 80px;
}

#icon img {
  width: 100%;
  height: 100%
}

#meta-info {
  display: flex;
  flex-direction: column;
  padding: 5px 0;
}

#date,
#title,
#employer {
  margin: 3px 0;
  padding: 2px 0;
  font-size: 14px;
  color: #495057;
}

#title {
  font-weight: bold;
  font-size: 16px;
  color: #343a40;
}

#employer {
  font-style: italic;
  color: #6c757d;
}

#description {
  padding-top: 10px;
  font-size: 14px;
  color: #343a40;
  line-height: 1.5;
}
</style>