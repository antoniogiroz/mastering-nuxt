<script lang="ts" setup>
const course = useCourse()
const route = useRoute()

const chapter = computed(() => {
  return course.chapters.find(
    chapter => chapter.slug === route.params.chapterSlug,
  )
})

const lesson = computed(() => {
  return chapter.value.lessons.find(
    lesson => lesson.slug === route.params.lessonSlug,
  )
})
</script>

<template>
  <div>
    <h2>Lesson</h2>
    <p>This is a lesson</p>
    <p>Chapter: {{ chapter.title }}</p>
    <p>Lesson: {{ lesson.title }}</p>
  </div>
</template>
