---
description: Notifica um filtro da janela do renderador de vídeo.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355d4ec8b5b6bea55a2f32f01cc2f83aabeab84443b28e431e5b0d6155acc6d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820107"
---
# <a name="ec_notify_window"></a>JANELA \_ NOTIFICAÇÃO \_ DE EC

Notifica um filtro da janela do renderador de vídeo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

(**HWND**) Lidar com a janela.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Esse evento é usado internamente por DirectShow. O gerenciador de grafo de filtro não passa esse evento para o aplicativo. Os aplicativos não podem substituir a ação padrão para esse evento.

## <a name="remarks"></a>Comentários

Quando um renderador de vídeo está conectado, ele verifica se o pino de saída upstream dá suporte à interface [**IMediaEventSink.**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) Nesse caso, o renderista envia esse evento para o filtro upstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




