# Others

## AnchorDetect

```
import AnchorDetect from '../../components/AnchorDetect';
<AnchorDetect
  className='vertical-anchor-nav'
  items={['anchor0', 'anchor1', 'anchor2', 'anchor3', 'anchor4']}
  activeClass='active'
  offsetTop={145}>
  <li>
    <span>來開箱</span>
  </li>
  <li>
    <span>配件介紹</span>
  </li>
  <li>
    <span>來試用</span>
  </li>
  <li>
    <span>來PK!</span>
  </li>
  <li>
    <span>寫在最後</span>
  </li>
</AnchorDetect>
<OnVisible id='anchor0'>
  anchor0 content
</OnVisible>
```

#### Properties

| 名稱         | 屬性   | 選項 | 必填 | 說明 |
| :----------- | :----- | :--- | :--- | :--- |
| items        | array  |      |      |      |
| itemsName    | array  |      |      |      |
| activeClass  | string |      | true |      |
| offsetTop    | number |      |      |      |
| componentTag | string |      |      |      |
| style        | obj    |      |      |      |
| container    | any    |      |      |      |
| className    | string |      |      |      |
| children     | any    |      |      |      |

---
description: 麵包屑
---

## Breadcrumb

{% tabs %}
{% tab title="First Tab" %}
![](../.gitbook/assets/image%20%28199%29.png)
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Usage" %}
```javascript
import Breadcrumb from '../components/Breadcrumb';

<Breadcrumb breadcrumb={BusinessLoginMock.breadcrumb} />
```
{% endtab %}

{% tab title="Source" %}
```javascript
import React from 'react';
import PropTypes from 'prop-types';

class Breadcrumb extends React.Component {
  overflow = (val) => {
    // console.log(val.length);
    if (val.length > 20) {
      return val.slice(0, 20) + '...'
    } else {
      return val
    }
  }
  render() {
    return (
      <section className='fui-breadcrumb-container' style={{top: this.props.top}}>
        <div className='fui-container'>
          <ul className={`fui-breadcrumb is-${this.props.color}`}>
            {this.props.breadcrumb.map((item, idx) => (
              <li key={`breadcrumb-item-${idx}`}>
                <a href={item.link}>{this.overflow(item.text)}</a>
              </li>
            ))}
          </ul>
        </div>
      </section>
    );
  }
}

Breadcrumb.propTypes = {
  color: PropTypes.string, // black | white
  top: PropTypes.number, // container position
  breadcrumb: PropTypes.arrayOf(
    PropTypes.shape({
      link: PropTypes.string.isRequired, // 麵包屑連結必要
      text: PropTypes.string.isRequired, // 麵包屑名稱必要
    })
  ),
};

export default Breadcrumb;

```
{% endtab %}

{% tab title="Mock" %}
```javascript
export const breadcrumb = [
  { text: '商務首頁', link: '/ebu/index' },
  { text: '企業行動優惠登入', link: '/page/BusinessLogin' },
];
```
{% endtab %}
{% endtabs %}



#### Properties

| 名稱       | 屬性   | 選項                                                                  | 必填 | 說明                       |
| :--------- | :----- | :-------------------------------------------------------------------- | :--- | :------------------------- |
| color      | string | black \| white                                                        |      |                            |
| top        | number |                                                                       |      | container position         |
| breadcrumb | array  | link: PropTypes.string.isRequired, text: PropTypes.string.isRequired} |      | 麵包屑連結, 麵包屑名稱必填 |


## button
* [Button](../elements/button.md)

## CheckModal

```
import CheckModal from '../CheckModal';
<CheckModal open={this.state.modalOpen} closeModal={this.closeModal} submit={this.submit} />
```

#### Properties

| 名稱    | 屬性 | 選項 | 必填 | 說明 |
| :------ | :--- | :--- | :--- | :--- |
| open    | bool |      |      |      |
| content | obj  |      |      |      |
| onClose | func |      |      |      |


## Cookie

```
import Cookie from './components/Cookie';
import Cookie from './components/Cookie';
```

## dropdown

* [Dropdown](../components/dropdown.md)

## Emma

