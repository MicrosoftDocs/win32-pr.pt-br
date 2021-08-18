---
description: Exemplo de filtros de origem por push
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Exemplo de filtros de origem por push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e72a9be7e5fa81d4fe2dc006c6d12e42f4f94d91561823b7f26a8400bbddda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747786"
---
# <a name="push-source-filters-sample"></a>Exemplo de filtros de origem por push

## <a name="description"></a>Descrição

Este exemplo consiste em um conjunto de três filtros de origem que fornecem os seguintes dados de origem como um fluxo de vídeo:

-   CPushSourceBitmap: bitmap único (carregado do diretório atual)
-   CPushSourceBitmapSet: conjunto de bitmaps (carregado do diretório atual)
-   CPushSourceDesktop: cópia da imagem da área de trabalho atual (somente GDI)

## <a name="usage"></a>Uso

Para usar um filtro, carregue-o no GraphEdit e renderizar seu pino de saída. Isso conectará um renderador de vídeo (e, possivelmente, um filtro do Conversor de Espaço de Cor) e permitirá que você exibir a saída. Se você quiser renderizar a saída em um arquivo AVI, carregue o Mux AVI, carregue um Filtro de Autor de Arquivos, forneça um nome de saída para o File Writer e renderizar o pino de saída do filtro PushSource. Você também pode carregar e conectar os videoclipes, efeitos de vídeo e assim por diante.

> [!Note]  
> O filtro de captura de área de trabalho não dá suporte a sobreposições de hardware, portanto, ele não capturará vídeo renderizado em uma superfície de sobreposição ou cursores exibidos por meio da sobreposição de hardware. Ele usa GDI para converter a imagem da área de trabalho atual em um bitmap, que é passado para o pino de saída como um exemplo de mídia.

 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os DirectShow exemplos do SDK, instale a versão mais recente do [SDK Windows .](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Este exemplo é instalado no seguinte caminho: *\[ SDK Root \]* \\ Samples Multimedia DirectShow Filters \\ \\ \\ \\ PushSource.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Amostras](directshow-samples.md)
</dt> </dl>

 

 



