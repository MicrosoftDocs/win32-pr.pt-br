---
description: Construtor de CDispParams. CDispParams-método de construtor.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Construtor CDispParams. CDispParams (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095784"
---
# <a name="cdispparamscdispparams-constructor"></a>Construtor CDispParams. CDispParams

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nArgs* 
</dt> <dd>

Número de argumentos passados para o método ou a propriedade.

</dd> <dt>

*pArgs* 
</dt> <dd>

Ponteiro para a lista de argumentos. Na lista, cada argumento é armazenado com seu tipo Variant.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CDispParams**](cdispparams.md)
</dt> </dl>

 

 




