---
description: O método addantes insere um item antes da posição especificada. Esse método usa os parâmetros ' p ' e ' pObj '.
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Método CGenericList. AddBefore (Wxlist. h)-p, pObj parâmetros
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
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103930778"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a>Método CGenericList. AddBefore (Wxlist. h)-p, pObj parâmetros

O `AddBefore` método insere um item antes da posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DTI* 
</dt> <dd>

Posição antes da qual inserir a lista. Se *p* for **NULL**, esse método adicionará o item à parte final da lista.

</dd> <dt>

*pObj* 
</dt> <dd>

Ponteiro para um objeto do tipo **Object** (o tipo de modelo).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o indicador de posição do item inserido.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Wxlist. h (incluir fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




