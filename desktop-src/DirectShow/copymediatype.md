---
description: A função CopyMediaType copia uma \_ estrutura de tipo de mídia am \_ para outra estrutura, incluindo o bloco de formato
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Função CopyMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759311"
---
# <a name="copymediatype-function"></a>Função CopyMediaType

A função **CopyMediaType** copia uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) para outra estrutura, incluindo o bloco de formato

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pmtTarget* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . O método copia o tipo de mídia nessa estrutura.

</dd> <dt>

*pmtSource* 
</dt> <dd>

Ponteiro para uma estrutura [**de \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) de origem a ser copiada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função aloca a memória para o bloco de formato. Se o parâmetro *pmtTarget* já contiver um bloco de formato alocado, ocorrerá um vazamento de memória. Para evitar um vazamento de memória, chame [**FreeMediaType**](freemediatype.md) antes de chamar essa função.

Depois que o método retornar, chame [**FreeMediaType**](freemediatype.md) em *pmtTarget* para liberar o bloco de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções de tipo de mídia**](media-type-functions.md)
</dt> </dl>

 

 




