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
ms.openlocfilehash: b5960ac5f9dc3e685aa0b8b281989185580fd5b683392aaf93a0891d0ebaa35d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016255"
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

## <a name="return-value"></a>Valor retornado

Retorna uma referência ao objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




