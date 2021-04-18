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
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105759137"
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
| parâmetro  | Mtype. h (incluir fluxos. h)                                                                                     |
| Biblioteca | Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




