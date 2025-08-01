<template>
  <div class="main-class">
    <div class="question-partition">
      <div class="teams">
        <div @click="fadeOthers($event)">الاخضر</div>
        <div @click="fadeOthers($event)">الاحمر</div>
        <div @click="fadeOthers($event)">الازرق</div>
        <div @click="fadeOthers($event)">الاصفر</div>

      </div>
      <div class="categories" v-if="alakhdar">
        <div class="text" v-bind:class="{ fade: categories['الاخضر'][1] }" @click="toggleCategory('الاخضر', 1)">طقس</div>
        <div class="text" v-bind:class="{ fade: categories['الاخضر'][2] }" @click="toggleCategory('الاخضر', 2)">الحان </div>
        <div class="text" v-bind:class="{ fade: categories['الاخضر'][3] }" @click="toggleCategory('الاخضر', 3)">فوازير</div>
        <div class="text" v-bind:class="{ fade: categories['الاخضر'][4] }" @click="toggleCategory('الاخضر', 4)">طلبات </div>
        <div class="text" v-bind:class="{ fade: categories['الاخضر'][5] }" @click="toggleCategory('الاخضر', 5)">معلومات رياضية 2</div>
        <div class="text" v-bind:class="{ fade: categories['الاخضر'][6] }" @click="toggleCategory('الاخضر', 6)">معلومات رياضية 1</div>
        <div class="text" v-bind:class="{ fade: categories['الاخضر'][7] }" @click="toggleCategory('الاخضر', 7)">معلومات عامة 2</div>
        <div class="text" v-bind:class="{ fade: categories['الاخضر'][8] }" @click="toggleCategory('الاخضر', 8)">معلومات عامة 1</div>
        <div class="text" v-bind:class="{ fade: categories['الاخضر'][9] }" @click="toggleCategory('الاخضر', 9)">2 معلومات دينية</div>
        <div class="text" v-bind:class="{ fade: categories['الاخضر'][10] }" @click="toggleCategory('الاخضر', 10)"> معلومات دينية 1</div>

      </div>
      <div class="categories" v-else-if="alahmar">
        <div class="text" v-bind:class="{ fade: categories['الاحمر'][1] }" @click="toggleCategory('الاحمر', 1)">طقس</div>
        <div class="text" v-bind:class="{ fade: categories['الاحمر'][2] }" @click="toggleCategory('الاحمر', 2)">الحان </div>
        <div class="text" v-bind:class="{ fade: categories['الاحمر'][3] }" @click="toggleCategory('الاحمر', 3)">فوازير</div>
        <div class="text" v-bind:class="{ fade: categories['الاحمر'][4] }" @click="toggleCategory('الاحمر', 4)">طلبات </div>
        <div class="text" v-bind:class="{ fade: categories['الاحمر'][5] }" @click="toggleCategory('الاحمر', 5)">معلومات رياضية 2</div>
        <div class="text" v-bind:class="{ fade: categories['الاحمر'][6] }" @click="toggleCategory('الاحمر', 6)">معلومات رياضية 1</div>
        <div class="text" v-bind:class="{ fade: categories['الاحمر'][7] }" @click="toggleCategory('الاحمر', 7)">معلومات عامة 2</div>
        <div class="text" v-bind:class="{ fade: categories['الاحمر'][8] }" @click="toggleCategory('الاحمر', 8)">معلومات عامة 1</div>
        <div class="text" v-bind:class="{ fade: categories['الاحمر'][9] }" @click="toggleCategory('الاحمر', 9)">2 معلومات دينية</div>
        <div class="text" v-bind:class="{ fade: categories['الاحمر'][10] }" @click="toggleCategory('الاحمر', 10)"> معلومات دينية 1</div>

      </div>
      <div class="categories" v-if="alazraa">
        <div class="text" v-bind:class="{ fade: categories['الازرق'][1] }" @click="toggleCategory('الازرق', 1)">طقس</div>
        <div class="text" v-bind:class="{ fade: categories['الازرق'][2] }" @click="toggleCategory('الازرق', 2)">الحان </div>
        <div class="text" v-bind:class="{ fade: categories['الازرق'][3] }" @click="toggleCategory('الازرق', 3)">فوازير</div>
        <div class="text" v-bind:class="{ fade: categories['الازرق'][4] }" @click="toggleCategory('الازرق', 4)">طلبات </div>
        <div class="text" v-bind:class="{ fade: categories['الازرق'][5] }" @click="toggleCategory('الازرق', 5)">معلومات رياضية 2</div>
        <div class="text" v-bind:class="{ fade: categories['الازرق'][6] }" @click="toggleCategory('الازرق', 6)">معلومات رياضية 1</div>
        <div class="text" v-bind:class="{ fade: categories['الازرق'][7] }" @click="toggleCategory('الازرق', 7)">معلومات عامة 2</div>
        <div class="text" v-bind:class="{ fade: categories['الازرق'][8] }" @click="toggleCategory('الازرق', 8)">معلومات عامة 1</div>
        <div class="text" v-bind:class="{ fade: categories['الازرق'][9] }" @click="toggleCategory('الازرق', 9)">2 معلومات دينية</div>
        <div class="text" v-bind:class="{ fade: categories['الازرق'][10] }" @click="toggleCategory('الازرق', 10)"> معلومات دينية 1</div>
