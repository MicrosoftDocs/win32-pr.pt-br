---
title: Sobre o MIDI
description: Sobre o MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Windows multimídia, MIDI (Interface Digital do Instrument Instrument)
- multimídia, MIDI (Interface Digital do Instrument Instrument)
- audio multimídia, MIDI (Interface Digital do Instrument Instrument)
- audio,MIDI (Instrument Digital Interface)
- MIDI (Interface Digital do Instrument Instrument), sobre
- MIDI (Interface Digital do Instrument Instrument), sobre
- MIDI (Interface Digital do Instrument Instrument), Interface de Controle de Mídia (MCI)
- MIDI (Interface Digital do Instrument Instrument), Interface de Controle de Mídia (MCI)
- MIDI (Instrument Digital Interface Instrument), buffers de fluxo
- MIDI (Interface Digital do Instrument Instrument), buffers de fluxo
- MIDI (Interface Digital) do Instrument Instrument, serviços MIDI
- MIDI (Interface Digital Instrument Instrument), serviços MIDI
- MCI (Interface de Controle de Mídia), MIDI (Interface Digital do Instrument instrument)
- MCI (Interface de Controle de Mídia), MIDI (Interface Digital do Instrument instrument)
- buffers de fluxo, sobre
- Serviços MIDI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1ce20164c42342c52defd27e7f3ccdfb0a44ec9a4e0a6679c1b190270fc62e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526686"
---
# <a name="about-midi"></a>Sobre o MIDI

A API (interface de programação de aplicativos) do Microsoft Win32 fornece os seguintes métodos para que os aplicativos funcionem com dados MIDI:

-   A MCI (Interface de Controle de Mídia). Embora a maneira mais simples de reproduzir um arquivo MIDI seja usar a classe de janela MCIWnd, você também pode usar comandos MCI para criar uma interface personalizada para um dispositivo MIDI. Para obter mais informações sobre a classe de janela MCIWnd, consulte Classe de janela [MCIWnd](mciwnd-window-class.md). Para obter mais informações sobre a MCI, consulte [MCI](mci.md)ou [MCI (Interface](media-control-interface--mci.md)de Controle de Mídia).
-   [Buffers de fluxo.](stream-buffers.md) Esse formato permite que um aplicativo manipule buffers de dados MIDI com carimbo de data/hora para reprodução. Buffers de fluxo são úteis para aplicativos que exigem um controle mais preciso sobre a saída do que as ofertas de MCI.
-   [Serviços MIDI.](midi-services.md) Os aplicativos que precisam do controle mais preciso dos dados MIDI normalmente usam esses serviços de baixo nível.

Os tópicos a seguir discutem cada um desses métodos e fornece uma visão geral do Mapeado MIDI.

-   [O mapeado MIDI](the-midi-mapper.md)
-   [Interface de Controle de Mídia (MCI)](media-control-interface--mci.md)
-   [Buffers de fluxo](stream-buffers.md)
-   [Serviços MIDI](midi-services.md)
-   [Reprodução de arquivos MIDI](playing-midi-files.md)
-   [Gravação de áudio MIDI](recording-midi-audio.md)
-   [Processamento de dados MIDI de duas fontes MIDI](processing-midi-data-from-two-midi-sources.md)
-   [Criando arquivos MIDI](creating-midi-files.md)

 

 




