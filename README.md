# preferenceFragement
实验四


实验总界面


![](https://github.com/huangzichun666/preferenceFragement/blob/master/image/3.png)


Edit text preference:


![](https://github.com/huangzichun666/preferenceFragement/blob/master/image/2.png)


List preference:


![](https://github.com/huangzichun666/preferenceFragement/blob/master/image/1.png)


Intent preference:


![](https://github.com/huangzichun666/preferenceFragement/blob/master/image/5.png)


Parent checkbox preference:


![](https://github.com/huangzichun666/preferenceFragement/blob/master/image/4.png)


PreferenceScreen.xml

<?xml version="1.0" encoding="utf-8"?>
<PreferenceScreen xmlns:android="http://schemas.android.com/apk/res/android">

    <EditTextPreference android:key="edit"
        android:title="Edit text preference"
        android:summary="An example that uses an edit text dialog"
        android:dialogTitle="Enter your favorite animal" />

    <ListPreference
        android:key="list"
        android:title="List preference"
        android:summary="An example that uses a list dialog"
        android:entries="@array/entry_list"
        android:entryValues="@array/values_list"
        android:dialogTitle="Choose one"
        android:defaultValue="1"
        />

    <PreferenceScreen
        android:key="screen"
        android:title="Screen preference"
        android:summary="Shows another screen of preferences">

        <CheckBoxPreference
            android:key="checkbox"
            android:title="Toggle preference"
            android:summary="Preference that is on the next screen but same hierachy" />

    </PreferenceScreen>

    <Preference
        android:key="progressBar"
        android:title="Intent preference"
        android:summary="Launches an Activity from an Intent">
        <intent android:action="android.intent.action.VIEW"
            android:data="https://www.baidu.com" />
    </Preference>

    <CheckBoxPreference
        android:key="pref_key_auto_delete"
        android:title="Parent checkbox preference"
        android:summary="This is vissually a parent"
        android:defaultValue="false" />

    <CheckBoxPreference
        android:key="pref_sync"
        android:title="Parent checkbox preference"
        android:summary="This is vissually a parent"
        android:dependency="pref_key_auto_delete"
        android:defaultValue="true" />

</PreferenceScreen>
