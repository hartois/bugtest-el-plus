<template>
  <div class="hello">
    <el-menu
        mode="horizontal"
        class="menu-list__internal"
    >
      <template v-for="cat in items">
        <template v-if="!cat.hidden">
          <sub-menu v-if="cat.children && cat.children.length" :items="cat.children" :index="'root-'+cat.id" :key="'root-'+cat.id">
            <template #title>
              <a :href="cat.url">{{ cat.name }}</a>
            </template>
          </sub-menu>
          <a v-else :href="cat.url" :key="'root-'+cat.id">
            <el-menu-item :index="'root-'+cat.id">
              {{ cat.name }}
            </el-menu-item>
          </a>
        </template>
      </template>
    </el-menu>
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
import SubMenu from "./SubMenu";

export default {
  name: 'HelloWorld',
  components: { SubMenu },
  props: {
    msg: String
  },
  data() {
    return {
      index: 'sub1',
      items: [
        {
          "id": "1-85217",
          "name": "item-85217",
          "url": "/path/85217",
          "children": [
            {
              "id": "1-50484",
              "name": "item-50484",
              "url": "/path/50484",
              "children": [
                {
                  "id": "1-73919",
                  "name": "item-73919",
                  "url": "/path/73919",
                  "children": []
                },
                {
                  "id": "2-26248",
                  "name": "item-26248",
                  "url": "/path/26248",
                  "children": []
                },
                {
                  "id": "3-61988",
                  "name": "item-61988",
                  "url": "/path/61988",
                  "children": []
                },
                {
                  "id": "4-17019",
                  "name": "item-17019",
                  "url": "/path/17019",
                  "children": []
                },
                {
                  "id": "5-88655",
                  "name": "item-88655",
                  "url": "/path/88655",
                  "children": []
                }
              ]
            },
            {
              "id": "2-96711",
              "name": "item-96711",
              "url": "/path/96711",
              "children": [
                {
                  "id": "1-48283",
                  "name": "item-48283",
                  "url": "/path/48283",
                  "children": []
                },
                {
                  "id": "2-87999",
                  "name": "item-87999",
                  "url": "/path/87999",
                  "children": []
                },
                {
                  "id": "3-63730",
                  "name": "item-63730",
                  "url": "/path/63730",
                  "children": []
                },
                {
                  "id": "4-95449",
                  "name": "item-95449",
                  "url": "/path/95449",
                  "children": []
                },
                {
                  "id": "5-87416",
                  "name": "item-87416",
                  "url": "/path/87416",
                  "children": []
                }
              ]
            },
            {
              "id": "3-33076",
              "name": "item-33076",
              "url": "/path/33076",
              "children": [
                {
                  "id": "1-44640",
                  "name": "item-44640",
                  "url": "/path/44640",
                  "children": []
                },
                {
                  "id": "2-38983",
                  "name": "item-38983",
                  "url": "/path/38983",
                  "children": []
                },
                {
                  "id": "3-52710",
                  "name": "item-52710",
                  "url": "/path/52710",
                  "children": []
                },
                {
                  "id": "4-38782",
                  "name": "item-38782",
                  "url": "/path/38782",
                  "children": []
                },
                {
                  "id": "5-36436",
                  "name": "item-36436",
                  "url": "/path/36436",
                  "children": []
                }
              ]
            },
            {
              "id": "4-40443",
              "name": "item-40443",
              "url": "/path/40443",
              "children": [
                {
                  "id": "1-52892",
                  "name": "item-52892",
                  "url": "/path/52892",
                  "children": []
                },
                {
                  "id": "2-25167",
                  "name": "item-25167",
                  "url": "/path/25167",
                  "children": []
                },
                {
                  "id": "3-21118",
                  "name": "item-21118",
                  "url": "/path/21118",
                  "children": []
                },
                {
                  "id": "4-22000",
                  "name": "item-22000",
                  "url": "/path/22000",
                  "children": []
                },
                {
                  "id": "5-78318",
                  "name": "item-78318",
                  "url": "/path/78318",
                  "children": []
                }
              ]
            },
            {
              "id": "5-55351",
              "name": "item-55351",
              "url": "/path/55351",
              "children": [
                {
                  "id": "1-23903",
                  "name": "item-23903",
                  "url": "/path/23903",
                  "children": []
                },
                {
                  "id": "2-31318",
                  "name": "item-31318",
                  "url": "/path/31318",
                  "children": []
                },
                {
                  "id": "3-18563",
                  "name": "item-18563",
                  "url": "/path/18563",
                  "children": []
                },
                {
                  "id": "4-96727",
                  "name": "item-96727",
                  "url": "/path/96727",
                  "children": []
                },
                {
                  "id": "5-87507",
                  "name": "item-87507",
                  "url": "/path/87507",
                  "children": []
                }
              ]
            }
          ]
        },
        {
          "id": "2-72900",
          "name": "item-72900",
          "url": "/path/72900",
          "children": [
            {
              "id": "1-36962",
              "name": "item-36962",
              "url": "/path/36962",
              "children": [
                {
                  "id": "1-77498",
                  "name": "item-77498",
                  "url": "/path/77498",
                  "children": []
                },
                {
                  "id": "2-92239",
                  "name": "item-92239",
                  "url": "/path/92239",
                  "children": []
                },
                {
                  "id": "3-44592",
                  "name": "item-44592",
                  "url": "/path/44592",
                  "children": []
                },
                {
                  "id": "4-42319",
                  "name": "item-42319",
                  "url": "/path/42319",
                  "children": []
                },
                {
                  "id": "5-47728",
                  "name": "item-47728",
                  "url": "/path/47728",
                  "children": []
                }
              ]
            },
            {
              "id": "2-19104",
              "name": "item-19104",
              "url": "/path/19104",
              "children": [
                {
                  "id": "1-67202",
                  "name": "item-67202",
                  "url": "/path/67202",
                  "children": []
                },
                {
                  "id": "2-54835",
                  "name": "item-54835",
                  "url": "/path/54835",
                  "children": []
                },
                {
                  "id": "3-66974",
                  "name": "item-66974",
                  "url": "/path/66974",
                  "children": []
                },
                {
                  "id": "4-14020",
                  "name": "item-14020",
                  "url": "/path/14020",
                  "children": []
                },
                {
                  "id": "5-15907",
                  "name": "item-15907",
                  "url": "/path/15907",
                  "children": []
                }
              ]
            },
            {
              "id": "3-32575",
              "name": "item-32575",
              "url": "/path/32575",
              "children": [
                {
                  "id": "1-26593",
                  "name": "item-26593",
                  "url": "/path/26593",
                  "children": []
                },
                {
                  "id": "2-18723",
                  "name": "item-18723",
                  "url": "/path/18723",
                  "children": []
                },
                {
                  "id": "3-35902",
                  "name": "item-35902",
                  "url": "/path/35902",
                  "children": []
                },
                {
                  "id": "4-82496",
                  "name": "item-82496",
                  "url": "/path/82496",
                  "children": []
                },
                {
                  "id": "5-67442",
                  "name": "item-67442",
                  "url": "/path/67442",
                  "children": []
                }
              ]
            },
            {
              "id": "4-32038",
              "name": "item-32038",
              "url": "/path/32038",
              "children": [
                {
                  "id": "1-72190",
                  "name": "item-72190",
                  "url": "/path/72190",
                  "children": []
                },
                {
                  "id": "2-31418",
                  "name": "item-31418",
                  "url": "/path/31418",
                  "children": []
                },
                {
                  "id": "3-20227",
                  "name": "item-20227",
                  "url": "/path/20227",
                  "children": []
                },
                {
                  "id": "4-58960",
                  "name": "item-58960",
                  "url": "/path/58960",
                  "children": []
                },
                {
                  "id": "5-42275",
                  "name": "item-42275",
                  "url": "/path/42275",
                  "children": []
                }
              ]
            },
            {
              "id": "5-61686",
              "name": "item-61686",
              "url": "/path/61686",
              "children": [
                {
                  "id": "1-47980",
                  "name": "item-47980",
                  "url": "/path/47980",
                  "children": []
                },
                {
                  "id": "2-28702",
                  "name": "item-28702",
                  "url": "/path/28702",
                  "children": []
                },
                {
                  "id": "3-72016",
                  "name": "item-72016",
                  "url": "/path/72016",
                  "children": []
                },
                {
                  "id": "4-89188",
                  "name": "item-89188",
                  "url": "/path/89188",
                  "children": []
                },
                {
                  "id": "5-23151",
                  "name": "item-23151",
                  "url": "/path/23151",
                  "children": []
                }
              ]
            }
          ]
        },
        {
          "id": "3-61568",
          "name": "item-61568",
          "url": "/path/61568",
          "children": [
            {
              "id": "1-59479",
              "name": "item-59479",
              "url": "/path/59479",
              "children": [
                {
                  "id": "1-53726",
                  "name": "item-53726",
                  "url": "/path/53726",
                  "children": []
                },
                {
                  "id": "2-78310",
                  "name": "item-78310",
                  "url": "/path/78310",
                  "children": []
                },
                {
                  "id": "3-14467",
                  "name": "item-14467",
                  "url": "/path/14467",
                  "children": []
                },
                {
                  "id": "4-63015",
                  "name": "item-63015",
                  "url": "/path/63015",
                  "children": []
                },
                {
                  "id": "5-14591",
                  "name": "item-14591",
                  "url": "/path/14591",
                  "children": []
                }
              ]
            },
            {
              "id": "2-76060",
              "name": "item-76060",
              "url": "/path/76060",
              "children": [
                {
                  "id": "1-44621",
                  "name": "item-44621",
                  "url": "/path/44621",
                  "children": []
                },
                {
                  "id": "2-96577",
                  "name": "item-96577",
                  "url": "/path/96577",
                  "children": []
                },
                {
                  "id": "3-15428",
                  "name": "item-15428",
                  "url": "/path/15428",
                  "children": []
                },
                {
                  "id": "4-39067",
                  "name": "item-39067",
                  "url": "/path/39067",
                  "children": []
                },
                {
                  "id": "5-70601",
                  "name": "item-70601",
                  "url": "/path/70601",
                  "children": []
                }
              ]
            },
            {
              "id": "3-62898",
              "name": "item-62898",
              "url": "/path/62898",
              "children": [
                {
                  "id": "1-97464",
                  "name": "item-97464",
                  "url": "/path/97464",
                  "children": []
                },
                {
                  "id": "2-79321",
                  "name": "item-79321",
                  "url": "/path/79321",
                  "children": []
                },
                {
                  "id": "3-33234",
                  "name": "item-33234",
                  "url": "/path/33234",
                  "children": []
                },
                {
                  "id": "4-97379",
                  "name": "item-97379",
                  "url": "/path/97379",
                  "children": []
                },
                {
                  "id": "5-70001",
                  "name": "item-70001",
                  "url": "/path/70001",
                  "children": []
                }
              ]
            },
            {
              "id": "4-15436",
              "name": "item-15436",
              "url": "/path/15436",
              "children": [
                {
                  "id": "1-52829",
                  "name": "item-52829",
                  "url": "/path/52829",
                  "children": []
                },
                {
                  "id": "2-81339",
                  "name": "item-81339",
                  "url": "/path/81339",
                  "children": []
                },
                {
                  "id": "3-19527",
                  "name": "item-19527",
                  "url": "/path/19527",
                  "children": []
                },
                {
                  "id": "4-27515",
                  "name": "item-27515",
                  "url": "/path/27515",
                  "children": []
                },
                {
                  "id": "5-27639",
                  "name": "item-27639",
                  "url": "/path/27639",
                  "children": []
                }
              ]
            },
            {
              "id": "5-44386",
              "name": "item-44386",
              "url": "/path/44386",
              "children": [
                {
                  "id": "1-21436",
                  "name": "item-21436",
                  "url": "/path/21436",
                  "children": []
                },
                {
                  "id": "2-38897",
                  "name": "item-38897",
                  "url": "/path/38897",
                  "children": []
                },
                {
                  "id": "3-93034",
                  "name": "item-93034",
                  "url": "/path/93034",
                  "children": []
                },
                {
                  "id": "4-61212",
                  "name": "item-61212",
                  "url": "/path/61212",
                  "children": []
                },
                {
                  "id": "5-66418",
                  "name": "item-66418",
                  "url": "/path/66418",
                  "children": []
                }
              ]
            }
          ]
        },
        {
          "id": "4-84512",
          "name": "item-84512",
          "url": "/path/84512",
          "children": [
            {
              "id": "1-25530",
              "name": "item-25530",
              "url": "/path/25530",
              "children": [
                {
                  "id": "1-12991",
                  "name": "item-12991",
                  "url": "/path/12991",
                  "children": []
                },
                {
                  "id": "2-68533",
                  "name": "item-68533",
                  "url": "/path/68533",
                  "children": []
                },
                {
                  "id": "3-54558",
                  "name": "item-54558",
                  "url": "/path/54558",
                  "children": []
                },
                {
                  "id": "4-45747",
                  "name": "item-45747",
                  "url": "/path/45747",
                  "children": []
                },
                {
                  "id": "5-12162",
                  "name": "item-12162",
                  "url": "/path/12162",
                  "children": []
                }
              ]
            },
            {
              "id": "2-64550",
              "name": "item-64550",
              "url": "/path/64550",
              "children": [
                {
                  "id": "1-75448",
                  "name": "item-75448",
                  "url": "/path/75448",
                  "children": []
                },
                {
                  "id": "2-82262",
                  "name": "item-82262",
                  "url": "/path/82262",
                  "children": []
                },
                {
                  "id": "3-84364",
                  "name": "item-84364",
                  "url": "/path/84364",
                  "children": []
                },
                {
                  "id": "4-18846",
                  "name": "item-18846",
                  "url": "/path/18846",
                  "children": []
                },
                {
                  "id": "5-29864",
                  "name": "item-29864",
                  "url": "/path/29864",
                  "children": []
                }
              ]
            },
            {
              "id": "3-98639",
              "name": "item-98639",
              "url": "/path/98639",
              "children": [
                {
                  "id": "1-43032",
                  "name": "item-43032",
                  "url": "/path/43032",
                  "children": []
                },
                {
                  "id": "2-59321",
                  "name": "item-59321",
                  "url": "/path/59321",
                  "children": []
                },
                {
                  "id": "3-13503",
                  "name": "item-13503",
                  "url": "/path/13503",
                  "children": []
                },
                {
                  "id": "4-87831",
                  "name": "item-87831",
                  "url": "/path/87831",
                  "children": []
                },
                {
                  "id": "5-32790",
                  "name": "item-32790",
                  "url": "/path/32790",
                  "children": []
                }
              ]
            },
            {
              "id": "4-90411",
              "name": "item-90411",
              "url": "/path/90411",
              "children": [
                {
                  "id": "1-58918",
                  "name": "item-58918",
                  "url": "/path/58918",
                  "children": []
                },
                {
                  "id": "2-31587",
                  "name": "item-31587",
                  "url": "/path/31587",
                  "children": []
                },
                {
                  "id": "3-58794",
                  "name": "item-58794",
                  "url": "/path/58794",
                  "children": []
                },
                {
                  "id": "4-98632",
                  "name": "item-98632",
                  "url": "/path/98632",
                  "children": []
                },
                {
                  "id": "5-48100",
                  "name": "item-48100",
                  "url": "/path/48100",
                  "children": []
                }
              ]
            },
            {
              "id": "5-69186",
              "name": "item-69186",
              "url": "/path/69186",
              "children": [
                {
                  "id": "1-43084",
                  "name": "item-43084",
                  "url": "/path/43084",
                  "children": []
                },
                {
                  "id": "2-98632",
                  "name": "item-98632",
                  "url": "/path/98632",
                  "children": []
                },
                {
                  "id": "3-34454",
                  "name": "item-34454",
                  "url": "/path/34454",
                  "children": []
                },
                {
                  "id": "4-66883",
                  "name": "item-66883",
                  "url": "/path/66883",
                  "children": []
                },
                {
                  "id": "5-10997",
                  "name": "item-10997",
                  "url": "/path/10997",
                  "children": []
                }
              ]
            }
          ]
        },
        {
          "id": "5-15059",
          "name": "item-15059",
          "url": "/path/15059",
          "children": [
            {
              "id": "1-79849",
              "name": "item-79849",
              "url": "/path/79849",
              "children": [
                {
                  "id": "1-39026",
                  "name": "item-39026",
                  "url": "/path/39026",
                  "children": []
                },
                {
                  "id": "2-29184",
                  "name": "item-29184",
                  "url": "/path/29184",
                  "children": []
                },
                {
                  "id": "3-25230",
                  "name": "item-25230",
                  "url": "/path/25230",
                  "children": []
                },
                {
                  "id": "4-28359",
                  "name": "item-28359",
                  "url": "/path/28359",
                  "children": []
                },
                {
                  "id": "5-82368",
                  "name": "item-82368",
                  "url": "/path/82368",
                  "children": []
                }
              ]
            },
            {
              "id": "2-80652",
              "name": "item-80652",
              "url": "/path/80652",
              "children": [
                {
                  "id": "1-80455",
                  "name": "item-80455",
                  "url": "/path/80455",
                  "children": []
                },
                {
                  "id": "2-48631",
                  "name": "item-48631",
                  "url": "/path/48631",
                  "children": []
                },
                {
                  "id": "3-53894",
                  "name": "item-53894",
                  "url": "/path/53894",
                  "children": []
                },
                {
                  "id": "4-61974",
                  "name": "item-61974",
                  "url": "/path/61974",
                  "children": []
                },
                {
                  "id": "5-85801",
                  "name": "item-85801",
                  "url": "/path/85801",
                  "children": []
                }
              ]
            },
            {
              "id": "3-64530",
              "name": "item-64530",
              "url": "/path/64530",
              "children": [
                {
                  "id": "1-50017",
                  "name": "item-50017",
                  "url": "/path/50017",
                  "children": []
                },
                {
                  "id": "2-51665",
                  "name": "item-51665",
                  "url": "/path/51665",
                  "children": []
                },
                {
                  "id": "3-35799",
                  "name": "item-35799",
                  "url": "/path/35799",
                  "children": []
                },
                {
                  "id": "4-13835",
                  "name": "item-13835",
                  "url": "/path/13835",
                  "children": []
                },
                {
                  "id": "5-21312",
                  "name": "item-21312",
                  "url": "/path/21312",
                  "children": []
                }
              ]
            },
            {
              "id": "4-69322",
              "name": "item-69322",
              "url": "/path/69322",
              "children": [
                {
                  "id": "1-52926",
                  "name": "item-52926",
                  "url": "/path/52926",
                  "children": []
                },
                {
                  "id": "2-99251",
                  "name": "item-99251",
                  "url": "/path/99251",
                  "children": []
                },
                {
                  "id": "3-42765",
                  "name": "item-42765",
                  "url": "/path/42765",
                  "children": []
                },
                {
                  "id": "4-21626",
                  "name": "item-21626",
                  "url": "/path/21626",
                  "children": []
                },
                {
                  "id": "5-75415",
                  "name": "item-75415",
                  "url": "/path/75415",
                  "children": []
                }
              ]
            },
            {
              "id": "5-27565",
              "name": "item-27565",
              "url": "/path/27565",
              "children": [
                {
                  "id": "1-48167",
                  "name": "item-48167",
                  "url": "/path/48167",
                  "children": []
                },
                {
                  "id": "2-64141",
                  "name": "item-64141",
                  "url": "/path/64141",
                  "children": []
                },
                {
                  "id": "3-17159",
                  "name": "item-17159",
                  "url": "/path/17159",
                  "children": []
                },
                {
                  "id": "4-90549",
                  "name": "item-90549",
                  "url": "/path/90549",
                  "children": []
                },
                {
                  "id": "5-90082",
                  "name": "item-90082",
                  "url": "/path/90082",
                  "children": []
                }
              ]
            }
          ]
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
