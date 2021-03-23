---
title: Visão geral das tabelas de descritores
description: Cada tabela de descritores armazena os descritores de um ou mais tipos-SRVs, UAVe, CBVs e amostras. Uma tabela de descritores não é uma alocação de memória; é simplesmente um deslocamento e um comprimento em um heap de descritor.
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104024"
---
# <a name="descriptor-tables-overview"></a>Visão geral das tabelas de descritores

Cada tabela de descritores armazena os descritores de um ou mais tipos-SRVs, UAVe, CBVs e amostras. Uma tabela de descritores não é uma alocação de memória; é simplesmente um deslocamento e um comprimento em um heap de descritor.

-   [Referenciando tabelas de descritores](#referencing-descriptor-tables)
-   [Tópicos relacionados](#related-topics)

## <a name="referencing-descriptor-tables"></a>Referenciando tabelas de descritores

O pipeline de gráficos, por meio da assinatura raiz, tem acesso aos recursos fazendo referência a tabelas de descritores por índice.

Na verdade, uma tabela de descritores é apenas um subintervalo de um heap de descritor. Heaps de descritor representam a alocação de memória subjacente para uma coleção de descritores. Como a alocação de memória é uma propriedade de criação de um heap de descritor, a definição de uma tabela de descritores de um é garantida para ser tão barata quanto a identificação de uma região no heap para o hardware. As tabelas de descritores não precisam ser criadas ou destruídas no nível de API – elas são meramente identificadas para drivers como um deslocamento e tamanho fora de um heap sempre que forem referenciados.

Certamente, é possível que um aplicativo defina tabelas de descritor muito grandes quando seus sombreadores desejam ter a liberdade de selecionar de um grande conjunto de descritores disponíveis (geralmente fazendo referência a texturas) em tempo real (talvez orientado por dados materiais).

A assinatura raiz faz referência à entrada da tabela de descritores com uma referência ao heap, o local de início da tabela (um deslocamento do início do heap) e o comprimento (em entradas) da tabela. A imagem abaixo mostra esses conceitos: os ponteiros da tabela de descritores da assinatura raiz e os descritores dentro do heap de descritores que fazem referência a dados de textura ou de buffer completos em um heap de carregamento.

![tabelas de descritores](images/descriptor-table.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabelas de descritores](descriptor-tables.md)
</dt> </dl>

 

 




