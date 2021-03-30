---
title: Alterando o volume de Audio-Devices auxiliares
description: Alterando o volume de Audio-Devices auxiliares
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- áudio de formato de onda, alterando o volume do dispositivo de áudio auxiliar
- alterando o volume do dispositivo de áudio auxiliar
- áudio auxiliar, alterando o volume do dispositivo
- interface de áudio auxiliar
- dispositivos de áudio auxiliares, alterando o volume
- áudio auxiliar, interface
- áudio auxiliar, dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641104"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a>Alterando o volume de Audio-Devices auxiliares

O Windows fornece as seguintes funções para consultar e definir o volume para dispositivos de áudio auxiliares.



| Função                             | Descrição                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | Recupera a configuração de volume atual do dispositivo de saída auxiliar especificado. |
| [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | Define o volume do dispositivo de saída auxiliar especificado.                      |



 

Nem todos os dispositivos de áudio auxiliar dão suporte a alterações de volume. Alguns dispositivos podem dar suporte a alterações de volume individuais nos canais esquerdo e direito.

O volume é especificado em um valor doubleword, assim como as funções de controle de volume de wave-áudio e MIDI. Quando o formato de áudio é estéreo, os 16 bits superiores especificam o volume relativo do canal correto e os 16 bits inferiores especificam o volume relativo do canal esquerdo. Para dispositivos que não dão suporte ao controle de volume de canal esquerdo e direito, os 16 bits inferiores especificam o nível de volume e os 16 bits superiores são ignorados.

Os valores de nível de volume variam de 0x0 (silêncio) a 0xFFFF (volume máximo) e são interpretados logaritmicamente. O aumento do volume percebido é o mesmo ao aumentar o nível de volume de 0x5000 para 0x6000, pois ele é de 0x4000 para 0x5000.

 

 