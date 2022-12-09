# Deepchain is an ai powerd blockchain wallet , coded in java using machine learning and bitcoin intergration . kindly note cardano isnt surported due to technical and security glitches.

below is the xml summary 


<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android" android:versionCode="241" android:versionName="6.3.3" android:installLocation="auto" package="piuk.blockchain.android" platformBuildVersionCode="25" platformBuildVersionName="7.1.1">
    <uses-sdk android:minSdkVersion="14" android:targetSdkVersion="25"/>
    <uses-permission android:name="com.google.android.providers.gsf.permission.READ_GSERVICES"/>
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>
    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
    <uses-permission android:name="android.permission.INTERNET"/>
    <uses-permission android:name="android.permission.CAMERA"/>
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
    <uses-permission android:name="android.permission.USE_FINGERPRINT"/>
    <uses-feature android:name="android.hardware.location.gps"/>
    <uses-feature android:glEsVersion="0x20000" android:required="true"/>
    <uses-permission android:name="android.permission.WAKE_LOCK"/>
    <uses-permission android:name="com.google.android.c2dm.permission.RECEIVE"/>
    <permission android:name="piuk.blockchain.android.permission.C2D_MESSAGE" android:protectionLevel="signature"/>
    <uses-permission android:name="piuk.blockchain.android.permission.C2D_MESSAGE"/>
    <application android:theme="@style/AppTheme" android:label="@string/app_name" android:icon="@mipmap/ic_launcher_round" android:name="piuk.blockchain.android.BlockchainApplication" android:allowBackup="false" android:roundIcon="@mipmap/ic_launcher_round">
        <activity android:name="piuk.blockchain.android.p012ui.launcher.LauncherActivity" android:launchMode="singleTask" android:configChanges="screenSize|orientation|keyboardHidden">
            <intent-filter>
                <action android:name="android.intent.action.MAIN"/>
                <category android:name="android.intent.category.LAUNCHER"/>
            </intent-filter>
            <intent-filter>
                <action android:name="android.intent.action.VIEW"/>
                <data android:scheme="bitcoin"/>
                <category android:name="android.intent.category.DEFAULT"/>
                <category android:name="android.intent.category.BROWSABLE"/>
            </intent-filter>
        </activity>
        <activity android:theme="@style/AppTheme.MainActivity" android:name="piuk.blockchain.android.p012ui.home.MainActivity" android:configChanges="screenSize|orientation|keyboardHidden" android:windowSoftInputMode="adjustPan"/>
        <activity android:name="piuk.blockchain.android.p012ui.settings.SettingsActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:name="piuk.blockchain.android.p012ui.auth.PinEntryActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:name="piuk.blockchain.android.p012ui.auth.LandingActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:name="piuk.blockchain.android.p012ui.pairing.PairOrCreateWalletActivity" android:configChanges="screenSize|orientation|keyboardHidden" android:windowSoftInputMode="adjustResize"/>
        <activity android:name="piuk.blockchain.android.p012ui.directory.MapActivity"/>
        <activity android:name="piuk.blockchain.android.p012ui.directory.SuggestMerchantActivity"/>
        <activity android:name="piuk.blockchain.android.p012ui.account.AccountActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:name="piuk.blockchain.android.p012ui.account.AccountEditActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:name="piuk.blockchain.android.p012ui.backup.BackupWalletActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:name="piuk.blockchain.android.p012ui.upgrade.UpgradeWalletActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:name="piuk.blockchain.android.p012ui.pairing.ManualPairingActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:theme="@android:style/Theme.NoDisplay" android:name="piuk.blockchain.android.p012ui.auth.LogoutActivity" android:excludeFromRecents="true" android:noHistory="true"/>
        <activity android:name="piuk.blockchain.android.p012ui.auth.PasswordRequiredActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:name="piuk.blockchain.android.p012ui.recover.RecoverFundsActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:name="piuk.blockchain.android.p012ui.zxing.CaptureActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:theme="@style/AppTheme.ReceiveQrWindow" android:name="piuk.blockchain.android.p012ui.receive.ReceiveQrActivity" android:configChanges="screenSize|orientation|keyboardHidden"/>
        <activity android:name="piuk.blockchain.android.p012ui.transactions.TransactionDetailActivity" android:configChanges="screenSize|orientation|keyboardHidden" android:windowSoftInputMode="stateHidden"/>
        <service android:name="piuk.blockchain.android.data.websocket.WebSocketService" android:stopWithTask="true"/>
        <meta-data android:name="com.google.android.maps.v2.API_KEY" android:value="@string/google_maps_key"/>
        <meta-data android:name="com.google.android.gms.version" android:value="@integer/google_play_services_version"/>
        <provider android:name="android.support.p000v4.content.FileProvider" android:exported="false" android:authorities="piuk.blockchain.android.fileProvider" android:grantUriPermissions="true">
            <meta-data android:name="android.support.FILE_PROVIDER_PATHS" android:resource="@xml/provider_paths"/>
        </provider>
        <service android:name="piuk.blockchain.android.data.notifications.FcmCallbackService" android:exported="false">
            <intent-filter>
                <action android:name="com.google.firebase.MESSAGING_EVENT"/>
            </intent-filter>
        </service>
        <service android:name="piuk.blockchain.android.data.notifications.InstanceIdService" android:exported="false">
            <intent-filter>
                <action android:name="com.google.firebase.INSTANCE_ID_EVENT"/>
            </intent-filter>
        </service>
        <service android:name="com.google.firebase.messaging.FirebaseMessagingService" android:exported="true">
            <intent-filter android:priority="-500">
                <action android:name="com.google.firebase.MESSAGING_EVENT"/>
            </intent-filter>
        </service>
        <activity android:theme="@android:style/Theme.Translucent.NoTitleBar" android:name="com.google.android.gms.common.api.GoogleApiActivity" android:exported="false"/>
        <receiver android:name="com.google.android.gms.measurement.AppMeasurementReceiver" android:enabled="true" android:exported="false"/>
        <receiver android:name="com.google.android.gms.measurement.AppMeasurementInstallReferrerReceiver" android:permission="android.permission.INSTALL_PACKAGES" android:enabled="true">
            <intent-filter>
                <action android:name="com.android.vending.INSTALL_REFERRER"/>
            </intent-filter>
        </receiver>
        <service android:name="com.google.android.gms.measurement.AppMeasurementService" android:enabled="true" android:exported="false"/>
        <receiver android:name="com.google.firebase.iid.FirebaseInstanceIdReceiver" android:permission="com.google.android.c2dm.permission.SEND" android:exported="true">
            <intent-filter>
                <action android:name="com.google.android.c2dm.intent.RECEIVE"/>
                <action android:name="com.google.android.c2dm.intent.REGISTRATION"/>
                <category android:name="piuk.blockchain.android"/>
            </intent-filter>
        </receiver>
        <receiver android:name="com.google.firebase.iid.FirebaseInstanceIdInternalReceiver" android:exported="false"/>
        <service android:name="com.google.firebase.iid.FirebaseInstanceIdService" android:exported="true">
            <intent-filter android:priority="-500">
                <action android:name="com.google.firebase.INSTANCE_ID_EVENT"/>
            </intent-filter>
        </service>
        <provider android:name="com.google.firebase.provider.FirebaseInitProvider" android:exported="false" android:authorities="piuk.blockchain.android.firebaseinitprovider" android:initOrder="100"/>
    </application>
</manifest>
