---
title: Atributos de tipo
description: RPC (chamada de procedimento remoto) e os atributos de tipo MIDL que podem ser aplicados a declarações de tipo.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823781"
---
# <a name="type-attributes"></a>Atributos de tipo

Atributos de tipo são os atributos MIDL que podem ser aplicados a declarações de tipo:

-   **\[**[**processamento**](/windows/desktop/Midl/handle)**\]**
-   **\[**[**identificador de contexto \_**](/windows/desktop/Midl/context-handle)**\]**
-   **\[**[**tipo de comutador \_**](/windows/desktop/Midl/switch-type)**\]**
-   [atributos de tipo de ponteiro](three-pointer-types.md)

O atributo **\[ \_ tipo \] de comutador** designa o tipo de um discriminador Union. Esse atributo se aplica somente a uma União não encapsulada.

Um identificador de contexto é um ponteiro com um atributo de **\[ \_ identificador \] de contexto** . O atributo **\[ \_ identificador \] de contexto** permite que você escreva procedimentos que mantêm informações de estado entre chamadas de procedimento remoto. Um identificador de contexto com um valor não nulo representa o contexto salvo e serve para duas finalidades:

-   No lado do cliente, ele contém as informações necessárias para a biblioteca de tempo de execução RPC para direcionar a chamada para o servidor.
-   No lado do servidor, ele serve como um identificador no contexto ativo.

O **\[** [](/windows/desktop/Midl/handle) **\]** atributo Handle especifica que um tipo pode ocorrer como um identificador definido pelo usuário (genérico). Esse recurso permite o design de identificadores que são significativos para o aplicativo. O usuário deve fornecer associações e desvinculação de rotinas para converter entre o tipo de identificador definido pelo usuário e o tipo de identificador de RPC primitivo, **tratar \_ t**. Um identificador primitivo contém informações de destino significativas para as bibliotecas de tempo de execução RPC. Um identificador definido pelo usuário só pode ser definido em uma declaração de tipo, não em uma declaração de função. Um parâmetro com o atributo **\[ Handle \]** tem uma finalidade dupla. Ele é usado para determinar a associação para a chamada e é transmitido para o procedimento chamado como um parâmetro de dados normal.

 

 