---
title: Quando responder à mensagem de WM_GETOBJECT
description: Se um aplicativo oferecer suporte ao Microsoft Acessibilidade Ativa ou automação de interface do usuário para um elemento de interface do usuário, o aplicativo não deverá responder à mensagem do WM \_ GetObject antes que o objeto que representa o elemento da interface do usuário seja totalmente inicializado ou depois que o aplicativo começar a fechar.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdb12edde21b7906fdda91d1bc5d46e453696214b93a331e26034527e163a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114611"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a>Quando responder à mensagem do WM \_ GETobject

Se um aplicativo oferecer suporte ao Microsoft Acessibilidade Ativa ou automação de interface do usuário para um elemento de interface do usuário, o aplicativo não deverá responder à mensagem do [**WM \_ GetObject**](wm-getobject.md) antes que o objeto que representa o elemento da interface do usuário seja totalmente inicializado ou depois que o aplicativo começar a fechar. Quando um aplicativo cria uma nova janela, o sistema gera o [**objeto de evento \_ \_ Create**](event-constants.md) WinEvent para notificar os clientes antes de enviar a mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) para o procedimento de janela do aplicativo. Como muitos aplicativos usam o **WM \_ Create** para iniciar o processo de inicialização, qualquer implementação de acessibilidade de um elemento de interface do usuário não responderá à mensagem do [**WM \_ GetObject**](wm-getobject.md) até que o aplicativo tenha terminado de processar a mensagem de **\_ criação do WM** .

 

 