</div>
      <div class="categories" v-if="alasfar">
        <div class="text" v-bind:class="{ fade: categories['الاصفر'][1] }" @click="toggleCategory('الاصفر', 1)">طقس</div>
        <div class="text" v-bind:class="{ fade: categories['الاصفر'][2] }" @click="toggleCategory('الاصفر', 2)">الحان </div>
        <div class="text" v-bind:class="{ fade: categories['الاصفر'][3] }" @click="toggleCategory('الاصفر', 3)">فوازير</div>
        <div class="text" v-bind:class="{ fade: categories['الاصفر'][4] }" @click="toggleCategory('الاصفر', 4)">طلبات </div>
        <div class="text" v-bind:class="{ fade: categories['الاصفر'][5] }" @click="toggleCategory('الاصفر', 5)">معلومات رياضية 2</div>
        <div class="text" v-bind:class="{ fade: categories['الاصفر'][6] }" @click="toggleCategory('الاصفر', 6)">معلومات رياضية 1</div>
        <div class="text" v-bind:class="{ fade: categories['الاصفر'][7] }" @click="toggleCategory('الاصفر', 7)">معلومات عامة 2</div>
        <div class="text" v-bind:class="{ fade: categories['الاصفر'][8] }" @click="toggleCategory('الاصفر', 8)">معلومات عامة 1</div>
        <div class="text" v-bind:class="{ fade: categories['الاصفر'][9] }" @click="toggleCategory('الاصفر', 9)">2 معلومات دينية</div>
        <div class="text" v-bind:class="{ fade: categories['الاصفر'][10] }" @click="toggleCategory('الاصفر', 10)"> معلومات دينية 1</div>
</div>
    </div>
         <div class="scores-partition">
      <div class="outer-space"></div>
      <div class="car-container">
        <div style="color: white; font-weight: bold"> الاخضر </div>
        <br>
        <div @click="open1" class="jumping-object1" :style="{ width: objectWidth + 'px', height: objectWidth + 'px', bottom: correctAnswers1 === totalScores ? maxHeight + 'px' : step * correctAnswers1 + 'px' }">
          <div class="score-display">{{ correctAnswers1 }}</div>
        </div>
      </div>
      <div class="double-space"></div>
      <div class="car-container">
        <div style="color: white; font-weight: bold">الاحمر </div>
        <br>
        <div @click="open2" class="jumping-object2" :style="{ width: objectWidth + 'px', height: objectWidth + 'px', bottom: correctAnswers2 === totalScores ? maxHeight + 'px' : step * correctAnswers2 + 'px' }">
          <div class="score-display">{{ correctAnswers2 }}</div>
        </div>
      </div>
      <div class="double-space"></div>
      <div class="car-container">
        <div style="color: white; font-weight: bold"> الازرق </div>
        <br>
        <div @click="open3" class="jumping-object3" :style="{ width: objectWidth + 'px', height: objectWidth + 'px', bottom: correctAnswers3 === totalScores ? maxHeight + 'px' : step * correctAnswers3 + 'px' }">
          <div class="score-display">{{ correctAnswers3 }}</div>
        </div>
      </div>
      <div class="double-space"></div>
      <div class="car-container">
        <div style="color: white; font-weight: bold"> الاصفر</div>
        <br>
        <div @click="open4" class="jumping-object4" :style="{ width: objectWidth + 'px', height: objectWidth + 'px', bottom: correctAnswers4 === totalScores ? maxHeight + 'px' : step * correctAnswers4 + 'px' }">
          <div class="score-display">{{ correctAnswers4 }}</div>
        </div>
      </div>
      <div class="outer-space"></div>
    </div>
  </div>
