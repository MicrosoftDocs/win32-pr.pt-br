---
description: Exemplo de filtro de despejo
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Exemplo de filtro de despejo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500641"
---
# <a name="dump-filter-sample"></a>Exemplo de filtro de despejo

## <a name="description"></a>Descrição

O filtro de despejo é um filtro de renderizador que grava os exemplos de mídia que recebe para um arquivo de texto.

Este exemplo ilustra como usar a classe de filtro base [**CBaseFilter**](cbasefilter.md) e a classe de pino de entrada renderizada [**CRenderedInputPin**](crenderedinputpin.md). Ele também demonstra como implementar a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) . O filtro de despejo tem um único pino de entrada, que grava cada exemplo que recebe diretamente para um arquivo.

## <a name="usage"></a>Uso

Esse filtro é uma ferramenta de depuração útil. Por exemplo, você pode verificar, bit por bit, os resultados de um filtro de transformação. Você pode criar um grafo manualmente usando GraphEdit e conectar o filtro de despejo à saída de um filtro de transformação ou qualquer outro pino de saída. Você também pode conectar um filtro de alto desempenho e colocar o filtro de despejo em um segmento do filtro de alto desempenho e a saída típica em outro trecho para monitorar os resultados em um cenário em tempo real.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ amostras de multimídia do DirectShow de \\ \\ \\ \\ despejo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras do DirectShow](directshow-samples.md)
</dt> </dl>

 

 



