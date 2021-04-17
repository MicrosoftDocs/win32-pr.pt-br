---
description: O operador = atribui um novo tempo de referência. Esse método usa o parâmetro *ll* .
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: CReftime. Operator = método (REFTIME. h)-o parâmetro ll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187839"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a>CReftime. Operator = método (REFTIME. h)-o parâmetro ll

O operador = atribui um novo tempo de referência.

## <a name="syntax"></a>Sintaxe


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*precisa* 
</dt> <dd>

Novo tempo de referência, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma referência ao objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | REFTIME. h (incluir fluxos. h)                                                                                   |
| Biblioteca | Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |



 

 




