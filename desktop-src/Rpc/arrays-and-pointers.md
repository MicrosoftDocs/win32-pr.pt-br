---
title: Matrizes e ponteiros
description: A RPC (Chamada de Procedimento Remoto) foi projetada para ser principalmente transparente para os desenvolvedores.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- RPC de Chamada de Procedimento Remoto , descrito, matrizes e ponteiros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cc588d4db7cb222ec0fb2689bf645a2a7ed0e12b632392264d480c26777531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073496"
---
# <a name="arrays-and-pointers"></a>Matrizes e ponteiros

A RPC (Chamada de Procedimento Remoto) foi projetada para ser principalmente transparente para os desenvolvedores. Para obter essa transparência, o stub do cliente transmite para o servidor o ponteiro e o objeto de dados para o qual ele aponta. Se o procedimento remoto mudar os dados, o servidor deverá transmitir os novos dados de volta para o cliente para que o cliente possa copiar os novos dados sobre os dados originais.

Em geral, uma chamada de procedimento remoto se comporta como uma chamada de procedimento local. Ou seja, quando um ponteiro é um parâmetro, o procedimento remoto pode acessar o objeto de dados ao que o ponteiro se refere da mesma maneira que um procedimento local pode.

Como os programas de cliente e servidor são executados em espaços de endereço diferentes, os desenvolvedores devem usar atributos midl (linguagem IDL da Microsoft) para descrever como os dados de matriz e ponteiro são transmitidos entre o cliente e o servidor. Esta seção apresenta uma visão geral de como usar matrizes e ponteiros em aplicativos distribuídos, nos tópicos a seguir:

-   [Matrizes e RPC](arrays-and-rpc.md)
-   [Ponteiros e RPC](pointers-and-rpc.md)
-   [Usando matrizes, cadeias de caracteres e ponteiros](using-arrays-strings-and-pointers.md)

 

 




