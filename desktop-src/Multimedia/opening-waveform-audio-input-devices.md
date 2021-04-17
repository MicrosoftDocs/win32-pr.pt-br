---
title: Abrindo Waveform-Audio dispositivos de entrada
description: Abrindo Waveform-Audio dispositivos de entrada
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- áudio de formato de onda, abrindo dispositivos de entrada
- formato de onda-interface de áudio, abertura de dispositivos de entrada
- gravando áudio de onda, abrindo dispositivos de entrada
- abrindo Wave-dispositivos de entrada de áudio
- função waveInOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105766373"
---
# <a name="opening-waveform-audio-input-devices"></a>Abrindo Waveform-Audio dispositivos de entrada

Use a função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir um dispositivo de entrada de formato de onda-áudio para gravação. Essa função abre o dispositivo associado ao identificador de dispositivo especificado e retorna um identificador do dispositivo aberto gravando o identificador de um local de memória especificado.

Alguns computadores de multimídia têm vários dispositivos de entrada de wave-áudio. A menos que você saiba que deseja abrir um dispositivo de entrada de áudio de forma de onda específico em um sistema, use a \_ constante do mapeador de ondas para o identificador do dispositivo ao abrir um dispositivo. A função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) escolherá o dispositivo no sistema com a melhor capacidade de registrar no formato de dados especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio de onda](recording-waveform-audio.md)
</dt> </dl>

 

 