```
import EmmaService from './components/Emma';
const getEmma = () => {
  return {
    text: path.indexOf('/cbu/5g') > -1 ? '我有興趣' : null,
    link: getEmmaLink(),
    show: true,
    useEmmaAvatar: true
  }
}
const getEmmaLink = () => {
  return path.indexOf('/cbu/5g') > -1 ? 'https://enterprise.fetnet.net/content/ebu/tw/5g/form/5G-cbu-form.html' : ''
}
const displayEmma = () => {
  let notDisplayGroup = [
    '/404',
    '/under-maintainance',
    '/ebu/news',
    '/ebu/news/newscontent',
    '/ebu/news/newscontentversion2',
    '/ebu/form/micro-form',
    '/ebu/form/medium-form',
    '/ebu/form/large-form',
    '/ebu/form/public-sector-form',
    '/ebu/form/cloud-form',
    '/ebu/form/smart-wifi-form',
    '/ebu/form/event-form',
    '/ebu/form/5g-form',
    '/ebu/form/5g-event',
    '/ebu/5g',
    '/broadcast',
    '/entrymainframepage',
    '/seednet',
    '/seednet-domain',
    '/office365',
    '/mrtg',
    '/ebu/business-login',
    '/error',
    '/module/section',
  ];
  let result = true;
  for (let i = 0; i < notDisplayGroup.length; i++) {
    if (notDisplayGroup[i] === path.toLowerCase()) {
      result = false
      break
    } else {
      result = true
    }
  }
  // console.log(result);

  return result;
};
<EmmaService {...getEmma()} />
```

#### Properties

| 名稱          | 屬性   | 選項 | 必填 | 說明 |
| :------------ | :----- | :--- | :--- | :--- |
| link          | string |      |      |      |
| useEmmaAvatar | bool   |      |      |      |
| show          | bool   |      |      |      |
| text          | string |      |      |      |


## GoTop
```
import GoTop from './components/GoTop';
<GoTop />
```

## HotWord

```
import HotWord from '../../HotWord';
<HotWord {...{
  path: '/roamingPlan/Apply',
  label: '依地區搜尋',
  // hotword: [
  //   '亞洲',
  //   '美洲',
  //   '歐洲',
  //   '大洋洲',
  //   '中東',
  //   '非洲',
  // ],
  // active: [
  //   true,
  //   false,
  //   false,
  //   false,
  //   false
  // ],
  hotword: [
    { text: '亞洲', active: true },
    { text: '美洲', active: false },
    { text: '歐洲', active: false },
    { text: '大洋洲', active: false },
    { text: '中東', active: false },
    { text: '非洲', active: false },
  ],
}} />
```

#### Properties

| 名稱    | 屬性   | 選項 | 必填 | 說明                                           |
| :------ | :----- | :--- | :--- | :--------------------------------------------- |
| path    | string |      |      |                                                |
| hotword | array  |      |      | text: PropTypes.string,active: PropTypes.bool, |

### KeywordInput

{% tabs %}
{% tab title="Desktop" %}
![](../.gitbook/assets/image%20%28232%29.png)
{% endtab %}

{% tab title="Mobile" %}
![](../.gitbook/assets/image%20%2851%29.png)
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="First Tab" %}
```javascript
import KeywordInput from '../../KeywordInput';

<KeywordInput
  title={mock.keywordInput}
  defaultKeyword={[
    'Gogoro',
    'Gogoro 699',
    'google',
    'GPS',
    'GPS Google',
    'Gogo',
    'GoPro',
    'Geo',
    'SEO',
    'OPPO',
  ]}
/>
```
{% endtab %}

