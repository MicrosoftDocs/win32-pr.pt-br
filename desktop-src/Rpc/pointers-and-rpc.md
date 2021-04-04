---
title: Ponteiros e RPC
description: É muito eficiente usar ponteiros como parâmetros de função C.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822878"
---
# <a name="pointers-and-rpc"></a>Ponteiros e RPC

É muito eficiente usar ponteiros como parâmetros de função C. O ponteiro custa apenas alguns bytes e pode ser usado para acessar uma grande quantidade de memória. No entanto, em um aplicativo distribuído, os procedimentos de cliente e servidor residem em espaços de endereço diferentes — eles podem estar em computadores diferentes. Portanto, o cliente e o servidor normalmente não têm acesso ao mesmo espaço de memória.

Quando um dos parâmetros do procedimento remoto é um ponteiro para um objeto, o cliente deve transmitir uma cópia desse objeto e seu ponteiro para o servidor. Se o procedimento remoto modificar o objeto por meio de seu ponteiro, o servidor retornará o ponteiro e sua cópia modificada.

O MIDL oferece atributos de ponteiro para minimizar a quantidade de sobrecarga necessária e o tamanho do seu aplicativo. Esta seção aborda a finalidade e os usos dos atributos de ponteiro de MIDL. Ele também apresenta informações sobre manipulação de ponteiros em aplicativos RPC. Ele é dividido nos seguintes tópicos:

-   [Tipos de ponteiros](kinds-of-pointers.md)
-   [Ponteiros e alocação de memória](pointers-and-memory-allocation.md)
-   [Tipos de ponteiro padrão](default-pointer-types.md)
-   [Herança de tipo de atributo de ponteiro](pointer-attribute-type-inheritance.md)

 

 




