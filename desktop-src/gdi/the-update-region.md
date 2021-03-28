---
description: A região de atualização identifica a parte de uma janela que está desatualizada ou inválida e precisa de redesenho.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: A região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989086"
---
# <a name="the-update-region"></a>A região de atualização

A *região de atualização* identifica a parte de uma janela que está desatualizada ou inválida e precisa de redesenho. O sistema usa a região de atualização para gerar mensagens de [**\_ pintura do WM**](wm-paint.md) para aplicativos e minimizar o tempo gasto pelos aplicativos colocando o conteúdo de suas janelas atualizadas. O sistema adiciona apenas a parte inválida da janela à região de atualização, exigindo que apenas essa parte seja desenhada.

Quando o sistema determina que uma janela precisa ser atualizada, ele define as dimensões da região de atualização para a parte inválida da janela. Definir a região de atualização não faz com que o aplicativo seja desenhado imediatamente. Em vez disso, o aplicativo continua recuperando mensagens da fila de mensagens do aplicativo até que nenhuma mensagem permaneça. Em seguida, o sistema verifica a região de atualização e, se a região não estiver vazia (não nula), ela enviará uma mensagem de [**\_ pintura do WM**](wm-paint.md) para o procedimento de janela.

Um aplicativo pode usar a região de atualização para gerar suas mensagens do [**WM \_ Paint**](wm-paint.md) . Por exemplo, um aplicativo que carrega dados de arquivos abertos normalmente define a região de atualização durante o carregamento para que novos dados sejam desenhados durante o processamento da próxima mensagem do **WM \_ Paint** . Em geral, um aplicativo não deve ser desenhado no momento em que seus dados são alterados, mas roteia todas as operações de desenho por meio da mensagem do **WM \_ Paint** .

 

 



