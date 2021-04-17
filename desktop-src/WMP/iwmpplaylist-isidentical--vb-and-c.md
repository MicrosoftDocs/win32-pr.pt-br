---
title: IWMPPlaylist. isidêntico (VB e C)
description: A propriedade isidêntica (o \_ método Get Isidênticos em C \) Obtém um valor que indica se a playlist especificada é idêntica à playlist atual.
ms.assetid: 0e5520ee-3d41-4e36-98f4-7bc2ec45fcb8
keywords:
- IWMPPlaylist. isidêntico (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee30441e8f0275bba06f71a01095c39da8eae9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813149"
---
# <a name="iwmpplaylistisidentical-vb-and-c"></a>IWMPPlaylist. isidêntico (VB e C#)

A propriedade **isidêntica** (o método **Get \_ isidênticos** em C#) Obtém um valor que indica se a playlist especificada é idêntica à playlist atual.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPPlaylist As IWMPPlaylist
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPPlaylist pIWMPPlaylist
);
```



## <a name="parameters"></a>Parâmetros

*pIWMPPlaylist*

Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução que esse método compara à playlist atual.

## <a name="property-value"></a>Valor da propriedade

Um **System. Boolean** que indica se as playlists comparadas são idênticas.

## <a name="remarks"></a>Comentários

**IWMPPlaylist. isidêntico** é uma propriedade em Visual Basic que usa um parâmetro, enquanto em C# ele é referido como o método **IWMPPlaylist. get \_ isidêntico** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





