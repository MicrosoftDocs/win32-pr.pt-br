---
description: O método SourceThreadCanWait contém ou libera o thread de streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Método CBaseRenderer.SourceThreadCanWait (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba9f8e202d7c98bfea5d7068fa63a8d889d88fb10b4c6a7cb3516fadbca7ebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954765"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>Método CBaseRenderer.SourceThreadCanWait

O `SourceThreadCanWait` método contém ou libera o thread de streaming.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bCanWait* 
</dt> <dd>

Valor booliana que indica se o thread de streaming deve ser re mão. Se **TRUE**, o thread de streaming será bloqueado enquanto o filtro aguarda para renderizar os próximos exemplos. Se **FALSE**, o thread de streaming será liberado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Chamar o método com o valor FALSE força o filtro a retornar de uma chamada `SourceThreadCanWait` [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloqueada.  Quando o filtro está em execução, ele bloqueia **Receber chamadas** até a hora de apresentação do exemplo atual. Quando o filtro é pausado, ele bloqueia **receber chamadas** indefinidamente. Esse comportamento regula o fluxo de dados no fluxo. No entanto, quando o filtro é interrompido ou liberado, ele não deve ser bloqueado.

O bloqueio é controlado pelo [**método CBaseRenderer::WaitForRenderTime,**](cbaserenderer-waitforrendertime.md) que aguarda dois eventos: [**CBaseRenderer::m \_ RenderEvent**](cbaserenderer-m-renderevent.md) e [**CBaseRenderer::m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md). O **evento m \_ RenderEvent** é sinalizado quando a hora da apresentação chega. O **evento m \_ ThreadSignal** é sinalizado quando `SourceThreadCanWait` é chamado com o valor **FALSE.** Chamar `SourceThreadCanWait` com o valor **TRUE** redefine o evento.

Os [**métodos CBaseRenderer::Stop**](cbaserenderer-stop.md) e [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) chamam com o valor `SourceThreadCanWait` **FALSE** (liberando o thread de streaming). Os [**métodos CBaseRenderer::P ause**](cbaserenderer-pause.md), [**CBaseRenderer::Run**](cbaserenderer-run.md)e [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) chamam com o valor `SourceThreadCanWait` **TRUE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




