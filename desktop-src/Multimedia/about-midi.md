---
title: Sobre MIDI
description: Sobre MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Multimídia do Windows, MIDI (interface digital de instrumentos musicais)
- multimídia, MIDI (interface digital de instrumentos musicais)
- áudio multimídia, MIDI (interface digital de instrumentos musicais)
- áudio, MIDI (interface digital de instrumento musical)
- MIDI (interface digital de instrumento musical), sobre
- MIDI (interface digital de instrumentos musicais), sobre
- MIDI (interface digital de instrumento musical), MCI (interface de controle de mídia)
- MIDI (interface digital de instrumentos musicais), MCI (interface de controle de mídia)
- MIDI (interface digital de instrumento musical), buffers de fluxo
- MIDI (interface digital de instrumentos musicais), buffers de fluxo
- MIDI (interface digital de instrumento musical), serviços de MIDI
- MIDI (interface digital de instrumentos musicais), serviços de MIDI
- MCI (interface de controle de mídia), MIDI (interface digital de instrumento musical)
- MCI (interface de controle de mídia), MIDI (interface digital de instrumento musical)
- buffers de fluxo, sobre
- Serviços de MIDI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635377"
---
# <a name="about-midi"></a>Sobre MIDI

A API (interface de programação de aplicativo) do Microsoft Win32 fornece os seguintes métodos para que os aplicativos funcionem com dados MIDI:

-   A interface de controle de mídia (MCI). Embora a maneira mais simples de reproduzir um arquivo MIDI seja usar a classe Window MCIWnd, você também pode usar comandos MCI para criar uma interface personalizada para um dispositivo MIDI. Para obter mais informações sobre a classe de janela MCIWnd, consulte [classe de janela MCIWnd](mciwnd-window-class.md). Para obter mais informações sobre o MCI, consulte [MCI](mci.md)ou [MCI (interface de controle de mídia)](media-control-interface--mci.md).
-   [Buffers de fluxo](stream-buffers.md). Esse formato permite que um aplicativo manipule buffers de dados MIDI com carimbo de data/hora para reprodução. Os buffers de fluxo são úteis para aplicativos que exigem um controle mais preciso sobre a saída do que as ofertas MCI.
-   [Serviços de Midi](midi-services.md). Os aplicativos que precisam do controle mais preciso de dados MIDI normalmente usam esses serviços de nível baixo.

Os tópicos a seguir abordam cada um desses métodos e fornecem uma visão geral do mapeador de MIDI.

-   [O mapeador de MIDI](the-midi-mapper.md)
-   [MCI (interface de controle de mídia)](media-control-interface--mci.md)
-   [Buffers de fluxo](stream-buffers.md)
-   [Serviços MIDI](midi-services.md)
-   [Executando arquivos MIDI](playing-midi-files.md)
-   [Gravando áudio MIDI](recording-midi-audio.md)
-   [Processando dados MIDI de duas fontes MIDI](processing-midi-data-from-two-midi-sources.md)
-   [Criando arquivos MIDI](creating-midi-files.md)

 

 




