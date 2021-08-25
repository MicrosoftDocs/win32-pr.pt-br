---
title: Propriedade currentPositionString de IWMPControls
description: A propriedade currentPositionString obtém a posição atual no item de mídia como uma cadeia de caracteres formatada como HH MM SS (horas, minutos e segundos).
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- propriedade currentPositionString Windows Media Player
- propriedade currentPositionString Windows Media Player interface , IWMPControls
- Interface IWMPControls Windows Media Player , propriedade currentPositionString
topic_type:
- apiref
api_name:
- IWMPControls.currentPositionString
- IWMPControls.get_currentPositionString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61e3c98937a12c145742895979ccccb8118f8349f82b2840c902dfe625ad0472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861906"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a>Propriedade IWMPControls::currentPositionString

A **propriedade currentPositionString** obtém a posição atual no item de mídia como uma cadeia de caracteres formatada como HH:MM:SS (horas, minutos e segundos).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System.String formatado** que é a posição atual.

## <a name="remarks"></a>Comentários

Se o item de mídia tiver menos de uma hora, a posição atual será formatada como MM:SS (minutos e segundos).

## <a name="examples"></a>Exemplos

O exemplo a seguir inicia um temporizador que dispara um evento em intervalos de um segundo. No manipulador de eventos do temporizador, um rótulo é atualizado com **o currentPositionString.** O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 
   
// Update the text of the label with the currentPositionString.
private void TimerEventProcessor(object sender, System.EventArgs e)
{
    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString;
}
```


```VB

' Set the timer to fire an event every second and start the timer.
timer.Interval = 1000
timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
&#39; determine when to start and stop the timer. 

&#39; Update the text of the label with the currentPositionString.
Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString

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

[**Interface IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentPosition (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





