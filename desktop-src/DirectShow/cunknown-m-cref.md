---
description: 'CUnknown:: m_cRef contagem de referência de membro.'
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: 'Membro CUnknown:: m_cRef (combase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3f6be7d09149f651bce8d1042b7f3e3a5dc9307
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084574"
---
# <a name="cunknownm_cref-member"></a>Membro cRef CUnknown:: m \_

Contagem de referência.

## <a name="syntax"></a>Sintaxe


```C++
LONG m_cRef;
```



## <a name="remarks"></a>Comentários

Use essa variável de membro se você substituir o método [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) ou [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




