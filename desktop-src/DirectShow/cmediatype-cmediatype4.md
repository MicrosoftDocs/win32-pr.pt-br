---
description: Construtor CMediaType. CMediaType (mtype. h)-método de construtor.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: Construtor CMediaType. CMediaType (mtype. h)-parâmetros cmtype e PHR
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
ms.openlocfilehash: 2f686d1338073c65ce3e5bc3871ae8f4a5b9102e78d7678d5bcf6f77a565397d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792946"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a>Construtor CMediaType. CMediaType (mtype. h)

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cmtype* \[ referência\]
</dt> <dd>

Referência a um `CMediaType` objeto. O construtor copia o tipo de mídia para o novo objeto, incluindo o bloco de formato, se houver.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor HRESULT. Esse parâmetro pode ser um ponteiro **nulo** . Caso contrário, o chamador deve definir o valor como S \_ OK antes de chamar o construtor. Se o Construtor falhar, ele definirá o valor como um código de falha.

</dd> </dl>

## <a name="remarks"></a>Comentários

O construtor chama o método [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) para inicializar o tipo de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




