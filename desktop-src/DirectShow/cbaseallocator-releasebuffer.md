---
description: 'O método ReleaseBuffer retorna um exemplo de mídia para a lista de amostras de mídia gratuita. Esse método implementa o método IMemAllocator:: ReleaseBuffer.'
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Método CBaseAllocator. ReleaseBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779856"
---
# <a name="cbaseallocatorreleasebuffer-method"></a>Método CBaseAllocator. ReleaseBuffer

O `ReleaseBuffer` método retorna um exemplo de mídia para a lista de amostras de mídia gratuita. Esse método implementa o método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do objeto de exemplo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Quando a contagem de referência de um exemplo de mídia chega a zero, o exemplo chama **ReleaseBuffer** com ele mesmo como o parâmetro. Esse método executa as seguintes ações.

-   Retorna o exemplo de mídia para a lista livre ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).
-   Chama o método [**CBaseAllocator:: NotifySample**](cbaseallocator-notifysample.md) , que libera todos os threads bloqueados em chamadas para o método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) .
-   Se o método [**CBaseAllocator:: Setnotificar**](cbaseallocator-setnotify.md) foi chamado anteriormente, chama o método **IMemAllocatorNotifyCallbackTemp:: NotifyRelease** .
-   Quando a última amostra for liberada, se houver uma [**CBaseAllocator pendente::D ecommit**](cbaseallocator-decommit.md) chamada, chamará o método [**CBaseAllocator:: Free**](cbaseallocator-free.md) para liberar a memória do buffer. (Na classe base, **Free** é um método virtual puro.)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




