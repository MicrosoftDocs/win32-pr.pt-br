---
description: O método addcauda acrescenta um item ao final da lista.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: Método CGenericList. addcauda (Wxlist. h)-parâmetro pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105755350"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a>Método CGenericList. addcauda (Wxlist. h)-parâmetro pObj

O `AddTail` método anexa um item ao final da lista.

## <a name="syntax"></a>Sintaxe


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pObj* 
</dt> <dd>

Ponteiro para um objeto do tipo **Object** (o tipo de modelo).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de posição para a nova posição de cauda. Se o método falhar, ele retornará **NULL**.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Wxlist. h (incluir fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




