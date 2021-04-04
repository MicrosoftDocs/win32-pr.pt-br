---
description: Saiba mais sobre o método de construtor para CGenericList. CGenericList (Wxlist. h). Esse método usa o parâmetro ' pName '.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: Construtor CGenericList. CGenericList (Wxlist. h)-pName parâmetro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103837988"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>Construtor CGenericList. CGenericList (Wxlist. h)-pName parâmetro

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Ponteiro para o nome da lista.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para eficiência, a `CGenericList` classe mantém um cache de nós de lista. Esta versão do construtor usa um tamanho de cache padrão.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Wxlist. h (incluir fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




