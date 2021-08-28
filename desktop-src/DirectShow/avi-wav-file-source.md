---
description: Origem do arquivo AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Origem do arquivo AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8c99de9eed21afa716c4f3ee81a5d1cc4e9731739526f7c9531c758b30a22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689356"
---
# <a name="aviwav-file-source"></a>Origem do arquivo AVI/WAV

(Preterido. Para arquivos AVI e WAV, use a Fonte de Arquivo [(Assíncrona)](file-source--async--filter.md) e o [Divisor AVI](avi-splitter-filter.md) ou [o Analisador WAVE](wave-parser-filter.md).)

O filtro Origem do Arquivo AVI/WAV lê os arquivos de origem AVI e WAV e gera os pinos de saída apropriados para o tipo de arquivo.

Para arquivos WAV, o filtro cria um pino de saída de áudio, que produz um fluxo de áudio que pode ser conectado a um filtro de renderização de áudio ou filtro de transformação de áudio intermediária.

Para arquivos AVI, o filtro cria um pino de saída de vídeo, que produz um fluxo AVI compactado adequado para o filtro codec AVI e um pino de saída de áudio, que produz um fluxo de áudio adequado para um filtro de renderização de áudio ou um filtro de transformação de áudio intermediária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



