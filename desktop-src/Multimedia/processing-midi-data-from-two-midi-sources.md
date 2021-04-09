---
title: Processando dados MIDI de duas fontes MIDI
description: Processando dados MIDI de duas fontes MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Multimídia do Windows, processamento de dados MIDI de duas fontes
- multimídia, processamento de dados MIDI de duas fontes
- áudio multimídia, processamento de dados MIDI de duas fontes
- áudio, processamento de dados MIDI de duas fontes
- MIDI (interface digital de instrumento musical), processamento de dados de duas fontes
- MIDI (interface digital de instrumentos musicais), processamento de dados de duas fontes
- processando dados MIDI de duas fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007482"
---
# <a name="processing-midi-data-from-two-midi-sources"></a>Processando dados MIDI de duas fontes MIDI

O subsistema MIDI pode rotear mensagens MIDI de duas fontes de dados para um único dispositivo de saída de MIDI para reprodução simultânea. Por exemplo, uma fonte pode ser uma música em segundo plano ou uma linha de baixo que tenha sido previamente registrada e armazenada em um arquivo. A segunda fonte pode ser dados dinâmicos de um instrumento MIDI, como um teclado ou uma guitarra.

Ambas as fontes de dados enviam dados MIDI para um único dispositivo MIDI identificado com um identificador. Envie um fluxo de dados usando a função [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) e um ou mais buffers de fluxo. Esse fluxo de dados normalmente contém dados pré-gravados que são empacotados no buffer.

Envie o segundo fluxo de dados (normalmente de um instrumento MIDI) de forma assíncrona usando a função [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) . O status de execução de um buffer de fluxo não será afetado negativamente pelas chamadas assíncronas feitas pelo segundo fluxo de dados.

Cada mensagem curta enviada com **midiOutShortMsg** deve ser uma mensagem MIDI completa, com um byte de status e o número apropriado de bytes de dados. Se o byte de status for omitido, **midiOutShortMsg** retornará um erro. (No entanto, não há nenhum status de execução com saída de fluxo.)

 

 