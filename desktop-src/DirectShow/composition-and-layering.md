---
description: Composição e camadas
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composição e camadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b173ed0727869d3630a2241d7237cf74fb5143a907a95fcc53901a7b85f285c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954225"
---
# <a name="composition-and-layering"></a>Composição e camadas

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Em uma coleção de faixas, a primeira faixa tem a prioridade mais baixa (prioridade 0) e cada faixa subsequente tem uma prioridade um nível mais alto. Em cada nível de prioridade, os clipes de origem nessa faixa ocultam os clipes de origem nas faixas abaixo dele, a menos que essa camada também contenha uma transição. Portanto, você pode imaginar o DES fazendo várias passagens ao renderizar.

Primeiro, ele renderiza a faixa 0. Não há nada "abaixo" da Faixa 0, portanto, as regiões vazias são renderizadas como uma imagem preta sólida. As transições nessa camada ocorrem entre a imagem preta e a faixa 0 ou vice-versa. O DES estabelece a faixa 1 na parte superior da faixa 0, gerando qualquer transição entre as duas faixas. O resultado é a composição das duas faixas. Em seguida, ele coloca a faixa 2 nessa composição. As transições nessa camada ocorrem entre a composição e a faixa 2. O processo continua até que a última faixa (prioridade mais alta) seja colocada.

Quando várias faixas são compostas juntas, elas se comportam como uma única faixa (chamada de faixa virtual). O objeto de composição encapsula esse comportamento, possibilitando transições complexas. Por exemplo, um clipe de vídeo pode ser apagado para um segundo clipe, enquanto a composição (ambos os clipes mais o apagando) esmaece para um terceiro clipe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida com os DirectShow de Edição](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



