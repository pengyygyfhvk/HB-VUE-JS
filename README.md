import Vue from 'vue'
import VueI18n from 'vue-i18n'
Vue.use(VueI18n)
import zh from './zh'
import en from './en'
import jp from './jp'
import hk from './hk'
import kor from'./kor'
let locale=uni.getStorageSync('lang') || '';
if(locale==''){
	locale='en';
	uni.setStorageSync('lang',locale)
	uni.setStorageSync('locale',locale)
}
const i18n=new VueI18n({
	locale:locale,
	messages:{
		zh: zh,
		en: en,
		jp:jp,
		hk:hk
	    kor:kor
	}
})
export default i18n

{
    //多语言切换
    import VueI18n from 'vue-i18n'
    Vue.use(VueI18n)
    const i18n = new VueI18n({
    // locale: '', // 语言标识
    messages: {
    //中文
    'zh-CN': require('./common/lang/zh-CN'),
    //英文
    'en-US': require('./common/lang/en-US'),
    //同理，以下可以引多种语言
    }
    })// 注意：本文档仅支持单行注释，并且'//'前不能有任何非空字符！！！
    //
