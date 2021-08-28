---
description: O método AddAfter insere uma lista após a posição especificada e usa os parâmetros 'pos' e 'plist'.
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Método CGenericList.AddAfter (Wxlist.h) – parâmetros pos, plist
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
ms.openlocfilehash: 846e37b961af8d2492b3aff032193e87fb3603eb1751c25f0e3ca8e0c5d38618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697476"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>Método CGenericList.AddAfter (Wxlist.h) – parâmetros pos, plist

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

Posição para inserir a lista. A lista é inserida após essa posição.

</dd> <dt>

*Plist* 
</dt> <dd>

Ponteiro para a lista a ser inserida.

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

 

 




