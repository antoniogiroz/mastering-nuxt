<template>
  <div>
    <h2>Lesson</h2>
    <p>This is a lesson</p>
    <p>Chapter: {{ $route.params.chapterSlug }}</p>
    <p>Lesson: {{ $route.params.lessonSlug }}</p>
  </div>
</template>
