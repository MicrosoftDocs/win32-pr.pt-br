---
description: 'O método GetBuffer Recupera um exemplo de mídia que contém um buffer. Esse método implementa o método IMemAllocator:: GetBuffer.'
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Método CBaseAllocator. GetBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a183079e954b3a0d8b07fc1d7daf039db8fcc840243a6ea421b2390ce02a3625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661678"
---
# <a name="cbaseallocatorgetbuffer-method"></a>Método CBaseAllocator. GetBuffer

O `GetBuffer` método recupera um exemplo de mídia que contém um buffer. Esse método implementa o método [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Recebe um ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do buffer. O chamador deve liberar a interface.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Ponteiro para a hora de início do exemplo.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Ponteiro para a hora de término do exemplo.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Combinação de bits bit a zero ou mais sinalizadores. A classe base oferece suporte ao sinalizador a seguir.



| Valor                                                                                                                                                          | Significado                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <dt>**\_gbf \_ nowait**</dt> </dl> | Não aguarde até que um buffer fique disponível. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                           | Descrição                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                     |
| <dl> <dt>**VFW \_ E \_ não \_ confirmado**</dt> </dl> | O alocador não foi confirmado.<br/> |
| <dl> <dt>**\_ \_ tempo limite de VFW E**</dt> </dl>        | Tempo limite atingido.<br/>                   |



 

## <a name="remarks"></a>Comentários

A menos que o chamador especifique o sinalizador **am \_ gbf \_ nowait** no *dwFlags*, esse método será bloqueado até que a próxima amostra esteja disponível.

O exemplo de mídia recuperada tem um ponteiro válido para o buffer alocado. O chamador é responsável por definir quaisquer outras propriedades no exemplo, como carimbos de data/hora, horários de mídia ou a propriedade de ponto de sincronização. Para obter mais informações, consulte [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).

Na classe base, os parâmetros *pStartTime* e *pEndTime* são ignorados. Classes derivadas podem usar esses valores. Por exemplo, o alocador do filtro de [processador de vídeo](video-renderer-filter.md) usa esses valores para sincronizar a alternância entre as superfícies do DirectDraw.

Se o método precisar aguardar um exemplo, ele incrementará a contagem de objetos em espera ([**CBaseAllocator:: m \_ lCount**](cbaseallocator-m-lcount.md)) e a função calls [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) no semáforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)). Quando um exemplo se torna disponível, ele chama o método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) no alocador, o que aumenta a contagem de semáforos por **m \_ lCount** (liberando assim os threads em espera) e define **m \_ lCount** de volta para zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

