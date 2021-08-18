---
title: O objeto CommandsWindow
description: O objeto CommandsWindow
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336bdff598a75a9b0b07adabb11c271a45ca84940f528ebe082de17841592d31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882460"
---
# <a name="the-commandswindow-object"></a>O objeto CommandsWindow

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O objeto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) fornece acesso às propriedades da janela de comandos de voz. A janela de comandos de voz é um recurso compartilhado projetado principalmente para permitir que os usuários exibam comandos habilitados para voz. Se o reconhecimento de fala estiver desabilitado, a janela comandos de voz ainda será exibida, com o texto "entrada de fala desabilitada" (no idioma do caractere). Se não houver nenhum mecanismo de fala instalado que corresponda à configuração de idioma do caractere, a janela será exibida, "entrada de fala não disponível". Se o cliente de entrada-ativo não tiver definido parâmetros de voz para seus comandos e tiver desabilitado os comandos de voz globais, a janela exibirá "nenhum comando de voz". Você também pode consultar as propriedades da janela de comandos de voz independentemente se a entrada de fala está desabilitada ou se um mecanismo de fala compatível está instalado.

-   [Propriedades de CommandsWindow](commandswindow-properties.md)

 

 