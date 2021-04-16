---
description: O método SourceThreadCanWait mantém ou libera o thread de streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Método CBaseRenderer. SourceThreadCanWait (Renbase. h)
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
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750668"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>Método CBaseRenderer. SourceThreadCanWait

O `SourceThreadCanWait` método mantém ou libera o thread de streaming.

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

Valor booliano que indica se o thread de streaming deve ser mantido. Se **for true**, o thread de streaming será bloqueado enquanto o filtro aguardar para renderizar os próximos exemplos. Se for **false**, o thread de streaming será liberado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Chamar o `SourceThreadCanWait` método com o valor **false** força o filtro a retornar de uma chamada [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloqueada. Quando o filtro está em execução, ele bloqueia as chamadas de **recebimento** até o tempo de apresentação do exemplo atual. Quando o filtro é pausado, ele bloqueia o **recebimento** de chamadas indefinidamente. Esse comportamento regula o fluxo de dados no fluxo. No entanto, quando o filtro é interrompido ou liberado, ele não deve bloquear.

O bloqueio é controlado pelo método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) , que aguarda dois eventos: [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) e [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md). O evento **m \_ RenderEvent** é sinalizado quando o tempo de apresentação chega. O evento **m \_ ThreadSignal** é sinalizado quando `SourceThreadCanWait` é chamado com o valor **false**. Chamar `SourceThreadCanWait` com o valor **true** redefine o evento.

Os métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chamam `SourceThreadCanWait` com o valor **false** (liberando o thread de streaming). Os métodos [**CBaseRenderer::P ause**](cbaserenderer-pause.md), [**CBaseRenderer:: Run**](cbaserenderer-run.md)e [**CBaseRenderer:: EndFlush**](cbaserenderer-endflush.md) chamam `SourceThreadCanWait` com o valor **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




