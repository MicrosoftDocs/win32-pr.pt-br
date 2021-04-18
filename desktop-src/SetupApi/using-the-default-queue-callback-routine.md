---
description: A rotina de retorno de chamada de fila padrão pode ser especificada para lidar com notificações enviadas pelo SetupCommitFileQueue ou pode ser chamada por uma rotina de retorno de chamada personalizada que se baseia na funcionalidade da rotina de retorno de chamada de fila padrão.
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: Usando a rotina de retorno de chamada de fila padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771801"
---
# <a name="using-the-default-queue-callback-routine"></a>Usando a rotina de retorno de chamada de fila padrão

A rotina de retorno de chamada de fila padrão pode ser especificada para lidar com notificações enviadas pelo [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)ou pode ser chamada por uma rotina de retorno de chamada personalizada que se baseia na funcionalidade da rotina de retorno de chamada de fila padrão.

As seções a seguir explicam como inicializar e encerrar o contexto usado por uma rotina de retorno de chamada de fila padrão. As seções também descrevem como usar a rotina de retorno de chamada de fila padrão com [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) ou uma rotina de retorno de chamada personalizada.

-   [Inicializando e encerrando o contexto de retorno de chamada](initializing-and-terminating-the-callback-context.md)
-   [Chamando a rotina de retorno de chamada de fila padrão](calling-the-default-queue-callback-routine.md)

 

 