{% tab title="Second Tab" %}
```javascript
import React from 'react';
import Autocomplete from 'react-autocomplete';
import Button from './Button';
import PropTypes from 'prop-types';

class KeywordInput extends React.Component {
  constructor(props) {
    super(props);
    this.input = React.createRef();
    this.state = {
      isEBU: window.location.pathname.indexOf('ebu') > -1,
      keywordMenu: this.props.defaultKeyword.slice(0, 6),
      keyword: this.props.keyword || '',
    };

    this.doSearch = this.doSearch.bind(this);
  }

  componentDidMount() {
    this.setState({
      keyword: this.props.keyword || '',
    });
  }

  highlightKeyword(word) {
    let value = this.state.keyword.toLowerCase();
    let index = word.toLowerCase().indexOf(value);

    if (index === -1 || value.value === '') {
      return word;
    } else {
      // console.log(word.substring(0,index) + "<span class='highlight'>" + word.substring(index,index+value.length) + "</span>" + word.substring(index + value.length))
      return (
        word.substring(0, index) +
        "<span class='highlight'>" +
        word.substring(index, index + value.length) +
        '</span>' +
        word.substring(index + value.length)
      );
    }
  }

  resetInput = () => {
    this.setState({
      keyword: '',
    });
  };

  doSearch(text) {
    window.location.href = `${this.props.path || '/ebu/search'}?keyword=${text || this.state.keyword}`;
  }

  render() {
    return (
      <div className='keyword-input-container'>
        {this.props.title ? <h2>{this.props.title}</h2> : ''}
        <Autocomplete
          wrapperStyle={{ width: '100%', position: 'relative' }}
          getItemValue={item => item}
          items={this.state.keywordMenu}
          value={this.state.keyword}
          onKeyDowe={this.inputChange}
          renderInput={props => (
            <div className={`fui-input-group is-keyword`}>
              <div className='fui-input'>
                <input ref={this.input} {...props} type='text' placeholder={this.props.placeholder || '立即搜尋 IOT'} />
                {props.value !== '' ? (
                  <div className='reset' onClick={this.resetInput}>
                    <i className='icon-close'></i>
                  </div>
                ) : (
                  ''
                )}
              </div>
              <div className='fui-action'>
                <Button onClick={this.doSearch} btnStyle='primary'>
                  搜尋
                </Button>
              </div>
            </div>
          )}
          onSelect={(value, item) => {
            this.setState({ keyword: item });
          }}
          onChange={(event, value) => {
            this.setState({ keywordMenu: [] });
            this.setState({ keyword: value });
            let menu = this.props.defaultKeyword.filter(menu => menu.toLowerCase().indexOf(value.toLowerCase()) > -1);
            this.setState({ keywordMenu: menu });
          }}
          renderMenu={children => <div className='fui-dropdown fui-keyword-menu'>{children}</div>}
          renderItem={(item, isHighlighted) => (
            <div key={`autocompelte-${item}`} className={`fui-item ${isHighlighted ? 'is-selected' : ''}`}>
              <span className='prefix'>
                <i className='icon-search'></i>
              </span>
              <div className='content' dangerouslySetInnerHTML={{ __html: this.highlightKeyword(item) }}></div>
            </div>
          )}
        />
      </div>
    );
  }
}

KeywordInput.propTypes = {
  path: PropTypes.string,
  title: PropTypes.string,
  placeholder: PropTypes.string,
  keyword: PropTypes.string,
  defaultKeyword: PropTypes.arrayOf(PropTypes.string),
};

export default KeywordInput;

```
{% endtab %}
{% endtabs %}

#### Properties

| 名稱           | 屬性   | 必填 | 選項 | 說明           |
| :------------- | :----- | :--- | :--- | :------------- |
| path           | string |      |      | 轉址位置       |
| title          | string |      |      | 標題           |
| placeholder    | string |      |      | 預設顯示       |
| keyword        | string |      |      | 輸入關鍵字     |
| defaultKeyword | array  |      |      | 預設關鍵字陣列 |

## Link

```
import Link from './Link';
<Link
  role='button'
  to="#"
  className='fui-button'>
  content
</Link>
```

### KeywordInput

{% tabs %}
{% tab title="Desktop" %}
![](../.gitbook/assets/image%20%28232%29.png)
{% endtab %}

{% tab title="Mobile" %}
![](../.gitbook/assets/image%20%2851%29.png)
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="First Tab" %}
```javascript
import KeywordInput from '../../KeywordInput';

<KeywordInput
  title={mock.keywordInput}
  defaultKeyword={[
    'Gogoro',
    'Gogoro 699',
    'google',
    'GPS',
    'GPS Google',
    'Gogo',
    'GoPro',
    'Geo',
    'SEO',
    'OPPO',
  ]}
/>
```
{% endtab %}

