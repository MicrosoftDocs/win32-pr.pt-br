---
title: Propriedade de contagem IWMPPlaylist
description: A propriedade count obtém o número de itens de mídia em uma playlist.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- propriedade count Windows Media Player
- propriedade count Windows Media Player , interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player , propriedade count
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
ms.openlocfilehash: aad690278b45563395c926adb4d0329bff8a01c7e8ace2f25ff3fefdb9c39cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568691"
---
# <a name="iwmpplaylistcount-property"></a>Propriedade IWMPPlaylist::count

A **propriedade count** obtém o número de itens de mídia em uma playlist.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Int32 que** é o número de itens de mídia na playlist.

## <a name="remarks"></a>Comentários

Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

Consulte a [propriedade attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para ver o código de exemplo que usa essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