</template>

<script>
import swal from 'sweetalert2';
export default {
  name: 'Quiz',
  props: {
    msg: String
  },
  data() {
    return {
      alakhdar: false,
      alazraa: false,
      alahmar: false,
      alasfar: false,
      categories: {
        'الاخضر': {1: false, 2: false, 3: false, 4: false, 5: false, 6: false, 7: false, 8: false, 9: false, 10: false },
        'الاحمر': {1: false, 2: false, 3: false, 4: false, 5: false, 6: false, 7: false, 8: false, 9: false, 10: false },
        'الازرق': {1: false, 2: false, 3: false, 4: false, 5: false, 6: false, 7: false, 8: false, 9: false, 10: false },
        'الاصفر': {1: false, 2: false, 3: false, 4: false, 5: false, 6: false, 7: false, 8: false, 9: false, 10: false },
      },
      correctAnswers1: 0,
      correctAnswers2: 0,
      correctAnswers3: 0,
      correctAnswers4: 0,
      totalScores: 11, // number of points + 1
      maxHeight: 0,
      Questions: {
       'الاخضر': {
          1: {
            question: `<span>السيد المسيح قعد كام يوم في القبر؟</span><br><span>(2 - 3 - 4)</span>`,
            answer: '3'
          },
          2: {
            question: 'كنت واقف تحت بابا يسوع وكانت معايا ماما العدرا',
            answer: 'يوحنا الحبيب'
          },
          3: {
            question: 'قابلت المسيح وكنت فاكراه البستاني؟',
            answer: 'مريم المجدلية'
          },
          4: {
            question: 'مكنتش مصدق ان المسيح قام والسيد المسيح خلاني اشوف أماكن المسامير؟',
            answer: 'توما'
          },
          5: {
            question: `<span>بنصلي قداس القيامة بالطقس</span><br><span>(الفرايحي -الحزايني - السنوي)</span>`,
            answer: 'الفرايحي'
          },
          6: {
            question: 'مين التلميذين اللي جريوا على القبر ولقوا القبر فاضي؟',
            answer: 'بطرس و يوحنا'
          },
          7: {
            question: 'قابلت المسيح وكنت فاكراه البستاني؟',
            answer: 'مريم المجدلية'
          },
          8: {
            question: 'مكنتش مصدق ان المسيح قام والسيد المسيح خلاني اشوف أماكن المسامير؟',
            answer: 'توما'
          },
          9: {
            question: `<span>بنصلي قداس القيامة بالطقس</span><br><span>(الفرايحي -الحزايني - السنوي)</span>`,
            answer: 'الفرايحي'
          },
          10: {
            question: 'مين التلميذين اللي جريوا على القبر ولقوا القبر فاضي؟',
            answer: 'بطرس و يوحنا'
          }
        },
        'الاحمر': {
          1: {
            question: 'كم عدد التلاميذ الذين كانوا يصلون في العلية بعد القيامة عندما ظهر لهم الرب يسوع ؟',
            answer: '10'
          },
          2: {
            question: 'احد القيامة هو الاحد الكام ؟',
            answer: 'الثامن'
          },
          3: {
            question: 'المريمات هما اللي دحرجوا الحجر',
            answer: 'غلط'
          },
          4: {
            question: 'مين من التلاميذ خان المسيح ؟',
            answer: 'يهوذا الاسخريوطي'
          },
          5: {
            question: 'مين من التلاميذ انكر المسيح ؟',
            answer: 'بطرس'
          },
          6: {
            question: 'مين كان موجود تحت الصليب ؟',
            answer: 'ماما العدرا و يوحنا الحبيب'
          },
          7: {
            question: 'قابلت المسيح وكنت فاكراه البستاني؟',
            answer: 'مريم المجدلية'
          },
          8: {
            question: 'مكنتش مصدق ان المسيح قام والسيد المسيح خلاني اشوف أماكن المسامير؟',
            answer: 'توما'
          },
          9: {
            question: `<span>بنصلي قداس القيامة بالطقس</span><br><span>(الفرايحي -الحزايني - السنوي)</span>`,
            answer: 'الفرايحي'
          },
          10: {
            question: 'مين التلميذين اللي جريوا على القبر ولقوا القبر فاضي؟',
            answer: 'بطرس و يوحنا'
          }
        },
         'الازرق': {
          1: {
            question: `<span>مين اول حد راح لقبر بابا يسوع يوم الحد الفجر</span><br><span>(مريم المجدلية - يوحنا - بطرس)</span>`,
            answer: 'مريم المجدلية'
          },
          2: {
            question: `<span>بنفضل نحتفل بقيامة ربنا يسوع كام يوم</span><br><span>(1 - 40 - 50 - 55)</span>`,
            answer: '50'
          },
          3: {
            question: `<span>مين دحرج الحجر لما المريمات راحوا القبر</span><br><span>البستاني - بطرس - الحراس - الحجر كان متدحرج قبل ما يوصلوا</span>`,
            answer: 'الحجر كان متدحرج قبل ما يوصلوا'
          },
          4: {
            question: `<span>ايه الحاجة الوحيدة اللي بنعملها زيادة في قداس احد القيامة و فترة الخماسين و مبنعملهاش في القداسات العاديه</span><br><span>(الزفة - لبس التونية - التناول)</span>`,
            answer: 'الزفة'
          },
          5: {
            question: `<span>مريم المجدلية قالت ايه لما بابا يسوع نداها في البستان</span><br><span>(ربوني - القبر فاضي - اين البستاني)</span>`,
            answer: 'ربوني'
          },
          6: {
            question: `<span>ايه الرقم اللي مش مكتوب على ولا ورقة فلوس في مصر</span><br><span>(5 - 20 - 30 - 50)</span>`,
            answer: '30'
          },
          7: {
            question: 'قابلت المسيح وكنت فاكراه البستاني؟',
            answer: 'مريم المجدلية'
          },
          8: {
            question: 'مكنتش مصدق ان المسيح قام والسيد المسيح خلاني اشوف أماكن المسامير؟',
            answer: 'توما'
          },
          9: {
            question: `<span>بنصلي قداس القيامة بالطقس</span><br><span>(الفرايحي -الحزايني - السنوي)</span>`,
            answer: 'الفرايحي'
          },
          10: {
            question: 'مين التلميذين اللي جريوا على القبر ولقوا القبر فاضي؟',
            answer: 'بطرس و يوحنا'
          }
        },
         'الاصفر': {
          1: {
            question: 'انا من الرامة و كنت غني جدا و قعد المسيح في ممتلكاتي 3 ايام',
            answer: 'يوسف الرامي'
          },
          2: {
            question: 'كنت مجرم مسجون و هتف الشعب بأسمي و في الاخر المسيح اخد مكاني',
            answer: 'باراباس'
          },
          3: {
            question: 'ما الذي يفعله أبونا في القداس يشير الى دحرجة الحجر عن القبر؟',
            answer: 'رفع الابروسفارين'
          },
          4: {
            question: 'نقول في الهيتنيات ان مبوق القيامة هو اول من أعلن عن قيامة المسيح فمن هو؟',
            answer: 'الملاك ميخائيل'
          },
          5: {
            question: ' قصة في سفر الخروج بتشير الى صلب المسيح ـــــ و اتاخد منها تسمية بصخة اللي معناها ـــــ',
            answer: 'خروف الفصح - عبور'
          },
          6: {
            question: 'من أي ماده يتم تصنيع الزجاج',
            answer: 'الرمال'
          },
          7: {
            question: 'قابلت المسيح وكنت فاكراه البستاني؟',
            answer: 'مريم المجدلية'
          },
          8: {
            question: 'مكنتش مصدق ان المسيح قام والسيد المسيح خلاني اشوف أماكن المسامير؟',
            answer: 'توما'
          },
          9: {
            question: `<span>بنصلي قداس القيامة بالطقس</span><br><span>(الفرايحي -الحزايني - السنوي)</span>`,
            answer: 'الفرايحي'
          },
          10: {
            question: 'مين التلميذين اللي جريوا على القبر ولقوا القبر فاضي؟',
            answer: 'بطرس و يوحنا'
          }
        }
      }
      
    }
  },
  created() {
    this.maxHeight = window.innerHeight - 5;
  },
  computed: {
    step() {
      return this.maxHeight / this.totalScores;
    },
    objectWidth() {
      return 0.06 * window.innerWidth;
    },
  },
  methods: {
    toggleCategory(team, index) {
 let q = this.Questions[team][index].question;
    let ans = this.Questions[team][index].answer;
    swal.fire({
      width: '800px',
      height: '500px',
      title: `<span style="font-size: 50px; font-weight: bold">${q}</span>`,
      confirmButtonText: "الاجابة",
    }).then((result) => {
      if (result.isConfirmed) {
        swal.fire({
          title: `<span style="font-size: 50px; font-weight: bold">${ans}</span>`,
          showDenyButton: true,
          showCancelButton: true,
          confirmButtonText: `<span style="font-size: 30px; font-weight: bold; color: white;">صح ✓</span>`,
          denyButtonText: `<span style="font-size: 30px; font-weight: bold; color: white;">غلط ✗</span>`,
          cancelButtonText: `<span style="font-size: 20px; font-weight: bold;">إلغاء</span>`,
          confirmButtonColor: '#28a745',
          denyButtonColor: '#dc3545',
          cancelButtonColor: '#6c757d'
        }).then((answerResult) => {
          if (answerResult.isConfirmed) {
            // Green button clicked - correct answer
            this.addScore(team);
            this.Winner();
          } else if (answerResult.isDenied) {
            // Red button clicked - wrong answer
            this.Loser();
          }
          // If cancel is clicked, do nothing
        });
      }
    });
    this.categories[team][index] = true;
    const categoryDiv = document.querySelector('.categories > *:nth-child(' + index + ')');
    if (this.categories[team][index]) {
      categoryDiv.classList.add('fade');
    }
  },
  addScore(team) {
    switch(team) {
      case 'الاخضر':
        if (this.correctAnswers1 < this.totalScores - 1) {
          this.correctAnswers1++;
          const jumpingObject = document.querySelector('.jumping-object1');
          jumpingObject.classList.remove('jump');
          void jumpingObject.offsetWidth;
          jumpingObject.classList.add('jump');
        }
        break;
      case 'الاحمر':
        if (this.correctAnswers2 < this.totalScores - 1) {
          this.correctAnswers2++;
          const jumpingObject = document.querySelector('.jumping-object2');
          jumpingObject.classList.remove('jump');
          void jumpingObject.offsetWidth;
          jumpingObject.classList.add('jump');
        }
        break;
      case 'الازرق':
        if (this.correctAnswers3 < this.totalScores - 1) {
          this.correctAnswers3++;
          const jumpingObject = document.querySelector('.jumping-object3');
          jumpingObject.classList.remove('jump');
          void jumpingObject.offsetWidth;
          jumpingObject.classList.add('jump');
        }
        break;
      case 'الاصفر':
        if (this.correctAnswers4 < this.totalScores - 1) {
          this.correctAnswers4++;
          const jumpingObject = document.querySelector('.jumping-object4');
          jumpingObject.classList.remove('jump');
          void jumpingObject.offsetWidth;
          jumpingObject.classList.add('jump');
        }
        break;
    }
  },
    fadeOthers(event) {
      const teamsDiv = document.querySelector('.teams');
      const children = teamsDiv.children;
      for (let i = 0; i < children.length; i++) {
        if (children[i] !== event.target) {
          children[i].classList.add('fade');
        } else {
          children[i].classList.remove('fade');
        }
      }
      this.alahmar = false;
      this.alakhdar = false;
      this.alasfar = false;
      this.alazraa = false;
      if (event.target.textContent === 'الاخضر') {
        this.alakhdar = true;
      } else if (event.target.textContent === 'الاحمر') {
        this.alahmar = true;
      } else if (event.target.textContent === 'الازرق') {
        this.alazraa = true;
      } else if (event.target.textContent === 'الاصفر') {
        this.alasfar = true;
      }
    },
    Winner(){
      var audio = new Audio("https://audio.code.org/goal1.mp3");
      audio.play();
    },
    Loser(){
      var audio = new Audio("https://audio.code.org/losepoint2.mp3");
      audio.play();
    },
    open1(){
      swal.fire({
        title: "الاخضر",
        showDenyButton: true,
        showCancelButton: false,
        confirmButtonText: `<span style="font-size: 30px; font-weight: bold">&#43;</span>`,
        denyButtonText: `<span style="font-size: 30px; font-weight: bold">&#8722;</span>`,
      }).then((result) => {
        if (result.isConfirmed) {
          this.answerQuestion1(true);
          this.Winner();
        } else if (result.isDenied) {
          this.decreaseAnswer1();
          this.Loser();
        }
      });
    },
    open2(){
      swal.fire({
        title: "الاحمر",
        showDenyButton: true,
        showCancelButton: false,
        confirmButtonText: `<span style="font-size: 30px; font-weight: bold">&#43;</span>`,
        denyButtonText: `<span style="font-size: 30px; font-weight: bold">&#8722;</span>`,
      }).then((result) => {
        if (result.isConfirmed) {
          this.answerQuestion2(true);
          this.Winner();
        } else if (result.isDenied) {
          this.decreaseAnswer2();
          this.Loser();
        }
      });
    },
    open3(){
      swal.fire({
        title: "الازرق",
        showDenyButton: true,
        showCancelButton: false,
        confirmButtonText: `<span style="font-size: 30px; font-weight: bold">&#43;</span>`,
        denyButtonText: `<span style="font-size: 30px; font-weight: bold">&#8722;</span>`,
      }).then((result) => {
        if (result.isConfirmed) {
          this.answerQuestion3(true);
          this.Winner();
        } else if (result.isDenied) {
          this.decreaseAnswer3();
          this.Loser();
        }
      });
    },
    open4(){
      swal.fire({
        title: "الاصفر",
        showDenyButton: true,
        showCancelButton: false,
        confirmButtonText: `<span style="font-size: 30px; font-weight: bold">&#43;</span>`,
        denyButtonText: `<span style="font-size: 30px; font-weight: bold">&#8722;</span>`,
      }).then((result) => {
        if (result.isConfirmed) {
          this.answerQuestion4(true);
          this.Winner();
        } else if (result.isDenied) {
          this.decreaseAnswer4();
          this.Loser();
        }
      });
    },
    answerQuestion1(isCorrect) {
      if (isCorrect) {
        if (this.correctAnswers1=== this.totalScores - 1) {
          return;
        }
        this.correctAnswers1++;
        const jumpingObject = document.querySelector('.jumping-object1');
        jumpingObject.classList.remove('jump');
        void jumpingObject.offsetWidth;
        jumpingObject.classList.add('jump');
      }
    },
    decreaseAnswer1() {
      if (this.correctAnswers1 > 0) {
        this.correctAnswers1--;
        const jumpingObject = document.querySelector('.jumping-object1');
        jumpingObject.classList.remove('jump');
        void jumpingObject.offsetWidth;
        jumpingObject.classList.add('jump');
      }
    },
    answerQuestion2(isCorrect) {
      if (isCorrect) {
        if (this.correctAnswers2 === this.totalScores - 1) {
          return;
        }
        this.correctAnswers2++;
        const jumpingObject = document.querySelector('.jumping-object2');
        jumpingObject.classList.remove('jump');
        void jumpingObject.offsetWidth;
        jumpingObject.classList.add('jump');
      }
    },
    decreaseAnswer2() {
      if (this.correctAnswers2 > 0) {
        this.correctAnswers2--;
        const jumpingObject = document.querySelector('.jumping-object2');
        jumpingObject.classList.remove('jump');
        void jumpingObject.offsetWidth;
        jumpingObject.classList.add('jump');
      }
    },
    answerQuestion3(isCorrect) {
      if (isCorrect) {
        if (this.correctAnswers3 === this.totalScores - 1) {
          return;
        }
        this.correctAnswers3++;
        const jumpingObject = document.querySelector('.jumping-object3');
        jumpingObject.classList.remove('jump');
        void jumpingObject.offsetWidth;
        jumpingObject.classList.add('jump');
      }
    },
    decreaseAnswer3() {
      if (this.correctAnswers3 > 0) {
        this.correctAnswers3--;
        const jumpingObject = document.querySelector('.jumping-object3');
        jumpingObject.classList.remove('jump');
        void jumpingObject.offsetWidth;
        jumpingObject.classList.add('jump');
      }
    },
    answerQuestion4(isCorrect) {
      if (isCorrect) {
        if (this.correctAnswers4 === this.totalScores - 1) {
          return;
        }
        this.correctAnswers4++;
        const jumpingObject = document.querySelector('.jumping-object4');
        jumpingObject.classList.remove('jump');
        void jumpingObject.offsetWidth;
        jumpingObject.classList.add('jump');
      }
    },
    decreaseAnswer4() {
      if (this.correctAnswers4 > 0) {
        this.correctAnswers4--;
        const jumpingObject = document.querySelector('.jumping-object4');
        jumpingObject.classList.remove('jump');
        void jumpingObject.offsetWidth;
        jumpingObject.classList.add('jump');
      }
    },
  }
}
</script>

