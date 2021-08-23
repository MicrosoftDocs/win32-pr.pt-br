---
title: IAgentCommandsEx
description: IAgentCommandsEx
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff4ff8e6dc87eb1a5fa5c3e79fe26b00d8bd3c8eb18a5fc6ca7cac22d3dfd07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976256"
---
# <a name="iagentcommandsex"></a>IAgentCommandsEx

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

[**IAgentCommandsEx**](iagentcommandex.md) define uma interface que estende a interface [**IAgentCommands.**](iagentcommands.md)

**Métodos em ordem Vtable**



| Métodos IAgentCommandsEx                                                             | Descrição                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SetDefaultID](iagentcommandsex--setdefaultid.md)                                   | Define o comando padrão para o menu pop-up do caractere.                                                     |
| [GetDefaultID](iagentcommandsex--getdefaultid.md)                                   | Retorna o comando padrão para o menu pop-up do caractere.                                                  |
| [**SetHelpContextID**](iagentcommandex--sethelpcontextid.md)                        | Define a ID do tópico de ajuda contextitivo para um [**objeto Command.**](/windows/desktop/lwef/the-command-object)                     |
| [**GetHelpContextID**](iagentcommandex--gethelpcontextid.md)                        | Retorna a ID do tópico de ajuda contextitivo para um [**objeto Command.**](/windows/desktop/lwef/the-command-object)                  |
| [SetFontName](iagentcommandsex--setfontname.md)                                     | Define a fonte a ser usada no menu pop-up do caractere.                                                          |
| [GetFontName](iagentcommandsex--getfontname.md)                                     | Retorna a fonte usada no menu pop-up do caractere.                                                         |
| [Setfontsize](iagentcommandsex--setfontsize.md)                                     | Define o tamanho da fonte a ser usado no menu pop-up do caractere.                                                     |
| [GetFontSize](iagentcommandsex--getfontsize.md)                                     | Retorna o tamanho da fonte usado no menu pop-up do caractere.                                                    |
| [**SetVoiceCaption**](iagentcommandex--setvoicecaption.md)                          | Define a legenda de voz para o objeto [**Command do**](/windows/desktop/lwef/the-command-object) caractere.                         |
| [**GetVoiceCaption**](iagentcommandex--getvoicecaption.md)                          | Retorna a legenda de voz para o objeto [**Command do**](/windows/desktop/lwef/the-command-object) caractere.                      |
| [AddEx](iagentcommandsex--addex.md)                                                 | Adiciona um [**objeto Command**](/windows/desktop/lwef/the-command-object) a uma [**coleção Commands.**](/windows/desktop/lwef/the-commands-collection-object)    |
| [InsertEx](iagentcommandsex--insertex.md)                                           | Insere um [**objeto Command**](/windows/desktop/lwef/the-command-object) em uma [**coleção De**](/windows/desktop/lwef/the-commands-collection-object) comandos. |
| [SetGlobalVoiceCommandsEnabled](iagentcommandsex--setglobalvoicecommandsenabled.md) | Habilita a gramática de voz para comandos globais do Agent.                                                        |
| [GetGlobalVoiceCommandsEnabled](iagentcommandsex--getglobalvoicecommandsenabled.md) | Retorna se a gramática de voz dos comandos globais do Agent está habilitada.                                     |



 

 

 