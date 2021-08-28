---
description: Exemplo de filtro de bola
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Exemplo de filtro de bola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df215f6f4be5fa1bc94872ac4e5855d4e9c0f19a136708d0c9377b19c5d79dda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084536"
---
# <a name="ball-filter-sample"></a>Exemplo de filtro de bola

## <a name="description"></a>Descrição

O Filtro de Bola é um filtro de origem de vídeo que produz uma imagem de uma bola de salto. Este exemplo ilustra a negociação de formato e o uso das classes base de filtro de origem [**CSource**](csource.md) e [**CSourceStream.**](csourcestream.md)

O código em Fball.h e Fball.cpp gerencia as interfaces de filtro. Esses dois arquivos contêm aproximadamente o código mínimo necessário para um filtro de origem. Os arquivos Ball.h e Ball.cpp contêm o código que quica a bola.

Esse filtro tem um único pino de saída, que fornece um fluxo de vídeo que mostra uma bola rolando no quadro. O filtro Bola também aceita solicitações de gerenciamento de qualidade do filtro downstream, que ilustra uma estratégia de gerenciamento de qualidade simples. Esse filtro implementa a interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) para essa finalidade.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos DirectShow SDK, instale a versão mais recente do [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: Bola de filtros multimídia de exemplos raiz do \[ *SDK* \] \\ DirectShow \\ \\ \\ \\ filtros.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Amostras](directshow-samples.md)
</dt> </dl>

 

 



