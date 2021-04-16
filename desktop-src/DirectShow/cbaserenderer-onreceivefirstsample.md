---
description: O método OnReceiveFirstSample é chamado quando o filtro recebe um exemplo enquanto está em pausa.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Método CBaseRenderer. OnReceiveFirstSample (Renbase. h)
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
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750486"
---
# <a name="cbaserendereronreceivefirstsample-method"></a>Método CBaseRenderer. OnReceiveFirstSample

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

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) chama esse método. Ele não faz nada na classe base, mas a classe derivada pode substituí-la. Esse método destina-se principalmente a renderizadores de vídeo. Quando um processador de vídeo é pausado, ele normalmente exibe a primeira amostra como uma imagem ainda.

Procurar o grafo enquanto estiver em pausa também faz com que esse método seja chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




