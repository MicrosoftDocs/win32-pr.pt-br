---
description: Exemplo de filtro de bola
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Exemplo de filtro de bola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825987"
---
# <a name="ball-filter-sample"></a>Exemplo de filtro de bola

## <a name="description"></a>Descrição

O filtro de bola é um filtro de fonte de vídeo que produz uma imagem de uma bola saltando. Este exemplo ilustra a negociação de formato e o uso das classes base de filtro de origem [**CSource**](csource.md) e [**CSourceStream**](csourcestream.md).

O código em Fball. h e Fball. cpp gerencia as interfaces de filtro. Esses dois arquivos contêm aproximadamente o código mínimo necessário para um filtro de origem. Os arquivos Ball. h e Ball. cpp contêm o código que salta a bola.

Esse filtro tem um único pino de saída, que fornece um fluxo de vídeo que mostra uma bola saltando no quadro. O filtro de bola também aceita solicitações de gerenciamento de qualidade do filtro downstream, que ilustra uma estratégia de gerenciamento de qualidade simples. Esse filtro implementa a interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) para essa finalidade.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado sob o seguinte caminho: exemplo de \[ *raiz do SDK* \] \\ exemplos de \\ multimídia do \\ DirectShow \\ \\ .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras do DirectShow](directshow-samples.md)
</dt> </dl>

 

 