<style scoped>
div img {
  max-width: 100%;
  max-height: 100%;
}
.text{
  display: flex;
  align-items: center;
  justify-content: center;
}
.main-class {
  display: flex;
  justify-content: space-around;
  width: 99%;
}

.question-partition {
  flex: 0 0 63%;
  display: flex;
  justify-content: space-around;
  flex-direction: column;

}
.teams{
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  font-weight: bold;
}
.teams :nth-child(1){
  padding: 2.5%;
  background: rgba(9, 106, 10, 0.74);
  backdrop-filter: blur();
  color: rgb(0, 0, 0);
  border-radius: 20px;
  font-size: 210%;
}

.teams :nth-child(2){
  padding: 2.5%;
  background: rgba(150, 7, 7, 0.74);
  backdrop-filter: blur();
  color: rgb(0, 0, 0);
  border-radius: 20px;
  font-size: 210%;
}

.teams :nth-child(3){
  padding: 2.5%;
  background: rgba(12, 94, 165, 0.74);
  backdrop-filter: blur();
  color: rgb(0, 0, 0);
  border-radius: 20px;
  font-size: 210%;
}

.teams :nth-child(4){
  padding: 2.5%;
  background: rgba(255, 221, 3, 0.74);
  backdrop-filter: blur();
  color: rgb(0, 0, 0);
  border-radius: 20px;
  font-size: 210%;
}