{% tab title="Second Tab" %}
```javascript
import React from 'react';
import Autocomplete from 'react-autocomplete';
import Button from './Button';
import PropTypes from 'prop-types';

class KeywordInput extends React.Component {
  constructor(props) {
    super(props);
    this.input = React.createRef();
    this.state = {
      isEBU: window.location.pathname.indexOf('ebu') > -1,
      keywordMenu: this.props.defaultKeyword.slice(0, 6),
      keyword: this.props.keyword || '',
    };

    this.doSearch = this.doSearch.bind(this);
  }

  componentDidMount() {
    this.setState({
      keyword: this.props.keyword || '',
    });
  }

  highlightKeyword(word) {
    let value = this.state.keyword.toLowerCase();
    let index = word.toLowerCase().indexOf(value);

    if (index === -1 || value.value === '') {
      return word;
    } else {
      // console.log(word.substring(0,index) + "<span class='highlight'>" + word.substring(index,index+value.length) + "</span>" + word.substring(index + value.length))
      return (
        word.substring(0, index) +
        "<span class='highlight'>" +
        word.substring(index, index + value.length) +
        '</span>' +
        word.substring(index + value.length)
      );
    }
  }

  resetInput = () => {
    this.setState({
      keyword: '',
    });
  };

  doSearch(text) {
    window.location.href = `${this.props.path || '/ebu/search'}?keyword=${text || this.state.keyword}`;
  }

  render() {
    return (
      <div className='keyword-input-container'>
        {this.props.title ? <h2>{this.props.title}</h2> : ''}
        <Autocomplete
          wrapperStyle={{ width: '100%', position: 'relative' }}
          getItemValue={item => item}
          items={this.state.keywordMenu}
          value={this.state.keyword}
          onKeyDowe={this.inputChange}
          renderInput={props => (
            <div className={`fui-input-group is-keyword`}>
              <div className='fui-input'>
                <input ref={this.input} {...props} type='text' placeholder={this.props.placeholder || '立即搜尋 IOT'} />
                {props.value !== '' ? (
                  <div className='reset' onClick={this.resetInput}>
                    <i className='icon-close'></i>
                  </div>
                ) : (
                  ''
                )}
              </div>
              <div className='fui-action'>
                <Button onClick={this.doSearch} btnStyle='primary'>
                  搜尋
                </Button>
              </div>
            </div>
          )}
          onSelect={(value, item) => {
            this.setState({ keyword: item });
          }}
          onChange={(event, value) => {
            this.setState({ keywordMenu: [] });
            this.setState({ keyword: value });
            let menu = this.props.defaultKeyword.filter(menu => menu.toLowerCase().indexOf(value.toLowerCase()) > -1);
            this.setState({ keywordMenu: menu });
          }}
          renderMenu={children => <div className='fui-dropdown fui-keyword-menu'>{children}</div>}
          renderItem={(item, isHighlighted) => (
            <div key={`autocompelte-${item}`} className={`fui-item ${isHighlighted ? 'is-selected' : ''}`}>
              <span className='prefix'>
                <i className='icon-search'></i>
              </span>
              <div className='content' dangerouslySetInnerHTML={{ __html: this.highlightKeyword(item) }}></div>
            </div>
          )}
        />
      </div>
    );
  }
}

KeywordInput.propTypes = {
  path: PropTypes.string,
  title: PropTypes.string,
  placeholder: PropTypes.string,
  keyword: PropTypes.string,
  defaultKeyword: PropTypes.arrayOf(PropTypes.string),
};

export default KeywordInput;

```
{% endtab %}
{% endtabs %}

#### Properties

| 名稱      | 屬性   | 必填 | 選項 | 說明 |
| :-------- | :----- | :--- | :--- | :--- |
| to        | string |      | true |      |
| target    | string |      |      |      |
| className | string |      |      |      |
| children  | node   |      |      |      |

## Loader

```
import Loader from './components/Loader';
<Loader />
```

## Loadmore

components/loadmore.md
* [loadmore](./loadmore.md)

## Marker

```
import Marker from '../Marker'
<Marker
  key={place.id}
  text={place.name}
  lat={place.geometry.location.lat}
  lng={place.geometry.location.lng}
  onClick={() => this.openInfo(place)}
  className={place === this.state.currentStore ? 'active' : ''}
/>
```

## Marquee

```
import Marquee from '../../Marquee';
const marqueeData = props.list.reduce((accumulator, value, index, array) => {
    accumulator.push({ img: value.logo });
    return accumulator;
  }, []);
<Marquee direction={'landscape'} loopData={marqueeData} />
```

#### Properties

