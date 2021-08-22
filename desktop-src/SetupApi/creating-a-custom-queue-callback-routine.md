---
description: Além de usar o retorno de chamada de fila padrão, você pode escrever uma rotina de retorno de chamada personalizada.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Criando uma rotina de retorno de chamada de fila personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0602e32ef97ea962ca91375318bb563c0809da0dc4877aa6c9439644b52408e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887498"
---
# <a name="creating-a-custom-queue-callback-routine"></a>Criando uma rotina de retorno de chamada de fila personalizada

Além de usar o retorno de chamada de fila padrão, você pode escrever uma rotina de retorno de chamada personalizada. Essa função deve ter o mesmo formato que [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Isso será útil se você precisar de uma rotina de retorno de chamada para lidar com uma notificação de maneira diferente da fornecida pela rotina de retorno de chamada de fila padrão.

Se apenas uma pequena parte do comportamento da rotina de retorno de chamada da fila padrão precisar ser alterada, você poderá criar uma rotina de retorno de chamada personalizada para filtrar as notificações, tratando apenas aquelas que exigem comportamento especial e chamando [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) para os outros.

Por exemplo, se você quiser manipular erros de exclusão de arquivo personalizado, poderá criar uma função de retorno de chamada personalizada, *MyCallback*. Essa função interceptaria e processaria notificações [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md) e chamaria a função de retorno de chamada de fila padrão para todas as outras notificações. *MyCallback* retorna um valor para as notificações de erro de exclusão. Para todas as outras notificações, *MyCallback* passa qualquer valor que a rotina de retorno de chamada de fila padrão retornada para a fila.

Esse fluxo de controle é ilustrado no diagrama a seguir.

![setas e caixas mostrando o fluxo de dados para a função de retorno de chamada personalizada](images/callback.png)

> [!IMPORTANT]
> Se a função de retorno de chamada personalizada chamar a rotina de retorno de chamada da fila padrão, ela deverá passar o ponteiro nulo retornado por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) para a rotina de retorno de chamada padrão.

 

 

 
