---
title: Método getProxySettings de IWMPNetwork
description: O método getProxySettings retorna informações sobre as configurações de proxy de um protocolo.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- Método getProxySettings Windows Media Player
- Método getProxySettings Windows Media Player , interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player , método getProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e69c990b01ed885b80c96e3e36ad28c2793baf618fea68b0e20006390c2adeed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331636"
---
# <a name="iwmpnetworkgetproxysettings-method"></a>Método IWMPNetwork::getProxySettings

O **método getProxySettings** retorna informações sobre as configurações de proxy de um protocolo.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrProtocol* \[ Em\]
</dt> <dd>

Um **System.String que** é o nome do protocolo. Para ver uma lista de protocolos com suporte, consulte [Protocolos com suporte e tipos de arquivo](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System.Int32** que é um dos valores a seguir.



| Valor | Descrição                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Um servidor proxy não está sendo usado.                                                |
| 1     | As configurações de proxy para o navegador atual estão sendo usadas (válidas somente para HTTP). |
| 2     | As configurações de proxy especificadas manualmente estão sendo usadas.                            |
| 3     | As configurações de proxy estão sendo detectadas automaticamente.                                      |



 

## <a name="remarks"></a>Comentários

Esse método falha, a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **getProxySettings** para exibir uma mensagem, que fornece informações sobre as configurações de proxy atuais do Player, em um rótulo. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.setProxySettings (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





