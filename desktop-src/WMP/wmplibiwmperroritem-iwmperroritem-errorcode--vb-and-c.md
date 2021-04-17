---
title: Propriedade errorCode IWMPErrorItem
description: A propriedade errorCode Obtém o código de erro atual.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- Propriedade errorCode Windows Media Player
- Propriedade errorCode Windows Media Player, interface IWMPErrorItem
- Interface IWMPErrorItem Windows Media Player, Propriedade errorCode
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f284d5655fc1f4007695a1f681c744a9c5c6fc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812156"
---
# <a name="iwmperroritemerrorcode-property"></a>Propriedade IWMPErrorItem:: errorCode

A propriedade **ErrorCode** Obtém o código de erro atual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o código de erro.

## <a name="remarks"></a>Comentários

Você deve definir **IWMPSettings. enableErrorDialogs** como **false** se optar por exibir mensagens de erro personalizadas.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **ErrorCode** em um manipulador de eventos de erro para exibir o código de erro para o usuário. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

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

[**Interface IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





