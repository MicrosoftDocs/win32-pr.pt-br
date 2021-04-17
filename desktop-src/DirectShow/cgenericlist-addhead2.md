---
description: O método AddHead adiciona uma lista à frente da lista.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Método CGenericList. AddHead (Wxlist. h)-parâmetro pList
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
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105754539"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>Método CGenericList. AddHead (Wxlist. h)-parâmetro pList

O `AddHead` método adiciona uma lista à frente da lista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pList* 
</dt> <dd>

Ponteiro para a lista de itens a serem adicionados.

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

 

 




