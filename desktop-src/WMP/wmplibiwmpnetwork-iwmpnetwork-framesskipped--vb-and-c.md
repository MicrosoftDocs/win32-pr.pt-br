---
title: Propriedade IWMPNetwork framesSkipped
description: A propriedade framesSkipped Obtém o número total de quadros ignorados durante a reprodução.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- Propriedade framesSkipped Windows Media Player
- Propriedade framesSkipped Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade framesSkipped
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749425"
---
# <a name="iwmpnetworkframesskipped-property"></a>Propriedade IWMPNetwork:: framesSkipped

A propriedade **framesSkipped** Obtém o número total de quadros ignorados durante a reprodução.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o número de quadros ignorados.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **framesSkipped** para exibir o número total de quadros ignorados durante a reprodução. As informações são exibidas em um rótulo quando o usuário clica em um botão. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

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

 

 





