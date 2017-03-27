##jq etalage 图片轮播放大
###使用
```
  <link rel="stylesheet" href="etalage.css">
  <script src="http://apps.bdimg.com/libs/jquery/2.1.1/jquery.min.js"></script>
  <script src="jquery.etalage.min.js"></script>
  ```
###html
```
  <ul id="etalage" class="etalage">
      <li>
          <img class="etalage_thumb_image" src="images/image1_thumb.jpg" /><!--这里的src放的是略缩图 -->
          <img class="etalage_source_image" src="images/image1_large.jpg" title="这里放本图片的描述" />                             <!--第二行img的src是第一行图片的放大图，也就是放大镜显示出来的部分 -->
      </li>
      <li>
          <img class="etalage_thumb_image" src="images/image2_thumb.jpg" />
          <img class="etalage_source_image" src="images/image2_large.jpg" title="这个图片的描述也可以放在图片顶部<br>而且中间还可以换行" />
      </li>
      <li>
          <img class="etalage_thumb_image" src="images/image3_thumb.jpg" />
          <img class="etalage_source_image" src="images/image3_large.jpg" />
      </li>
      <li>
          <img class="etalage_thumb_image" src="images/image4_thumb.jpg" />
          <img class="etalage_source_image" src="images/image4_large.jpg" />
      </li>
      <li>
          <img class="etalage_thumb_image" src="images/image_thumb.jpg" />
          <img class="etalage_source_image" src="images/image_large.jpg" />
      </li>
  </ul>
  ```
  
###js
```
  <script>
      $('#etalage').etalage({
          thumb_image_width: 500,
          thumb_image_height: 334,
          source_image_width: 1000,
          source_image_height: 900,
          zoom_area_width: 500,//放大镜的大小
          zoom_area_height: 500,//放大镜的高度
          zoom_area_distance: 5,//大图显示的位置
          small_thumbs: 4,//略缩图的个数
          smallthumb_inactive_opacity: 0.3,//没有放大镜部分的透明度
          smallthumbs_position: 'bottom',//略缩图的位置，本例是在左边从上到下排列，默认是在底部从左到右排列
          show_icon: false,
          autoplay: true,//是否自动轮播，默认是true，也就是默认是自动
          keyboard: false,
          zoom_easing: true//淡入淡出效果
      });
  </script>
  ```
###跳页
  方法名与id对应
  
  ```
  <button onclick="etalage_previous()">Previous image</button>
  <button onclick="etalage_next()">Next image</button>
  <button onclick="etalage_show(1)">Show image 1</button>
  <button onclick="etalage_show(4)">Show image 4</button>
   ```
