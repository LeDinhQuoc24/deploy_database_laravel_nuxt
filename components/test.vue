<template>
  <div >
    <h1>獲得スタッフ一覧</h1>
    <div class="wrap">
      <div class="content">
        <h2 class="mt-0">アカウント詳細</h2>
        <div class="table">
          <div class="col-02">
            <div class="th wf125"><p class="ttl">ライセンスID</p></div>
            <div class="inner"><p>ABCD55555</p></div>
          </div>
          <div class="col-02">
            <div class="th wf125"><p class="ttl">獲得取次店</p></div>
            <div class="inner inner--form flex align-ic">
              <p class="flex-01">○○○○○○○○○○○○</p>
              <a @click.prevent="showModal = !showModal"

                 class="btn-tool wf45 ml-15 open-modal"
                 tabindex="0"
                 role="button">選択</a>

              <!-- Modal Start -->
              <Modal
                id="modal"
                v-model="showModal"
                wrapper="modal-wrap"
              >

                <h2  >取次店選択</h2>
                <div class="table">
                  <div class="col-02">
                    <div class="th wf150"><p class="ttl">名前</p></div>
                    <div class="inner flex flex-01"><p>○○○○○○○○○○○○○○○○○○</p></div>
                  </div>
                  <div class="col-02">
                    <div class="th wf150"><p class="ttl">フリガナ</p></div>
                    <div class="inner flex flex-01"><p>○○○○○○○○○○○○○○○○○○</p></div>
                  </div>
                </div>

                <button class="btn_main-color wf190 btn-bk-arrow mt-30 mb-20" type="button"
                        　onclick="location.href=''">登録する
                </button>
                <div class="table">
                  <div class="col-02">
                    <div class="th wf150"><p class="ttl">獲得手法</p></div>
                    <div class="inner inner--form flex flex-01">
                      <div class="pw-select sl01 flex-01">
                        <select name="">
                          <option value="選択してください" selected="">選択してください</option>
                          <option value="獲得手法">獲得手法</option>
                        </select>
                      </div>
                      <a href="" class="btn-tool ml-15" tabindex="0" role="button">絞込</a>
                    </div>
                  </div>
                  <div class="col-02">
                    <div class="th wf150"><p class="ttl">取次店名</p></div>
                    <div class="inner inner--form flex flex-01">
                      <input class="pw-input flex-01" type="text" name="" placeholder="">
                      <a href="" class="btn-tool ml-15" tabindex="0" role="button">絞込</a>
                    </div>
                  </div>
                  <div class="col-02">
                    <div class="th wf150"><p class="ttl">コミッション区分</p></div>
                    <div class="inner-row-01 inner--form flex flex-01">
                      <div class="pw-select sl01 flex-01">
                        <select name="">
                          <option value="選択してください" selected="">選択してください</option>
                          <option value="コミッション区分">コミッション区分</option>
                        </select>
                      </div>
                      <a href="" class="btn-tool ml-15" tabindex="0" role="button">絞込</a>
                    </div>
                  </div>
                </div>
                <div class="table mt-30">
                  <div class="col-02">
                    <div class="th-row-01 wf150"><p class="ttl">獲得取次店</p></div>
                    <div class="inner-row-01 inner--form flex flex-01" v-click-outside="hide">
                      <div class="ms-parent">
                        <div class="ms-choice" tabindex="0"
                             @click="show('open1','arrow')">
                          <span style="width: 269px;"> options </span>
                          <div class="" v-bind:class="{open: arrow}">
                          </div>
                        </div>

                        <div v-if="open1" class="ms-drop" style="width: 289px; "
                             :style="{display:selected}">
                          <select-box-multip :arrayOptions="arrayOptions"></select-box-multip>
                        </div>
                      </div>
                      <a href="" class="btn-tool ml-15" tabindex="0" role="button">追加</a>
                    </div>

                  </div>
                </div>
                <div class="table mt-30">
                  <div class="col-th flex col-02">
                    <div class="th flex-01"><p class="ttl">表示順</p></div>
                    <div class="th wf45 align-c"><p class="ttl">削除</p></div>
                  </div>
                  <div class="col-02">
                    <div class="inner flex-01 th-border-r"><p>○○○○○○○○○○○○</p></div>
                    <div class="inner wf45 flex jc-c"><input type="checkbox" name="" value="削除する"
                                                             id="delete"
                                                             class="check check--single"><label
                      for="delete"></label>
                    </div>
                  </div>
                </div>
                <button class="btn_main-color wf190 btn-bk-arrow mt-20" type="button"
                        　onclick="location.href=''">登録する
                </button>

              </Modal>
              <!-- Modal end -->
            </div>
          </div>
          <div class="col-02">
            <div class="th wf125"><p class="ttl">名前</p></div>
            <div class="th th-name"><p class="ttl">姓</p></div>
            <div class="inner">
              <p>富士</p>
            </div>
            <div class="th th-name"><p class="ttl">名</p></div>
            <div class="inner">
              <p>山麓</p>
            </div>
          </div>
          <div class="col-02">
            <div class="th wf125"><p class="ttl">フリガナ</p></div>
            <div class="th th-name"><p class="ttl">セイ</p></div>
            <div class="inner">
              <p>フジ</p>
            </div>
            <div class="th th-name"><p class="ttl">メイ</p></div>
            <div class="inner">
              <p>サンロク</p>
            </div>
          </div>
          <div class="col-02">
            <div class="th wf125"><p class="ttl">ログインID</p></div>
            <div class="inner">
              <p class="flex-01">ABCD55555</p>
            </div>
          </div>
          <div class="col-02">
            <div class="th wf125"><p class="ttl">販売員証有無</p></div>
            <div class="inner--row">
              <p>販売員証必要</p>
              <p>販売員証不要（○○○○○○○○○○のため）</p>
            </div>
          </div>
          <div class="col-02">
            <div class="th wf125"><p class="ttl">性別</p></div>
            <div class="inner">
              <p>男性／女性／指定しない</p>
            </div>
          </div>
          <div class="col-02">
            <div class="th wf125"><p class="ttl">表示順</p></div>
            <div class="inner">
              <p>1</p>
            </div>
          </div>
          <div class="col-02">
            <div class="th wf125"><p class="ttl">コメント</p></div>
            <div class="inner">
              <p>コメントが入ります。コメントが入ります。コメントが入ります。コメントが入ります。コメントが入ります。コメントが入ります。</p>
            </div>
          </div>
        </div><!--table-->
      </div><!--content-->
      <div class="flex jc-sb wf-content">
        <nuxt-link to="/10-01" tag="button" class="btn_bk-color wf190 btn-bk-arrow-l mt-30">戻る</nuxt-link>
      </div>
    </div><!--wrap-->
  </div>
