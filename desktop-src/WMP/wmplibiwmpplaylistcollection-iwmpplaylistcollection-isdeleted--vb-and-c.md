---
title: Método IsDeleted IWMPPlaylistCollection
description: O método IsDeleted retorna um valor que indica se a playlist especificada está na pasta itens excluídos.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- método IsDeleted Windows Media Player
- método isdeleted Windows Media Player, interface IWMPPlaylistCollection
- Windows Media Player de interface IWMPPlaylistCollection, método isdeleted
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c332a524b334933d587929cdd0e5b5fa61bc15d9110260af8af8e472d7c05fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568473"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a>Método IWMPPlaylistCollection:: IsDeleted

O método **IsDeleted** retorna um valor que indica se a playlist especificada está na pasta itens excluídos.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pItem* \[ no\]
</dt> <dd>

Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução consultada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System. Boolean** que especifica se a playlist foi excluída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





