---
description: O método addapós insere uma lista após a posição especificada e usa os parâmetros ' pos ' e ' plist '.
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Método CGenericList. AddAfter (Wxlist. h)-Pos, parâmetros do plist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104506545"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>Método CGenericList. AddAfter (Wxlist. h)-Pos, parâmetros do plist

O `AddAfter` método insere uma lista após a posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Posição para inserir a lista. A lista é inserida após esta posição.

</dd> <dt>

*pList* 
</dt> <dd>

Ponteiro para a lista a ser inserida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Wxlist. h (incluir fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




