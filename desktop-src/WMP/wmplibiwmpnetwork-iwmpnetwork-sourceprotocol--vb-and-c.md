---
title: Propriedade IWMPNetwork sourceProtocol
description: A propriedade sourceProtocol Obtém o protocolo de origem usado para receber dados.
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- Propriedade sourceProtocol Windows Media Player
- Propriedade sourceProtocol Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade sourceProtocol
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5017e1a053c124a1f7f50668c6f392eb541d57f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798403"
---
# <a name="iwmpnetworksourceprotocol-property"></a>Propriedade IWMPNetwork:: sourceProtocol

A propriedade **sourceProtocol** Obtém o protocolo de origem usado para receber dados.

## <a name="syntax"></a>Syntax


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System. String** que é o nome do protocolo de origem.

## <a name="remarks"></a>Comentários

Essa propriedade Obtém uma cadeia de caracteres de comprimento zero ("") ao reproduzir um CD ou DVD.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **sourceProtocol** para exibir o protocolo de origem usado para receber dados. As informações são exibidas em um rótulo, em resposta ao evento **PlayStateChange** . O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

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
</dt> </dl>

 

 