| 名稱               | 屬性   | 選項 | 必填 | 說明                                                                                              |
| :----------------- | :----- | :--- | :--- | :------------------------------------------------------------------------------------------------ |
| loop               | bool   |      |      |                                                                                                   |
| loopData           | array  |      | true | retinaImg: PropTypes.string,img: PropTypes.string,height: PropTypes.string,txt: PropTypes.string, |
| getMarquee         | func   |      |      |                                                                                                   |
| direction          | string |      | true |                                                                                                   |
| verticalItemHeight | string |      |      |                                                                                                   |


## Menu

```
import Menu from './Menu';
<Menu
  id={this.props.id}
  anchorEl={this.state.anchorEl}
  keepMounted
  open={Boolean(this.state.anchorEl)}
  onClose={this.readyToClose}>
  <div className='menu-wrapper'>
    {this.props.list.map((item, idx) =>
      Array.isArray(item) ? (
        item.length > 0 && (
          <div className='fui-menu-group' key={'menu-item-group-' + idx + this.props.id}>
            {item.map((it, i) => (
              <Item
                {...it}
                className={`${
                  (this.props.selected && this.props.selected === it.text) ||
                    (!this.props.selected &&
                      (this.state.selectedItem === it.text ||
                        (this.props.value && this.props.value === it.value)))
                    ? 'active'
                    : ''
                  } ${this.props.hasCheck ? 'check-icon' : ''}`}
                key={'menu-item' + idx + this.props.id + i}
                onClick={(e) => this.selectItem(it, idx, e)}>
                {it.text}
              </Item>
            ))}
          </div>
        )
      ) : (
          <Item
            {...item}
            className={`${
              (this.props.selected && this.props.selected === item.text) ||
                (!this.props.selected &&
                  (this.state.selectedItem === item.text || (this.props.value && this.props.value === item.value)))
                ? 'active'
                : ''
              } ${this.props.hasCheck ? 'check-icon' : ''} ${this.getSelected(item)}`}
            key={'menu-item' + this.props.id + idx}
            onClick={(e) => this.selectItem(item, idx, e)}>
            {item.text}
          </Item>
        )
    )}
  </div>
</Menu>
```

#### Properties

| 名稱      | 屬性   | 選項 | 必填 | 說明 |
| :-------- | :----- | :--- | :--- | :--- |
| id        | string |      |      |      |
| anchorEl  | obj    |      |      |      |
| className | string |      |      |      |
| children  | any    |      | true |      |
| onClose   | func   |      |      |      |


## Notification

```
import NotificationBar from '../../Notification';
<NotificationBar
  onLoad={(e) => {
    notibarLoad();
  }}
  className='image-bulletin'
  image={{
    appIcon: '',
    md: '/resources/cbu/cbu-index/img-splash-promo@2x.jpg',
    sm: '/resources/cbu/cbu-index/img-splash-promo.jpg',
    alt: '廣告圖',
  }}
  appText=''
  count={5}
  activityName='小米促銷活動'
  link=''
  type='image-bulletin'
  title='小米體重計2只要 $399'
  click={2}
  second={5}
  target='_blank'
  activityDsc=''
  appDesc=''
  btn='查看詳情'
  sound={true}
/>
```

#### Properties

| 名稱            | 屬性   | 選項 | 必填 | 說明 |
| :-------------- | :----- | :--- | :--- | :--- |
| className       | string |      |      |      |
| message         | string |      |      |      |
| closeIconStyles | obj    |      |      |      |
| sound           | bool   |      |      |      |


## ProgressBar

```
import ProgressBar from '../../components/ProgressBar';
<ProgressBar progress={60} bold={true} color='red' />
```

#### Properties

| 名稱     | 屬性   | 選項 | 必填 | 說明         |
| :------- | :----- | :--- | :--- | :----------- |
| progress | number |      |      |              |
| color    | string |      |      | red  or blue |
| bold     | bool   |      |      |              |

## SearchBoxList

```
import SearchBoxList from '../../components/SearchBoxList';
<SearchBoxList 
  match={this.props.match}
  tab={this.state.currentTab}
  location={this.props.location}
  history={this.props.history}
  searchList={this.state.searchList} 
/>
```

## SelectedArticle

