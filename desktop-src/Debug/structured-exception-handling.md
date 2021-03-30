---
description: Uma exceção é um evento que ocorre durante a execução de um programa e requer a execução de código fora do fluxo de controle normal.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Tratamento de exceções estruturado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826167"
---
# <a name="structured-exception-handling"></a>Tratamento de exceções estruturado

Uma *exceção* é um evento que ocorre durante a execução de um programa e requer a execução de código fora do fluxo de controle normal. Há dois tipos de exceções: exceções de hardware e exceções de software. As *exceções de hardware* são iniciadas pela CPU. Eles podem resultar da execução de determinadas sequências de instrução, como divisão por zero ou uma tentativa de acessar um endereço de memória inválido. As *exceções de software* são iniciadas explicitamente por aplicativos ou pelo sistema operacional. Por exemplo, o sistema pode detectar quando um valor de parâmetro inválido é especificado.

A *manipulação de exceção estruturada* é um mecanismo para lidar com exceções de hardware e software. Portanto, seu código tratará as exceções de hardware e software de forma idêntica. A manipulação de exceção estruturada permite que você tenha controle total sobre a manipulação de exceções, fornece suporte para depuradores e é utilizável em todas as linguagens de programação e computadores. A *manipulação de exceção em vetor* é uma extensão da manipulação de exceção estruturada.

O sistema também dá suporte ao *tratamento de terminação*, o que permite que você garanta que sempre que um corpo de código protegido for executado, um bloco de código de encerramento especificado também será executado. O código de encerramento é executado independentemente de como o fluxo de controle deixa o corpo protegido. Por exemplo, um manipulador de encerramento pode garantir que as tarefas de limpeza sejam executadas mesmo se uma exceção ou algum outro erro ocorrer enquanto o corpo de código protegido estiver sendo executado.

-   [Sobre manipulação de exceção estruturada](about-structured-exception-handling.md)
-   [Usando manipulação de exceção estruturada](using-structured-exception-handling.md)
-   [Referência de manipulação de exceção estruturada](structured-exception-handling-reference.md)

 

 



