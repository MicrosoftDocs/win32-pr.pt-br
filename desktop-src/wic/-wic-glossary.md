---
description: Define os termos que são usados no WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Glossário do componente de imagem do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783698"
---
# <a name="windows-imaging-component-glossary"></a>Glossário do componente de imagem do Windows

## <a name="b"></a>B

<dl> <dt>

**profundidade de bits**
</dt> <dd>

O número de valores de cor que podem ser atribuídos a um único pixel em uma imagem. A profundidade de cor pode variar de 1 bit (preto e branco) a 32 bits (mais de 16,7 milhões cores). Consulte também: profundidade de cor

</dd> <dt>

**bits por pixel (BPP)**
</dt> <dd>

O número de bits que representam o valor de cor de cada pixel em uma imagem digitalizada. Consulte também: BPP

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Clipper**
</dt> <dd>

Um objeto IWICBitmapClipper.

</dd> <dt>

**codec**
</dt> <dd>

Um filtro que compacta (codifica) ou descompacta (decodifica) um fluxo de dados.

</dd> <dt>

**contexto de cor**
</dt> <dd>

Uma abstração para um perfil de cor. O perfil pode ser carregado de um arquivo (por ex. "sRGB Color Space Profile. icm") ou de um buffer de memória obtido pela leitura. As informações de contexto de cor são definidas pela interface IWICColorContext para o WIC e são recuperadas com o método GetColorContext.

</dd> <dt>

**transformação de cor**
</dt> <dd>

Mapear cores do contexto de cor de origem para o contexto de cor de destino em um determinado formato de pixel de saída.

</dd> <dt>

**Modelo de cores CYMK**
</dt> <dd>

O espaço de cores multidimensional que consiste nas intensidades ciano, magenta, amarelo e preto que compõem uma determinada cor.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**decodificador**
</dt> <dd>

Consulte outro termo: codec

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**fita**
</dt> <dd>

Consulte outro termo: codec

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**Compact**
</dt> <dd>

Um tipo de compactação que garante que os dados originais possam ser recuperados exatamente, sem perda na qualidade da imagem.

</dd> <dt>

**com perdas**
</dt> <dd>

Um processo para compactação de dados em que as informações consideradas desnecessárias é removido e não pode ser recuperado após a descompactação. Normalmente usado com áudio e dados visuais em que uma pequena degradação da qualidade é aceitável.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**apartamento multithread (MTA)**
</dt> <dd>

Uma forma de multithreading com suporte do COM (Component Object Model). Em um modelo de apartamento multi-threaded, todos os threads no processo que foram inicializados como de thread livre residem em um único apartamento.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**formato de pixel nativo**
</dt> <dd>

Um dos formatos de pixel fornecidos pelo WIC, no qual o layout de memória de cada pixel em um bitmap é descrito.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**Palette**
</dt> <dd>

Conjunto de cores usado por um objeto ou aplicativo.

</dd> <dt>

**política de metadados de foto**
</dt> <dd>

A política do Windows para leitura, gravação e remoção de metadados de imagem.

</dd> <dt>

**formato de pixel**
</dt> <dd>

Tamanho e organização de componentes de cor de pixel na memória. Ele é especificado pelo número total de bits usados por pixel e pelo número de bits usados para armazenar os componentes vermelho, verde, azul e alfa da cor. Por exemplo, o formato de pixel RGB24 usa 24 bits para armazenar uma cor de pixel, com oito bits cada para vermelho, verde e azul. O formato de pixel ARGB32 usa 32 bits, com 24 bits de informações de cores e 8 bits de informações de canal alfa.

</dd> <dt>

**decodificação progressiva**
</dt> <dd>

O processo de decodificação de imagens que foram codificadas com informações sobre os diferentes níveis de decodificação.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**fluxo**
</dt> <dd>

Refere-se a uma interface COM de IStream que pode ser usada para ler ou gravar dados em arquivos, memória ou locais de rede em sequência.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**curva de Tom**
</dt> <dd>

Um grafo usado em fotos digitais que exibe o intervalo de tons da imagem.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Windows Imaging Component (WIC)**
</dt> <dd>

Uma plataforma extensível que fornece uma API de nível baixo para imagens digitais.

</dd> </dl>

 

 