```
import SelectedArticle from '../../components/SelectedArticle';
<SelectedArticle article={[
    {
      id: 'link_01',
      content: 'Dyson TP06智慧空氣清淨機 消除甲醛 為家中長輩、小孩帶來室內清新好空氣',
      link: '#',
    },
    {
      id: 'link_02',
      content: '今天起就讓LG WiFi濕拖清潔機器人幫你做家事！ LG CordZero...',
      link: '#',
    },
    {
      id: 'link_03',
      content: '簡單生活之居家空間三要素，下一個居家IG網紅就是你',
      link: '#',
    },
    {
      id: 'link_04',
      content: '恆壓電控水箱的石頭 S5 Max',
      link: '#',
    },
    {
      id: 'link_05',
      content: '麗克特微笑鬆餅機 | Recolte Smile Baker RSM-1 在家自製鬆餅，好吃又...',
      link: '#',
    },
    {
      id: 'link_06',
      content: '[開箱] 夏天這麼長，風扇更不能隨便！Stadler Form 完整你對夏天的涼爽想像',
      link: '#',
    },
  ]} title='人氣文章' />
```

#### Properties

| 名稱    | 屬性   | 選項 | 必填 | 說明 |
| :------ | :----- | :--- | :--- | :--- |
| title   | string |      |      |      |
| article | array  |      |      |      |


## SingleVideo

```
import SingleVideo from '../../components/SingleVideo';
<SingleVideo
  videoId='9FaXQK51iM8'
  imgSmall='/resources/cbu/img/video-02.jpg'
  imgLarge='/resources/cbu/img/video-02.jpg'
  videoLink='df-gMDkuC08'
  alterVideo={null}
/>
```
#### Properties

| 名稱       | 屬性   | 選項 | 必填 | 說明 |
| :--------- | :----- | :--- | :--- | :--- |
| title      | string |      |      |      |
| videoId    | string |      |      |      |
| imgLarge   | string |      |      |      |
| imgSmall   | string |      |      |      |
| videoLink  | string |      |      |      |
| alterVideo | string |      |      |      |


## SocialMedia
```
import SocialMedia from '../../components/SocialMedia';
<SocialMedia
  theme="light"
  fbLink="#"
  lineLink="#"
  size={48}
  displayContent="分享遠傳優惠"
/>
```

#### Properties

| 名稱           | 屬性   | 選項 | 必填 | 說明 |
| :------------- | :----- | :--- | :--- | :--- |
| fbLink         | string |      |      |      |
| lineLink       | string |      |      |      |
| displayContent | string |      |      |      |
| size           | number |      |      |      |
| theme          | string |      |      |      |


## switch

```
import Switch from '../../Switch';
<Switch
  on='開啟'
  off='關閉'
  name='type'
  checked={form.type.value}
  onChange={(e, checked) => this.inputChange('type', checked)}
/>
```
#### Properties

| 名稱     | 屬性   | 選項 | 必填 | 說明 |
| :------- | :----- | :--- | :--- | :--- |
| checked  | bool   |      |      |      |
| name     | string |      | true |      |
| on       | string |      | true |      |
| off      | string |      | true |      |
| onChange | func   |      |      |      |

## tableBtnModal

```
import Modal from '../../components/tableBtnModal';
<Modal open={this.state.openModal} detailContent={this.state.detailContent} onClose={this.closeModal} />
```
#### Properties

| 名稱          | 屬性 | 選項 | 必填 | 說明 |
| :------------ | :--- | :--- | :--- | :--- |
| open          | bool |      |      |      |
| detailContent | obj  |      |      |      |
| onClose       | func |      |      |      |

## Tooltip

```
import Tooltip from '../../components/Tooltip';
<Tooltip
  parentNode={null}
  content={<i className='icon-information'></i>}
  trigger="click"
  tooltip={card.tooltip} />
```

#### Properties

| 名稱       | 屬性   | 選項 | 必填 | 說明 |
| :--------- | :----- | :--- | :--- | :--- |
| parentNode | obj    |      |      |      |
| content    | node   |      |      |      |
| trigger    | string |      |      |      |
| tooltip    | string |      |      |      |
| className  | string |      |      |      |
| onOpen     | func   |      |      |      |
| position   | string |      |      |      |


## VideoCarousel

