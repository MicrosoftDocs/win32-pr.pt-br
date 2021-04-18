---
description: Composição e disposição em camadas
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composição e disposição em camadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105778496"
---
# <a name="composition-and-layering"></a>Composição e disposição em camadas

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Em uma coleção de faixas, a primeira faixa tem a prioridade mais baixa (prioridade 0) e cada faixa subsequente tem uma prioridade um nível acima. Em cada nível de prioridade, os clipes de origem nesse controle ocultam os clipes de origem nas faixas abaixo dela, a menos que essa camada também contenha uma transição. Assim, você pode imaginar que o DES faz várias passagens ao renderizar.

Primeiro, ele processa Track 0. Não há nada "em" Track 0 ", portanto, as regiões vazias são renderizadas como uma imagem preta sólida. As transições nessa camada ocorrem entre a imagem preta e a trilha 0 ou vice-versa. O DES dispõe da trilha 1 sobre o Track 0, gerando qualquer transição entre as duas faixas. O resultado é a composição das duas faixas. Em seguida, ele coloca o Track 2 nesta composição. As transições nessa camada ocorrem entre a composição e a faixa 2. O processo continua até que a última faixa (de prioridade mais alta) seja colocada inativa.

Quando várias faixas são compostas juntas, elas se comportam como uma única faixa (chamada de faixa virtual). O objeto de composição encapsula esse comportamento, fazendo transições complexas possíveis. Por exemplo, um clipe de vídeo pode apagar para um segundo clipe, enquanto a composição (ambos os clipes mais o apagamento) esmaece para um terceiro clipe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com os serviços de edição do DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



