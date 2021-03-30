---
title: Matrizes e ponteiros
description: A RPC (chamada de procedimento remoto) foi projetada para ser praticamente transparente para os desenvolvedores.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Chamada de procedimento remoto RPC, descrito, matrizes e ponteiros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636180"
---
# <a name="arrays-and-pointers"></a>Matrizes e ponteiros

A RPC (chamada de procedimento remoto) foi projetada para ser praticamente transparente para os desenvolvedores. Para obter essa transparência, o stub do cliente transmite para o servidor o ponteiro e o objeto de dados para o qual ele aponta. Se o procedimento remoto alterar os dados, o servidor deverá transmitir os novos dados de volta para o cliente para que o cliente possa copiar os novos dados nos dados originais.

Em geral, uma chamada de procedimento remoto se comporta exatamente como uma chamada de procedimento local. Ou seja, quando um ponteiro é um parâmetro, o procedimento remoto pode acessar o objeto de dados ao qual o ponteiro se refere da mesma maneira que um procedimento local pode.

Como os programas cliente e servidor são executados em espaços de endereço diferentes, os desenvolvedores devem usar os atributos linguagem IDL da Microsoft (MIDL) para descrever como os dados da matriz e do ponteiro são transmitidos entre o cliente e o servidor. Esta seção apresenta uma visão geral de como usar matrizes e ponteiros em aplicativos distribuídos, nos seguintes tópicos:

-   [Matrizes e RPC](arrays-and-rpc.md)
-   [Ponteiros e RPC](pointers-and-rpc.md)
-   [Usando matrizes, cadeias de caracteres e ponteiros](using-arrays-strings-and-pointers.md)

 

 




