---
description: O método Receive recebe o exemplo de próxima mídia no fluxo.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Método CBaseRenderer. Receive (Renbase. h)
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
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770292"
---
# <a name="cbaserendererreceive-method"></a>Método CBaseRenderer. Receive

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

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

O pino de entrada chama esse método quando ele recebe uma amostra do filtro upstream.

Se o filtro estiver em execução, esse método executará as seguintes etapas:

1.  Agenda o exemplo de renderização ([**CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md)).
2.  Aguarda o horário agendado ([**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).
3.  Renderiza o exemplo ([**CBaseRenderer:: render**](cbaserenderer-render.md)).
4.  Libera o exemplo ([**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md)).

Se o filtro for pausado, o método executará as seguintes etapas:

1.  Notifica a classe derivada de que um exemplo está disponível ([**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).
2.  Aguarda o horário agendado.
3.  Renderiza o exemplo.
4.  Libera o exemplo.

Enquanto estiver em pausa, o método aguardará na etapa 2 até que o filtro alterne para um estado de execução. Nesse ponto, o filtro agenda o exemplo.

Na classe base, o método **OnReceiveFirstSample** não faz nada. A classe derivada pode substituí-la. Por exemplo, quando um processador de vídeo é pausado, ele exibe a primeira amostra como uma imagem ainda.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




