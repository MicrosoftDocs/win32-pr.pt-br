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
ms.openlocfilehash: 6de0037d76e63049294b0455c8ec1fbac82963d94febb35f7c9400ec8eae9ab5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697526"
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

## <a name="return-value"></a>Valor retornado

Retorna o indicador de posição do item inserido.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Wxlist. h (incluir Fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




