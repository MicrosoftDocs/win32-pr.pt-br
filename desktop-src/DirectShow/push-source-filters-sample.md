---
description: Exemplo de filtros de origem de push
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Exemplo de filtros de origem de push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500370"
---
# <a name="push-source-filters-sample"></a>Exemplo de filtros de origem de push

## <a name="description"></a>Descrição

Este exemplo consiste em um conjunto de três filtros de origem que fornecem os seguintes dados de origem como um fluxo de vídeo:

-   CPushSourceBitmap: bitmap único (carregado do diretório atual)
-   CPushSourceBitmapSet: conjunto de bitmaps (carregados do diretório atual)
-   CPushSourceDesktop: cópia da imagem da área de trabalho atual (somente GDI)

## <a name="usage"></a>Uso

Para usar um filtro, carregue-o em GraphEdit e processe seu pino de saída. Isso conectará um processador de vídeo (e, possivelmente, um filtro de conversor de espaço de cor) e permitirá que você exiba a saída. Se você quiser renderizar a saída em um arquivo AVI, carregue o AVI Mux, carregue um filtro de gravador de arquivo, forneça um nome de saída para o gravador de arquivo e processe o pino de saída do filtro de push. Você também pode carregar e conectar os compactadores de vídeo, efeitos de vídeo e assim por diante.

> [!Note]  
> O filtro de captura de desktop não oferece suporte a sobreposições de hardware, portanto, não capturará vídeo renderizado em uma superfície de sobreposição ou cursores exibidos por meio de sobreposição de hardware. Ele usa GDI para converter a imagem da área de trabalho atual em um bitmap, que é passado para o pino de saída como um exemplo de mídia.

 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado sob o seguinte caminho: exemplos de *\[ raiz \] do SDK* \\ \\ multimídia \\ DirectShow filtros de \\ \\ multipush.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras do DirectShow](directshow-samples.md)
</dt> </dl>

 

 



