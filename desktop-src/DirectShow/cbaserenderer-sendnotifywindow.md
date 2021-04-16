---
description: O método SendNotifyWindow notifica o filtro upstream do identificador da janela de vídeo.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Método CBaseRenderer. SendNotifyWindow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752298"
---
# <a name="cbaserenderersendnotifywindow-method"></a>Método CBaseRenderer. SendNotifyWindow

O `SendNotifyWindow` método notifica o filtro upstream do identificador da janela de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída do filtro upstream.

</dd> <dt>

*HWND* 
</dt> <dd>

Manipular para a janela de vídeo ou **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o pino de saída do filtro upstream der suporte à interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) , esse método enviará a ele o código de evento da [**janela de \_ notificação \_ do EC**](ec-notify-window.md) junto com o identificador de janela.

Os renderizadores de vídeo podem substituir seus métodos [**CBaseRenderer:: CompleteConnect**](cbaserenderer-completeconnect.md) para chamar esse método. Ele fornece um mecanismo para informar o filtro upstream do identificador de janela. Se você fizer isso, substitua o método [**CBaseRenderer:: BreakConnect**](cbaserenderer-breakconnect.md) também e chame `SendNotifyWindow` um identificador **nulo** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




