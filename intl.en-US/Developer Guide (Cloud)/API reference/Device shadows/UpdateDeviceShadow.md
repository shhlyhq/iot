# UpdateDeviceShadow {#reference_yc1_2kd_xdb .reference}

Call this operation to update the shadow information of a specified device.

## Request parameters {#section_ydm_wkb_ydb .section}

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|The operation that you want to perform. Set the value to UpdateDeviceShadow.|
|ProductKey|String|Yes|The product key of the device whose shadow information you want to update.|
|DeviceName|String|Yes|The name of the device whose shadow information you want to update.|
|ShadowMessage|String|Yes| The new message of the device shadow. The following is an example:

 ```
{
"method": "update",
"state": {
"desired": {
"color": "green"
}
},
  "version": 2
}
```

 For more information, see the following table [ShadowMessage](reseller.en-US/Developer Guide (Cloud)/API reference/Device shadows/UpdateDeviceShadow.md#table_ry1_nlb_ydb).

 |
|Common request parameters|-|Yes|See [Common parameters](reseller.en-US/Developer Guide (Cloud)/API reference/Common parameters.md#).|

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|method|String|Yes|The specified action type. Set the value to update.|
|state|String|Yes|The specific state that is sent to the shadow by the device, where desired is the desired state of the shadow.|
|version|String|Yes|The version of the device shadow, which must be higher than the current version.|

## Response parameters {#section_agx_xb5_j2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|The globally unique ID generated by Alibaba Cloud for the request.|
|Success|Boolean|Indicates whether the call is successful. A value of true indicates that the call is successful. A value of false indicates that the call has failed.|
|ErrorMessage|String|The error message returned when the call fails.|
|Code|String|The error code returned when the call fails. For more information on error codes, see [Error codes](reseller.en-US/Developer Guide (Cloud)/API reference/Error codes.md#).|

## Examples {#section_kxf_jmb_ydb .section}

**Request example**

```
https://iot.cn-shanghai.aliyuncs.com/?Action=UpdateDeviceShadow
&ProductKey=al*********
&DeviceName=device1
&ShadowMessage=[{"method":"update","state":{"desired":{"color":"green"},"reported":"\"},"version":1}]
&Common request parameters
```

**Response example**

-   JSON format

    ```
    {
          "RequestId":"BB71E443-4447-4024-A000-EDE09922891E",
          "Success":true,
      }
    ```

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
      <UpdateDeviceShadowResponse>
          <RequestId>BB71E443-4447-4024-A000-EDE09922891E</RequestId>
          <Success>true</Success>
      </UpdateDeviceShadowResponse>
    ```


