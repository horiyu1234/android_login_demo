# �T�v

�P�j[�j�t�e�B�N���E�h mobile backend - mBaaS](http://mb.cloud.nifty.com/)�ł̉���̔F�ؕ��@�͈ȉ���4������܂��B

 * ���[�U���E�p�X���[�h�ł̔F��
 * ���[���A�h���X�E�p�X���[�h�ł̔F��
    * [�h�L�������g](http://mb.cloud.nifty.com/doc/current/user/authorize_email_android.html)
 * SNS�A�J�E���g�ł̔F��
   * [�h�L�������g�iFacebook�A�J�E���g�j](http://mb.cloud.nifty.com/doc/current/sns/facebook_android.html)
   * [�h�L�������g�iTwitter�A�J�E���g�j](http://mb.cloud.nifty.com/doc/current/sns/twitter_android.html)
   * [�h�L�������g�iGoogle�A�J�E���g�j](http://mb.cloud.nifty.com/doc/current/sns/google_android.html)
 * �����F��
   * [�h�L�������g](http://mb.cloud.nifty.com/doc/current/user/authorize_anonymous_android.html)

�Q�j�����Android�ŁA���[�U���E�p�X���[�h�ł̔F�ؕ��@�ɂ��Đ������Ă����܂��B
�C���[�W�I�͈ȉ��̂悤�ɂȂ�܂��B
![device.png](https://qiita-image-store.s3.amazonaws.com/0/126379/82ae570f-45ec-824c-e8f1-94c588b6034e.png)


# ����

* Android Studio
* mBaaS��[�A�J�E���g�쐬](http://mb.cloud.nifty.com/signup.htm)

# �菇

* �e���v���[�g�v���W�F�N�g���_�E�����[�h
* SDK��ǉ��i�ς݁E�ŐVSDK�𗘗p�������ꍇ�A�X�V��ƂƂ��čs���Ă��������j
* �A�v���쐬���A�L�[��ݒ�
* ����m�F

# STEP 1. �e���v���[�g�v���W�F�N�g

* �v���W�F�N�g��[Github�y�[�W](https://github.com/ncmbadmin/android_login_demo)����uDownload ZIP�v���N���b�N���܂��B
* �v���W�F�N�g���𓀂��܂��B
* AndroidStudio���J���܂��A�𓀃v���W�F�N�g���J�����Ƃ�I�����܂��B
![OpenFileProject.png](https://qiita-image-store.s3.amazonaws.com/0/126379/ce219fcc-c51b-8d3b-7698-14970e2d62b7.png)

�v���W�F�N�g��I�����J���܂��B
![MainDesing.png](https://qiita-image-store.s3.amazonaws.com/0/126379/41091466-c5d5-10a6-86e3-656713734c7a.png)


# STEP 2. SDK��ǉ��Ɛݒ� (�ς�)

SDK�Ƃ̓j�t�e�B�N���E�hmobile backend���񋟂��Ă���u�f�[�^�X�g�A�v�u�v�b�V���ʒm�v�Ȃǂ̋@�\��Android������ȒP�ɃR�[�h������i���s���炢�j���C�u�����[�̂��̂ł��B

![002.png](https://qiita-image-store.s3.amazonaws.com/0/18698/75b7512c-7dec-9931-b8f6-66f6dd5a73af.png)

mBaaS�ł́AAndroid, iOS, Unity, JavaScript SDK��񋟂��Ă��܂��B
����Android SDK�̒ǉ������Ɛݒ���Љ�܂��B
���_�E�����[�h�����v���W�F�N�g�ɂ͊��ɐݒ�ς݂ł����A�ŐV�ł͂Ȃ��ꍇ�A�����g�œ���ւ��Ă��������I�܂������g�̃v���W�F�N�g�ɂ�SDK��ǉ��������ꍇ�������������K�v�ł��B

* SDK�_�E�����[�h
SDK�͂����iSDK[�����[�X�y�[�W](https://github.com/NIFTYCloud-mbaas/ncmb_android/releases)�j����擾���Ă�������.
  - NCMB.jar�t�@�C�����_�E�����[�h���܂��B
* SDK���C���|�[�g
  - app/libs�t�H���_��NCMB.jar���R�s�[���܂�
* �ݒ�ǉ�
  - app/build.gradle�t�@�C���Ɉȉ���ǉ����܂�

```
dependencies {
    compile 'com.google.code.gson:gson:2.3.1'
    compile files('libs/NCMB.jar')
}
```
  - androidManifest�̐ݒ�

<application>�^�O�̒��O�Ɉȉ���permission��ǉ����܂��B

```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```


# STEP 3. �A�v���L�[�ݒ�

* ����o�^�i�����j�����A�o�^���ł����烍�O�C��������Ɖ��}�̂悤�Ɂu�A�v���̐V�K�쐬�v��ʏo��̂ŃA�v�����쐬���܂��B
![mBass1-2.png](https://qiita-image-store.s3.amazonaws.com/0/126379/3088b146-737b-1726-38ba-e16d6010d774.png)

* �A�v���쐬�����Ɖ��}�̂悤�ȉ�ʂɂȂ�܂��B
* ���̂Q��ނ�API�L�[�i�A�v���P�[�V�����L�[�ƃN���C�A���g�L�[�j�͐�قǃC���|�[�g����AndroidStudio�ō쐬����Android�A�v���Ƀj�t�e�B�N���E�hmobile backend�̕R�t���邽�߁A���ƂŎg���܂�.
![mBass3-4.png](https://qiita-image-store.s3.amazonaws.com/0/126379/8531d19c-99ca-47e3-628c-dcd8baff6070.png)

���̌㓮��m�F�Ńf�[�^���ۑ������ꏊ���m�F���Ă����܂��傤�B
![mBass5-6.png](https://qiita-image-store.s3.amazonaws.com/0/126379/fec223ae-7af3-8605-0436-4dd375c0e69f.png)

* AndroidStudio�Ŏ擾API�L�[(�A�v���P�[�V�����L�[�A�N���C���g�L�[)��ݒ肷��B
![MainActivity.png](https://qiita-image-store.s3.amazonaws.com/0/126379/d0996a98-cf26-a367-c8bd-c93febc592ba.png)
![APIKey.png](https://qiita-image-store.s3.amazonaws.com/0/126379/48c45a2a-9536-d110-72eb-5fccf7454b95.png)

* AndroidStudio����r���h����B
    * �u�v���W�F�N�g�ꏊ�v\app\build\outputs\apk\ ***.apk �t�@�C�������������

# STEP 4. �m�F

�A�v���ɂă{�^�����^�u���A�V�K�o�^�A���O�C�����鎖���m�F�o���܂��B
![AccountPattern.png](https://qiita-image-store.s3.amazonaws.com/0/126379/bc2a4349-defe-5d5d-59d4-136959ee269b.png)
![LoginPattern.png](https://qiita-image-store.s3.amazonaws.com/0/126379/c3bf4f83-b12c-3ebd-7af4-9350db6212bd.png)

mBaaS��������Ǘ��f�[�^���ۑ����ꂽ���Ƃ��m�F���Ă��܂��I
![mBassMember.png](https://qiita-image-store.s3.amazonaws.com/0/126379/399d5dbe-ceaa-1a7a-6bb4-306f6fcbad94.png)


# �R�[�h����

* SDK����ѕK�v�ȃ��C�u�����[���C���|�[�g���܂�

```java:MainActivity.java

import com.nifty.cloud.mb.core.DoneCallback;
import com.nifty.cloud.mb.core.NCMB;
import com.nifty.cloud.mb.core.NCMBException;
import com.nifty.cloud.mb.core.NCMBUser;
```

* SDK��������

MainActivity��OnCreate���\�b�h�Ɏ����A������API�L�[��n���܂��B

```java:MainActivity.java

 @Override
    protected void onCreate(Bundle savedInstanceState) {
       <�ȗ�>
        //**************** API�L�[�̐ݒ��SDK�̏����� **********************
        NCMB.initialize(this, "YOUR_APPLICATION_KEY", "YOUR_CLIENT_KEY");
    }
```

�P�j����̐V�K�o�^����

* mBaaS��Android SDK���񋟂���NCMBUser�N���X������Ǘ��𑀍삷�邽�߂̃N���X�B�f�[�^��ۑ�����ɂ́A���̃N���X���񋟂���signUpInBackground���\�b�h�𗘗p���A�o�^�A���O�C�����܂��B
* ���̓��[�U���ƃp�X���[�h�̑Ó������m�F���A�ݒ肵�����[�U��(userName)�ƃp�X���[�h(password)�ŉ���o�^���s���܂��B
* signUpInBackground()�����{���邱�ƂŁA�񓯊��ɕۑ����s���܂��B�񓯊����{���邽�߁ADoneCallBack()���g���āA�����E���s�������w�肵�܂��B
 - ��������ꍇ�A���O�C�������y�[�W��\�����܂��B
 - ���s����ꍇ�A�A���[�g�Ń��O�C�����s��\�����܂��B

```java:SignupActivity.java

      public void signup() {
�@�@�@�@<�ȗ�>
 �@�@�@�@// TODO: Implement your own signup logic here.
        //NCMBUser�̃C���X�^���X���쐬
        NCMBUser user = new NCMBUser();
        //���[�U����ݒ�
        user.setUserName(name);
        //�p�X���[�h��ݒ�
        user.setPassword(password);
        //�ݒ肵�����[�U���ƃp�X���[�h�ŉ���o�^���s��
        user.signUpInBackground(new DoneCallback() {
            @Override
            public void done(NCMBException e) {
                if (e != null) {
                    //����o�^���ɃG���[�����������ꍇ�̏���
                    onSignupFailed();
                } else {
                    new android.os.Handler().postDelayed(
                            new Runnable() {
                                public void run() {
                                    // On complete call either onSignupSuccess or onSignupFailed
                                    // depending on success
                                    onSignupSuccess();
                                    // onSignupFailed();
                                    progressDialog.dismiss();
                                }
                            }, 3000);
                }
            }
        });
    }
```

�Q�j��������̃��O�C������

* mBaaS��Android SDK���񋟂���NCMBUser�N���X������Ǘ����삷�邽�߂̃N���X�B���̃N���X���񋟂���loginInBackground���\�b�h�𗘗p���A���O�C�����܂��B
* ���̓��[�U���ƃp�X���[�h�̑Ó������m�F���A���[�U���ƃp�X���[�h�Ń��O�C�������s���܂��B
* loginInBackground()�����{���ʂŁA
 - ��������ꍇ�A���O�C�������y�[�W��\�����܂��B
 - ���s����ꍇ�A�A���[�g�Ń��O�C�����s��\�����܂��B

```java:LoginActivity.java

      public void login() {
�@�@�@�@<�ȗ�>
        // TODO: Implement your own authentication logic here.
        //���[�U���ƃp�X���[�h���w�肵�ă��O�C�������s
        try {
            NCMBUser.loginInBackground(name, password, new LoginCallback() {
                @Override
                public void done(NCMBUser user, NCMBException e) {
                    if (e != null) {
                        //�G���[���̏���
                        onLoginFailed();
                    } else {
                        new android.os.Handler().postDelayed(
                                new Runnable() {
                                    public void run() {
                                        // On complete call either onLoginSuccess or onLoginFailed
                                        onLoginSuccess();
                                        // onLoginFailed();
                                        progressDialog.dismiss();
                                    }
                                }, 3000);
                    }
                }
            });
        } catch (NCMBException e) {
            e.printStackTrace();
        }

    }
```

# �Q�l

�T���v���R�[�h���J�X�^�}�C�Y���邱�ƂŁA�l�X�ȋ@�\�������ł��܂��I
�f�[�^�ۑ��E�f�[�^�����E����Ǘ��E�v�b�V���ʒm�Ȃǂ̋@�\�������������ꍇ�ɂ́A
�ȉ��̃h�L�������g�����Q�l���������B

* [�h�L�������g](http://mb.cloud.nifty.com/doc/current/)
* [�h�L�������g�E�f�[�^�X�g�A](http://mb.cloud.nifty.com/doc/current/datastore/basic_usage_android.html)
* [�h�L�������g�E����Ǘ�](http://mb.cloud.nifty.com/doc/current/user/basic_usage_android.html)
* [�h�L�������g�E�v�b�V���ʒm](http://mb.cloud.nifty.com/doc/current/push/basic_usage_android.html)

# �Ō��

�f�[�^��ۑ�������ăT�[�o�𗧂Ă���A�����ŃT�[�o�^�p�Ƃ��A�݌v�Ƃ��A�A�v������T�[�o�[�Ƃ̂��Ƃ���F�X�l�����Ȃ���΂Ȃ�܂���B
�ŒZ���@�Ƃ����̂́A���̂悤��mBaaS�T�[�r�X���g���āA�^�p�A�݌v�Ȃǎ����ł��Ȃ��čςށA�J�������s�R�[�h�����΂����Ƃ����֗��Ȃ��̂͂������ł��傤���H

# Contributing

*    Fork it!
*    Create your feature branch: git checkout -b my-new-feature
*    Commit your changes: git commit -am 'Add some feature'
*    Push to the branch: git push origin my-new-feature
*    Submit a pull request :D

# License

    MIT���C�Z���X
    NIFTY Cloud mobile backend��Android SDK�̃��C�Z���X