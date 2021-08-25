---
title: Processamento de dados MIDI de duas fontes MIDI
description: Processamento de dados MIDI de duas fontes MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Windows multimídia, processando dados MIDI de duas fontes
- multimídia, processamento de dados MIDI de duas fontes
- áudio multimídia, processamento de dados MIDI de duas fontes
- áudio, processamento de dados MIDI de duas fontes
- MIDI (Instrument Digital Interface Instrument), processando dados de duas fontes
- MIDI (Interface Digital do Instrument Instrument), processando dados de duas fontes
- ing MIDI data from two sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a5eb31c4c6b4b965321b7458d058a3547426b95236d6e0b52d6eb0f55b3e74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805786"
---
# <a name="processing-midi-data-from-two-midi-sources"></a>Processamento de dados MIDI de duas fontes MIDI

O subsistema MIDI pode rotear mensagens MIDI de duas fontes de dados para um único dispositivo de saída MIDI para reprodução simultânea. Por exemplo, uma fonte pode ser uma música em segundo plano ou uma linha de grave que foi previamente gravada e armazenada em um arquivo. A segunda fonte pode ser dados ao vivo de um instrumento MIDI, como um teclado ou um teclado.

Ambas as fontes de dados enviam dados MIDI para um único dispositivo MIDI identificado com um identificador. Envie um fluxo de dados usando a [**função midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) e um ou mais buffers de fluxo. Esse fluxo de dados normalmente contém dados pré-gravados que são empacotados no buffer.

Envie o segundo fluxo de dados (normalmente de um instrumento MIDI) de forma assíncrona usando a [**função midiOutShortMsg.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) O status de execução de um buffer de fluxo não será afetado negativamente pelas chamadas assíncronas feitas pelo segundo fluxo de dados.

Cada mensagem curta enviada com **midiOutShortMsg** deve ser uma mensagem MIDI completa, com um byte de status e o número apropriado de bytes de dados. Se o byte de status for omitido, **midiOutShortMsg** retornará um erro. (No entanto, não há nenhum status de execução com saída de fluxo.)

 

 