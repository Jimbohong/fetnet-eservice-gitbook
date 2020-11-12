# other

## AddValueSection

```
import AddValueSection from '../../components/partials/AddValueSection'
<AddValueSection
  id="addValue"
  h1="你想找什麼樣的儲值方案呢？"
  tab={Mock.tabContent[0].tabs}
  tabContent={Mock.tabContent[0].tabContent}
  ad={{
    id: 'wayOfAddValue',
    patternColor: 'green',
    title: `除了遠傳官網，還可以透過APP、月租帳單、門市等多種方式儲值`,
    action: [{
      text: '查看儲值方式',
      line: '#',
      target: '_blank',
    }]
  }}
  carousel={{
    title: '更多優惠',
    id: "promotion",
    cards: [
      {
        image: '/resources/cbu/prepaid/images/cover.png',
        title: '儲值語音送上網',
        description: '至指定通路儲值語音通話，立即送上網流量，儲值越多送越多！',
        link: '#',
        target: '_self'
      },
      {
        image: '/resources/cbu/prepaid/images/cover.png',
        title: '儲值語音送上網',
        description: '至指定通路儲值語音通話，立即送上網流量，儲值越多送越多！',
        link: '#',
        target: '_self'
      },
      {
        image: '/resources/cbu/prepaid/images/cover.png',
        title: '儲值語音送上網',
        description: '至指定通路儲值語音通話，立即送上網流量，儲值越多送越多！',
        link: '#',
        target: '_self'
      },
    ],
    more: { text: '看更多', link: '#', target: '_blank' },
  }}
/>
```

#### Properties

| 名稱       | 屬性   | 選項 | 必填 | 說明 |
| :--------- | :----- | :--- | :--- | :--- |
| id         | string |      |      |      |
| h1         | string |      |      |      |
| tab        | obj    |      |      |      |
| tabContent | array  |      |      |      |
| ad         | obj    |      |      |      |
| carousel   | obj    |      |      |      |
| more       | obj    |      |      |      |

```
import ApplicationSection from '../../components/partials/ApplicationSection'
<ApplicationSection
  id="addValue"
  h1="預付卡方案免綁約、零負擔"
  tabContent={Mock.tabContent[0].tabContent}
  ad={{
      patternColor: 'green',
      title: `現在就到離你最近的門市申辦預付卡吧！`,
      action: [
          {
              text: '查詢遠傳門市',
              line: '#',
              btnStyle: 'primary',
          },
          {
              text: '查詢全虹門市',
              line: '#',
          },
      ]
  }}
  applySteps={
      {
          title: '申辦預付卡，3步驟輕鬆完成！',
          subtitle: '申辦成功後，可再依上網或講電話需求，儲值語音或上網',
          background: '/resources/cbu/prepaid/images/cbu-prepaid-step-1920x470.jpg',
          mobileBackground: '/resources/cbu/prepaid/images/cbu-prepaid-step-mobile.jpg',
      }
  }
  carousel={{
      title: '更多優惠',
      id: "promotion",
      cards: [
          {
              image: '/resources/cbu/prepaid/images/prepaid-sale-promotion-02.jpg',
              title: '超省$1.8親子輕鬆講',
              description: '網內、網外或市話，每分鐘只要$1.8元，家人、朋友，怎麼撥打都划算。',
              link: '#',
          },
          {
              image: '/resources/cbu/prepaid/images/prepaid-sale-promotion-02.jpg',
              title: '超省$1.8親子輕鬆講',
              description: '網內、網外或市話，每分鐘只要$1.8元，家人、朋友，怎麼撥打都划算。',
              link: '#',
          },
          {
              image: '/resources/cbu/prepaid/images/prepaid-sale-promotion-02.jpg',
              title: '超省$1.8親子輕鬆講',
              description: '網內、網外或市話，每分鐘只要$1.8元，家人、朋友，怎麼撥打都划算。',
              link: '#',
          },
      ],
      more: { text: '看更多', link: '#' },
  }}
/>
```
#### Properties

| 名稱     | 屬性   | 選項 | 必填 | 說明 |
| :------- | :----- | :--- | :--- | :--- |
| id       | string |      |      |      |
| h1       | string |      |      |      |
| cards    | array  |      |      |      |
| title    | string |      |      |      |
| ad       | obj    |      |      |      |
| carousel | obj    |      |      |      |
| more     | obj    |      |      |      |

## AppPromotion

