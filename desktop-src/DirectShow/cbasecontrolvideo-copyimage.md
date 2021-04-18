---
description: Cria uma cópia de memória de uma imagem.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Método CBaseControlVideo. CopyImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751285"
---
# <a name="cbasecontrolvideocopyimage-method"></a>Método CBaseControlVideo. CopyImage

Cria uma cópia de memória de uma imagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para o exemplo que contém a imagem de vídeo.

</dd> <dt>

*pVideoInfo* 
</dt> <dd>

Ponteiro para o formato que representa a imagem de vídeo.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Ponteiro para o tamanho do buffer de saída.

</dd> <dt>

*pVideoImage* 
</dt> <dd>

Ponteiro para o buffer de saída.

</dd> <dt>

*pSourceRect* 
</dt> <dd>

Ponteiro para o retângulo de vídeo de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o parâmetro *pVideoImage* for **NULL**, o parâmetro *pBufferSize* será preenchido com o número de bytes que o buffer de saída exigirá para armazenar a imagem. Se o buffer passado for muito pequeno ou a função membro falhar em alocar memória suficiente, a função de membro retornará E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A função membro recupera a imagem do exemplo e a copia para o buffer de saída. A seção de vídeo copiada no buffer de saída reflete o retângulo de origem que é definido por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) (embora não reflita o retângulo de destino).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




