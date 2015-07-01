# broadcast-receiver
using wifi


public class BroadCast extends BroadcastReceiver{


    @Override
        public void onReceive(Context context, Intent intent) {
//            Log.d(LOGTAG, "WiFi Status Changed");
        Toast.makeText(context, "Wifi Status Changes", Toast.LENGTH_SHORT).show();
        


    }


    }

<receiver android:name=".BroadCast">
            <uses-permission
                android:name="android.permission.CHANGE_WIFI_STATE"
                android:maxSdkVersion="21" />
            <intent-filter>
                <!--<action android:name="android.intent.action.ACTION_POWER_CONNECTED"></action>
                <action android:name="android.intent.CONN"/>-->
                <action android:name="android.net.conn.CONNECTIVITY_CHANGE" />
                <action android:name="android.net.wifi.STATE_CHANGE" />


            </intent-filter>
        </receiver>
