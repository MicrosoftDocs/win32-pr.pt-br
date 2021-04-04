---
title: IAgentCharacterEx
description: IAgentCharacterEx
ms.assetid: 8defc836-cc54-40c7-8afc-ec90f941861b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92a9f9c39804d6b5d3ac777457fff5b7f03823c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822798"
---
# <a name="iagentcharacterex"></a>IAgentCharacterEx

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

**IAgentCharacterEx** deriva da interface [**IAgentCharacter**](iagentcharacter.md) . Ele inclui todos os métodos **IAgentCharacter** , bem como fornece acesso a funções adicionais.

**Métodos em ordem vtable**



| Métodos IAgentCharacterEx                                         | Descrição                                                                    |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)         | Exibe o menu pop-up do caractere.                                    |
| [**SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)   | Define se o servidor exibe automaticamente o menu pop-up do caractere.    |
| [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md)   | Retorna se o servidor exibe automaticamente o menu pop-up do caractere. |
| [**Getarquivodeajudaname**](iagentcharacterex--gethelpfilename.md)     | Retorna o nome de arquivo da ajuda para o caractere.                                   |
| [**Setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)     | Define o nome de arquivo da ajuda para o caractere.                                      |
| [**SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)         | Define o modo de ajuda no.                                                             |
| [**GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md)         | Retorna se o modo de ajuda está ativado.                                               |
| [**Setidentificaçãodocontextodaajuda**](iagentcharacterex--sethelpcontextid.md)   | Define o HelpContextid para o caractere.                                      |
| [**Getidentificaçãodocontextodaajuda**](iagentcharacterex--gethelpcontextid.md)   | Retorna o HelpContextid para o caractere.                                   |
| [**Getactive**](iagentcharacterex--getactive.md)                 | Retorna o estado ativo do caractere.                                    |
| [**Escutar**](iagentcharacterex--listen.md)                       | Define o estado de escuta para o caractere.                                    |
| [**Setlanguageid**](iagentcharacterex--setlanguageid.md)         | Define a ID de idioma para o caractere.                                        |
| [**getlanguageid**](iagentcharacterex--getlanguageid.md)         | Retorna a ID de idioma do caractere.                                     |
| [**getTTSModeID**](iagentcharacterex--getttsmodeid.md)           | Retorna a ID do modo TTS definido para o caractere.                                 |
| [**SetTTSModeID**](iagentcharacterex--setttsmodeid.md)           | Define a ID do modo TTS para o caractere.                                        |
| [**getSRModeID**](iagentcharacterex--getsrmodeid.md)             | Retorna a ID do modo do mecanismo de reconhecimento de fala atual.                       |
| [**setSRModeID**](iagentcharacterex--setsrmodeid.md)             | Define o mecanismo de reconhecimento de fala.                                            |
| [**GetGUID**](iagentcharacterex--getguid.md)                     | Retorna o identificador do caractere.                                            |
| [**GetOriginalSize**](iagentcharacterex--getoriginalsize.md)     | Retorna o tamanho original do quadro de caracteres.                              |
| [**Pensar**](iagentcharacterex--think.md)                         | Exibe o texto especificado no balão "pensamento" do caractere.              |
| [**Obter versão**](iagentcharacterex--getversion.md)               | Retorna a versão do caractere.                                          |
| [**Getanimationnames**](iagentcharacterex--getanimationnames.md) | Retorna os nomes das animações para o caractere.                         |
| [**getSRStatus**](iagentcharacterex--getsrstatus.md)             | Retorna as condições necessárias para dar suporte à entrada de fala.                      |



 

 

 




