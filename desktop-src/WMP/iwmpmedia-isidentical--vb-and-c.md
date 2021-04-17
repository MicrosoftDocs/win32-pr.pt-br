---
title: IWMPMedia. isidêntico (VB e C)
description: A propriedade isidêntica (o \_ método Get Isidênticos em C \) Obtém um valor que indica se o item de mídia especificado é o mesmo que o atual.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia. isidêntico (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758194"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>IWMPMedia. isidêntico (VB e C#)

A propriedade **isidêntica** (o método **Get \_ isidênticos** em C#) Obtém um valor que indica se o item de mídia especificado é o mesmo que o atual.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a>Parâmetros

*pIWMPMedia*

Uma interface **WMPLib. IWMPMedia** para o item de mídia a ser comparado com o item de mídia atual.

## <a name="property-value"></a>Valor da propriedade

Um valor **System. Boolean** que indica se os dois itens de mídia são idênticos.

## <a name="remarks"></a>Comentários

**IWMPMedia. isidêntico** é uma propriedade em Visual Basic que usa um parâmetro. Em C#, ele é chamado de método **IWMPMedia. get \_ isidêntico** .

## <a name="examples"></a>Exemplos

O exemplo a seguir usa a propriedade **isidêntica** (o método **Get \_ isidêntico** em C#) para verificar se um item de mídia chamado newMedia é o mesmo que o item de mídia atual. Se eles não forem iguais, o novo item de mídia será reproduzido. Caso contrário, a mídia atual continuará a ser executada sem interrupção. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

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

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





