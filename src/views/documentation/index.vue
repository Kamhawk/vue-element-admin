<template>
  <div class="app-container documentation-container">
    <a class="document-btn" target="_blank" href="https://cliniquedesvergers.ch/">Documentation interne</a>
    <a class="document-btn" target="_blank" href="https://cliniquedesvergers.ch/">Document plateforme Allmed</a>
    <a class="document-btn" target="_blank" href="https://cliniquedesvergers.ch/">Procédure de facturation</a>
    <a class="document-btn" target="_blank" href="https://cliniquedesvergers.ch/">Procédure pour soignants</a>
    <dropdown-menu class="document-btn" :items="articleList" title="Liste des articles" />
  </div>
</template>

<script>
import DropdownMenu from '@/components/Share/DropdownMenu'

export default {
  name: 'Documentation',
  components: { DropdownMenu },
  data() {
    return {
      articleList: [
        { title: 'Article 1', href: 'https://cliniquedesvergers.ch/' },
        { title: 'Article 2', href: 'https://cliniquedesvergers.ch/' },
        { title: 'Article 3', href: 'https://cliniquedesvergers.ch/' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.documentation-container {
  margin: 50px;
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;

  .document-btn {
    flex-shrink: 0;
    display: block;
    cursor: pointer;
    background: rgb(111, 174, 211);
    color: white;
    height: 60px;
    padding: 0 16px;
    margin: 16px;
    line-height: 60px;
    font-size: 20px;
    text-align: center;
  }
}
</style>