.teams :hover{
  cursor: pointer;
  transform: scale(1.15);
}

.categories{
  flex: 0 0 70%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around
}

.categories > * {
  flex: 1 0 150pt;
  height: 150pt;
  padding: 2.5%;
  background: rgba(0, 0, 0, 0.74);
  backdrop-filter: blur();
  color: white;
  border-radius: 20px;
  font-size: 200%;
  margin: 1%;
  text-align: center;
  font-weight: bold;

}
.categories :hover{
  cursor: pointer;
}

.score-display {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: white;
  color: black;
  font-weight: bold;
  font-size: 24px;
  padding: 5px 10px;
  border-radius: 10px;
  min-width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 3px solid black;
}

.scores-partition {
    flex: 0 0 35%;
  display: flex;
  align-items: flex-end;
  height: 98vh;
  background: #292525;
  background: url(road.png) repeat;
  background-size: calc(100% / 5);
}

.outer-space {
  flex: 5
}

.double-space {
  flex: 1;
}

.car-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-end;
  flex: 0 0 auto;
}

.jumping-object1{
  position: relative;
  background: url(car3.png);
  transition: bottom 1s ease-in-out;
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}
.jumping-object2{
  position: relative;
  background: url(car1.png);
  transition: bottom 1s ease-in-out;
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}
.jumping-object3{
  position: relative;
  background: url(car2.png);
  transition: bottom 1s ease-in-out;
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}

.jumping-object4{
  position: relative;
  background: url(car6.png);
  transition: bottom 1s ease-in-out;
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}

.jumping-object4:hover{
  cursor: pointer;
}
.jumping-object3:hover{
  cursor: pointer;
}
.jumping-object2:hover{
  cursor: pointer;
}
.jumping-object1:hover{
  cursor: pointer;
}
.fade {
  opacity: 0.5;
  transition: opacity 0.5s ease;
}
</style>


