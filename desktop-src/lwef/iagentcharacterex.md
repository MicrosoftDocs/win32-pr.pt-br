---
title: IAgentCharacterEx
description: IAgentCharacterEx
ms.assetid: 8defc836-cc54-40c7-8afc-ec90f941861b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04e4b6661641ebf472001e502a7fec3042332ea039ec94c01349d58bbe93346d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961956"
---
# <a name="iagentcharacterex"></a>IAgentCharacterEx

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

**IAgentCharacterEx** deriva da interface [**IAgentCharacter.**](iagentcharacter.md) Ele inclui todos os **métodos IAgentCharacter,** bem como fornece acesso a funções adicionais.

**Métodos em ordem Vtable**



| Métodos IAgentCharacterEx                                         | Descrição                                                                    |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)         | Exibe o menu pop-up para o caractere.                                    |
| [**SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)   | Define se o servidor exibe automaticamente o menu pop-up do caractere.    |
| [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md)   | Retorna se o servidor exibe automaticamente o menu pop-up do caractere. |
| [**GetHelpFileName**](iagentcharacterex--gethelpfilename.md)     | Retorna o nome do arquivo de Ajuda para o caractere.                                   |
| [**SetHelpFileName**](iagentcharacterex--sethelpfilename.md)     | Define o nome do arquivo de Ajuda para o caractere.                                      |
| [**SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)         | Define o modo de Ajuda.                                                             |
| [**GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md)         | Retorna se o modo de Ajuda está em.                                               |
| [**SetHelpContextID**](iagentcharacterex--sethelpcontextid.md)   | Define o HelpContextID para o caractere.                                      |
| [**GetHelpContextID**](iagentcharacterex--gethelpcontextid.md)   | Retorna o HelpContextID para o caractere.                                   |
| [**GetActive**](iagentcharacterex--getactive.md)                 | Retorna o estado ativo do caractere.                                    |
| [**Escute**](iagentcharacterex--listen.md)                       | Define o estado de escuta para o caractere.                                    |
| [**SetLanguageID**](iagentcharacterex--setlanguageid.md)         | Define a ID de idioma do caractere.                                        |
| [**getLanguageID**](iagentcharacterex--getlanguageid.md)         | Retorna a ID de idioma do caractere.                                     |
| [**getTTSModeID**](iagentcharacterex--getttsmodeid.md)           | Retorna a ID do modo TTS definida para o caractere.                                 |
| [**SetTTSModeID**](iagentcharacterex--setttsmodeid.md)           | Define a ID do modo TTS para o caractere.                                        |
| [**getSRModeID**](iagentcharacterex--getsrmodeid.md)             | Retorna a ID de modo do mecanismo de reconhecimento de fala atual.                       |
| [**setSRModeID**](iagentcharacterex--setsrmodeid.md)             | Define o mecanismo de reconhecimento de fala.                                            |
| [**GetGUID**](iagentcharacterex--getguid.md)                     | Retorna o identificador do caractere.                                            |
| [**GetOriginalSize**](iagentcharacterex--getoriginalsize.md)     | Retorna o tamanho original do quadro de caracteres.                              |
| [**Pensar**](iagentcharacterex--think.md)                         | Exibe o texto especificado no balão "thought" do caractere.              |
| [**Getversion**](iagentcharacterex--getversion.md)               | Retorna a versão do caractere.                                          |
| [**GetAnimationNames**](iagentcharacterex--getanimationnames.md) | Retorna os nomes das animações para o caractere.                         |
| [**getSRStatus**](iagentcharacterex--getsrstatus.md)             | Retorna as condições necessárias para dar suporte à entrada de fala.                      |



 

 

 




