---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 77d0ffc2-76a2-4a21-88e1-1ca85b8c5d2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0a56272ba095f244e48e335049ec5b88b64855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761272"
---
# <a name="iagentcharacter"></a>IAgentCharacter

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

**IAgentCharacter** define uma interface que permite que os aplicativos consultem as propriedades de caractere e reproduzam animações. Essas funções também estão disponíveis em [**IAgentCharacterEx**](iagentcharacterex.md). Você pode usar algumas IDs de solicitação de retorno de método para controlar seu status na fila de caracteres e sincronizar seu código com o estado de animação atual do caractere.

**Métodos em ordem vtable**



| Métodos IAgentCharacter                                           | Descrição                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**GetVisible**](iagentcharacter--getvisible.md)                 | Retorna se o caractere (quadro) está visível no momento.                       |
| [**SETPOSITION**](iagentcharacter--setposition.md)               | Define a posição do quadro de caracteres.                                         |
| [**GetPosition**](iagentcharacter--getposition.md)               | Retorna a posição do quadro de caracteres.                                      |
| [**Size**](iagentcharacter--setsize.md)                       | Define o tamanho do quadro de caracteres.                                             |
| [**GetSize**](iagentcharacter--getsize.md)                       | Retorna o tamanho do quadro de caracteres.                                          |
| [**GetName**](iagentcharacter--getname.md)                       | Retorna o nome do caractere.                                                |
| [**GetDescription**](iagentcharacter--getdescription.md)         | Retorna a descrição do caractere.                                        |
| [**GetTTSSpeed**](iagentcharacter--getttsspeed.md)               | Retorna a configuração de velocidade de saída TTS atual para o caractere.                   |
| [**GetTTSPitch**](iagentcharacter--getttspitch.md)               | Retorna a configuração de densidade do TTS atual para o caractere.                          |
| [**Activate**](iagentcharacter--activate.md)                     | Define se um cliente está ativo ou se um caractere está no nível mais alto.                        |
| [**Setocioso**](iagentcharacter--setidleon.md)                   | Define o processamento ocioso do servidor.                                                |
| [**Getociosidade**](iagentcharacter--getidleon.md)                   | Retorna a configuração do processamento ocioso do servidor.                              |
| [**Preparar**](iagentcharacter--prepare.md)                       | Recupera dados de animação para o caractere.                                       |
| [**Reproduzir**](iagentcharacter--play.md)                             | Reproduz uma animação especificada.                                                      |
| [**Stop**](iagentcharacter--stop.md)                             | Interrompe uma animação de um caractere.                                               |
| [**Do opAll**](iagentcharacter--stopall.md)                       | Interrompe todas as animações de um caractere.                                             |
| [**Aguarde**](iagentcharacter--wait.md)                             | Mantém a fila de animação do caractere.                                            |
| [**Atividades**](iagentcharacter--interrupt.md)                   | Interrompe a animação de um caractere.                                               |
| [**programa**](iagentcharacter--show.md)                             | Exibe o caractere e reproduz a animação de estado de **exibição** do caractere.     |
| [**Ocultar**](iagentcharacter--hide.md)                             | Reproduz a animação de estado **oculto** do caractere e oculta o quadro do caractere. |
| [**Speak**](iagentcharacter--speak.md)                           | Reproduz a saída falada para o caractere.                                            |
| [**Mover**](iagentcharacter--moveto.md)                         | Move o quadro de caracteres para o local especificado.                              |
| [**GestureAt**](iagentcharacter--gestureat.md)                   | Reproduz uma animação gesturing com base no local especificado.                      |
| [**GetMoveCause**](iagentcharacter--getmovecause.md)             | Recupera a causa da última movimentação do caractere.                                 |
| [**GetVisibilityCause**](iagentcharacter--getvisibilitycause.md) | Recupera a causa da última alteração no estado de visibilidade do caractere.       |
| [**HasOtherClients**](iagentcharacter--hasotherclients.md)       | Recupera se o caractere tem outros clientes atuais.                        |
| [**SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)   | Determina se os efeitos sonoros de uma animação de caractere são executados.                    |
| [**GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)   | Recupera se a configuração de efeitos de som de um caractere está habilitada.                 |
| [**SetName**](iagentcharacter--setname.md)                       | Define o nome do caractere.                                                        |
| [**SetDescription**](iagentcharacter--setdescription.md)         | Define a descrição do caractere.                                                 |
| [**GetExtraData**](iagentcharacter--getextradata.md)             | Recupera dados adicionais armazenados com o caractere.                              |



 

 

 




