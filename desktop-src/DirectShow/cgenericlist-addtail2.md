---
description: O método addcauda acrescenta uma lista ao final da lista.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: Método CGenericList. addcauda (Wxlist. h)-parâmetro pList
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
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105747593"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a>Método CGenericList. addcauda (Wxlist. h)-parâmetro pList

O `AddTail` método anexa uma lista ao final da lista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pList* 
</dt> <dd>

Ponteiro para a lista a ser acrescentada.

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

 

 




