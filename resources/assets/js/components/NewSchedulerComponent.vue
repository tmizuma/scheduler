<style>
    .required {
        color: red;
    }
</style>
<template>
<div class="">
    <div class="container">
        <h3>予約画面</h3>
            <div class="form-group">
                <label class="control-label col-xs-2">会議室名<span class="required"> *</span></label>
                <div class="col-xs-5">
                    <select v-model="room_id" class="form-control">
                        <option v-for="room in roomList" v-bind:value="room.id">{{ room.name }}</option>
                    </select>
                </div>
            </div>
            <div class="form-group">
                <label class="control-label col-xs-2">日付<span class="required"> *</span></label>
                <div class="col-xs-5">
                    <el-date-picker
                            v-model="target_date"
                            type="date"
                            placeholder="日付を選んでください">
                    </el-date-picker>
                </div>
            </div>
            <div class="form-group">
                <label class="control-label">予約時間<span class="required"> *</span></label>
                <div style="display: table">
                    <div style="display: table-cell; width: 50%;">
                        <select v-model="start_time" class="form-control">
                            <option value="00:00">00:00</option>
                            <option value="00:15">00:15</option>
                            <option value="00:30">00:30</option>
                            <option value="00:45">00:45</option>
                            <option value="01:00">01:00</option>
                            <option value="01:15">01:15</option>
                            <option value="01:30">01:30</option>
                            <option value="01:45">01:45</option>
                            <option value="02:00">02:00</option>
                            <option value="02:15">02:15</option>
                            <option value="02:30">02:30</option>
                            <option value="02:45">02:45</option>
                            <option value="03:00">03:00</option>
                            <option value="03:15">03:15</option>
                            <option value="03:30">03:30</option>
                            <option value="03:45">03:45</option>
                            <option value="04:00">04:00</option>
                            <option value="04:15">04:15</option>
                            <option value="04:30">04:30</option>
                            <option value="04:45">04:45</option>
                            <option value="05:00">05:00</option>
                            <option value="05:15">05:15</option>
                            <option value="05:30">05:30</option>
                            <option value="05:45">05:45</option>
                            <option value="06:00">06:00</option>
                            <option value="06:15">06:15</option>
                            <option value="06:30">06:30</option>
                            <option value="06:45">06:45</option>
                            <option value="07:00">07:00</option>
                            <option value="07:15">07:15</option>
                            <option value="07:30">07:30</option>
                            <option value="07:45">07:45</option>
                            <option value="08:00">08:00</option>
                            <option value="08:15">08:15</option>
                            <option value="08:30">08:30</option>
                            <option value="08:45">08:45</option>
                            <option value="09:00">09:00</option>
                            <option value="09:15">09:15</option>
                            <option value="09:30">09:30</option>
                            <option value="09:45">09:45</option>
                            <option value="10:00">10:00</option>
                            <option value="10:15">10:15</option>
                            <option value="10:30">10:30</option>
                            <option value="10:45">10:45</option>
                            <option value="11:00">11:00</option>
                            <option value="11:15">11:15</option>
                            <option value="11:30">11:30</option>
                            <option value="11:45">11:45</option>
                            <option value="12:00">12:00</option>
                            <option value="12:15">12:15</option>
                            <option value="12:30">12:30</option>
                            <option value="12:45">12:45</option>
                            <option value="13:00">13:00</option>
                            <option value="13:15">13:15</option>
                            <option value="13:30">13:30</option>
                            <option value="13:45">13:45</option>
                            <option value="14:00">14:00</option>
                            <option value="14:15">14:15</option>
                            <option value="14:30">14:30</option>
                            <option value="14:45">14:45</option>
                            <option value="15:00">15:00</option>
                            <option value="15:15">15:15</option>
                            <option value="15:30">15:30</option>
                            <option value="15:45">15:45</option>
                            <option value="16:00">16:00</option>
                            <option value="16:15">16:15</option>
                            <option value="16:30">16:30</option>
                            <option value="16:45">16:45</option>
                            <option value="17:00">17:00</option>
                            <option value="17:15">17:15</option>
                            <option value="17:30">17:30</option>
                            <option value="17:45">17:45</option>
                            <option value="18:00">18:00</option>
                            <option value="18:15">18:15</option>
                            <option value="18:30">18:30</option>
                            <option value="18:45">18:45</option>
                            <option value="19:00">19:00</option>
                            <option value="19:15">19:15</option>
                            <option value="19:30">19:30</option>
                            <option value="19:45">19:45</option>
                            <option value="20:00">20:00</option>
                            <option value="20:15">20:15</option>
                            <option value="20:30">20:30</option>
                            <option value="20:45">20:45</option>
                            <option value="21:00">21:00</option>
                            <option value="21:15">21:15</option>
                            <option value="21:30">21:30</option>
                            <option value="21:45">21:45</option>
                            <option value="22:00">22:00</option>
                            <option value="22:15">22:15</option>
                            <option value="22:30">22:30</option>
                            <option value="22:45">22:45</option>
                            <option value="23:00">23:00</option>
                            <option value="23:15">23:15</option>
                            <option value="23:30">23:30</option>
                            <option value="23:45">23:45</option>
                        </select>
                    </div>　〜　
                    <div style="display: table-cell; width: 50%;">
                        <select v-model="end_time" class="form-control">
                                <option value="00:00">00:00</option>
                                <option value="00:15">00:15</option>
                                <option value="00:30">00:30</option>
                                <option value="00:45">00:45</option>
                                <option value="01:00">01:00</option>
                                <option value="01:15">01:15</option>
                                <option value="01:30">01:30</option>
                                <option value="01:45">01:45</option>
                                <option value="02:00">02:00</option>
                                <option value="02:15">02:15</option>
                                <option value="02:30">02:30</option>
                                <option value="02:45">02:45</option>
                                <option value="03:00">03:00</option>
                                <option value="03:15">03:15</option>
                                <option value="03:30">03:30</option>
                                <option value="03:45">03:45</option>
                                <option value="04:00">04:00</option>
                                <option value="04:15">04:15</option>
                                <option value="04:30">04:30</option>
                                <option value="04:45">04:45</option>
                                <option value="05:00">05:00</option>
                                <option value="05:15">05:15</option>
                                <option value="05:30">05:30</option>
                                <option value="05:45">05:45</option>
                                <option value="06:00">06:00</option>
                                <option value="06:15">06:15</option>
                                <option value="06:30">06:30</option>
                                <option value="06:45">06:45</option>
                                <option value="07:00">07:00</option>
                                <option value="07:15">07:15</option>
                                <option value="07:30">07:30</option>
                                <option value="07:45">07:45</option>
                                <option value="08:00">08:00</option>
                                <option value="08:15">08:15</option>
                                <option value="08:30">08:30</option>
                                <option value="08:45">08:45</option>
                                <option value="09:00">09:00</option>
                                <option value="09:15">09:15</option>
                                <option value="09:30">09:30</option>
                                <option value="09:45">09:45</option>
                                <option value="10:00">10:00</option>
                                <option value="10:15">10:15</option>
                                <option value="10:30">10:30</option>
                                <option value="10:45">10:45</option>
                                <option value="11:00">11:00</option>
                                <option value="11:15">11:15</option>
                                <option value="11:30">11:30</option>
                                <option value="11:45">11:45</option>
                                <option value="12:00">12:00</option>
                                <option value="12:15">12:15</option>
                                <option value="12:30">12:30</option>
                                <option value="12:45">12:45</option>
                                <option value="13:00">13:00</option>
                                <option value="13:15">13:15</option>
                                <option value="13:30">13:30</option>
                                <option value="13:45">13:45</option>
                                <option value="14:00">14:00</option>
                                <option value="14:15">14:15</option>
                                <option value="14:30">14:30</option>
                                <option value="14:45">14:45</option>
                                <option value="15:00">15:00</option>
                                <option value="15:15">15:15</option>
                                <option value="15:30">15:30</option>
                                <option value="15:45">15:45</option>
                                <option value="16:00">16:00</option>
                                <option value="16:15">16:15</option>
                                <option value="16:30">16:30</option>
                                <option value="16:45">16:45</option>
                                <option value="17:00">17:00</option>
                                <option value="17:15">17:15</option>
                                <option value="17:30">17:30</option>
                                <option value="17:45">17:45</option>
                                <option value="18:00">18:00</option>
                                <option value="18:15">18:15</option>
                                <option value="18:30">18:30</option>
                                <option value="18:45">18:45</option>
                                <option value="19:00">19:00</option>
                                <option value="19:15">19:15</option>
                                <option value="19:30">19:30</option>
                                <option value="19:45">19:45</option>
                                <option value="20:00">20:00</option>
                                <option value="20:15">20:15</option>
                                <option value="20:30">20:30</option>
                                <option value="20:45">20:45</option>
                                <option value="21:00">21:00</option>
                                <option value="21:15">21:15</option>
                                <option value="21:30">21:30</option>
                                <option value="21:45">21:45</option>
                                <option value="22:00">22:00</option>
                                <option value="22:15">22:15</option>
                                <option value="22:30">22:30</option>
                                <option value="22:45">22:45</option>
                                <option value="23:00">23:00</option>
                                <option value="23:15">23:15</option>
                                <option value="23:30">23:30</option>
                                <option value="23:45">23:45</option>
                        </select>
                    </div>
            </div>
            </div>
            <div class="form-group">
                <label class="control-label col-xs-2">予約者名<span class="required"> *</span></label>
                <div class="col-xs-5">
                    <input type="text" name="name" v-model="user_name" class="form-control" placeholder="例) 山田 太郎">
                </div>
            </div>
            <div class="form-group">
                <label class="control-label col-xs-2">内容</label>
                <div class="col-xs-5">
                    <input type="text" name="name" v-model="description" class="form-control" placeholder="打ち合わせのため">
                </div>
            </div>
            <div class="form-group">
                <div class="col-xs-offset-2 col-xs-10">
                    <button v-bind:disabled="isButtonDisabled" @click="postData" class="btn btn-primary">登録</button>
                    <router-link :to="'/'" v-bind:disabled="isButtonDisabled" tag="button" class="btn btn-secondary">戻る</router-link>
                </div>
            </div>
    </div>
