---
title: Método IWMPNetwork setProxyBypassForLocal
description: O método setProxyBypassForLocal especifica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.
ms.assetid: b308957a-0d7e-45be-8625-db198b276dad
keywords:
- método setProxyBypassForLocal Windows Media Player
- método setProxyBypassForLocal Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, método setProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f869125d43529a039804fe28c0f0dc493f481e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763078"
---
# <a name="iwmpnetworksetproxybypassforlocal-method"></a>Método IWMPNetwork:: setProxyBypassForLocal

O método **setProxyBypassForLocal** especifica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.

## <a name="syntax"></a>Sintaxe


```CSharp
public void setProxyBypassForLocal(
  System.String bstrProtocol,
  System.Boolean fBypassForLocal
);
```


```VB

Public Sub setProxyBypassForLocal( _
  ByVal bstrProtocol As System.String, _
  ByVal fBypassForLocal As System.Boolean _
)
Implements IWMPNetwork.setProxyBypassForLocal
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrProtocol* \[ no\]
</dt> <dd>

Um **System. String** que é o nome do protocolo. Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).

</dd> <dt>

*fBypassForLocal* \[ no\]
</dt> <dd>

Um valor **System. Boolean** que indica se o servidor proxy é ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método não tem efeito, a menos que o valor recuperado de **IWMPNetwork. getProxySettings** seja 2 (use as configurações manuais).

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **setProxyBypassForLocal** para especificar se o servidor proxy do Windows Media Player foi ignorado, ao usar o protocolo MMS, se o servidor de origem estiver em uma rede local. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Prepare a message, a caption and buttons for the user prompt.
string message = ("Bypass proxy server for local addresses?");
string caption = "Proxy Settings";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.YesNo;

// Test whether the proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    // Prompt the user for a setting. 
    System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

    // Store the return value of the DialogResult in a boolean variable.
    bool proxybypass;
    
    if(result == System.Windows.Forms.DialogResult.Yes)
    {
        proxybypass = true;
    }
    else
    {
        proxybypass = false;
    }

    // Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal("MMS", proxybypass);
}
else
{
    // Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
}
```


```VB

' Prepare a message, a caption and buttons for the user prompt.
Dim message As String = &quot;Bypass proxy server for local addresses?&quot;
Dim caption As String = &quot;Proxy Settings&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.YesNo

&#39; Test whether the proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    &#39; Prompt the user for a setting. 
    Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

    &#39; Store the return value of the DialogResult as a boolean.
    Dim proxybypass As Boolean

    If (result = System.Windows.Forms.DialogResult.Yes) Then

        proxybypass = True

    Else

        proxybypass = False

    End If

    &#39; Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal(&quot;MMS&quot;, proxybypass)

Else

    &#39; Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

End If
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxyBypassForLocal (VB e C#)**](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxySettings (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





