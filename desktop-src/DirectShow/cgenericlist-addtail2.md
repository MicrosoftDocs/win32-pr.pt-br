---
description: O método AddTail acrescenta uma lista ao final da lista.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: Método CGenericList.AddTail (Wxlist.h) – parâmetro pList
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
ms.openlocfilehash: 1cf647fb70b6d2896991bda2e8558ad34407f3427a2eef2d2ce8cd4295c95486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813996"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a>Método CGenericList.AddTail (Wxlist.h) – parâmetro pList

O `AddTail` método anexa uma lista ao final da lista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Plist* 
</dt> <dd>

Ponteiro para a lista a ser anexada.

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

 

 




