# Intent-Filter

In Android, you can use an Intent Filter to specify that your app is capable of handling certain types of actions, such as sending emails.
<activity android:name=".SendEmailActivity">
    <intent-filter>
        <action android:name="android.intent.action.SEND" />
        <category android:name="android.intent.category.DEFAULT" />
        <data android:mimeType="text/plain" />
    </intent-filter>
</activity>

In this example:

The <action> element specifies that the activity can handle the SEND action.
The <category> element with the value DEFAULT indicates that this is a default action for the specified MIME type.
The <data> element with the attribute android:mimeType is used to specify the MIME type of the data the activity can handle. In this case, it's set to "text/plain," which is a common MIME type for plain text.
This Intent Filter is declaring that the associated activity (SendEmailActivity) can handle the SEND action with plain text data. When another app or component sends an Intent with the action SEND and data of MIME type text/plain, the system will consider your app as a candidate to handle that Intent.

Remember to replace SendEmailActivity with the actual name of your activity that will handle the email sending functionality.
