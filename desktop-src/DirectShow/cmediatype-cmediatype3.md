---
description: Saiba mais sobre o método do construtor CMediaType.CMediaType (Mtype.h). Esse método usa os parâmetros 'mtype' e 'phr'.
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: Construtor CMediaType.CMediaType (Mtype.h) – parâmetros mtype e phr
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
ms.openlocfilehash: 0c399073794f025122e1cfade3f15b3a96784f28e171482e4dcfb7bcec6a8271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084476"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>Construtor CMediaType.CMediaType (Mtype.h) – parâmetros mtype e phr

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mtype* \[ Ref\]
</dt> <dd>

Referência a uma [**estrutura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) O construtor copia o tipo de mídia para o novo objeto, incluindo o bloco de formato, se for o caso.

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor HRESULT. Esse parâmetro pode ser um **ponteiro NULL.** Caso contrário, o chamador deverá definir o valor como S \_ OK antes de chamar o construtor. Se o construtor falhar, ele define o valor como um código de falha.

</dd> </dl>

## <a name="remarks"></a>Comentários

O construtor chama o [**método CMediaType::InitMediaType**](cmediatype-initmediatype.md) para inicializar o tipo de mídia.

## <a name="requirements"></a>Requisitos

| Requisito                   | Valor                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | Mtype.h (incluir Fluxos.h)                                                                                     |
| Biblioteca | Strmbase.lib (builds de varejo); Strmbasd.lib (builds de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




