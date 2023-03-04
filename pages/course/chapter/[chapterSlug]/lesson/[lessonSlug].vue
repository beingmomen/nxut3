<template>
  <div>
    <p>Lesson {{ chapter.number }} - {{ lesson.number }}</p>
    <h2>{{ lesson.title }}</h2>

    <div class="flex space-x-4 mt-2 mb-8">
      <a
        v-if="lesson.sourceUrl"
        class="font-normal text-md text-gray-500"
        :href="lesson.sourceUrl"
      >
        Download source code
      </a>
      <a
        v-if="lesson.downloadUrl"
        class="font-normal text-md text-gray-500"
        :href="lesson.downloadUrl"
      >
        Download Video
      </a>
    </div>
    <VideoPlayer v-if="lesson.videoId" :video-id="lesson.videoId" />
    <p>{{ lesson.text }}</p>
  </div>
</template>

<script setup>
const course = useCourse();
const route = useRoute();

const chapter = computed(() => {
  return course.chapters.find(
    (chapter) => chapter.slug == route.params.chapterSlug
  );
});

const lesson = computed(() => {
  return chapter.value.lessons.find(
    (lesson) => lesson.slug === route.params.lessonSlug
  );
});
</script>

<style lang="scss" scoped>
</style>