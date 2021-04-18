---
description: Saiba mais sobre o método do Construtor CMediaType. CMediaType (mtype. h). Esse método usa os parâmetros ' mtype ' e ' PHR '.
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: Construtor CMediaType. CMediaType (mtype. h)-parâmetros mtype e PHR
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
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105811326"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>Construtor CMediaType. CMediaType (mtype. h)-parâmetros mtype e PHR

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mtype* \[ referência\]
</dt> <dd>

Referência a uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . O construtor copia o tipo de mídia para o novo objeto, incluindo o bloco de formato, se houver.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor HRESULT. Esse parâmetro pode ser um ponteiro **nulo** . Caso contrário, o chamador deve definir o valor como S \_ OK antes de chamar o construtor. Se o Construtor falhar, ele definirá o valor como um código de falha.

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

 

 




