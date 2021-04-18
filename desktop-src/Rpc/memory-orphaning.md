---
title: Órfão de memória
description: Se seu aplicativo distribuído usar um parâmetro \ in, out, Unique \ ou \ in, out, PTR \ pointer, o lado do servidor do aplicativo poderá alterar o valor do parâmetro pointer para NULL.
ms.assetid: 65588b4d-6bf4-44f7-994c-29a5b185c6b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32042911695f377e0a628168e91387bfa25f0d79
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789734"
---
# <a name="memory-orphaning"></a>Órfão de memória

Se seu aplicativo distribuído usar um \[ parâmetro [de ponteiro in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl), [Unique](/windows/desktop/Midl/unique) \] ou \[ **in**, **out**, [PTR](/windows/desktop/Midl/ptr) , \] o lado do servidor do aplicativo poderá alterar o valor do parâmetro pointer para NULL. Quando o servidor retorna subsequentemente o valor nulo para o cliente, a memória referenciada pelo ponteiro antes da chamada de procedimento remoto ainda está presente no lado do cliente, mas não é mais acessível a partir desse ponteiro (exceto no caso de um ponteiro completo com alias). Essa memória é considerada *órfã*. Isso também tem como termo um *vazamento de memória*. O órfão repetitivo de memória no cliente faz com que o cliente fique sem recursos de memória disponíveis.

A memória também pode ser órfã quando o servidor altera um ponteiro inserido para um valor nulo. Por exemplo, se o parâmetro apontar para uma estrutura de dados complexa, como uma árvore, o lado do servidor do aplicativo poderá excluir nós da árvore e definir ponteiros dentro da árvore para NULL.

Outra situação que pode levar a uma perda de memória envolve matrizes em conformidade, variáveis e abertas que contêm ponteiros. Quando o aplicativo de servidor modifica o parâmetro que especifica o tamanho da matriz ou o intervalo transmitido para que ele represente um valor menor, os stubs usam os valores menores para liberar memória. Os elementos de matriz com índices maiores que o parâmetro de tamanho ficam órfãos. Seu aplicativo deve liberar elementos fora do intervalo transmitido.

 

 