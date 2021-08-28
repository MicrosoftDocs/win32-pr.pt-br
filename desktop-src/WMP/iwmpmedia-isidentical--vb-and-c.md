---
title: IWMPMedia.isIdentical (VB e C )
description: A propriedade isIdentical (o método get isIdentical em C\ ) obtém um valor que indica se o item de mídia especificado é o mesmo que \_ o atual.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia.isIdentical (VB e C ) Windows Media Player
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
ms.openlocfilehash: 24e8de133003bdddcf0438e5a13dc3fa74227ede7bf42350e2b7c3c96f2c197e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003576"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>IWMPMedia.isIdentical (VB e C#)

A **propriedade isIdentical** (o método **get \_ isIdentical** em C#) obtém um valor que indica se o item de mídia especificado é o mesmo que o atual.


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

Uma **interface WMPLib.IWMPMedia** para o item de mídia a ser comparada com o item de mídia atual.

## <a name="property-value"></a>Valor da propriedade

Um **valor System.Boolean** que indica se os dois itens de mídia são idênticos.

## <a name="remarks"></a>Comentários

**IWMPMedia.isIdentical** é uma propriedade no Visual Basic que aceita um parâmetro . Em C#, ele é conhecido como **o método \_ isIdentical IWMPMedia.get.**

## <a name="examples"></a>Exemplos

O exemplo a seguir usa a propriedade **isIdentical** (o método **\_ get isIdentical** em C#) para verificar se um item de mídia chamado newMedia é o mesmo que o item de mídia atual. Se eles não são os mesmos, o novo item de mídia é interpretado. Caso contrário, a mídia atual continuará a reproduzir ininterruptamente. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


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
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





