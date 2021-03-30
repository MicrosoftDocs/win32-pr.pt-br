---
title: Conversão de formato de várias etapas
description: Conversão de formato de várias etapas
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Gerenciador de compactação de áudio (ACM), convertendo dados
- ACM (Gerenciador de compactação de áudio), convertendo dados
- Exemplos do ACM, convertendo dados
- convertendo dados
- função acmFormatSuggest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916328"
---
# <a name="multistep-format-conversion"></a>Conversão de formato de várias etapas

Às vezes, o ACM não pode converter dados de um formato para outro em uma única etapa. Por exemplo, um aplicativo pode precisar converter dados estéreo de 16 bits 44-kHz para a ADPCM do mono de 11 kHz. Se o compressor ou o descompactador não puder fazer essa conversão diretamente, o aplicativo poderá tentar em duas etapas. Isso geralmente significa fazer uma conversão entre dois formatos PCM e, em seguida, outra conversão para o tipo de formato final.

Para converter em duas etapas, use a função [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) para encontrar um formato PCM que corresponda ao formato ADPCM. Em seguida, use dois fluxos de conversão para executar a conversão. Por exemplo, execute uma conversão de PCM estéreo de 16 bits, 44-kHz para mono de 16 bits, 11-kHz e, em seguida, converta de mono de 16 bits, de 11 kHz a 11-kHz mono ADPCM.

A conversão em várias etapas também ocorre quando o formato de origem ou destino não é PCM. Se o formato de origem não for PCM, ele deverá ser alterado para um formato PCM antes da conversão. Se o formato de destino não for PCM, a origem deverá ser convertida em um formato PCM intermediário e, em seguida, convertida no formato de destino final.

As conversões mais diretas ocorrem quando os formatos de origem e destino são ambos formatos PCM. Quando o formato de origem ou destino não é PCM, a conversão pode exigir uma etapa adicional. Se os formatos de origem e destino não forem PCM, a conversão geralmente exigirá mais de uma etapa e, em alguns casos, a conversão poderá não ser possível.

 

 




