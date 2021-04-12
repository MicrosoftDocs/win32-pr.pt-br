---
description: O método addapós insere um item após a posição especificada e usa os parâmetros ' p ' e ' pObj '.
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Método CGenericList. AddAfter (Wxlist. h)-p, pObj parâmetros
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
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104298880"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a>Método CGenericList. AddAfter (Wxlist. h)-p, pObj parâmetros

O `AddAfter` método insere um item após a posição especificada.

## <a name="syntax"></a>Sintaxe


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DTI* 
</dt> <dd>

Posição após a qual adicionar o item. Se *p* for **NULL**, o método adicionará o item ao cabeçalho da lista.

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

 

 




