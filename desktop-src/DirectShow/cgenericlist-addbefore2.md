---
description: O método addantes insere uma lista antes da posição especificada. Esse método usa os parâmetros ' pos ' e ' pList '.
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Método CGenericList. AddBefore (Wxlist. h)-Pos, parâmetros do pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f05d67477bb7e6c89eddfe0a68ad47d83760762fc68cddf6f73c731886f88d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697446"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a>Método CGenericList. AddBefore (Wxlist. h)-Pos, parâmetros do pList

O `AddBefore` método insere uma lista antes da posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Posição para inserir a lista. A lista é inserida antes dessa posição.

</dd> <dt>

*pList* 
</dt> <dd>

Ponteiro para a lista a ser inserida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se for bem-sucedido. Caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Wxlist. h (incluir Fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




