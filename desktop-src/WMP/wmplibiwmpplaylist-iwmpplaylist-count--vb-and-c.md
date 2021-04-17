---
title: Propriedade Count de IWMPPlaylist
description: A propriedade Count Obtém o número de itens de mídia em uma lista de reprodução.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- Propriedade Count Windows Media Player
- Propriedade Count Windows Media Player, interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player, Propriedade Count
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d988fefc436b65652d2b0765320ca289417c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782716"
---
# <a name="iwmpplaylistcount-property"></a>Propriedade IWMPPlaylist:: Count

A propriedade **Count** Obtém o número de itens de mídia em uma lista de reprodução.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o número de itens de mídia na lista de reprodução.

## <a name="remarks"></a>Comentários

Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

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
</dt> </dl>

 

 





