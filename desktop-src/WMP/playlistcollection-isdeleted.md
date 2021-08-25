---
title: Método playlistcollection. IsDeleted
description: O método IsDeleted recupera um valor que indica se a lista de reprodução especificada está na pasta itens excluídos.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- método IsDeleted Windows Media Player
- método isdeleted Windows Media Player, classe playlistcollection
- classe playlistcollection Windows Media Player, método isdeleted
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59f6ad587740911d55ae2837607c651e3f3be875bfb24f8bfa765ba415e9bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862196"
---
# <a name="playlistcollectionisdeleted-method"></a>Método playlistcollection. IsDeleted

O método **IsDeleted** recupera um valor que indica se a lista de reprodução especificada está na pasta itens excluídos.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de reprodução* \[ no\]
</dt> <dd>

O objeto de **playlist** a ser procurado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **valor booleano**.

**Windows Media Player 10 Mobile**: esse método sempre retorna **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0, Windows Media Player versão 7,1 ou Windows Media Player para Windows XP. não há suporte para esse método no Windows Media Player 9 Series ou posterior.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto playlistcollection**](playlistcollection-object.md)
</dt> </dl>

 

 





