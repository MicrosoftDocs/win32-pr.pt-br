---
description: O método OnReceiveFirstSample é chamado quando o filtro recebe uma amostra enquanto está em pausa.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Método CBaseRenderer.OnReceiveFirstSample (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 882a356f47aa146ec8ba1b06d7af43235c8213334c0d82d0a241c590654bf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157696"
---
# <a name="cbaserendereronreceivefirstsample-method"></a>Método CBaseRenderer.OnReceiveFirstSample

O `OnReceiveFirstSample` método é chamado quando o filtro recebe um exemplo enquanto está em pausa.

## <a name="syntax"></a>Sintaxe


```C++
virtual void OnReceiveFirstSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample do**](/windows/desktop/api/Strmif/nn-strmif-imediasample) exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O [**método CBaseRenderer::Receive**](cbaserenderer-receive.md) chama esse método. Ele não faz nada na classe base, mas a classe derivada pode substituí-la. Esse método destina-se principalmente a renderadores de vídeo. Quando um renderador de vídeo é pausado, ele normalmente exibe o primeiro exemplo como uma imagem ainda.

Buscar o grafo enquanto está em pausa também faz com que esse método seja chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




