---
title: IWMPControls. IsAvailable (VB e C)
description: A propriedade IsAvailable (o \_ método Get IsAvailable em C \) Obtém um valor que indica se um tipo de informação especificado está disponível ou uma ação especificada pode ser executada.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls. IsAvailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73562fb4f96731216c30ada33db8e13d1468b31fb6fcefe7eedef6dd7892348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054844"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a>IWMPControls. IsAvailable (VB e C#)

A propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#) Obtém um valor que indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Parâmetros

*bstrItem*

Um System. String que é um dos valores a seguir.



| Valor           | Descrição                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | Descobre se o usuário pode definir a propriedade **IWMPControls. currentItem** .                                                                                     |
| currentMarker   | Descobre se o usuário pode buscar um marcador específico.                                                                                                         |
| currentPosition | Descobre se o usuário pode buscar uma posição específica no arquivo. Alguns arquivos não dão suporte à busca.                                                        |
| fastForward     | Descobre se o arquivo dá suporte ao encaminhamento rápido e se essa funcionalidade pode ser invocada. Muitos tipos de arquivo (e transmissões ao vivo) não dão suporte a fastForward. |
| fastReverse     | Descobre se o arquivo dá suporte a fastReverse e se essa funcionalidade pode ser invocada. Muitos tipos de arquivo (e transmissões ao vivo) não dão suporte a fastReverse.     |
| Próximo            | Descobre se o usuário pode buscar a próxima entrada em uma lista de reprodução.                                                                                              |
| pause           | Descobre se o método **IWMPControls. Pause** está disponível.                                                                                                 |
| jogar            | Descobre se o método **IWMPControls. Play** está disponível.                                                                                                  |
| previous        | Descobre se o usuário pode buscar a entrada anterior em uma lista de reprodução.                                                                                          |
| Etapa            | Descobre se o método **IWMPControls2. Step** está disponível durante a reprodução.                                                                                 |
| parar            | Descobre se o método **IWMPControls. Stop** está disponível.                                                                                                  |



 

## <a name="property-value"></a>Valor da propriedade

**System.Boolean**

Um **System. Boolean** que indica se um tipo especificado de informações está disponível ou se uma ação especificada pode ser executada.

## <a name="remarks"></a>Comentários

**IWMPControls. isavailable** é uma propriedade em Visual Basic que usa um parâmetro. Em C#, ele é conhecido como o método **IWMPControls. get \_ IsAvailable** .

## <a name="examples"></a>Exemplos

O exemplo a seguir usa a propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#) para verificar se o item de mídia atual dá suporte à propriedade **CurrentPosition** . O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

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

[**Interface IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentItem (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPControls. PAUSE (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Stop (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPControls2. Step (VB e C#)**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





