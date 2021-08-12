---
description: O método ReleaseBuffer retorna um exemplo de mídia para a lista de exemplos de mídia livre. Esse método implementa o método IMemAllocator::ReleaseBuffer.
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Método CBaseAllocator.ReleaseBuffer (Amfilter.h)
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
ms.openlocfilehash: 5d1096cc7cd4ed31346b38719a3f622edf780408fd50262d93515f68d92b421d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661502"
---
# <a name="cbaseallocatorreleasebuffer-method"></a>Método CBaseAllocator.ReleaseBuffer

O `ReleaseBuffer` método retorna um exemplo de mídia para a lista de exemplos de mídia livre. Esse método implementa o [**método IMemAllocator::ReleaseBuffer.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer)

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

Ponteiro para a [**interface IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do objeto de exemplo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Quando a contagem de referência de um exemplo de mídia atinge zero, o exemplo chama **ReleaseBuffer** com si mesmo como o parâmetro . Esse método executa as seguintes ações.

-   Retorna o exemplo de mídia para a lista gratuita ([**CBaseAllocator::m \_ lFree**](cbaseallocator-m-lfree.md)).
-   Chama o [**método CBaseAllocator::NotifySample,**](cbaseallocator-notifysample.md) que libera todos os threads bloqueados em chamadas para o [**método CBaseAllocator::GetBuffer.**](cbaseallocator-getbuffer.md)
-   Se o [**método CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) tiver sido chamado anteriormente, chamará o método **IMemAllocatorNotifyCallbackTemp::NotifyRelease.**
-   Quando o último exemplo for liberado, se houver uma chamada [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) pendente, chamará o método [**CBaseAllocator::Free**](cbaseallocator-free.md) para liberar a memória do buffer. (Na classe base, **Free** é um método virtual puro.)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




