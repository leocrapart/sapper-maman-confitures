<script context="module">
    export function preload(page) {
      return {page}
    }
  </script>
  
  <script>
    export let page
    console.log(page)
  </script>
  
  <div>
   {page.params.id}
  </div>