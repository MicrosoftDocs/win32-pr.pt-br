---
description: Um filtro está solicitando que o grafo seja reiniciado.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766994"
---
# <a name="ec_need_restart"></a>o EC \_ precisa ser \_ reiniciado

Um filtro está solicitando que o grafo seja reiniciado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Zero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

O Gerenciador de gráfico de filtro pausa e reinicia o grafo. Ele não passa o evento para o aplicativo.

## <a name="remarks"></a>Comentários

Se um filtro rejeitar um exemplo no meio de um fluxo, o PIN de upstream deixará de fornecer exemplos. O filtro pode reiniciar o fluxo enviando este evento. Por exemplo, o processador de áudio pode perder o acesso ao dispositivo de som, pois uma janela de vídeo perdeu o foco. Nesse ponto, o processador de áudio começa a rejeitar amostras. Quando ele recupera o acesso ao dispositivo de som, ele envia esse evento para reiniciar o fluxo de áudio.

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

 

 




