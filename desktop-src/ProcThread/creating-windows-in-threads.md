---
description: Qualquer thread pode criar uma janela.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Criando Windows em threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2084536ff43ea4c52efb179177fe6f6c803c49b9f580b2d298b73e9b528f1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143089"
---
# <a name="creating-windows-in-threads"></a>Criando Windows em threads

Qualquer thread pode criar uma janela. O thread que cria a janela possui a janela e sua fila de mensagens associada. Portanto, o thread deve fornecer um loop de mensagem para processar as mensagens em sua fila de mensagens. Além disso, você deve usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) ou [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) nesse thread, em vez das outras funções de [espera,](/windows/desktop/Sync/wait-functions)para que ele possa processar mensagens. Caso contrário, o sistema poderá se tornar deadlock quando o thread for enviado uma mensagem enquanto ele estiver aguardando.

A [**função AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) pode ser usada para permitir que um conjunto de threads compartilhe o mesmo estado de entrada. Ao compartilhar o estado de entrada, os threads compartilham seu conceito de janela ativa. Ao fazer isso, um thread sempre pode ativar a janela de outro thread. Essa função também é útil para compartilhar o estado de foco, o estado de captura do mouse, o estado do teclado e o estado da ordem Z da janela entre janelas criadas por threads diferentes cujo estado de entrada é compartilhado.

Para obter informações sobre como criar janelas, [consulte Windows Classes](../winmsg/window-classes.md).

 

 
