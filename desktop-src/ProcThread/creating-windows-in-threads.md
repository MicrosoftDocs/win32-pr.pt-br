---
description: Qualquer thread pode criar uma janela.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Criando janelas em threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787040"
---
# <a name="creating-windows-in-threads"></a>Criando janelas em threads

Qualquer thread pode criar uma janela. O thread que cria a janela possui a janela e sua fila de mensagens associada. Portanto, o thread deve fornecer um loop de mensagem para processar as mensagens em sua fila de mensagens. Além disso, você deve usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) ou [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) nesse thread, em vez de outras [funções Wait](/windows/desktop/Sync/wait-functions), para que ele possa processar mensagens. Caso contrário, o sistema poderá ser bloqueado quando o thread receber uma mensagem enquanto estiver aguardando.

A função [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) pode ser usada para permitir que um conjunto de threads Compartilhe o mesmo estado de entrada. Ao compartilhar o estado de entrada, os threads compartilham seu conceito de janela ativa. Ao fazer isso, um thread sempre pode ativar outra janela do thread. Essa função também é útil para compartilhar o estado de foco, o estado de captura do mouse, o estado do teclado e o estado de ordem Z da janela entre o Windows criado por diferentes threads cujo estado de entrada é compartilhado.

Para obter informações sobre como criar janelas, consulte [classes do Windows](../winmsg/window-classes.md).

 

 
