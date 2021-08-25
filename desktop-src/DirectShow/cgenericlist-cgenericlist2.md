---
description: Saiba mais sobre o método do construtor para CGenericList.CGenericList (Wxlist.h). Esse método usa o parâmetro 'pName'.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: Construtor CGenericList.CGenericList (Wxlist.h) – parâmetro pName
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
ms.openlocfilehash: 117138e80db91529d6a2baf93577a6a4dfd542d2975bf2ce6f89124a3d7aefe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813836"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>Construtor CGenericList.CGenericList (Wxlist.h) – parâmetro pName

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pname* 
</dt> <dd>

Ponteiro para o nome da lista.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para eficiência, a `CGenericList` classe mantém um cache de nós de lista. Esta versão do construtor usa um tamanho de cache padrão.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Wxlist.h (incluir Fluxos.h) |
| Biblioteca| Strmbase.lib (builds de varejo); Strmbasd.lib (builds de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




