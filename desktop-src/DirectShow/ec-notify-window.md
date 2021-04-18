---
description: Notifica um filtro sobre a janela do processador de vídeo.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810175"
---
# <a name="ec_notify_window"></a>\_janela de notificação do EC \_

Notifica um filtro sobre a janela do processador de vídeo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HWND**) Identificador para a janela.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Esse evento é usado internamente pelo DirectShow. O Gerenciador do grafo de filtro não passa esse evento para o aplicativo. Os aplicativos não podem substituir a ação padrão para este evento.

## <a name="remarks"></a>Comentários

Quando um processador de vídeo é conectado, ele verifica se o pino de saída upstream dá suporte à interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) . Nesse caso, o renderizador envia esse evento para o filtro upstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




