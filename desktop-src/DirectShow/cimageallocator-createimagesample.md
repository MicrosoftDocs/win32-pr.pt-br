---
description: O método CreateImageSample cria um exemplo de mídia.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Método CImageAllocator. CreateImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750045"
---
# <a name="cimageallocatorcreateimagesample-method"></a>Método CImageAllocator. CreateImageSample

O `CreateImageSample` método cria um exemplo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* 
</dt> <dd>

Ponteiro para um buffer de *comprimento* de tamanho, alocado pelo chamador.

</dd> <dt>

*Comprimento* 
</dt> <dd>

Comprimento do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um objeto [**CImageSample**](cimagesample.md) .

## <a name="remarks"></a>Comentários

Esse método cria um novo exemplo de mídia, implementado como um objeto **CImageSample** . O método [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) do exemplo retorna um ponteiro para o buffer especificado no parâmetro *pData* .

Se você derivar uma nova classe de alocador de [**CImageAllocator**](cimageallocator.md) e uma nova classe de exemplo de mídia de [**CImageSample**](cimagesample.md), deverá substituir esse método para criar uma instância da classe de exemplo de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator:: Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




