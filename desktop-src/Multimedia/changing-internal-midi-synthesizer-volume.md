---
title: Alterando o volume do sintetizador MIDI interno
description: Alterando o volume do sintetizador MIDI interno
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- MIDI (Instrument Digital Interface Instrument), sintetizadores internos
- MIDI (Interface Digital Do instrumentar), sintetizadores internos
- reprodução de arquivos MIDI, sintetizadores internos
- sintetizadores MIDI internos
- MIDI (Interface Digital do Instrument Instrument), alterando o volume
- MIDI (Interface Digital do Instrument Instrument), alterando o volume
- reprodução de arquivos MIDI, alteração de volume
- alterando o volume MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646c7e17a7e8c0a6902e26dd8bbfdf8eb89c39297fdacdf062749d8c47a3d487
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808206"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>Alterando o volume do sintetizador MIDI interno

Windows fornece as seguintes funções para recuperar e definir o nível de volume de dispositivos sintetizadores MIDI internos:



| Valor                                        | Significado                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | Recupera o nível de volume do dispositivo de sintetizador MIDI interno especificado. |
| [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | Define o nível de volume do dispositivo de sintetizador MIDI interno especificado.      |



 

Nem todos os dispositivos de saída MIDI são compatíveis com alterações de volume. Alguns dispositivos podem dar suporte a alterações de volume individuais nos canais esquerdo e direito. Para obter informações sobre como determinar se um dispositivo específico dá suporte a alterações de volume, consulte [Consultando dispositivos de saída MIDI](querying-midi-output-devices.md).

A menos que seu aplicativo seja projetado para ser um aplicativo mestre de controle de volume (fornece ao usuário controle de volume para todos os dispositivos de áudio em um sistema), você deve abrir um dispositivo de áudio antes de alterar seu volume. Você também deve verificar o nível de volume antes de alterar e restaurar o nível de volume para seu nível anterior assim que possível.

O volume é especificado como um valor doubleword. Os 16 bits superiores especificam o volume relativo do canal direito e os 16 bits inferiores especificam o volume relativo do canal esquerdo.

Para dispositivos que não são compatíveis com alterações de volume individuais nos canais esquerdo e direito, os 16 bits inferiores especificam o nível de volume e os 16 bits superiores são ignorados. Os valores para o intervalo de nível de volume 0x0 (silêncio) a 0xFFFF (volume máximo) e são interpretados logarítmicamente. O aumento de volume percebido é o mesmo ao aumentar o nível de volume de 0x5000 para 0x6000, pois ele é de 0x4000 para 0x5000.

 

 