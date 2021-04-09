---
description: O método AddHead adiciona um item à frente da lista.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: Método CGenericList. AddHead (Wxlist. h)-pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104012194"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a>Método CGenericList. AddHead (Wxlist. h)-pObj

O `AddHead` método adiciona um item à frente da lista.

## <a name="syntax"></a>Sintaxe


```C++
POSITION AddHead(
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

Retorna um valor de posição que indica a nova posição de cabeçalho. Se o método falhar, o valor de retorno será **nulo**.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Wxlist. h (incluir fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




