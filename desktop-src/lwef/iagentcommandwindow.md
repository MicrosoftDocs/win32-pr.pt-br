---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765713"
---
# <a name="iagentcommandwindow"></a>IAgentCommandWindow

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

**IAgentCommandWindow** define uma interface que permite que os aplicativos definam e consultem as propriedades da janela de comandos de voz. A janela de comandos de voz é um recurso compartilhado projetado principalmente para permitir que os usuários exibam comandos habilitados para voz. Se o reconhecimento de fala estiver desabilitado, a janela comandos de voz ainda será exibida, com o texto "entrada de fala desabilitada" (no idioma do caractere). Se nenhum mecanismo de fala estiver instalado que corresponda à configuração de idioma do caractere, a janela será exibida, "entrada de fala não disponível". Se o cliente de entrada-ativo não tiver definido parâmetros de voz para seus comandos e tiver desabilitado os comandos de voz globais, a janela exibirá "nenhum comando de voz". Você também pode consultar as propriedades da janela de comandos de voz independentemente se a entrada de fala está desabilitada ou se um mecanismo de fala compatível está instalado.

**Métodos em ordem vtable**



| Métodos IAgentCommandWindow                             | Descrição                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Não visível**](iagentcommandwindow--setvisible.md)   | Define o valor da propriedade [**Visible**](visible-property.md) da janela de comandos de voz.    |
| [**GetVisible**](iagentcommandwindow--getvisible.md)   | Retorna o valor da propriedade [**Visible**](visible-property.md) da janela de comandos de voz. |
| [**GetPosition**](iagentcommandwindow--getposition.md) | Retorna a posição da janela de comandos de voz.                                                  |
| [**GetSize**](iagentcommandwindow--getsize.md)         | Retorna o tamanho da janela de comandos de voz.                                                      |



 

 

 




