---
description: Exemplo de filtro infTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Exemplo de filtro infTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd0bbbb4df30f549a8ea0ba15d33696dcb7c108cbeffa6658bbb1842291517d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398014"
---
# <a name="inftee-filter-sample"></a>Exemplo de filtro infTee

## <a name="description"></a>Descrição

O filtro InfTee fornece uma implementação de exemplo do filtro DirectShow [Tee de Pino](infinite-pin-tee-filter.md) Infinito. O filtro tem um pino de entrada e um número dinâmico de pinos de saída. Todos os exemplos de mídia enviados ao filtro são entregues simultaneamente de todos os pinos de saída.

Esse filtro aparece no GraphEdit sob o nome "Exemplo de Pin Infinito De Exemplo", para diferenciá-lo do filtro Padrão de Pin Infinito fornecido DirectShow.

## <a name="usage"></a>Uso

Como esse filtro não altera os dados recebidos, todos os pinos devem concordar com o mesmo tipo de mídia. Durante o processo de conexão, o filtro pode reconectar alguns pinos para fazer os tipos de mídia corresponderem.

Os dados que chegam ao pin de entrada não são copiados antes que eles são enviados para os pinos de saída. O filtro também garante que os dados são entregues aos filtros downstream, para garantir que ambas as saídas recebam o serviço em tempo há tempo. Em particular, se uma das saídas puder bloquear na função membro [**COutputQueue::Receive,**](coutputqueue-receive.md) o valor será desligado de um thread para entregar o exemplo. Se não houvesse nenhum thread para entregar o exemplo, o thread que entrega o exemplo para o pin de entrada tee poderia passar os dados para um filtro downstream; nesse ponto, ele pode bloquear, mantendo os dados do outro filtro downstream por longos períodos de tempo.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos DirectShow SDK, instale a versão mais recente do [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: *\[ SDK Root \]* \\ Samples Multimedia DirectShow Filters \\ \\ \\ \\ InfTee.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Amostras](directshow-samples.md)
</dt> </dl>

 

 



