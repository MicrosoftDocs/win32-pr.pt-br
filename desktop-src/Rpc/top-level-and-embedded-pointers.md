---
title: Top-Level e ponteiros inseridos
description: Para entender como os ponteiros e seus elementos de dados associados são alocados no Microsoft RPC, você precisa diferenciar os ponteiros de nível superior e os ponteiros inseridos.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453704"
---
# <a name="top-level-and-embedded-pointers"></a>Top-Level e ponteiros inseridos

Para entender como os ponteiros e seus elementos de dados associados são alocados no Microsoft RPC, você precisa diferenciar os *ponteiros de nível superior* e os *ponteiros inseridos*. Também é útil fazer referência ao conjunto de todos os ponteiros que não são ponteiros de nível superior.

Os *ponteiros de nível superior* são aqueles especificados como os nomes dos parâmetros nos protótipos de função. Ponteiros de nível superior e seus referents são sempre alocados no servidor.

*Ponteiros inseridos* são ponteiros inseridos em estruturas de dados como matrizes, estruturas e uniões. Quando os ponteiros inseridos só gravam a saída em um buffer e são nulos na entrada, o aplicativo do servidor pode alterar seus valores para não nulo. Nesse caso, os stubs de cliente alocam a nova memória para esses dados.

Se o ponteiro inserido não for nulo no cliente antes da chamada, os stubs não alocarão memória no cliente no retorno. Em vez disso, os stubs tentam gravar a memória associada ao ponteiro inserido na memória existente no cliente associado a esse ponteiro, substituindo os dados já ali.

> [!Note]  
> Para dados lidos ou gravados em um buffer, e que não especifica o tamanho do buffer, o comprimento da saída deve ser menor ou igual ao comprimento da entrada. Uma exceção RPC é gerada quando o estouro é detectado. Para dados de cadeia de caracteres, o comprimento de saída é determinado pela verificação do comprimento da cadeia de caracteres de entrada. Portanto, cadeias de caracteres de saída não podem exceder o comprimento das cadeias de caracteres As diretrizes de práticas recomendadas são evitar isso sempre incluindo um parâmetro de tamanho especificado para indicar o tamanho do buffer.

 

Ponteiros de somente gravação inseridos são discutidos na [combinação de ponteiros e atributos direcionais](combining-pointer-and-directional-attributes.md).

O termo *ponteiros de nível nontop* refere-se a todos os ponteiros que não são especificados como nomes de parâmetro no protótipo de função, incluindo ponteiros incorporados e vários níveis de ponteiros aninhados.

 

 