</template>
<script>
import ClickOutside from 'vue-click-outside'
export default {
  layout:'layout4',
  data() {
    return {
      showModal: false,
      items: [
        {
          id: 1,
          value: "獲得取次店A",
          check: false
        },
        {
          id: 2,
          value: "獲得取次店B",
          check: false
        },
        {
          id: 3,
          value: "獲得取次店C",
          check: false
        },
        {
          id: 4,
          value: "イオンモール西船橋店",
          check: false
        },
      ]
      ,
      showOption: false,
      selected: 'none',
      arrayOptions: [],
      arrow: false,
      open1: false,
      options: ""
    }
  },
  methods: {
    openOptions: function () {
      this.showOption = !this.showOption;
      this.showOption ? this.selected = 'block' : this.selected = 'none';
    },
    show(open1, arrow) {
      this.open1 = !this.open1;
      this.arrow = !this.arrow;
      this.openOptions();
    },
    hide(){
      if (this.open1) {
        this.open1 = !this.open1;
        this.arrow = !this.arrow;
        this.openOptions();
      }
    },

    toStringOptions() {
      this.options = "";
      this.arrayOptions=this.arrayOptions.sort((function(a, b){
        if(a.id < b.id) { return -1; }
        if(a.id > b.id) { return 1; }
        return 0;
      }));
      this.arrayOptions.forEach((element) => {
        this.arrayOptions[this.arrayOptions.length - 1] === element ? this.options += element.value : this.options += element.value + ",";
      });
    },
  },
  created() {
    this.$nuxt.$on('addArrayParent', (arrayOptions) => {
      this.arrayOptions=arrayOptions;
      this.toStringOptions();
    })
  },
  directives: {
    ClickOutside
  }
}
</script>