```
import VideoCarousel from '../../components/VideoCarousel';
<VideoCarousel
  title="達人帶你玩"
  videos={[
    {
      videoId: '9FaXQK51iM8',
      title: '關西賞櫻超夯打卡景點',
      content: '日本 5 天遠遊卡只要 $199',
      imgSmall: '/resources/cbu/roaming/i-stock-970064046.jpg',
      imgLarge: '/resources/cbu/roaming/i-stock-970064046.jpg',
      videoLink: 'https://youtu.be/u9YYwJKQ0aQ',
      alterVideo: null,
    },
    {
      videoId: '9FaXQK51iM8',
      title: '關西賞櫻超夯打卡景點22',
      content: '日本 5 天遠遊卡只要 $199',
      imgSmall: '/resources/cbu/roaming/i-stock-970064046.jpg',
      imgLarge: '/resources/cbu/roaming/i-stock-970064046.jpg',
      videoLink: 'https://youtu.be/u9YYwJKQ0aQ',
      alterVideo: null,
    },
    {
      videoId: '9FaXQK51iM8',
      title: '關西賞櫻超夯打卡景點33',
      content: '日本 5 天遠遊卡只要 $199',
      imgSmall: '/resources/cbu/roaming/i-stock-970064046.jpg',
      imgLarge: '/resources/cbu/roaming/i-stock-970064046.jpg',
      videoLink: 'https://youtu.be/CwfE29SgSZE',
      alterVideo: 'http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ElephantsDream.mp4',
    }
  ]}
/>
```

#### Properties

| 名稱      | 屬性   | 選項 | 必填 | 說明                                                                                                                                                           |
| :-------- | :----- | :--- | :--- | :------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| className | string |      |      |                                                                                                                                                                |
| title     | string |      |      |                                                                                                                                                                |
| videos    | array  |      | true | videoId: PropTypes.string,title: PropTypes.string,content: PropTypes.string,imgSmall: PropTypes.string,imgLarge: PropTypes.string,alterVideo: PropTypes.string |


## VideoModal

```
import VideoModal from './VideoModal';
openVideoModal = (data) => {
    this.setState({
      modalOpen: true,
      alterVideo: data.alterVideo ? data.alterVideo : null,
      currentVideo: data.videoId,
    });
  };

  closeModal = () => {
    this.setState({
      modalOpen: false,
      alterVideo: '',
      currentVideo: '',
    });
  };
<VideoModal
  open={this.state.modalOpen}
  alterVideo={this.state.alterVideo}
  videoUrl={this.state.currentVideo}
  onClose={this.closeModal}
/>
```

#### Properties

| 名稱       | 屬性   | 選項 | 必填 | 說明 |
| :--------- | :----- | :--- | :--- | :--- |
| open       | bool   |      | true |      |
| videoUrl   | string |      |      |      |
| alterVideo | string |      |      |      |
| onClose    | func   |      | true |      |

## HotWordMulti

```
import HotWord from '../../components/HotWordMulti';
<HotWord {...{
  path: '/roamingPlan/Apply',
  label: '依地區搜尋',
  // hotword: [
  //   '亞洲',
  //   '美洲',
  //   '歐洲',
  //   '大洋洲',
  //   '中東',
  //   '非洲',
  // ],
  // active: [
  //   true,
  //   false,
  //   false,
  //   false,
  //   false
  // ],
  hotword: [
    { showName: '亞洲', value: 'asia',active: true },
    { showName: '美洲', value: 'america',active: false },
    { showName: '歐洲', value: 'urope',active: false },
    { showName: '大洋洲',value: 'australia', active: false },
    { showName: '中東', value: 'middleeast',active: false },
    { showName: '非洲', value: 'africa',active: false },
  ],
}} 
  name="hotword"
  onChange={this.hotWordChange}
/>
```

#### Properties

| 名稱     | 屬性   | 選項 | 必填 | 說明                                           |
| :------- | :----- | :--- | :--- | :--------------------------------------------- |
| path     | string |      |      |                                                |
| hotword  | array  |      |      | text: PropTypes.string,active: PropTypes.bool, |
| onChange | func   |      |      |                                                |

```
HotWord.propTypes = {
  path: PropTypes.string,
  hotword: PropTypes.arrayOf(
    PropTypes.shape({
      text: PropTypes.string,
      active: PropTypes.bool,
    })
  ),
  onChange: PropTypes.func
};
```

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