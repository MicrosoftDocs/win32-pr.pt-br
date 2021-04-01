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
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103664130"
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

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido. Caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Wxlist. h (incluir fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




