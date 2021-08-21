---
description: O método AddHead adiciona uma lista à frente da lista.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Método CGenericList.AddHead (Wxlist.h) – parâmetro pList
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
ms.openlocfilehash: c26667ce12af902f3d5cf355a6556dc95e5dd1f5e0cad77f944e663eeef8ce67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656142"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>Método CGenericList.AddHead (Wxlist.h) – parâmetro pList

O `AddHead` método adiciona uma lista à frente da lista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Plist* 
</dt> <dd>

Ponteiro para a lista de itens a adicionar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Wxlist.h (incluir Fluxos.h) |
| Biblioteca| Strmbase.lib (builds de varejo); Strmbasd.lib (builds de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




