---
description: O método Copy copia um exemplo de mídia.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: Método CTransInPlaceFilter.Copy (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10a7a2927789ffe49d37912862580222f0ed06d9648b6312cbb044e357d6e61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053516"
---
# <a name="ctransinplacefiltercopy-method"></a>Método CTransInPlaceFilter.Copy

O `Copy` método copia um exemplo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Psource* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para a interface **IMediaSample** no novo exemplo.

## <a name="remarks"></a>Comentários

Esse método recupera um buffer vazio do alocador downstream. Ele copia todas as propriedades de exemplo do *pSource* para o novo exemplo, juntamente com os dados reais no exemplo. Se o filtro estiver usando dois alocadores, ele chamará esse método para copiar dados entre buffers.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




