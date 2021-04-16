---
description: Origem do arquivo AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Origem do arquivo AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779244"
---
# <a name="aviwav-file-source"></a>Origem do arquivo AVI/WAV

(Preterido. Para arquivos AVI e WAV, use a [origem do arquivo (Async)](file-source--async--filter.md) e o [divisor AVI](avi-splitter-filter.md) ou o [analisador Wave](wave-parser-filter.md).)

O filtro de origem de arquivo AVI/WAV lê arquivos de origem AVI e WAV e gera os Pins de saída apropriados para o tipo de arquivo.

Para arquivos WAV, o filtro cria um PIN de saída de áudio, que produz um fluxo de áudio que pode ser conectado a um filtro de renderização de áudio ou ao filtro de transformação de áudio intermediário.

Para arquivos AVI, o filtro cria um pino de saída de vídeo, que produz um fluxo AVI compactado adequado para o filtro de codec AVI e um PIN de saída de áudio, que produz um fluxo de áudio adequado para um filtro de renderização de áudio ou um filtro de transformação de áudio intermediário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