```
import AppPromotion from '../../components/partials/AppPromotion';
<AppPromotion
  bgImage={process.env.PUBLIC_URL + '/resources/cbu/e-service/images/appdownload-1920x400.png'}
  title="遠傳行動客服 APP"
  subtitle="貼心服務不用等"
  description={`
    <p>
      以遠傳門號快速登入, 上網流量即時看，查帳單、繳帳單，一鍵完成！
      <br />
      還有許多用戶獨享驚喜優惠
    </p>`
  }
  icon={process.env.PUBLIC_URL + '/resources/cbu/help-center/images/img-logo-fet.png'}
  android={{
    qrCode: process.env.PUBLIC_URL + '/resources/cbu/help-center/images/qr-android.jpg',
    icon: process.env.PUBLIC_URL + '/resources/cbu/help-center/images/google-play.png',
    link: '/',
    title: '支援 Android 7 以上版本'
  }}
  ios={{
    qrCode: process.env.PUBLIC_URL + '/resources/cbu/help-center/images/qr-android.jpg',
    icon: process.env.PUBLIC_URL + '/resources/cbu/help-center/images/google-play.png',
    link: '/',
    title: '支援 Android 7 以上版本'
  }}
/>
```

#### Properties

| 名稱        | 屬性   | 選項 | 必填 | 說明 |
| :---------- | :----- | :--- | :--- | :--- |
| id          | string |      |      |      |
| bgImage     | string |      |      |      |
| title       | string |      |      |      |
| subtitle    | string |      |      |      |
| description | string |      |      |      |
| android     | obj    |      |      |      |
| ios         | obj    |      |      |      |

```
AppPromotion.propTypes = {
  id: PropTypes.string,
  bgImage: PropTypes.string,
  title: PropTypes.string,
  subtitle: PropTypes.string,
  icon: PropTypes.string,
  description: PropTypes.string,
  android: PropTypes.shape({
    link: PropTypes.string,
    qrCode: PropTypes.string,
    title: PropTypes.string,
    icon: PropTypes.string,
  }),
  ios: PropTypes.shape({
    link: PropTypes.string,
    qrCode: PropTypes.string,
    title: PropTypes.string,
    icon: PropTypes.string,
  }),
};
```

## ESectionContent

```
import ESectionContent from '../../components/partials/ESectionContent';
<ESectionContent title='需要更即時的幫助?'>
...content
<ESectionContent/>
```

#### Properties

| 名稱      | 屬性   | 選項 | 必填 | 說明 |
| :-------- | :----- | :--- | :--- | :--- |
| title     | string |      |      |      |
| content   | string |      |      |      |
| checklist | array  |      |      |      |
| children  | any    |      |      |      |

## ForeignContent

```
import ForeignContent from '../../components/partials/ForeignContent';
<ForeignContent
  title={this.state.currentLang.TabPane.title}
  cards={this.state.currentLang.tabContent.program}
  dial={this.state.currentLang.dial}
  pane={this.state.currentLang.dial.panel}
  panelTable={this.state.currentLang.dial.PanelTable}
  panelInformationTitle={this.state.currentLang.dial.PanelInformation.title}
  panelInformationContent={this.state.currentLang.dial.PanelInformation.content}
  whereToBuy={this.state.currentLang.whereToBuy}
/>
```

#### Properties

| 名稱                    | 屬性   | 選項 | 必填 | 說明 |
| :---------------------- | :----- | :--- | :--- | :--- |
| carousel                | obj    |      |      |      |
| dialTitle               | string |      |      |      |
| pane                    | string |      |      |      |
| panelTable              | string |      |      |      |
| panelInformationTitle   | string |      |      |      |
| panelInformationContent | string |      |      |      |
| whereToBuy              | obj    |      |      |      |

## GreetingGuide

```
import GreetingGuide from '../components/partials/GreetingGuide'
<GreetingGuide {...{
  greetingMsg: '',
  bubbles: [
    {
      type: 'text',
      text: '我是愛瑪！請問你想找什麼服務呢？還是想看看我們的最新優惠呢？'
    },
    {
      type: 'cards',
      cards: [
        {
          description: '讓我來幫你：',
          actions: [
            {
              link: '#',
              text: '去繳費'
            },
            {
              link: '#',
              text: '查合約'
            }
          ]
        }
      ]
    },
    {
      type: 'cards',
      cards: [
        {
          image: {
            default: '/resources/cbu/cbu-index/bubble-image-1.jpg',
            retina: '/resources/cbu/cbu-index/bubble-image-1@2x.jpg'
          },
          title: '本月送免費看一部影片喔!',
          description: '話題電影、日劇、韓劇應有盡有',
          actions: [
            {
              link: '#',
              text: '馬上領取'
            }
          ]
        },
        {
          image: {
            default: '/resources/cbu/cbu-index/bubble-image-2.jpg',
            retina: '/resources/cbu/cbu-index/bubble-image-2@2x.jpg'
          },
          title: '中午不知道要吃什麼嗎?!',
          description: 'Uber Eats 送遠傳新客優惠金200元',
          actions: [
            {
              link: '#',
              text: '立即索取'
            }
          ]
        },
        {
          image: {
            default: '/resources/cbu/cbu-index/bubble-image-3.jpg',
            retina: '/resources/cbu/cbu-index/bubble-image-3@2x.jpg'
          },
          title: 'friday 57 存錢也能同時賺錢！!',
          description: '現在申辦即可享 2.6% 利率 ',
          actions: [
            {
              link: '#',
              text: '馬上申辦'
            }
          ]
        },
        {
          image: {
            default: '/resources/cbu/cbu-index/bubble-image-3.jpg',
            retina: '/resources/cbu/cbu-index/bubble-image-3@2x.jpg'
          },
          title: 'friday 57 存錢也能同時賺錢！!',
          description: '現在申辦即可享 2.6% 利率 ',
          actions: [
            {
              link: '#',
              text: '馬上申辦'
            }
          ]
        }
      ]
    }
  ]
}} />
```

