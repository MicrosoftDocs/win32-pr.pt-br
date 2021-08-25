---
title: Visão geral da interface de programação do Microsoft Agent
description: Visão geral da interface de programação do Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4dc087064afb0e3beaaf97d987e496239d3fd378461acaf5601927ac6d929
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887916"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Visão geral da interface de programação do Microsoft Agent

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A API do Microsoft Agent fornece serviços que suportam a exibição e animação de caracteres animados. Implementado como um servidor com COM (Automação OLE Component Object Model), o Microsoft Agent permite que vários aplicativos, chamados de clientes ou aplicativos cliente, hospedem e acessem seus serviços de animação, entrada e saída ao \[ \] mesmo tempo. Um cliente pode ser qualquer aplicativo que se conecta às interfaces COM do Microsoft Agent.

Como um servidor COM, o Microsoft Agent é iniciado automaticamente somente quando um aplicativo cliente usa as interfaces COM e solicitações para se conectar a ele. Ele permanece em execução até que todos os clientes fechem suas conexões. Quando nenhum cliente conectado permanece, o Microsoft Agent sai automaticamente.

Embora você possa chamar as interfaces COM do Microsoft Agent diretamente, o Microsoft Agent também inclui um controle microsoft ActiveX. Esse controle facilita o acesso aos serviços do Microsoft Agent de linguagens de programação que suportam a interface ActiveX controle.

Além de dar suporte a programas autônomos escritos para Windows, o Agent pode ser roteado para dar suporte a páginas da Web, desde que o navegador seja compatível com a interface ActiveX. O Microsoft Internet Explorer inclui suporte para ActiveX, bem como linguagens de script que você pode usar para programar o Agent. Se você não estiver usando Internet Explorer, consulte seu fornecedor ou fornecedor sobre o suporte do navegador para ActiveX.

As informações a seguir fornece uma breve visão geral das interfaces de programação para o software do Microsoft Agent.

-   [Serviços de animação](animation-services.md)
-   [Serviços de Entrada](input-services.md)
-   [A janela Comandos de Voz](the-voice-commands-window.md)
-   [Serviços de Saída](output-services.md)

 

 