</div>
</template>
<script>
    import alertComponent from './mixin/Alert.vue';
    import myDatepicker from 'vue-datepicker';
    export default {
        mixins: [alertComponent],
        created() {
            this.getRooms()
            this.today()
            this.target_date = null
        },
        data() {
            return {
                room_id: 0,
                start_time: '',
                end_time: '',
                user_name: '',
                description: '',
                isButtonDisabled: false,
                target_date: null,
                roomList: {},
                option: {
                    type: 'day',
                    week: ['月', '火', '水', '木', '金', '土', '日'],
                    month: ['1月', '2月', '3月', '4月', '5月', '6月', '7月', '8月', '9月', '10月', '11月', '12月'],
                    format: 'YYYY-MM-DD',
                    placeholder: '日付',
                    inputStyle: {
                        'display': 'inline-block',
                        'padding': '6px',
                        'line-height': '22px',
                        'font-size': '16px',
                        'border': '2px solid #fff',
                        'box-shadow': '0 1px 3px 0 rgba(0, 0, 0, 0.2)',
                        'border-radius': '2px',
                        'color': '#5F5F5F'
                    },
                    color: {
                        header: '#ccc',
                        headerText: '#888'
                    },
                    buttons: {
                        ok: 'Ok',
                        cancel: 'Cancel'
                    },
                    overlayOpacity: 0.5, // 0.5 as default
                    dismissible: true // as true as default
                },
                limit: [{
                    type: 'weekday',
                    available: [0, 1, 2, 3, 4, 5, 6]
                },
                    {
                        type: 'fromto',
                        from: '1970-01-01',
                        to: '2099-012-31'
                    }
                ]
            }
        },
        methods: {
            getRooms() {
                var self = this
                $.ajax({
                    type: "GET",
                    url: '/api/rooms/'
                }).done(function (res) {
                    self.roomList = res['data']
                    self.isLoading = false
                });
            },
            today() {
                this.target_date = this.getYyyyMmDdStr(new Date());
            },
            postData() {
                var self = this;
                this.isButtonDisabled = true;
                if (this.room_id == 0) {
                    this.showFailed('会議室が選択されていません。');
                    this.isButtonDisabled = false;
                    return;
                }
                if (this.target_date.length == 0 || this.start_time.length == 0 || this.end_time.length == 0 || this.user_name.length == 0) {
                    this.showFailed('必須項目が入力されていません。');
                    this.isButtonDisabled = false;
                    return;
                }
                if (this.start_time >= this.end_time) {
                    this.showFailed('開始時刻と終了時刻の指定が不正です。');
                    this.isButtonDisabled = false;
                    return;
                }
                // カレンダー対応
                var targetDayStr = this.getTargetDayStr();
                if (!targetDayStr.match(/^\d{4}\-\d{2}\-\d{2}$/)) {
                    this.showFailed('日付の値が不正です。2018-01-01の形式で入力してください。');
                    this.isButtonDisabled = false;
                    return;
                }
                var start_time = targetDayStr + ' ' + this.start_time;
                var end_time = targetDayStr + ' ' + this.end_time;
                $.ajax({
                    type: "POST",
                    data: {
                        'room_id': self.room_id,
                        'start_time': start_time,
                        'end_time': end_time,
                        'user_name': self.user_name,
                        'description': self.description,
                    },
                    url: '/api/scheduler/'
                }).done(function (res) {
                    if (res.status == 220) {
                        self.showFailed('他の予定と重複しています。');
                        self.isButtonDisabled = false;
                        return;
                    }
                    self.showSuccess('登録に成功しました。');
                    location.href = '/' + self.getTargetDayStr();
                }).fail(function(res){
                    res.showFailed('入力内容に誤りがあります。');
                    res.isButtonDisabled = false;
                });
            },
            getTargetDayStr() {
                return this.getYyyyMmDdStr(this.target_date);
            },
            getWeekStr(day) {
                return [ "日", "月", "火", "水", "木", "金", "土" ][day.getDay()]
            },
            getYyyyMmDdStr(day) {
                return day.getFullYear() + '-' +
                        ( "0" + ( day.getMonth() + 1 ) ).slice(-2) + '-' +
                        ( "0" + day.getDate() ).slice(-2);
            },
            isSmartPhone() {
                var ua = navigator.userAgent;
                if (ua.indexOf('iPhone') > 0 || ua.indexOf('iPod') > 0 || ua.indexOf('Android') > 0 && ua.indexOf('Mobile') > 0 || ua.indexOf('iPad') > 0 || ua.indexOf('Android') > 0){
                    return true;
                }
                return false;
            }
        },
        components: {
            'date-picker': myDatepicker
        }
    }
</script>
