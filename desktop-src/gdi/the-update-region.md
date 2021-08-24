---
description: A região de atualização identifica a parte de uma janela que está des date ou inválida e que precisa ser redesenhada.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: A região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a8f847a1e2d479200cfe6ea4e60a1b3a8ebf4c02aaf7c89fc719f62d91e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717966"
---
# <a name="the-update-region"></a>A região de atualização

A *região de* atualização identifica a parte de uma janela que está des date ou inválida e que precisa ser redesenhada. O sistema usa a região de atualização para gerar mensagens [**WM \_ PAINT**](wm-paint.md) para aplicativos e minimizar o tempo que os aplicativos gastam para atualizar o conteúdo de suas janelas. O sistema adiciona apenas a parte inválida da janela à região de atualização, exigindo que apenas essa parte seja desenhada.

Quando o sistema determina que uma janela precisa de atualização, ele define as dimensões da região de atualização para a parte inválida da janela. Definir a região de atualização não faz com que o aplicativo seja desenhar imediatamente. Em vez disso, o aplicativo continua recuperando mensagens da fila de mensagens do aplicativo até que nenhuma mensagem permaneça. Em seguida, o sistema verifica a região de atualização e, se a região não estiver vazia (não NULL), ele enviará uma mensagem [**WM \_ PAINT**](wm-paint.md) para o procedimento de janela.

Um aplicativo pode usar a região de atualização para gerar suas [**mensagens WM \_ PAINT.**](wm-paint.md) Por exemplo, um aplicativo que carrega dados de arquivos abertos normalmente define a região de atualização durante o carregamento para que novos dados são desenhados durante o processamento da próxima mensagem **WM \_ PAINT.** Em geral, um aplicativo não deve desenhar no momento em que seus dados são atualizados, mas roteia todas as operações de desenho por meio da **mensagem WM \_ PAINT.**

 

 



