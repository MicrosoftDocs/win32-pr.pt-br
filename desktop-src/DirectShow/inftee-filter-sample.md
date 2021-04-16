---
description: Exemplo de filtro InfTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Exemplo de filtro InfTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758509"
---
# <a name="inftee-filter-sample"></a>Exemplo de filtro InfTee

## <a name="description"></a>Descrição

O filtro InfTee fornece um exemplo de implementação do filtro de [t de pino infinito](infinite-pin-tee-filter.md) do DirectShow. O filtro tem um PIN de entrada e um número dinâmico de Pins de saída. Todos os exemplos de mídia enviados ao filtro são entregues simultaneamente de todos os Pins de saída.

Esse filtro aparece em GraphEdit, sob o nome "exemplo de PIN infinito ilimitado", para distingui-lo do filtro de padrões de PIN infinitos padrão que é fornecido no DirectShow.

## <a name="usage"></a>Uso

Como esse filtro não altera os dados recebidos, todos os Pins devem concordar com o mesmo tipo de mídia. Durante o processo de conexão, o filtro pode reconectar alguns Pins para que os tipos de mídia sejam correspondentes.

Os dados que chegam no pino de entrada não são copiados antes de serem enviados aos pins de saída. O filtro também garante que os dados sejam entregues aos filtros downstream, para garantir que ambas as saídas recebam serviço em tempo hábil. Em particular, se uma das saídas puder bloquear na função de membro [**COutputQueue:: Receive**](coutputqueue-receive.md) , o t girará um thread para entregar o exemplo. Se não havia nenhum thread para entregar o exemplo, o thread que entrega o exemplo para o pino de entrada de Altova pode passar os dados para um filtro downstream; Nesse ponto, ele pode bloquear, mantendo os dados do outro filtro downstream por longos períodos de tempo.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ amostras de multimídia do \\ \\ DirectShow \\ \\ InfTee.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras do DirectShow](directshow-samples.md)
</dt> </dl>

 

 



