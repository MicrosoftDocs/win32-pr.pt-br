---
description: O método Receive recebe o próximo exemplo de mídia no fluxo.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Método CBaseRenderer.Receive (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe440b7ac0c7b05c2d3cf9d7ca2019a788e272b7aca6acd6a747738a255ca39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131436"
---
# <a name="cbaserendererreceive-method"></a>Método CBaseRenderer.Receive

O `Receive` método recebe o próximo exemplo de mídia no fluxo.

## <a name="syntax"></a>Sintaxe


```C++
virtual Receive(
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

Retorna S \_ OK se bem-sucedido ou **um valor HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

O pino de entrada chama esse método quando recebe uma amostra do filtro upstream.

Se o filtro estiver em execução, esse método executará as seguintes etapas:

1.  Agenda o exemplo de renderização ([**CBaseRenderer::P repareReceive**](cbaserenderer-preparereceive.md)).
2.  Aguarda a hora agendada ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).
3.  Renderiza o exemplo ([**CBaseRenderer::Render**](cbaserenderer-render.md)).
4.  Libera o exemplo ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).

Se o filtro estiver em pausa, o método executará as seguintes etapas:

1.  Notifica a classe derivada de que um exemplo está disponível ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).
2.  Aguarda a hora agendada.
3.  Renderiza o exemplo.
4.  Libera o exemplo.

Enquanto pausado, o método aguarda na etapa 2 até que o filtro alterna para um estado de execução. Nesse ponto, o filtro agenda o exemplo.

Na classe base, o **método OnReceiveFirstSample** não faz nada. A classe derivada pode substituí-la. Por exemplo, quando um renderador de vídeo é pausado, ele exibe o primeiro exemplo como uma imagem ainda.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




