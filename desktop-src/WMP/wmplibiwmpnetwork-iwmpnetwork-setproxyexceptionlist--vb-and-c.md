---
title: Método IWMPNetwork setProxyExceptionList
description: O método setProxyExceptionList especifica a lista de exceções de proxy. | Método IWMPNetwork setProxyExceptionList
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- método setProxyExceptionList Windows Media Player
- método setProxyExceptionList Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, método setProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dad011dee8e1199e6111be60acfec41d85d1e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761926"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a>Método IWMPNetwork:: setProxyExceptionList

O método **setProxyExceptionList** especifica a lista de exceções de proxy.

## <a name="syntax"></a>Sintaxe


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrProtocol* \[ no\]
</dt> <dd>

Um **System. String** que é o nome do protocolo. Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).

</dd> <dt>

*pbstrExceptionList* \[ no\]
</dt> <dd>

Um **System. String** que é uma lista delimitada por ponto-e-vírgula de hosts para os quais o servidor proxy é ignorado. Espaços à esquerda e à direita não devem estar presentes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esta é uma lista de computadores, domínios e/ou endereços que irão ignorar o servidor proxy quando a parte do host da URL de destino corresponder a uma entrada na lista.

O \* caractere pode ser usado como um caractere curinga para listar entradas. Por exemplo, \* . com corresponderia a todos os hosts no domínio com, enquanto 67. \* corresponderia a todos os hosts da classe 67 uma sub-rede.

Esse método não tem efeito, a menos que o valor recuperado de **IWMPNetwork. getProxySettings** seja 2 (use as configurações manuais).

Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **setProxyExceptionList** para especificar uma lista de hosts para os quais o servidor proxy é ignorado ao usar o protocolo MMS. A nova lista é recuperada de uma caixa de texto quando um botão é clicado. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
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

[**IWMPNetwork. getProxyExceptionList (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxySettings (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





