---
title: Top-Level e ponteiros inseridos
description: Para entender como os ponteiros e seus elementos de dados associados são alocados no Microsoft RPC, você precisa diferenciar entre ponteiros de nível superior e ponteiros inseridos.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fab18cfb345587f4c152f6890d94c5177e5bd9344e542592c33e462915beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011264"
---
# <a name="top-level-and-embedded-pointers"></a>Top-Level e ponteiros inseridos

Para entender como os ponteiros e seus elementos de dados associados são alocados no Microsoft RPC, você precisa diferenciar entre *ponteiros* de nível superior e *ponteiros inseridos.* Também é útil fazer referência ao conjunto de todos os ponteiros que não são ponteiros de nível superior.

*Os ponteiros de nível* superior são aqueles especificados como os nomes dos parâmetros em protótipos de função. Ponteiros de nível superior e seus referenciados sempre são alocados no servidor.

*Ponteiros inseridos* são ponteiros inseridos em estruturas de dados, como matrizes, estruturas e uniões. Quando os ponteiros inseridos só escrevem a saída em um buffer e são nulos na entrada, o aplicativo de servidor pode alterar seus valores para não nulos. Nesse caso, os stubs de cliente alocam nova memória para esses dados.

Se o ponteiro inserido não for nulo no cliente antes da chamada, os stubs não alocam memória no cliente no retorno. Em vez disso, os stubs tentam gravar a memória associada ao ponteiro inserido na memória existente no cliente associado a esse ponteiro, sobrescrevendo os dados já existentes.

> [!Note]  
> Para dados lidos de ou writen em um buffer e que não especificam o tamanho do buffer, o comprimento da saída deve ser menor ou igual ao tamanho da entrada. Uma exceção RPC é gerado quando o estouro é detectado. Para dados de cadeia de caracteres, o comprimento da saída é determinado verificando o comprimento da cadeia de caracteres de entrada. Portanto, as cadeias de caracteres de saída não podem exceder o comprimento das cadeias de caracteres de entrada. As diretrizes de melhor prática são evitar isso sempre incluindo um parâmetro especificado de tamanho para indicar o tamanho do buffer.

 

Ponteiros somente gravação inseridos são discutidos em Combinando ponteiro e [atributos direcionais.](combining-pointer-and-directional-attributes.md)

O termo ponteiros de nível não superior *refere-se* a todos os ponteiros que não são especificados como nomes de parâmetro no protótipo de função, incluindo ponteiros inseridos e vários níveis de ponteiros aninhados.

 

 




