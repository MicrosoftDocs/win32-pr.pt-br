---
description: A \_ variável de membro m bModifiesData indica se o filtro modifica os dados de exemplo que são recebidos. O valor é definido no Construtor CTransInPlaceFilter, mas o padrão é TRUE.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Membro CTransInPlaceFilter:: m_bModifiesData (TRANSip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7461f7f62a6cbd1fea2ff18f6e8f2e4b73825ea04cb9e3b0a679ee7cf15fef90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654875"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>Membro de CTransInPlaceFilter:: m \_ bModifiesData

A `m_bModifiesData` variável de membro indica se o filtro modifica os dados de exemplo que são recebidos. O valor é definido no construtor **CTransInPlaceFilter** , mas o padrão é **true**.

## <a name="syntax"></a>Sintaxe


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>Comentários

Essa variável afeta como o filtro negocia o alocador. Se o valor for **true**, o filtro não poderá usar um alocador somente leitura para ambas as conexões de PIN.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




