---
title: Alterando o volume de Waveform-Audio reprodução
description: Alterando o volume de Waveform-Audio reprodução
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- áudio de onda, alterando volume de reprodução
- Wave-interface de áudio, alterando volume de reprodução
- áudio de onda, volume de reprodução
- Wave-interface de áudio, volume de reprodução
- alterando a onda-volume de reprodução de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59bca6dbc168d2c327c46e4d934d4abb3afa73cc8ef2cae8b1a6c283bd92c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807986"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a>Alterando o volume de Waveform-Audio reprodução

Windows fornece as seguintes funções para consultar e definir o nível de volume de dispositivos de saída de wave-áudio.



| Função                                     | Descrição                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | Recupera o nível de volume atual do dispositivo de saída de wave-áudio especificado. |
| [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | Define o nível de volume do dispositivo de saída de wave-áudio especificado.              |



 

Nem todos os dispositivos de wave-áudio dão suporte a alterações de volume. Alguns dispositivos dão suporte ao controle de volume individual nos canais esquerdo e direito. Para obter informações sobre como determinar os recursos de controle de volume dos dispositivos de formato de onda-áudio, consulte [dispositivos e tipos de dados](devices-and-data-types.md).

Alguns aplicativos permitem que o usuário controle o volume de todos os dispositivos de áudio em um sistema. (Muitos aplicativos desse tipo usam os serviços de mixer de áudio; para obter mais informações, consulte [mixers de áudio](audio-mixers.md).) A menos que seu aplicativo seja capaz desse tipo de controle de volume mestre, você deve abrir um dispositivo de áudio antes de alterar seu volume. Você também deve consultar o nível de volume antes de alterá-lo e restaurar o nível de volume para seu nível anterior assim que possível.

O volume é especificado em um valor doubleword. Quando o formato de áudio é estéreo, os 16 bits superiores especificam o volume relativo do canal correto e os 16 bits inferiores especificam o volume relativo do canal esquerdo. Para dispositivos que não dão suporte ao controle de volume de canal esquerdo e direito, os 16 bits inferiores especificam o nível de volume e os 16 bits superiores são ignorados.

Os valores de nível de volume variam de 0x0 (silêncio) a 0xFFFF (volume máximo) e são interpretados logaritmicamente. O aumento do volume percebido é o mesmo ao aumentar o nível de volume de 0x5000 para 0x6000, pois ele é de 0x4000 para 0x5000.

 

 