---
title: Ponteiros e RPC
description: É muito eficiente usar ponteiros como parâmetros de função C.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2ce934ed1440bc070fab1b59b76f87182419aada06acaf7699533ef9989697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019178"
---
# <a name="pointers-and-rpc"></a>Ponteiros e RPC

É muito eficiente usar ponteiros como parâmetros de função C. O ponteiro custa apenas alguns bytes e pode ser usado para acessar uma grande quantidade de memória. No entanto, em um aplicativo distribuído, os procedimentos de cliente e servidor residem em espaços de endereço diferentes– eles podem estar em computadores diferentes. Portanto, o cliente e o servidor geralmente não têm acesso ao mesmo espaço de memória.

Quando um dos parâmetros do procedimento remoto é um ponteiro para um objeto , o cliente deve transmitir uma cópia desse objeto e seu ponteiro para o servidor. Se o procedimento remoto modificar o objeto por meio de seu ponteiro, o servidor retornará o ponteiro e sua cópia modificada.

MIDL oferece atributos de ponteiro para minimizar a quantidade de sobrecarga necessária e o tamanho do seu aplicativo. Esta seção discute a finalidade e os usos de atributos de ponteiro MIDL. Ele também apresenta informações sobre o tratamento de ponteiro em aplicativos RPC. Ele é dividido nos seguintes tópicos:

-   [Tipos de ponteiros](kinds-of-pointers.md)
-   [Ponteiros e alocação de memória](pointers-and-memory-allocation.md)
-   [Tipos de ponteiro padrão](default-pointer-types.md)
-   [Herança de tipo de atributo de ponteiro](pointer-attribute-type-inheritance.md)

 

 




