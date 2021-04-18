---
title: Método IsDeleted IWMPPlaylistCollection
description: O método IsDeleted retorna um valor que indica se a playlist especificada está na pasta itens excluídos.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- método IsDeleted Windows Media Player
- método IsDeleted Windows Media Player, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection do Windows Media Player, método IsDeleted
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
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782544"
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

## <a name="return-value"></a>Retornar valor

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

 

 





