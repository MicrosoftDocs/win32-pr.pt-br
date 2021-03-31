---
title: Matrizes fixas
description: Se a sua interface especifica uma matriz com um número específico de elementos como um parâmetro, ele está usando uma matriz fixa. Ao usar MIDL, você define matrizes fixas da mesma maneira que as define em C. Especifique o tipo, o nome e o tamanho da matriz.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3a620e86bff47e04afb5078dff50faee9fef0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636212"
---
# <a name="fixed-arrays"></a>Matrizes fixas

Se a sua interface especifica uma matriz com um número específico de elementos como um parâmetro, ele está usando uma matriz fixa. Ao usar MIDL, você define matrizes fixas da mesma maneira que as define em C. Especifique o tipo, o nome e o tamanho da matriz.

O exemplo a seguir demonstra como definir uma matriz fixa.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

Quando um programa cliente passa uma matriz fixa para um programa de servidor, o stub do cliente envia a matriz inteira para o stub do servidor. O stub do servidor aloca memória para a matriz e armazena os dados da matriz que recebe pela rede na memória alocada. Em seguida, ele passa a matriz para o procedimento remoto no servidor. O servidor pode modificar os dados na matriz.

Quando o procedimento remoto é encerrado, o stub do servidor envia o conteúdo da matriz de volta para o cliente. O stub do cliente copia os dados recebidos do stub do servidor na matriz original. O programa cliente pode usar os dados como faria se eles recebissem os dados de uma chamada de procedimento local.

 

 




