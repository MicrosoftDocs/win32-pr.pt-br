---
description: A função CreateMediaType aloca uma nova \_ estrutura de tipo de mídia am \_ , incluindo o bloco de formato.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Função CreateMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782253"
---
# <a name="createmediatype-function"></a>Função CreateMediaType

A função **CreateMediaType** aloca uma nova estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , incluindo o bloco de formato.

## <a name="syntax"></a>Sintaxe


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrc* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . O método copia essa estrutura na nova estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma nova estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) ou **NULL** se houver um erro.

## <a name="remarks"></a>Comentários

Para liberar a memória alocada por essa função, chame [**DeleteMediaType**](deletemediatype.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções de tipo de mídia**](media-type-functions.md)
</dt> </dl>

 

 




