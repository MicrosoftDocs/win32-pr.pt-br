---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80509efbe4f9d6391b3ac6ffbdf5cb02580826fd1aa7a94f1536ba5706322606
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105164"
---
# <a name="iagentcommandwindow"></a>IAgentCommandWindow

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

**IAgentCommandWindow** define uma interface que permite que os aplicativos definam e consultem as propriedades da janela de comandos de voz. A janela de comandos de voz é um recurso compartilhado projetado principalmente para permitir que os usuários exibam comandos habilitados para voz. Se o reconhecimento de fala estiver desabilitado, a janela comandos de voz ainda será exibida, com o texto "entrada de fala desabilitada" (no idioma do caractere). Se nenhum mecanismo de fala estiver instalado que corresponda à configuração de idioma do caractere, a janela será exibida, "entrada de fala não disponível". Se o cliente de entrada-ativo não tiver definido parâmetros de voz para seus comandos e tiver desabilitado os comandos de voz globais, a janela exibirá "nenhum comando de voz". Você também pode consultar as propriedades da janela de comandos de voz independentemente se a entrada de fala está desabilitada ou se um mecanismo de fala compatível está instalado.

**Métodos em ordem vtable**



| Métodos IAgentCommandWindow                             | Descrição                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Não visível**](iagentcommandwindow--setvisible.md)   | Define o valor da propriedade [**Visible**](visible-property.md) da janela de comandos de voz.    |
| [**GetVisible**](iagentcommandwindow--getvisible.md)   | Retorna o valor da propriedade [**Visible**](visible-property.md) da janela de comandos de voz. |
| [**GetPosition**](iagentcommandwindow--getposition.md) | Retorna a posição da janela de comandos de voz.                                                  |
| [**GetSize**](iagentcommandwindow--getsize.md)         | Retorna o tamanho da janela de comandos de voz.                                                      |



 

 

 




