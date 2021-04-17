---
title: Propriedade IWMPError errorCount
description: A propriedade errorCount Obtém o número de erros na fila de erros.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- Propriedade errorCount Windows Media Player
- Propriedade errorCount Windows Media Player, interface IWMPError
- Interface IWMPError Windows Media Player, Propriedade errorCount
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762422"
---
# <a name="iwmperrorerrorcount-property"></a>Propriedade IWMPError:: errorCount

A propriedade **errorCount** Obtém o número de erros na fila de erros.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o número de erros.

## <a name="remarks"></a>Comentários

Você deve definir **IWMPSettings. enableErrorDialogs** como **false** se optar por exibir mensagens de erro personalizadas.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **errorCount** em um manipulador de eventos de erro para alertar o usuário sobre o erro mais recente na fila de erros. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

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

[**Interface IWMPError (VB e C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





