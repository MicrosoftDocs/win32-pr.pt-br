---
title: Órfão de memória
description: Se o aplicativo distribuído usar um parâmetro \ in, out, unique\ ou \ in, out, ptr\ pointer, o lado do servidor do aplicativo poderá alterar o valor do parâmetro de ponteiro para nulo.
ms.assetid: 65588b4d-6bf4-44f7-994c-29a5b185c6b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64b3a560eb1daecf3cd10bc18c62057cd2d09c1321c272f4e8fe73a65305832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019824"
---
# <a name="memory-orphaning"></a>Órfão de memória

Se o aplicativo distribuído usar um parâmetro \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl), [unique](/windows/desktop/Midl/unique) ou \] \[ **in**, **out**, [ptr](/windows/desktop/Midl/ptr) pointer, o lado do servidor do aplicativo poderá alterar o valor do parâmetro de ponteiro \] para null. Quando o servidor retorna subsequentemente o valor nulo para o cliente, a memória referenciada pelo ponteiro antes da chamada de procedimento remoto ainda está presente no lado do cliente, mas não é mais acessível desse ponteiro (exceto no caso de um ponteiro completo com alias). Diz-se que essa memória é *órfã.* Isso também é usado como vazamento *de memória.* A repetição de órfãos de memória no cliente faz com que o cliente ficar sem recursos de memória disponíveis.

A memória também pode ficar órfã sempre que o servidor altera um ponteiro inserido para um valor nulo. Por exemplo, se o parâmetro aponta para uma estrutura de dados complexa, como uma árvore, o lado do servidor do aplicativo pode excluir nós da árvore e definir ponteiros dentro da árvore como nulos.

Outra situação que pode levar a um vazamento de memória envolve matrizes compatíveis, variáveis e abertas que contêm ponteiros. Quando o aplicativo de servidor modifica o parâmetro que especifica o tamanho da matriz ou o intervalo transmitido para que ele represente um valor menor, os stubs usam os valores menores para liberar memória. Os elementos de matriz com índices maiores que o parâmetro de tamanho são órfãos. Seu aplicativo deve liberar elementos fora do intervalo transmitido.

 

 