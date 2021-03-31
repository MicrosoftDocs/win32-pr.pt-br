---
title: Erros do Sequencer
description: Erros do Sequencer
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- Valores de retorno de MCIERR, erros de sequenciador
- referência de multimídia, erros do Sequencer
- referência para multimídia, erros do Sequencer
- MCI (interface de controle de mídia), erros do Sequencer
- MCI (interface de controle de mídia), erros do Sequencer
- referência para MCI, erros do Sequencer
- Referência MCI, erros do Sequencer
- MCI (interface de controle de mídia), erros
- MCI (interface de controle de mídia), erros
- referência para MCI, erros
- Referência de MCI, erros
- erros do Sequencer
- Erros do sequenciador MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635882"
---
# <a name="sequencer-errors"></a>Erros do Sequencer

Os seguintes valores de retorno adicionais são definidos para sequenciais MCI:



| Valor                          | Significado                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_div Seq \_ MCIERR \_ incompatível | Os formatos de hora do "ponteiro de música" e SMPTE são singulares. Você não pode usá-los juntos.                                                              |
| MCIERR \_ Seq \_ NOMIDIPRESENT     | Este sistema não tem dispositivos MIDI instalados. Use a opção drivers do painel de controle para instalar um driver de MIDI.                                       |
| \_porta MCIERR \_ Seq \_ INUSE       | A porta MIDI especificada já está em uso. Aguarde até que seja gratuito; em seguida, tente novamente.                                                                       |
| MCIERR \_ Seq \_ porta \_ MAPNODEVICE | A instalação atual do mapeador de MIDI se refere a um dispositivo MIDI que não está instalado no sistema. Use o mapeador de MIDI no painel de controle para editar a configuração. |
| MCIERR \_ Seq \_ porta \_ MISCERROR   | Ocorreu um erro com a porta especificada.                                                                                                                   |
| \_porta MCIERR \_ Seq \_ inexistente | O dispositivo MIDI especificado não está instalado no sistema. Use a opção drivers do painel de controle para instalar um dispositivo MIDI.                        |
| MCIERR \_ Seq \_ PORTUNSPECIFIED   | O sistema não tem uma porta MIDI atual especificada.                                                                                                  |
| \_ \_ temporizador MCIERR Seq             | Todos os timers de multimídia estão sendo usados por outros aplicativos. Encerre um desses aplicativos; em seguida, tente novamente.                                             |



 

 

 




