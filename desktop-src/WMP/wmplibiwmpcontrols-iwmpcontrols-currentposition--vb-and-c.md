---
title: Propriedade IWMPControls currentPosition
description: A propriedade currentPosition Obtém ou define a posição atual no item de mídia em segundos desde o início.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- Propriedade currentPosition Windows Media Player
- Propriedade currentPosition Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, Propriedade currentPosition
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761319"
---
# <a name="iwmpcontrolscurrentposition-property"></a>Propriedade IWMPControls:: currentPosition

A propriedade **CurrentPosition** Obtém ou define a posição atual no item de mídia em segundos desde o início.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a>Valor da propriedade

Um **sistema. Double** que é a posição atual.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **CurrentPosition** para buscar uma posição fornecida pelo usuário. Em resposta a um clique de botão, **CurrentPosition** é definido como o valor inserido em uma caixa de texto chamada NewPosition. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

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

[**Interface IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentPositionString (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