#### Properties

| 名稱        | 屬性   | 選項 | 必填 | 說明 |
| :---------- | :----- | :--- | :--- | :--- |
| greetingMsg | string |      |      |      |
| bubbles     | array  |      |      |      |

```
GreetingGuide.propTypes = {
  greetingMsg: PropTypes.string,
  bubbles: PropTypes.arrayOf(
    PropTypes.shape({
      type: PropTypes.string,
      text: PropTypes.string,
      cards: PropTypes.arrayOf(
        PropTypes.shape({
          image: PropTypes.shape({
            default: PropTypes.string,
            retina: PropTypes.string,
          }),
          title: PropTypes.string,
          description: PropTypes.string,
          actions: PropTypes.arrayOf(
            PropTypes.shape({
              text: PropTypes.string,
              link: PropTypes.string,
            })
          ),
        })
      )
    })
  )
}

```

## ImageContent

```
import ImageContent from '../../components/partials/ImageContent';
<ImageContent
  img={process.env.PUBLIC_URL + '/resources/cbu/e-service/images/parking-fee-setting.jpg'}
  retinaImg={process.env.PUBLIC_URL + '/resources/cbu/e-service/images/parking-fee-setting@2x.jpg'}
  meta="申請步驟"
  title="代收設定好簡單"
  content="申請電信帳單代收停車費，只要填寫車輛資料並設定代收縣市。目前代收的地區已超過10個縣市，您可於登入後，輕鬆設定好各縣市路邊停車格及台北市公有停車場。"
  imgPlace='left'
/>

```
#### Properties

| 名稱      | 屬性   | 選項 | 必填 | 說明 |
| :-------- | :----- | :--- | :--- | :--- |
| title     | string |      |      |      |
| retinaImg | string |      |      |      |
| meta      | string |      |      |      |
| meta      | string |      |      |      |
| content   | any    |      |      |      |
| imgPlace  | string |      |      |      |

## ImageSlider

```

## InstructionItems

```
import InstructionItems from '../../components/partials/InstructionItems';
<InstructionItems
  loadMore={() => this.loadMore('internetSetting')}
  title="上網設定"
  list={this.state.internetSetting}
  settingLoad={this.state.internetSettingLoad}
/>
```

#### Properties

| 名稱   | 屬性   | 選項 | 必填 | 說明 |
| :----- | :----- | :--- | :--- | :--- |
| hotTag | string |      |      |      |
| tag    | array  |      |      |      |
| name   | string |      |      |      |
| list   | array  |      |      |      |
| brand  | array  |      |      |      |


## InstructionList

```
import InstructionList from '../../components/partials/InstructionList'
<InstructionList
  title="手機"
  list={this.state.phone}
