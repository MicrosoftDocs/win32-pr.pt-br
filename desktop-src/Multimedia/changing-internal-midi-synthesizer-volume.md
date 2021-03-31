---
title: Alterando o volume do sintetizador MIDI interno
description: Alterando o volume do sintetizador MIDI interno
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- MIDI (interface digital de instrumento musical), sintetizadores internos
- MIDI (interface digital de instrumentos musicais), sintetizadores internos
- executando arquivos MIDI, sintetizadores internos
- sintetizadores MIDI internos
- MIDI (interface digital de instrumento musical), alterando o volume
- MIDI (interface digital de instrumento musical), alterando o volume
- executando arquivos MIDI, alterando o volume
- alterando o volume MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917274"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>Alterando o volume do sintetizador MIDI interno

O Windows fornece as seguintes funções para recuperar e definir o nível de volume de dispositivos de sintetizador MIDI internos:



| Valor                                        | Significado                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | Recupera o nível de volume do dispositivo de sintetizador MIDI interno especificado. |
| [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | Define o nível de volume do dispositivo de sintetizador MIDI interno especificado.      |



 

Nem todos os dispositivos de saída MIDI dão suporte a alterações de volume. Alguns dispositivos podem dar suporte a alterações de volume individuais nos canais esquerdo e direito. Para obter informações sobre como determinar se um dispositivo específico dá suporte a alterações de volume, consulte [consultando dispositivos de saída de Midi](querying-midi-output-devices.md).

A menos que seu aplicativo seja projetado para ser um aplicativo mestre de controle de volume (fornece ao usuário controle de volume para todos os dispositivos de áudio em um sistema), você deve abrir um dispositivo de áudio antes de alterar seu volume. Você também deve verificar o nível de volume antes de alterá-lo e restaurar o nível de volume para seu nível anterior assim que possível.

O volume é especificado como um valor de doubleword. Os 16 bits superiores especificam o volume relativo do canal correto e os 16 bits inferiores especificam o volume relativo do canal esquerdo.

Para dispositivos que não dão suporte a alterações de volume individuais nos canais esquerdo e direito, os 16 bits inferiores especificam o nível de volume e os 16 bits superiores são ignorados. Valores para o intervalo de nível de volume de 0x0 (silêncio) a 0xFFFF (volume máximo) e são interpretados logaritmicamente. O aumento do volume percebido é o mesmo ao aumentar o nível de volume de 0x5000 para 0x6000, pois ele é de 0x4000 para 0x5000.

 

 