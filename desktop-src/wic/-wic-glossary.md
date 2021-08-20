---
description: Define os termos que são usados no WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Windows Glossário do componente de imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c851b4a0be5d5f90a5ff0cc030d68cc1010a0259c316811a7ca1c3b92c383b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668187"
---
# <a name="windows-imaging-component-glossary"></a>Windows Glossário do componente de imagens

## <a name="b"></a>B

<dl> <dt>

**profundidade de bits**
</dt> <dd>

O número de valores de cor que podem ser atribuídos a um único pixel em uma imagem. A profundidade da cor pode variar de 1 bit (preto e branco) a 32 bits (mais de 16,7 milhões de cores). Confira também: Profundidade da cor

</dd> <dt>

**bits por pixel (bpp)**
</dt> <dd>

O número de bits que representam o valor de cor de cada pixel em uma imagem digitalizada. Consulte também:BPP

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Clipper**
</dt> <dd>

Um objeto IWICBitmapClipper.

</dd> <dt>

**Codec**
</dt> <dd>

Um filtro que compacta (codifica) ou descompacta (decodifica) um fluxo de dados.

</dd> <dt>

**contexto de cor**
</dt> <dd>

Uma abstração para um perfil de cor. O perfil pode ser carregado de um arquivo (ou seja, "sRGB Color Space Profile.icm") ou de um buffer de memória obtido pela leitura. As informações de contexto de cor são definidas pela interface IWICColorContext para WIC e são recuperadas com o método GetColorContext.

</dd> <dt>

**transformação de cores**
</dt> <dd>

Mapeando cores do contexto de cor de origem para o contexto de cor de destino em um determinado formato de pixel de saída.

</dd> <dt>

**Modelo de cor CYMK**
</dt> <dd>

Espaço de cores multidimensional que consiste nas intensidades ciano, magenta, amarelo e preto que comem uma determinada cor.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Decodificador**
</dt> <dd>

Consulte Outro Termo: codec

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Codificador**
</dt> <dd>

Consulte Outro Termo: codec

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**Lossless**
</dt> <dd>

Um tipo de compactação que garante que os dados originais possam ser recuperados exatamente, sem perda na qualidade da imagem.

</dd> <dt>

**Lossy**
</dt> <dd>

Um processo para compactar dados em que as informações consideradas desnecessárias são removidas e não podem ser recuperadas após a descompactação. Normalmente usado com dados visuais e de áudio em que uma pequena degradação da qualidade é aceitável.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**MTA (multithreaded apartment)**
</dt> <dd>

Uma forma de multithreading que tem suporte Component Object Model (COM). Em um modelo de apartment multithreaded, todos os threads no processo que foram inicializados como thread livre residem em um único apartment.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**formato de pixel nativo**
</dt> <dd>

Um dos formatos de pixel fornecidos pelo WIC, em que o layout de memória de cada pixel em um bitmap é descrito.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**Paleta**
</dt> <dd>

Conjunto de cores usadas por um objeto ou aplicativo.

</dd> <dt>

**política de metadados de foto**
</dt> <dd>

A política do Windows para ler, escrever e remover metadados de imagem.

</dd> <dt>

**formato de pixel**
</dt> <dd>

Tamanho e disposição de componentes de cor de pixel na memória. Ele é especificado pelo número total de bits usados por pixel e pelo número de bits usados para armazenar os componentes vermelho, verde, azul e alfa da cor. Por exemplo, o formato de pixel RGB24 usa 24 bits para armazenar uma cor de pixel, com oito bits cada para vermelho, verde e azul. O formato de pixel ARGB32 usa 32 bits, com 24 bits de informações de cor e 8 bits de informações de canal alfa.

</dd> <dt>

**decodificação progressiva**
</dt> <dd>

O processo de decodificação de imagens codificadas com informações sobre os diferentes níveis de decodificação.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Fluxo**
</dt> <dd>

Refere-se a uma interface COM IStream que pode ser usada para ler ou gravar dados sequencialmente em arquivos, memória ou locais de rede.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**curva de tom**
</dt> <dd>

Um grafo usado na fotografia digital que exibe o intervalo tonal da imagem.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Windows Imaging Component (WIC)**
</dt> <dd>

Uma plataforma extensível que fornece API de baixo nível para imagens digitais.

</dd> </dl>

 

 



