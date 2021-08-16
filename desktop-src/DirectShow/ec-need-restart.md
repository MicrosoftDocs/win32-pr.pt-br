---
description: Um filtro está solicitando que o grafo seja reiniciado.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae3426048229c19b1d35a061d67d3d1d0a3149a8f820e891987c88405b76f7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820138"
---
# <a name="ec_need_restart"></a>EC \_ NEED \_ RESTART

Um filtro está solicitando que o grafo seja reiniciado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

Zero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

O gerenciador de grafo de filtro pausa e reinicia o grafo. Ele não passa o evento para o aplicativo.

## <a name="remarks"></a>Comentários

Se um filtro rejeitar uma amostra no meio de um fluxo, o pino upstream interromperá o fornecimento de amostras. O filtro pode reiniciar o fluxo enviando esse evento. Por exemplo, o renderador de áudio pode perder o acesso ao dispositivo de som, porque uma janela de vídeo perdeu o foco. Nesse ponto, o renderador de áudio começa a rejeitar exemplos. Quando ele recupera o acesso ao dispositivo de som, ele envia esse evento para reiniciar o fluxo de áudio.

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

 

 




