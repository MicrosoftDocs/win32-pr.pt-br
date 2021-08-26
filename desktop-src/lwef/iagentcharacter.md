---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 77d0ffc2-76a2-4a21-88e1-1ca85b8c5d2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7144c6d3379a2237d3f14c955d8052ff4d20d1ff98d9c2f2637796f8b931b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962086"
---
# <a name="iagentcharacter"></a>IAgentCharacter

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

**IAgentCharacter** define uma interface que permite que os aplicativos consultem propriedades de caracteres e reproduzam animações. Essas funções também estão disponíveis em [**IAgentCharacterEx.**](iagentcharacterex.md) Você pode usar algumas IDs de solicitação de retorno de método para acompanhar seu status na fila do caractere e sincronizar seu código com o estado de animação atual do caractere.

**Métodos em ordem Vtable**



| Métodos IAgentCharacter                                           | Descrição                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**Getvisible**](iagentcharacter--getvisible.md)                 | Retorna se o caractere (quadro) está visível no momento.                       |
| [**Setposition**](iagentcharacter--setposition.md)               | Define a posição do quadro de caracteres.                                         |
| [**Getposition**](iagentcharacter--getposition.md)               | Retorna a posição do quadro de caracteres.                                      |
| [**Setsize**](iagentcharacter--setsize.md)                       | Define o tamanho do quadro de caracteres.                                             |
| [**Getsize**](iagentcharacter--getsize.md)                       | Retorna o tamanho do quadro de caracteres.                                          |
| [**GetName**](iagentcharacter--getname.md)                       | Retorna o nome do caractere.                                                |
| [**Getdescription**](iagentcharacter--getdescription.md)         | Retorna a descrição do caractere.                                        |
| [**GetTTSSpeed**](iagentcharacter--getttsspeed.md)               | Retorna a configuração atual de velocidade de saída do TTS para o caractere.                   |
| [**GetTTSPitch**](iagentcharacter--getttspitch.md)               | Retorna a configuração de tom TTS atual para o caractere.                          |
| [**Ativar**](iagentcharacter--activate.md)                     | Define se um cliente está ativo ou se um caractere é mais alto.                        |
| [**SetIdleOn**](iagentcharacter--setidleon.md)                   | Define o processamento ocioso do servidor.                                                |
| [**GetIdleOn**](iagentcharacter--getidleon.md)                   | Retorna a configuração do processamento ocioso do servidor.                              |
| [**Preparar**](iagentcharacter--prepare.md)                       | Recupera dados de animação para o caractere.                                       |
| [**Reproduzir**](iagentcharacter--play.md)                             | Reproduz uma animação especificada.                                                      |
| [**Stop**](iagentcharacter--stop.md)                             | Interrompe uma animação para um caractere.                                               |
| [**Stopall**](iagentcharacter--stopall.md)                       | Interrompe todas as animações de um caractere.                                             |
| [**Aguarde**](iagentcharacter--wait.md)                             | Contém a fila de animação do caractere.                                            |
| [**Interromper**](iagentcharacter--interrupt.md)                   | Interrompe a animação de um caractere.                                               |
| [**Mostrar**](iagentcharacter--show.md)                             | Exibe o caractere e reproduz a animação de estado **Mostrando** o caractere.     |
| [**Ocultar**](iagentcharacter--hide.md)                             | Reproduz a animação oculta **de** estado do caractere e oculta o quadro do caractere. |
| [**Speak**](iagentcharacter--speak.md)                           | Reproduz a saída falada para o caractere.                                            |
| [**Moveto**](iagentcharacter--moveto.md)                         | Move o quadro de caracteres para o local especificado.                              |
| [**GestureAt**](iagentcharacter--gestureat.md)                   | Reproduz uma animação de gestação com base no local especificado.                      |
| [**GetMoveCause**](iagentcharacter--getmovecause.md)             | Recupera a causa da última movimentação do caractere.                                 |
| [**GetVisibilityCause**](iagentcharacter--getvisibilitycause.md) | Recupera a causa da última alteração no estado de visibilidade do caractere.       |
| [**HasOtherClients**](iagentcharacter--hasotherclients.md)       | Recupera se o caractere tem outros clientes atuais.                        |
| [**SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)   | Determina se os efeitos de som de uma animação de caractere são reproduzir.                    |
| [**GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)   | Recupera se a configuração de efeitos de som de um caractere está habilitada.                 |
| [**SetName**](iagentcharacter--setname.md)                       | Define o nome do caractere.                                                        |
| [**SetDescription**](iagentcharacter--setdescription.md)         | Define a descrição do caractere.                                                 |
| [**GetExtraData**](iagentcharacter--getextradata.md)             | Recupera dados adicionais armazenados com o caractere .                              |



 

 

 




