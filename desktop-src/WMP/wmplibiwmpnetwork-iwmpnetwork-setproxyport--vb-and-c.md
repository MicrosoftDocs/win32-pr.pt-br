---
title: Método IWMPNetwork setProxyPort
description: O método setProxyPort especifica a porta proxy a ser usada. | Método IWMPNetwork setProxyPort
ms.assetid: df4b33f6-52b5-437f-ade2-0d08ca2878a9
keywords:
- Método setProxyPort Windows Media Player
- Método setProxyPort Windows Media Player , interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player , método setProxyPort
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79453ee2d69a0c6b227006416e49b4d4c24b99b3b02dd2bd00cd3bafafc5b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734836"
---
# <a name="iwmpnetworksetproxyport-method"></a>Método IWMPNetwork::setProxyPort

O **método setProxyPort** especifica a porta proxy a ser usada.

## <a name="syntax"></a>Sintaxe


```CSharp
public void setProxyPort(
  System.String bstrProtocol,
  System.Int32 lProxyPort
);
```


```VB

Public Sub setProxyPort( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxyPort As System.Int32 _
)
Implements IWMPNetwork.setProxyPort
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrProtocol* \[ Em\]
</dt> <dd>

Um **System.String que** é o nome do protocolo. Para ver uma lista de protocolos com suporte, consulte [Protocolos com suporte e tipos de arquivo](supported-protocols-and-file-types.md).

</dd> <dt>

*lProxyPort* \[ Em\]
</dt> <dd>

Um **System.Int32 que** é a porta proxy a ser usada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método não tem efeito, a menos que o valor recuperado de **IWMPNetwork.getProxySettings** seja 2 (use configurações manuais).

Esse método falha, a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir **usa setProxyPort para** especificar o Windows Media Player de porta proxy para o protocolo MMS. O número da porta é recuperado de uma caixa de texto quando um botão é clicado. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
private void setProxyPort_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy port number.
        int portnumber = System.Convert.ToInt32(portText.Text);

        // Set the proxy port.
        player.network.setProxyPort("MMS", portnumber);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyPort_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyPort.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy port number.
        Dim portnumber As Integer = System.Convert.ToInt32(portText.Text)

        &#39; Set the proxy port.
        player.network.setProxyPort(&quot;MMS&quot;, portnumber)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
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

[**IWMPNetwork.getProxyPort (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxySettings (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





