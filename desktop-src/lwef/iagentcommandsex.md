---
title: IAgentCommandsEx
description: IAgentCommandsEx
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16616ccb86bf109dad85a8ee2ac5d2bd009827
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105793955"
---
# <a name="iagentcommandsex"></a>IAgentCommandsEx

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

[**IAgentCommandsEx**](iagentcommandex.md) define uma interface que estende a interface [**IAgentCommands**](iagentcommands.md) .

**Métodos em ordem vtable**



| Métodos IAgentCommandsEx                                                             | Descrição                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Setpadrãoid](iagentcommandsex--setdefaultid.md)                                   | Define o comando padrão para o menu pop-up do caractere.                                                     |
| [Getdefaultid](iagentcommandsex--getdefaultid.md)                                   | Retorna o comando padrão para o menu pop-up do caractere.                                                  |
| [**Setidentificaçãodocontextodaajuda**](iagentcommandex--sethelpcontextid.md)                        | Define a ID do tópico de ajuda sensível ao contexto para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                     |
| [**Getidentificaçãodocontextodaajuda**](iagentcommandex--gethelpcontextid.md)                        | Retorna a ID do tópico de ajuda sensível ao contexto de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                  |
| [Setnomedafonte](iagentcommandsex--setfontname.md)                                     | Define a fonte a ser usada no menu pop-up do caractere.                                                          |
| [GetFontName](iagentcommandsex--getfontname.md)                                     | Retorna a fonte usada no menu pop-up do caractere.                                                         |
| [Setfontize](iagentcommandsex--setfontsize.md)                                     | Define o tamanho da fonte a ser usada no menu pop-up do caractere.                                                     |
| [GetFontSize](iagentcommandsex--getfontsize.md)                                     | Retorna o tamanho da fonte usado no menu pop-up do caractere.                                                    |
| [**SetVoiceCaption**](iagentcommandex--setvoicecaption.md)                          | Define a legenda de voz para o objeto de [**comando**](/windows/desktop/lwef/the-command-object) do caractere.                         |
| [**GetVoiceCaption**](iagentcommandex--getvoicecaption.md)                          | Retorna a legenda da voz para o objeto de [**comando**](/windows/desktop/lwef/the-command-object) do caractere.                      |
| [AddEx](iagentcommandsex--addex.md)                                                 | Adiciona um objeto de [**comando**](/windows/desktop/lwef/the-command-object) a uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [InsertEx](iagentcommandsex--insertex.md)                                           | Insere um objeto de [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . |
| [SetGlobalVoiceCommandsEnabled](iagentcommandsex--setglobalvoicecommandsenabled.md) | Habilita a gramática de voz para comandos globais do agente.                                                        |
| [GetGlobalVoiceCommandsEnabled](iagentcommandsex--getglobalvoicecommandsenabled.md) | Retorna se a gramática de voz para comandos globais do agente está habilitada.                                     |



 

 

 