/>
```

#### Properties

| 名稱  | 屬性   | 選項 | 必填 | 說明 |
| :---- | :----- | :--- | :--- | :--- |
| title | string |      |      |      |
| list  | array  |      |      |      |

## MenuAutocomplete

```
import MenuAutocomplete from '../../components/partials/MenuAutocomplete';
<MenuAutocomplete
  {...{
  tabs: [
    { label: '亞洲' },
    { label: '美洲' },
    { label: '歐洲' },
    { label: '非洲' },
    { label: '大洋洲 / 其他' },
  ],
  content: [
    {
      title: '亞洲',
      all: [
        {showName: '日本 Japan', value: 'value'},
        {showName: '韓國 Korea', value: 'value'},
        {showName: '中國 China', value: 'value'},
        {showName: '泰國 Thailand', value: 'value'},
        {showName: '菲律賓 Philippines', value: 'value'},
        {showName: '越南 Vietnam', value: 'value'},
        {showName: '柬埔寨 Cambodia', value: 'value'},
        {showName: '緬甸 Myanmar', value: 'value'},
        {showName: '印尼 Country', value: 'value'},
        {showName: '印度 Country', value: 'value'},
        {showName: '香港 Country', value: 'value'},
        {showName: '澳門 Country', value: 'value'},
      ],
    },
    {
      title: '美洲',
      all: [
        { showName: '美國 U.S.A', value: 'country'},
        { showName: '加拿大 Canada', value: 'country'},
        { showName: '墨西哥 Mexico', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
      ],
    },
    {
      title: '歐洲',
      all: [
        { showName: '法國 France', value: 'country'},
        { showName: '德國 Deutschland', value: 'country'},
        { showName: '英國 ChiBritainna', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
      ],
    },
    {
      title: '非洲',
      all: [
        { showName: '南非 South Africa', value: 'country'},
        { showName: '埃及 Egypt', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
      ],
    },
    {
      title: '大洋洲 / 其他',
      all: [
        { showName: '澳洲 Australia', value: 'country'},
        { showName: '紐西蘭 New Zealand', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
        { showName: '國家 Country', value: 'country'},
      ],
    },
  ],
}}
  {...{
  defaultKeyword: [
    {showName: '巴西 Brasil', value: 'value'},
    {showName: '巴拉圭 Paraguay', value: 'value'},
    {showName: '巴貝多 Barbados', value: 'value'},
    {showName: '巴哈馬 Bahamas', value: 'value'},
    {showName: '巴拿馬 Panama', value: 'value'},
    {showName: '巴勒斯坦 Palestine', value: 'value'},
  ],
  path: '/roamingPlan/Apply',
  placeholder: '請選擇或輸入目的地',
}}
  onClick={word => console.log(word)}
/>
```

#### Properties

| 名稱           | 屬性   | 選項 | 必填 | 說明 |
| :------------- | :----- | :--- | :--- | :--- |
| title          | string |      |      |      |
| path           | string |      |      |      |
| placeholder    | string |      |      |      |
| keyword        | string |      |      |      |
| defaultKeyword | array  |      |      |      |
| storeType      | string |      |      |      |
| menu           | any    |      |      |      |
| content        | any    |      |      |      |
| onClick        | func   |      |      |      |


## MultiRuler

```
import MultiRuler from '../../components/partials/MultiRuler';
<MultiRuler
  key={index}
  {...item}
/>
```

#### Properties

| 名稱       | 屬性   | 選項 | 必填 | 說明 |
| :--------- | :----- | :--- | :--- | :--- |
| className  | string |      |      |      |
| size       | string |      |      |      |
| percentage | number |      |      |      |

## NavAnchor

```
import NavAnchor from '../components/partials/NavAnchor';
<NavAnchor
  pageTitle='優惠'
  button={{
    text: '優惠通知',
    link: '#'
}} />
```

#### Properties

| 名稱      | 屬性   | 選項 | 必填 | 說明 |
| :-------- | :----- | :--- | :--- | :--- |
| pageTitle | string |      |      |      |
| tabs      | array  |      |      |      |
| button    | any    |      |      |      |
| onChange  | func   |      |      |      |


```
NavAnchor.propTypes = {
  pageTitle: PropTypes.string,
  tabs: PropTypes.arrayOf(
    PropTypes.shape({
      label: PropTypes.string,
    })
  ),
  button: PropTypes.any,
  onChange: PropTypes.func,
};
```

## NavContentTab1

```
import NavContentTab1 from '../../components/partials/NavContentTab1';
<NavContentTab1
  default={0}
  tabs={{
    name: 'page-tab',
    list: [
      { label: '費用項目' },
      { label: '通話明細' },
    ]
  }}
  onChange={this.changeTab}
/>
```
#### Properties

| 名稱     | 屬性  | 選項 | 必填 | 說明 |
| :------- | :---- | :--- | :--- | :--- |
| tabs     | array |      |      |      |
| onChange | func  |      |      |      |

```
NavContentTab1.propTypes = {
  tabs: PropTypes.shape({
    default: PropTypes.number,
    name: PropTypes.string,
    list: PropTypes.arrayOf(
      PropTypes.shape({
        icon: PropTypes.string,
        focusIcon: PropTypes.string,
        label: PropTypes.string.isRequired,
        link: PropTypes.string
      })
    ),
  }),
  onChange: PropTypes.func,
};
```
## NavContentTab2

```
import NavContentTab2 from '../../components/partials/NavContentTab2';
<NavContentTab2 tabs={{
  name: 'add-value-tab',
  icon: false,
  title: true,
  default: 1,
  list: [
    {
      name: 'add-value',
      title: 'Wi-Fi 自動連網',
      label: '',
      link: '/otherService/Wifi',
      target: '_self',
    },
    {
      name: 'application',
      title: 'Wi-Fi 手動設定上網',
      label: '',
      link: '/otherService/WifiManual',
      target: '_self',
    },
  ],
}} onChange={e => this.changeMainTab(e)} />
```

#### Properties

| 名稱      | 屬性   | 選項 | 必填 | 說明 |
| :-------- | :----- | :--- | :--- | :--- |
| className | string |      |      |      |
| tabs      | array  |      |      |      |
| onChange  | func   |      |      |      |

```
NavContentTab2.propTypes = {
  tabs: PropTypes.shape({
    default: PropTypes.number,
    name: PropTypes.string.isRequired,
    icon: PropTypes.bool,
    title: PropTypes.bool,
    list: PropTypes.arrayOf(
      PropTypes.shape({
        icon: PropTypes.string,
        focusIcon: PropTypes.string,
        label: PropTypes.string.isRequired,
      })
    ).isRequired,
  }).isRequired,
  className: PropTypes.string,
  onChange: PropTypes.func,
};
```

## NavTab

```
import NavTab from '../../components/partials/NavTab';
<NavTab
  pageTitle='幫助中心'
  onChange={this.tabChange}
  default={2}
  tabs={{
      name: 'help-center-tab',
      list: [
          { name: 'tab-1', label: '個人用戶', link: '/help-center' },
          { name: 'tab-2', label: '商務用戶', link: 'http://fetnet-demo.aja.com.tw/help-center' },
          { name: 'tab-3', label: '聯絡我們', link: '#' },
          { name: 'tab-4', label: '服務條款', link: '/help-center/terms-of-service/privacy' },
      ],
  }}
  button={{
      text: '回首頁',
      link: '/help-center',
  }}
/>
```

#### Properties

| 名稱     | 屬性    | 選項 | 必填 | 說明 |
| :------- | :------ | :--- | :--- | :--- |
| showAll  | bool    |      |      |      |
| default  | default |      |      |      |
| tabs     | obj     |      |      |      |
| button   | obj     |      |      |      |
| onChange | func    |      |      |      |

NavTab.propTypes = {
  showAll: PropTypes.bool,
  pageTitle: PropTypes.string,
  default: PropTypes.number,
  tabs: PropTypes.shape({
    name: PropTypes.string,
    list: PropTypes.arrayOf(
      PropTypes.shape({
        icon: PropTypes.string,
        focusIcon: PropTypes.string,
        label: PropTypes.string.isRequired,
        link: PropTypes.string,
      })
    ),
  }),
  button: PropTypes.shape({
    link: PropTypes.string,
    text: PropTypes.string,
  }),
  onChange: PropTypes.func,
};

## PhoneSubscribe

```
import PhoneSubscribe from '../../components/partials/PhoneSubscribe';
<PhoneSubscribe
  title='遠傳門市好康，每月報給你知'
  url='/ebu/product/done-manage-newsletter'
  bg='/resources/cbu/img/web-pattern-cbu-subscribe@2x.png'
  sending='送出'
/>
```

#### Properties

| 名稱    | 屬性   | 選項 | 必填 | 說明 |
| :------ | :----- | :--- | :--- | :--- |
| url     | string |      |      |      |
| title   | string |      |      |      |
| sending | string |      |      |      |

## ProductMap
```
import ProductMap from '../components/partials/ProductMap'
<ProductMap {...{
  title: '我想尋找...',
  data: [
    {
      title: '找網路限定優惠',
      list: [
        { text: '網路門市限定吃到飽', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '新申辦門號', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '攜碼到遠傳', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '老客戶續約', link: '#', target: '_self', icon: 'chevron-right' },
      ],
    },
    {
      title: '找產品資費',
      list: [
        { text: '資費方案', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '優惠方案', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '易付/預付卡', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '國際漫遊', link: '#', target: '_self', icon: 'chevron-right' },
      ],
    },
    {
      title: '找我的專區',
      list: [
        { text: '會員資料查詢', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '訂閱會員好康報', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '密碼變更', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '領取本月免費會員好禮', link: '#', target: '_self', icon: 'chevron-right' },
      ],
    },
    {
      title: '找幫助',
      list: [
        { text: '服務公告', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '帳單/繳費/儲值', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '來電過濾黑名單設定', link: '#', target: '_self', icon: 'chevron-right' },
        { text: '門市據點查詢', link: '#', target: '_self', icon: 'chevron-right' },
      ],
    },
  ]
}} />
```

#### Properties

| 名稱  | 屬性   | 選項 | 必填 | 說明 |
| :---- | :----- | :--- | :--- | :--- |
| id    | string |      |      |      |
| title | string |      |      |      |
| data  | array  |      |      |      |
| more  | obj    |      |      |      |

```
ProductMap.propTypes = {
  id: PropTypes.string,
  title: PropTypes.string,
  data: PropTypes.arrayOf(
    PropTypes.shape({
      title: PropTypes.string,
      list: PropTypes.arrayOf(
        PropTypes.shape({
          text: PropTypes.string,
          link: PropTypes.string,
          target: PropTypes.string,
          icon: PropTypes.string,
        })
      ),
    })
  ),
  more: PropTypes.shape({
    text: PropTypes.string,
    isCollapse: PropTypes.bool,
  }),
};
```

## Ruler

```
import Ruler from '../../components/partials/Ruler';
<Ruler
  className="mb-md-4 mb-1"
  percentage={this.state.currentBill.usage.totalUsage}
  size="large"
/>
```

#### Properties

| 名稱           | 屬性   | 選項 | 必填 | 說明 |
| :------------- | :----- | :--- | :--- | :--- |
| className      | string |      |      |      |
| showPercentage | number |      |      |      |
| size           | string |      |      |      |
| percentage     | number |      |      |      |

## SectionAd2

```
import SectionAd2 from '../../components/partials/SectionAd2';
<SectionAd2 {...{
  image: {
    md: '/resources/cbu/life-circle-drama/images/cbu_event_banner_1920x195.jpg',
    sm: '/resources/cbu/life-circle-drama/images/cbu_event_banner_700x496.jpg',
  },
  title: '08/08邕聖祐、金香起、申承浩來台',
  description: '18歲的瞬間 Happy Together 遠傳 FriDay影音會員同樂會！',
  action: {
    text: '免費報名',
    link: '#',
  },
}} />
```

#### Properties

| 名稱        | 屬性   | 選項 | 必填 | 說明 |
| :---------- | :----- | :--- | :--- | :--- |
| image       | obj    |      |      |      |
| title       | string |      |      |      |
| description | string |      |      |      |
| id          | string |      |      |      |
| target      | string |      |      |      |
| target      | string |      |      |      |
| action      | obj    |      |      |      |

```
SectionAd2.propTypes = {
    image: PropTypes.shape({
        md: PropTypes.string,
        sm: PropTypes.string
    }),
    title: PropTypes.string,
    description: PropTypes.string,
    id: PropTypes.string,
    target: PropTypes.string,
    action: PropTypes.shape({
        text: PropTypes.string,
        link: PropTypes.string,
        btnStyle: PropTypes.string // only 'primary' or 'secondary
    })
}
```

## SectionAd3

```
import SectionAd3 from '../../components/partials/SectionAd3';
<SectionAd3 {...{
  patternColor: 'green',
  title: `透過遠傳官網儲值，立即享有網路限定優惠`,
  action: [{
      text: '立即儲值',
      line: '#',
  }]
}} />
```

#### Properties

| 名稱         | 屬性   | 選項 | 必填 | 說明 |
| :----------- | :----- | :--- | :--- | :--- |
| patternColor | string |      |      |      |
| title        | string |      |      |      |
| id           | string |      |      |      |
| action       | array  |      |      |      |

```
SectionAd3.propTypes = {
  patternColor: PropTypes.string, // only 'blue' or 'gray'
  title: PropTypes.string,
  id: PropTypes.string,
  action: PropTypes.arrayOf(
    PropTypes.shape({
      text: PropTypes.string,
      link: PropTypes.string,
      btnStyle: PropTypes.string, // only 'primary' or 'secondary
    })
  ),
};
```


<ServiceTag {...EbuLarge.serviceTags} />
```
{% endtab %}

{% tab title="Source" %}
```javascript
import React from 'react';
import {Link} from 'react-router-dom';
import {Grid} from '@material-ui/core';
import PropTypes from 'prop-types';

class ServiceTag extends React.Component {
    constructor(props) {
        super(props);
        window.addEventListener('resize', e => {
            this.scrollCenter();
        });
    }

    scrollCenter() {
        let width = window.innerWidth;
        let container = document.getElementsByClassName(".service-tag-container")[0];
        let scroller = document.getElementsByClassName(".service-scroller")[0];
        if (!container ) return
        // debugger
        if (scroller.clientWidth > width) {
            // debugger
            container.scrollLeft = (scroller.clientWidth - width) / 2
        }
    }

    componentDidMount() {
        this.scrollCenter()
    }

    render () {
        return (
            <section className="service-tags">
                <div className="fui-container">
                    <h3 className="align-center">
                        {this.props.title}
                    </h3>
                    <Grid container justify="center">
                        <Grid item xs={12} sm={12} md={10}>
                            <div className='service-tag-container'>
                                <div className='service-scroller'>
                                    {
                                        this.props.tags.map((item, key) => (
                                            <Link key={`service-tag-${key}`} to={item.link} className="fui-button is-tag">{item.name}</Link>  
                                        ))
                                    }
                                </div>
                            </div>
                        </Grid>
                    </Grid>
                </div>
            </section>
        )
    }
}

ServiceTag.propTypes = {
    title: PropTypes.string,
    tags: PropTypes.arrayOf(
        PropTypes.shape({
            name: PropTypes.string,
            link: PropTypes.string
        })
    )
}

export default ServiceTag;
```
{% endtab %}

{% tab title="Mock" %}
```javascript
export const serviceTags = {
  title: '其他企業家也在關注…',
  tags: [
    {
      name: '物聯網應用',
      link: '#',
    },
    {
      name: '機房雲端化',
      link: '#',
    },
    {
      name: '工業 4.0',
      link: '#',
    },
    {
      name: '智慧聯網',
      link: '#',
    },
    {
      name: 'NB-IoT',
      link: '#',
    },
    {
      name: '混合雲',
      link: '#',
    },
    {
      name: 'DDoS 攻擊',
      link: '#',
    },
    {
      name: '資安健診',
      link: '#',
    },
    {
      name: '智慧工廠',
      link: '#',
    },
    {
      name: '上雲端',
      link: '#',
    },
    {
      name: '企業VPN',
      link: '#',
    },
    {
      name: '行動裝置安全',
      link: '#',
    },
    {
      name: 'esim申請',
      link: '#',
    },
    {
      name: 'VOLTE',
      link: '#',
    },
    {
      name: '企業節能',
      link: '#',
    },
  ],
};

```
{% endtab %}
{% endtabs %}

## StoreFinder


```

import StoreFinder from '../../components/partials/StoreFinder'
<StoreFinder
  cityList={...[
        {
          value: 'TPC',
          text: '台北市',
          location: [
            { value: '大同區', text: '大同區' },
            {
              value: '中正區',
              text: '中正區'
            },
            {
              value: '松山區',
              text: '松山區'
            },
            {
              value: '大安區',
              text: '大安區'
            }
          ]
        },
        {
          value: 'NTPC',
          text: '新北市',
          location: [
            {
              value: '板橋區',
              text: '板橋區'
            },
            {
              value: '三重區',
              text: '三重區'
            },
            {
              value: '中和區',
              text: '中和區'
            }
          ]
        },
      ]}
  places={...[
        {
          name: '台北車站直營店',
          id: '001',
          geometry: {
            location: {
              lat: 25.046618,
              lng: 121.517907
            }
          },
          fb: {},
          phone: '02-23719265',
          addr: '台北市中正區忠孝西路１段４９號Ｂ１',
          time: ['平日 07:00-23:00', '週六 07:00-23:00', '週日 07:00-23:00'],
          services: ['5G體驗', '互動體驗區', '咖啡機', '舊機回收', '包膜服務(預約制)', '手機免費充電/消毒', '在地服務', '複合門市', '自助繳費機', '手機維修收件', 'ETC繳費儲值', '行動電源/手機租借(預約制)'],
          facilities: ['移動式坡道', '服務鈴'],
          filter: ['dayTime', 'special'],
          book: '',
          getDirection: 'https://www.google.com.tw/maps/place/%E5%8F%B0%E5%8C%97%E5%B8%82%E4%B8%AD%E5%B1%B1%E5%8D%80%E5%8C%97%E5%AE%89%E8%B7%AF%EF%BC%95%EF%BC%94%EF%BC%92%E4%B9%8B%EF%BC%91%E8%99%9F'
        },
        {
          name: '台北館前直營店',
          id: '002',
          geometry: {
            location: {
              lat: 25.045560,
              lng: 121.515106
            }
          },
          fb: {},
          phone: '02-23719265',
          addr: '台北市中山區忠孝西路１段４９號Ｂ１',
          time: ['平日 07:00-23:00', '週六 07:00-23:00', '週日 07:00-23:00'],
          services: ['5G體驗', '互動體驗區', '咖啡機', '舊機回收', '包膜服務(預約制)', '手機免費充電/消毒', '在地服務', '複合門市', '自助繳費機', '手機維修收件', 'ETC繳費儲值', '行動電源/手機租借(預約制)'],
          facilities: ['移動式坡道', '服務鈴'],
          filter: ['dayTime', 'nightTime'],
          book: '',
          getDirection: 'https://www.google.com.tw/maps/place/%E5%8F%B0%E5%8C%97%E5%B8%82%E4%B8%AD%E5%B1%B1%E5%8D%80%E5%8C%97%E5%AE%89%E8%B7%AF%EF%BC%95%EF%BC%94%EF%BC%92%E4%B9%8B%EF%BC%91%E8%99%9F'
        },
        {
          name: '善導寺直營店',
          id: '0021',
          geometry: {
            location: {
              lat: 25.045660,
              lng: 121.512106
            }
          },
          fb: {},
          phone: '02-23719265',
          addr: '台北市中正區忠孝西路2段４９號Ｂ１',
          time: ['平日 07:00-23:00', '週六 07:00-23:00', '週日 07:00-23:00'],
          services: ['5G體驗', '互動體驗區', '咖啡機', '舊機回收', '包膜服務(預約制)', '手機免費充電/消毒', '在地服務', '複合門市', '自助繳費機', '手機維修收件', 'ETC繳費儲值', '行動電源/手機租借(預約制)'],
          facilities: ['移動式坡道', '服務鈴'],
          filter: ['nightTime'],
          book: '',
          getDirection: 'https://www.google.com.tw/maps/place/%E5%8F%B0%E5%8C%97%E5%B8%82%E4%B8%AD%E5%B1%B1%E5%8D%80%E5%8C%97%E5%AE%89%E8%B7%AF%EF%BC%95%EF%BC%94%EF%BC%92%E4%B9%8B%EF%BC%91%E8%99%9F'
        },
        {
          name: '三重直營店',
          id: '003',
          geometry: {
            location: {
              lat: 25.027939,
              lng: 121.431750
            }
          },
          fb: {},
          phone: '02-23719265',
          addr: '新北市三重區區忠孝西路１段４９號Ｂ１',
          time: ['平日 07:00-23:00', '週六 07:00-23:00', '週日 07:00-23:00'],
          services: ['5G體驗', '互動體驗區', '咖啡機', '舊機回收', '包膜服務(預約制)', '手機免費充電/消毒', '在地服務', '複合門市', '自助繳費機', '手機維修收件', 'ETC繳費儲值', '行動電源/手機租借(預約制)'],
          facilities: ['移動式坡道', '服務鈴'],
          filter: ['dayTime', 'nightTime'],
          book: '',
          getDirection: 'https://www.google.com.tw/maps/place/%E5%8F%B0%E5%8C%97%E5%B8%82%E4%B8%AD%E5%B1%B1%E5%8D%80%E5%8C%97%E5%AE%89%E8%B7%AF%EF%BC%95%EF%BC%94%EF%BC%92%E4%B9%8B%EF%BC%91%E8%99%9F'
        },
        {
          name: '南投彰南直營店',
          id: '004',
          geometry: {
            location: {
              lat: 23.880898,
              lng: 120.691864
            }
          },
          fb: {},
          phone: '02-23719265',
          addr: '南投縣中正區忠孝西路１段４９號Ｂ１',
          time: ['平日 07:00-23:00', '週六 07:00-23:00', '週日 07:00-23:00'],
          services: ['5G體驗', '互動體驗區', '咖啡機', '舊機回收', '包膜服務(預約制)', '手機免費充電/消毒', '在地服務', '複合門市', '自助繳費機', '手機維修收件', 'ETC繳費儲值', '行動電源/手機租借(預約制)'],
          facilities: ['移動式坡道', '服務鈴'],
          filter: [],
          book: '',
          getDirection: 'https://www.google.com.tw/maps/place/%E5%8F%B0%E5%8C%97%E5%B8%82%E4%B8%AD%E5%B1%B1%E5%8D%80%E5%8C%97%E5%AE%89%E8%B7%AF%EF%BC%95%EF%BC%94%EF%BC%92%E4%B9%8B%EF%BC%91%E8%99%9F'
        },
      ]}
/>

```

## InstructionItems

```
import InstructionItems from '../../components/partials/InstructionItems';
<InstructionItems
  loadMore={() => this.loadMore('internetSetting')}
  title="上網設定"
  list={...[
        {
          name: '數據機模式',
          link: '#'
        },
        {
          name: '行動上網設定',
          link: '#'
        },
        {
          name: 'Wi-Fi上網設定',
          link: '#'
        },
        {
          name: 'Wi-Fi熱點設定',
          link: '#'
        },
        {
          name: '電子郵件設定',
          link: '#'
        },
        {
          name: '多媒體訊息設定',
          link: '#'
        },
      ]}
  settingLoad={true}
/>

```

#### Properties

| 名稱   | 屬性   | 選項 | 必填 | 說明 |
| :----- | :----- | :--- | :--- | :--- |
| hotTag | string |      |      |      |
| tag    | array  |      |      |      |
| name   | string |      |      |      |
| list   | array  |      |      |      |
| brand  | string |      |      |      |
| image  | array  |      |      |      |

## InstructionList
```
import InstructionList from '../../components/partials/InstructionList'
<InstructionList
  title="手機"
  list={...[
        {
          img: {
            url: 'resources/cbu/img/estore-product-phone-1.jpg',
            alt: 'img'
          },
          type: 'phone',
          brand: 'Xiaomi',
          model: 'Note 8T 64GB',
          text: 'Xiaomi 紅米 Note 8T 64GB',
          link: '#123'
        },
        {
          img: {
            url: 'resources/cbu/img/estore-product-phone-2.jpg',
            alt: 'img'
          },
          type: 'phone',
          brand: 'SAMSUNG',
          model: 'S20 5G',
          text: 'SAMSUNG Galaxy S20 5G',
          link: '#234'
        },
        {
          img: {
            url: 'resources/cbu/img/estore-product-phone-3.jpg',
            alt: 'img'
          },
          type: 'phone',
          brand: 'Apple',
          model: 'iPhone 11 Pro Max 256GB',
          text: 'iPhone 11 Pro Max 256GB',
          link: '#1111'
        },
        {
          img: {
            url: 'resources/cbu/img/estore-product-phone-4.jpg',
            alt: 'img'
          },
          type: 'phone',
          brand: 'SAMSUNG',
          model: 'S20 Ultra 5G',
          text: 'SAMSUNG Galaxy S20 Ultra 5G',
          link: '#222'
        },
      ]}
/>
```

#### Properties

| 名稱  | 屬性   | 選項 | 必填 | 說明 |
| :---- | :----- | :--- | :--- | :--- |
| title | string |      |      |      |
| list  | arry   |      |      |      |
