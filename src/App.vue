<template>
  <div id="app">
    <header>
      <h1>{{ translations[selectedLanguage].welcome }}</h1>
    </header>
    <main>
      <div class="language-selector">
        <label for="language">{{ translations[selectedLanguage].selectLanguage }}: </label>
        <select id="language" v-model="selectedLanguage">
          <option value="en">English</option>
          <option value="hi">Hindi</option>
          <option value="fr">French</option>
          <option value="es">Spanish</option>
          <option value="zh">Chinese</option>
          <option value="ru">Russian</option>
          <option value="ar">Arabic</option>
          <option value="pt">Portuguese</option>
          <option value="ja">Japanese</option>
        </select>
      </div>

      <div class="categories">
        <div class="category-card" style="background-color: #136cc7;">
          <h3>{{ translations[selectedLanguage].yogaAndPranayama }}</h3>
        </div>
        <div class="category-card" style="background-color: #e8b3d0;">
          <h3>{{ translations[selectedLanguage].mindfulnessMeditation }}</h3>
        </div>
        <div class="category-card" style="background-color: #d85b9e;">
          <h3>{{ translations[selectedLanguage].relaxationMusic }}</h3>
        </div>
        <div class="category-card" style="background-color: #32383b;">
          <h3>{{ translations[selectedLanguage].mantrasAndKirtan }}</h3>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      selectedLanguage: 'en', // Default language set to English
      translations: {
        en: {
          welcome: 'Welcome to AI-Powered EEG Driven Mental Wellness Companion App',
          selectLanguage: 'Select Language',
          yogaAndPranayama: 'Yoga and Pranayama',
          mindfulnessMeditation: 'Mindfulness Meditation',
          relaxationMusic: 'Relaxation Music',
          mantrasAndKirtan: 'Mantras and Kirtan'
        },
        hi: {
          welcome: 'एआई-पावर्ड ईईजी-ड्रिवन मानसिक कल्याण साथी ऐप में आपका स्वागत है',
          selectLanguage: 'भाषा चुनें',
          yogaAndPranayama: 'योग और प्राणायाम',
          mindfulnessMeditation: 'माइंडफुलनेस मेडिटेशन',
          relaxationMusic: 'विश्राम संगीत',
          mantrasAndKirtan: 'मंत्र और कीर्तन'
        },
        fr: {
          welcome: 'Bienvenue dans l\'application compagnon de bien-être mental alimentée par l\'IA et dirigée par l\'EEG',
          selectLanguage: 'Choisir la langue',
          yogaAndPranayama: 'Yoga et Pranayama',
          mindfulnessMeditation: 'Méditation de pleine conscience',
          relaxationMusic: 'Musique de relaxation',
          mantrasAndKirtan: 'Mantras et Kirtan'
        },
        es: {
          welcome: 'Bienvenido a la aplicación de bienestar mental impulsada por IA y EEG',
          selectLanguage: 'Seleccionar idioma',
          yogaAndPranayama: 'Yoga y Pranayama',
          mindfulnessMeditation: 'Meditación de atención plena',
          relaxationMusic: 'Música de relajación',
          mantrasAndKirtan: 'Mantras y Kirtan'
        },
        zh: {
          welcome: '欢迎使用AI驱动的EEG心理健康伴侣应用程序',
          selectLanguage: '选择语言',
          yogaAndPranayama: '瑜伽与呼吸法',
          mindfulnessMeditation: '正念冥想',
          relaxationMusic: '放松音乐',
          mantrasAndKirtan: '圣歌与赞美诗'
        },
        ru: {
          welcome: 'Добро пожаловать в ваше персонализированное Vue приложение с поддержкой ИИ и EEG для ментального благополучия',
          selectLanguage: 'Выберите язык',
          yogaAndPranayama: 'Йога и пранаяма',
          mindfulnessMeditation: 'Медитация осознанности',
          relaxationMusic: 'Музыка для расслабления',
          mantrasAndKirtan: 'Мантры и киртаны'
        },
        ar: {
          welcome: 'مرحبًا بك في تطبيق رفيق العافية العقلية المدعوم بالذكاء الاصطناعي والموجه بواسطة EEG',
          selectLanguage: 'اختار اللغة',
          yogaAndPranayama: 'اليوغا وبراناياما',
          mindfulnessMeditation: 'تأمل اليقظة',
          relaxationMusic: 'موسيقى الاسترخاء',
          mantrasAndKirtan: 'الترانيم والكيرتان'
        },
        pt: {
          welcome: 'Bem-vindo ao seu aplicativo de bem-estar mental impulsionado por IA e EEG',
          selectLanguage: 'Selecionar idioma',
          yogaAndPranayama: 'Yoga e Pranayama',
          mindfulnessMeditation: 'Meditação Mindfulness',
          relaxationMusic: 'Música Relaxante',
          mantrasAndKirtan: 'Mantras e Kirtan'
        },
        ja: {
          welcome: 'AI駆動のEEG精神的健康コンパニオンアプリへようこそ',
          selectLanguage: '言語を選択',
          yogaAndPranayama: 'ヨガとプラナヤマ',
          mindfulnessMeditation: 'マインドフルネス瞑想',
          relaxationMusic: 'リラクゼーション音楽',
          mantrasAndKirtan: 'マントラとキールタン'
        }
      }
    };
  }
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background-color: #fdfeff;
  text-align: center;
  padding: 20px;
}

.language-selector {
  margin-bottom: 30px;
}

.categories {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.category-card {
  background-color: #136cc7;
  color: white;
  padding: 20px;
  margin: 10px;
  border-radius: 8px;
  width: 20%;
  box-sizing: border-box;
}

h1 {
  color: #32383b;
}
</style>