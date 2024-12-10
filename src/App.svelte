<script>

    import LogoText from "./component/LogoText.svelte";
    import Image from "./component/Image.svelte";
    import Counter from "./component/Counter.svelte";
    import NumberCounter from "./component/NumberCounter.svelte";
    import Auth from "./component/Auth.svelte";
    import Todos from "./component/Todos.svelte";

  let name = 'frk'
  // 1.yöntem
  let src ='https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExZDViOWhzdnllaGJ2cDc0bWZ0dzBoN3libzBjeGRnZmNreHlodDB1dSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/UYBDCJjwOd9Re/giphy.gif'
  let alt = 'deneme'
  // 3. yöntem obje oluşturuldu
  let image= {
    src :'https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExZDViOWhzdnllaGJ2cDc0bWZ0dzBoN3libzBjeGRnZmNreHlodDB1dSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/UYBDCJjwOd9Re/giphy.gif',
    alt :'deneme',
    height: 200
  }
</script>

<main>

   <Auth/> 

   <!-- <h1>{name.toUpperCase()}</h1> -->

   <LogoText name={name}/>
   

   <Counter/>
   <br>

   <NumberCounter/>
   <br>

    <Todos/>
  <!-- 1. yöntem -->
   <!-- <img src="{src}" alt={alt} title={`bu bir ${alt}`}> -->

  <!-- 2. yöntem -->
   <!-- nitelik adı ile değer aynı ise direkt suslu parantez ile kullanılabilir -->
   <!-- <img {src} alt={alt} title={`bu bir ${alt}`}> -->

  <!-- 3. yöntem (spread ile) --> 
  <!-- <img {...image}> -->

  <Image src= {image.src} alt={image.alt} height={image.height}/>
</main>


