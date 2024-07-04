# 验证代码 validate  kimi
```angular2html
async validateCompanylogin() {
    if (this.login_type == 1) {
        if (isEmpty(this.companyVo.user_name)) {
        message.info('请输入用户名');
        return false;
    }
    if (isEmpty(this.companyVo.password)) {
        message.info('请输入密码');
        return false;
    }
    if (isEmpty(this.companyVo.code)) {
        message.info('请输入验证码');
        return false;
    }
    } else {
        if (isEmpty(this.companyVo.phone)) {
        message.info('请输入手机号');
        return false;
    }
    if (isEmpty(this.companyVo.phone_code)) {
        message.info('请输入手机验证码');
        return false;
        }
    }
    return true;
} 模仿上面的代码，对  personVo: {
    company_id: undefined,
    company_list: [],
    id_num: '330304199901019212',
    name: '张三',
    phone: '18826281281',
    account: 'a86356',
    pwd: 'Wengyance2',
    uuid: '',
    code: '',
    code_url: '',
    code_reload_num: 0,
    captchaEnabled: true
}, 做验证

```

# 提交代码 submit-view 
```angular2html
const submit = () => {
    if (!store.validatepersonlogin()) {
        return;
    }
    const d1 = personVo.value;
    
    let d = {
     
    };
    store.loginAsync(d, () => {});
};
```