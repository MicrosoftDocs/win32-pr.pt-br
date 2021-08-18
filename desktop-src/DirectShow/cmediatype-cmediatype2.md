---
description: Saiba mais sobre o método do Construtor CMediaType. CMediaType (mtype. h). Esse método usa o parâmetro ' majortype '.
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: Construtor CMediaType. CMediaType (mtype. h)-parâmetro majortype
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b1ebf3cec41c4180a4dcad4a5a7c273996f70bfdb6d052127ff71dd1b929238c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073990"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a>Construtor CMediaType. CMediaType (mtype. h)-parâmetro majortype

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*majortype* 
</dt> <dd>

Ponteiro para um **GUID** de tipo principal. O construtor inicializa o GUID de tipo principal para esse valor.

</dd> </dl>

## <a name="remarks"></a>Comentários

O construtor chama o método [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) para inicializar o tipo de mídia.

## <a name="requirements"></a>Requisitos

| Requisito                   | Valor                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | Mtype. h (incluir Fluxos. h)                                                                                     |
| Biblioteca | Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




