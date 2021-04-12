---
title: Alterando a taxa de densidade e reprodução
description: Alterando a taxa de densidade e reprodução
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- áudio de onda, densidade
- Wave-interface de áudio, pitch
- áudio de forma de onda, taxa de reprodução
- forma de onda-interface de áudio, taxa de reprodução
- áudio de onda, mudança de Tom
- Wave-interface de áudio, alterando a densidade
- áudio de forma de onda, alterando a taxa de reprodução
- forma de onda-interface de áudio, alterando taxa de reprodução
- alterando a forma de onda-taxa de reprodução de áudio
- alterando a onda-densidade de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454066"
---
# <a name="changing-pitch-and-playback-rate"></a>Alterando a taxa de densidade e reprodução

Alguns dispositivos de saída de wave-áudio podem variar a densidade e a taxa de reprodução dos dados de áudio de forma de onda. Nem todos os dispositivos de wave-áudio dão suporte a alterações de taxa de reprodução e de densidade. Para obter informações sobre como determinar se um dispositivo de wave-áudio específico dá suporte a alterações de taxa de reprodução e de densidade, consulte [dispositivos e tipos de dados](devices-and-data-types.md).

As diferenças entre a alteração da taxa de densidade e de reprodução são as seguintes:

-   A alteração da taxa de reprodução é executada pelo driver de dispositivo e não requer hardware especializado. A taxa de amostra não é alterada, mas o driver interpola-se ignorando ou sintetizando amostras. Por exemplo, se a taxa de reprodução for alterada por um fator de dois, o driver ignorará todas as outras amostras.
-   A alteração da densidade exige hardware especializado. A taxa de reprodução e a taxa de amostragem não são alteradas.

O Windows fornece as seguintes funções para consultar e definir o tom de onda-áudio e as taxas de reprodução.



| Função                                                 | Descrição                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | Recupera a densidade do dispositivo de saída de wave-áudio especificado.         |
| [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | Recupera a taxa de reprodução para o dispositivo de saída de wave-áudio especificado. |
| [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | Define a densidade para o dispositivo de saída de wave-áudio especificado.              |
| [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | Define a taxa de reprodução para o dispositivo de saída de wave-áudio especificado.      |



 

As taxas de densidade e reprodução são alteradas por um fator especificado com um número de ponto fixo empacotado em um valor de doubleword. Os 16 bits superiores especificam a parte inteira do número; os 16 bits inferiores especificam a parte fracionária. Por exemplo, o valor 1,5 é representado como 0x00018000L. O valor 0,75 é representado como 0x0000C000L. Um valor de 1,0 (0x00010000) significa que a taxa de densidade ou reprodução não foi alterada.

 

 