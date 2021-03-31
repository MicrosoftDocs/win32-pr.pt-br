---
title: MCI (interface de controle de mídia)
description: MCI (interface de controle de mídia)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Multimídia do Windows, MCI (interface de controle de mídia)
- multimídia, MCI (interface de controle de mídia)
- áudio de multimídia, MCI (interface de controle de mídia)
- áudio, interface de controle de mídia (MCI)
- MIDI (interface digital de instrumento musical), MCI (interface de controle de mídia)
- MIDI (interface digital de instrumentos musicais), MCI (interface de controle de mídia)
- MCI (interface de controle de mídia), MIDI (interface digital de instrumento musical)
- MCI (interface de controle de mídia), MIDI (interface digital de instrumento musical)
- MCI (interface de controle de mídia), Sequencer MIDI
- MCI (interface de controle de mídia), Sequencer MIDI
- Sequenciador MIDI MCI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005443"
---
# <a name="media-control-interface-mci"></a>MCI (interface de controle de mídia)

O Sequencer MIDI do MCI é o componente do sistema MCI que reproduz arquivos MIDI. Os aplicativos podem reproduzir arquivos MIDI facilmente usando o MCI, mas o MCI impõe as seguintes restrições em recursos de MIDI:

-   O MCI dá suporte apenas à saída de MIDI.
-   O MCI não permite a sincronização de fechamento entre eventos de MIDI e outros eventos em tempo real (como vídeo).

Se precisar de uma sincronização de MIDI precisa, você deverá usar os buffers de fluxo ou os serviços de MIDI. Se precisar de recursos de entrada de MIDI, você deverá usar os serviços de MIDI.

O sequenciador MIDI MCI reproduz arquivos MIDI padrão e arquivos MIDI RIFF (formato de arquivo de intercâmbio de recursos), conhecidos como arquivos RMID. Arquivos MIDI padrão estão em conformidade com a especificação [1,0 de arquivos MIDI padrão](creating-midi-files.md) . Como os arquivos RMID são arquivos MIDI padrão com um cabeçalho RIFF, as informações sobre os arquivos MIDI padrão também se aplicam aos arquivos RMID. Para obter mais informações sobre arquivos RIFF, consulte [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

Embora atualmente existam três tipos de arquivos MIDI padrão, o sequenciador MCI reproduz apenas dois deles: formato 0 e formato 1 arquivos MIDI.

Para obter mais informações sobre como controlar dispositivos multimídia (incluindo sequenciais) usando comandos MCI, consulte [MCI](mci.md).

 

 




