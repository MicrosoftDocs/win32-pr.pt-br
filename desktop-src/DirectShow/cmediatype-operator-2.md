---
description: Esse operador sobrecarrega o operador de atribuição para copiar um tipo de mídia.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'CMediaType. CMediaType:: Operator = Method (mtype. h)-parâmetro mtype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa577c8c8cfcdbcb0b62287a80cd998ab8775c6
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389035"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a>CMediaType. CMediaType:: Operator = método (mtype. h)

Esse operador sobrecarrega o operador de atribuição para copiar um tipo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mtype* \[ referência\]
</dt> <dd>

Referência a uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma referência ao objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




