---
description: Usando o divisor MPEG-2
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Usando o divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753495"
---
# <a name="using-the-mpeg-2-splitter"></a>Usando o divisor MPEG-2

> [!Note]  
> A partir do Microsoft® Windows® XP, o filtro de divisão MPEG-2 é preterido. Em vez disso, use o [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) .

 

O filtro divisor MPEG-2 dá suporte à reprodução de modo de recepção de fluxos de programas MPEG-2 que contêm pelo menos um dos seguintes tipos de fluxo.

-   Vídeo MPEG-2
-   Áudio MPEG-2
-   Áudio Dolby AC-3 codificado conforme definido para DVD-Video
-   Áudio LPCM (código de pulso linear modulado) codificado conforme definido para DVD-Video

Para obter uma lista de tipos de mídia com suporte do divisor MPEG-2, consulte [tipos de mídia divisor MPEG-2](mpeg-2-splitter-media-types.md).

O divisor MPEG-2 não analisa fluxos de transporte. Use o filtro de Desmultiplexador MPEG-2 para fluxos de transporte (somente no modo push).

**Carimbos de Data/Hora**

Ao reproduzir fluxos de programa MPEG-2, o filtro divisor MPEG-2 trata a primeira referência do relógio do sistema que ele encontra como a origem de tempo de qualquer fluxo. Isso difere do [divisor de fluxo MPEG-1](mpeg-1-stream-splitter-filter.md), que usa carimbos de data/hora de apresentação. O método [**IAMParse:: Getparsetime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) retorna o tempo de relógio do sistema de fluxo (possivelmente estimado) para os dados que ele processou.

Se o filtro de divisão MPEG-2 encontrar um exemplo de entrada com o conjunto de propriedades de descontinuidade (a propriedade de descontinuidade pode ser definida usando [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) ou [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), ele ignora os dados até encontrar o primeiro pacote nos dados e ajusta seus carimbos de data/hora para que a SCR (referência do relógio do sistema) desse pacote seja considerada idêntica ao tempo da SCR antes da descontinuidade. Se o relógio da SCR aparecer para voltar ou avançar por mais de um segundo, então (em linha com a especificação de fluxo de programa MPEG-2), isso também será tratado como uma descontinuidade do relógio e a discrepância do relógio aparente será subtraída dos carimbos de data/hora passados para os filtros de downstream.

**Seleção de fluxo**

Ao reproduzir o fluxo de programa MPEG-2, o primeiro fluxo de vídeo e o primeiro fluxo de áudio encontrados atravessando o fluxo do programa são escolhidos. Há suporte para até um pino de saída de áudio e um vídeo. Por meio da interface [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) , fluxos diferentes do mesmo tipo podem ser selecionados até o número especificado pelo limite de áudio no cabeçalho do sistema. Para áudio MPEG-2, atualmente supõe-se que os fluxos formam um intervalo contíguo a partir do fluxo 0xC0.

**Interfaces com suporte**

O filtro divisor MPEG-2 dá suporte às seguintes interfaces.

-   [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse). Somente fluxo de programa MPEG-2.
-   [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect). Somente fluxo de programa MPEG-2, somente fluxos de áudio.
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking). Inclui o modo de byte que busca.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a MPEG-2 no DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



