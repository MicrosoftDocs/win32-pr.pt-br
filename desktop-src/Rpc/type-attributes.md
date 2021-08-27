---
title: Atributos de tipo
description: RPC (Chamada de Procedimento Remoto) e os atributos de tipo MIDL que podem ser aplicados a declarações de tipo.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5da8f3beb62f443b95a42283d4625200812436bce1bc667edc07d68f2542544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011164"
---
# <a name="type-attributes"></a>Atributos de tipo

Atributos de tipo são os atributos MIDL que podem ser aplicados a declarações de tipo:

-   **\[**[**Lidar com**](/windows/desktop/Midl/handle)**\]**
-   **\[**[**alça de \_ contexto**](/windows/desktop/Midl/context-handle)**\]**
-   **\[**[**tipo \_ switch**](/windows/desktop/Midl/switch-type)**\]**
-   [atributos de tipo de ponteiro](three-pointer-types.md)

O **\[ atributo de \_ tipo \]** de opção designa o tipo de um discriminador de união. Esse atributo se aplica somente a uma união não truncada.

Um alça de contexto é um ponteiro com um atributo **\[ de alça \_ de \]** contexto. O **\[ atributo de \_ alça \]** de contexto permite que você escreva procedimentos que mantêm informações de estado entre chamadas de procedimento remoto. Um handle de contexto com um valor não nulo representa o contexto salvo e serve a duas finalidades:

-   No lado do cliente, ele contém as informações necessárias para a biblioteca de tempo de executar RPC direcionar a chamada para o servidor.
-   No lado do servidor, ele serve como um handle no contexto ativo.

O **\[** [**atributo**](/windows/desktop/Midl/handle) **\]** handle especifica que um tipo pode ocorrer como um identificador definido pelo usuário (genérico). Esse recurso permite o design de alças que são significativas para o aplicativo. O usuário deve fornecer rotinas de associação e desa associação para converter entre o tipo de identificador definido pelo usuário e o tipo de identificador primitivo RPC, **\_ identificador t**. Um alça primitivo contém informações de destino significativas para as bibliotecas de tempo de executar RPC. Um identificador definido pelo usuário só pode ser definido em uma declaração de tipo, não em uma declaração de função. Um parâmetro com o **\[ atributo handle \]** tem uma finalidade dupla. Ele é usado para determinar a associação para a chamada e é transmitido para o procedimento chamado como um parâmetro de dados normal.

 

 