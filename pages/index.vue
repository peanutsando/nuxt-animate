<template>
  <section class="container">
    <h2>CSS Animation Binding Test</h2>
    <table>
      <tbody>
        <tr>
          <th>Animation 5.0s</th>
          <th>Animation 2.0s</th>
          <th>Animation 0.8s</th>
        </tr>
        <tr v-for="a in anmiate" :key="a">
          <td v-for="d in delay" :key="d">
            <transition>
              <div class="animated" :class="[a, d]">
                <p>type: <span class="type">{{ a }}</span></p>
                <p>delay: <span class="delay">{{ d }}</span></p>
              </div>
            </transition>
          </td>
        </tr>
      </tbody>
    </table>
  </section>
</template>

<script>
export default {
  data:() => ({
    anmiate: [
      'bounce', 'flash', 'pulse', 'rubberBand', 'shake', 'headShake', 'swing', 'tada', 'wobbie', 'jello',	'bounceIn',	'bounceInDown', 'bounceInLeft',	'bounceInRight', 'bounceInUp', 'bounceOut',
      'bounceOutDown', 'bounceOutLeft', 'bounceOutRight', 'bounceOutUp', 'fadeIn', 'fadeInDown', 'fadeInDownBig', 'fadeInLeft', 'fadeInLeftBig', 'fadeInRight', 'fadeInRightBig', 'fadeInUp',
      'fadeInUpBig', 'fadeOut', 'fadeOutDown', 'fadeOutDownBig', 'fadeOutLeft', 'fadeOutLeftBig', 'fadeOutRight', 'fadeOutRightBig', 'fadeOutUp', 'fadeOutUpBig', 'flipInX', 'flipInY', 'flipOutX', 'flipOutY', 'lightSpeedIn', 'lightSpeedOut',
      'rotateIn', 'rotateInDownLeft', 'rotateInDownRight', 'rotateInUpLeft', 'rotateInUpRight', 'rotateOut', 'rotateOutDownLeft', 'rotateOutDownRight', 'rotateOutUpLeft', 'rotateOutUpRight', 'hinge', 'jackInTheBox',
      'rollIn', 'rollOut', 'zoomIn', 'zoomInDown', 'zoomInLeft', 'zoomInRight', 'zoomInUp', 'zoomOut', 'zoomOutDown', 'zoomOutLeft', 'zoomOutRight', 'zoomOutUp', 'slideInDown', 'slideInLeft', 'slideInRight', 'slideInUp',
      'slideOutDown', 'slideOutLeft', 'slideOutRight', 'slideOutUp', 'heartBeat'
    ],
    delay: [ 'slow', 'normal', 'fast' ]
  }),
}
</script>

<style lang='scss' scoped>
.container {
  overflow-x: hidden;
  h2 {
    margin: 24px auto;
    text-align: center;
  }

  table {
    max-width: 720px;
    margin: auto;
    th {
      padding: 10px;
      font-size: 24px;
    }
    td {
      text-align: center;
      padding: 16px;
      font-size: 18px;
      .slow {
        animation-duration: 5s;
      }

      .normal {
        animation-duration: 2s;
      }

      .fast {
        animation-duration: 0.8s;
      }
      span {
        font-weight: bold;
      }
      .type {
        color: palevioletred;
      }
      .delay {
        color: plum
      }
    }
  }
}

</style>
