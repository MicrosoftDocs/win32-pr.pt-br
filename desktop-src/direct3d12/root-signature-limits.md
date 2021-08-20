---
title: Limites de assinaturas raiz
description: A assinatura raiz é a principal imobiliária e há limites e custos rígidos a serem considerados.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7686c1d67d3c069167d6a1054bfe1bc0532f6e4f35304ccac985eeb5db530837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806656"
---
# <a name="root-signature-limits"></a>Limites de assinaturas raiz

A assinatura raiz é a principal imobiliária e há limites e custos rígidos a serem considerados.

-   [Limites e custos de memória](#memory-limits-and-costs)
-   [Custos de desempenho](#performance-costs)
-   [Amostras estáticas](#static-samplers)
-   [Tópicos relacionados](#related-topics)

## <a name="memory-limits-and-costs"></a>Limites e custos de memória

O tamanho máximo de uma assinatura raiz é de 64 DWORDs.

Esse tamanho máximo é escolhido para evitar o abuso da assinatura raiz como uma maneira de armazenar dados em massa. Cada entrada na assinatura raiz tem um custo em direção a este limite de 64 DWORD:

-   Tabelas de descritores custam 1 DWORD cada.
-   As constantes raiz custam 1 DWORD cada, pois são valores de 32 bits.
-   Os descritores de raiz (endereços virtuais de GPU de 64 bits) custam 2 DWORDs cada um.

Os exemplos estáticos não têm nenhum custo no tamanho da assinatura raiz.

## <a name="performance-costs"></a>Custos de desempenho

O custo de desempenho (em termos de níveis de indireção) é zero para uma constante raiz, 1 para um descritor raiz e 2 para uma tabela de descritores. Se uma assinatura raiz for grande e estourar a memória mais rápida em uma memória um pouco mais lenta (o que pode ocorrer em algum hardware), adicione 1 ao custo de desempenho para os itens de estouro no final da assinatura raiz.

Um estouro pode ocorrer em hardware que pode ter, por exemplo, um tamanho fixo de 16 DWORDs para o espaço de argumento raiz. Esse limite pode ser mais reduzido em um se o montador de entrada for usado. Nesse caso, há um estouro na memória um pouco mais lenta se a assinatura raiz for muito grande para a memória nativa de 15 ou 16 DWORD. Em outro hardware, não há memória de argumento de raiz nativa fixa (portanto, a situação de estouro nunca ocorre).

Para todo o hardware, se qualquer argumento raiz for alterado, o driver deverá manter uma versão de todos os argumentos raiz (ao contrário de outro armazenamento, como heaps de descritores e recursos de buffer, que não têm controle de versão do driver). No hardware em que ocorre uma situação de estouro, somente a área nativa ou de estouro precisa ter controle de versão, dependendo de onde a alteração ocorreu. Obviamente, a quantidade de controle de versão deve ser mantida no mínimo necessário.

Em geral, considere as seguintes diretrizes:

-   Use uma assinatura de raiz pequena, conforme necessário, mas equilibre isso com a flexibilidade de uma assinatura raiz maior.
-   Organize parâmetros em uma assinatura de raiz grande para que os parâmetros mais prováveis de serem alterados com frequência ou se a latência de acesso baixa de um determinado parâmetro for importante, ocorrer primeiro.
-   Se conveniente, use as constantes raiz ou as exibições de buffer de constantes raiz ao colocar exibições de buffer constantes em um heap de descritor.

## <a name="static-samplers"></a>Amostras estáticas

Os exemplos estáticos (os exemplos em que o estado é totalmente definido e imutável) fazem parte das assinaturas raiz, mas não contam para o limite de 64 DWORD. Se uma amostra puder ser definida como estática, não será necessário que a amostra faça parte de um heap de descritor.

Não há nenhum custo de desempenho no uso de amostras estáticas, e uma assinatura raiz pode conter uma mistura de amostras estáticas (armazenadas na assinatura raiz ou em espaço reservado em algum hardware) e amostras dinâmicas (armazenadas em um heap de descritor de amostra). Os exemplos de um heap de descritor podem ser atribuídos e indexados dinamicamente, quais amostras estáticas não podem.

Os exemplos estáticos podem ser escritos como parte da assinatura raiz em sombreadores HLSL (consulte [especificando assinaturas raiz no HLSL](specifying-root-signatures-in-hlsl.md)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assinaturas raiz](root-signatures.md)
</dt> </dl>

 

 




