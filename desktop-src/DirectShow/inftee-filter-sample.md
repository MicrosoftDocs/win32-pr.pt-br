---
description: Exemplo de filtro InfTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Exemplo de filtro InfTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd0bbbb4df30f549a8ea0ba15d33696dcb7c108cbeffa6658bbb1842291517d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398014"
---
# <a name="inftee-filter-sample"></a>Exemplo de filtro InfTee

## <a name="description"></a>Description

o filtro InfTee fornece um exemplo de implementação do filtro de [t de Pin infinito](infinite-pin-tee-filter.md) DirectShow. O filtro tem um PIN de entrada e um número dinâmico de Pins de saída. Todos os exemplos de mídia enviados ao filtro são entregues simultaneamente de todos os Pins de saída.

Esse filtro aparece em GraphEdit, sob o nome "exemplo de PIN infinito ilimitado", para distingui-lo do filtro de padrões de PIN infinitos padrão fornecido no DirectShow.

## <a name="usage"></a>Uso

Como esse filtro não altera os dados recebidos, todos os Pins devem concordar com o mesmo tipo de mídia. Durante o processo de conexão, o filtro pode reconectar alguns Pins para que os tipos de mídia sejam correspondentes.

Os dados que chegam no pino de entrada não são copiados antes de serem enviados aos pins de saída. O filtro também garante que os dados sejam entregues aos filtros downstream, para garantir que ambas as saídas recebam serviço em tempo hábil. Em particular, se uma das saídas puder bloquear na função de membro [**COutputQueue:: Receive**](coutputqueue-receive.md) , o t girará um thread para entregar o exemplo. Se não havia nenhum thread para entregar o exemplo, o thread que entrega o exemplo para o pino de entrada de Altova pode passar os dados para um filtro downstream; Nesse ponto, ele pode bloquear, mantendo os dados do outro filtro downstream por longos períodos de tempo.

## <a name="downloading-the-sample"></a>Baixando o exemplo

para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

este exemplo é instalado no seguinte caminho: exemplos de *\[ raiz \] do SDK* \\ \\ multimídia \\ DirectShow \\ filtros \\ InfTee.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Amostras](directshow-samples.md)
</dt> </dl>

 

 



