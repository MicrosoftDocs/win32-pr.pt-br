---
description: A infraestrutura de pares não garante a ordem de recebimento e processamento de registros.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Dependências de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8121c22525a3a2d8065014eaf27143a324b2f6410f194d3257ec3b840958d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675016"
---
# <a name="record-dependencies"></a>Dependências de registro

A infraestrutura de pares não garante a ordem de recebimento e processamento de registros. Se seu aplicativo tiver dependências de registro, o que significa que o processamento ou a validação de um registro depende de outro registro, o aplicativo deverá ser capaz de lidar com situações em que os registros possam ser recebidos em uma ordem arbitrária e imprevisível. Por exemplo, um aplicativo de chat pode ter dois tipos de registros: um registro que contém informações sobre um usuário específico e um registro que contém uma mensagem de chat que se refere ao registro do usuário.

Um aplicativo deve ser capaz de lidar com a situação quando um registro de mensagem de chat é recebido antes do registro de usuário para a mensagem de chat. Uma maneira de lidar com a situação é aguardar o registro do usuário usando uma **lista de espera**, ou um cache e um temporizador. O aplicativo pode examinar periodicamente cada registro na lista ou no cache e, em seguida, manipular a situação quando o registro de usuário necessário é recebido.

Para lidar com dependências de registro, um aplicativo bem projetado consiste no seguinte:

-   Sempre verifica dependências de registro antes de executar uma ação.
-   Prevê condições que podem ocorrer quando registros são recebidos em uma ordem inesperada e, em seguida, manipula a situação.

 

 



