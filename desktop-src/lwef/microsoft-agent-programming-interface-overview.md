---
title: Visão geral da interface de programação do Microsoft Agent
description: Visão geral da interface de programação do Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822667"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Visão geral da interface de programação do Microsoft Agent

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A API do Microsoft Agent fornece serviços que dão suporte à exibição e animação de caracteres animados. Implementado como um servidor de automação OLE (Component Object Model \[ com \] ), o Microsoft Agent permite que vários aplicativos, chamados de clientes ou aplicativos cliente, hospedem e acessem seus serviços de animação, entrada e saída ao mesmo tempo. Um cliente pode ser qualquer aplicativo que se conecta às interfaces COM do Microsoft Agent.

Como um servidor COM, o Microsoft Agent é iniciado automaticamente somente quando um aplicativo cliente usa as interfaces COM e as solicitações para se conectar a ele. Ele permanece em execução até que todos os clientes fechem suas conexões. Quando nenhum cliente conectado permanece, o Microsoft Agent é encerrado automaticamente.

Embora você possa chamar as interfaces COM do Microsoft Agent diretamente, o Microsoft Agent também inclui um controle Microsoft ActiveX. Esse controle facilita o acesso aos serviços do Microsoft Agent a partir de linguagens de programação que dão suporte à interface do controle ActiveX.

Além de dar suporte a programas autônomos escritos para o Windows, o Agent pode ser inserido no script para dar suporte a páginas da Web, desde que o navegador dê suporte à interface do ActiveX. O Microsoft Internet Explorer inclui suporte para ActiveX, bem como linguagens de script que você pode usar para programar o agente. Se você não estiver usando o Internet Explorer, consulte seu fornecedor ou fornecedor sobre o suporte do navegador para ActiveX.

As informações a seguir fornecem uma breve visão geral das interfaces de programação para o software Microsoft Agent.

-   [Serviços de animação](animation-services.md)
-   [Serviços de entrada](input-services.md)
-   [A janela comandos de voz](the-voice-commands-window.md)
-   [Serviços de saída](output-services.md)

 

 




