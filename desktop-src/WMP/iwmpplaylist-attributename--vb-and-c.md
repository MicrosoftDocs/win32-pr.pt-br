---
title: IWMPPlaylist. attributeName (VB e C)
description: A propriedade attributeName (o \_ método Get AttributeName em C \) Obtém o nome de um atributo de playlist especificado por um índice.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist. attributeName (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761438"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a>IWMPPlaylist. attributeName (VB e C#)

A propriedade **AttributeName** (o método **Get \_ AttributeName** em C#) Obtém o nome de um atributo playlist especificado por um índice.


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a>Parâmetros

*lIndex*

Um **System. Int32** que é o índice do atributo playlist.

## <a name="return-value"></a>Valor Retornado

Um **System. String** que é o nome do atributo playlist.

## <a name="remarks"></a>Comentários

**IWMPPlaylist. AttributeName** é uma propriedade somente leitura no Visual Basic que usa um parâmetro, enquanto em C# ele é referido como o método **IWMPPlaylist. get \_ AttributeName** .

O número de atributos associados a uma playlist é retornado pela propriedade **IWMPPlaylist. attributeCount** .

O nome retornado por essa propriedade pode ser fornecido para os métodos **setItemInfo** ou **getItemInfo** para especificar ou recuperar um valor para o atributo nomeado.

Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Para obter mais informações sobre atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).

## <a name="examples"></a>Exemplos

Consulte a propriedade [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para obter o código de exemplo que usa essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. attributeCount (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. getItemInfo (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. setItemInfo (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





