---
description: Além de usar o retorno de chamada de fila padrão, você pode escrever uma rotina de retorno de chamada personalizada.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Criando uma rotina de retorno de chamada de fila personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829300"
---
# <a name="creating-a-custom-queue-callback-routine"></a>Criando uma rotina de retorno de chamada de fila personalizada

Além de usar o retorno de chamada de fila padrão, você pode escrever uma rotina de retorno de chamada personalizada. Essa função deve ter a mesma forma que [*filecallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Isso será útil se você precisar de uma rotina de retorno de chamada para manipular uma notificação de uma maneira diferente daquela fornecida pela rotina de retorno de chamada de fila padrão.

Se apenas uma pequena parte do comportamento da rotina de retorno de chamada da fila padrão precisar ser alterada, você poderá criar uma rotina de retorno de chamada personalizada para filtrar as notificações, tratando apenas aquelas que exigem comportamento especial e chamando [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) para as outras.

Por exemplo, se você quisesse personalizar o identificador de erros de exclusão de arquivo, poderia criar uma função de retorno de chamada personalizada, *MyCallback*. Essa função interceptaria e processará notificações [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md) e chamaria a função de retorno de chamada de fila padrão para todas as outras notificações. *MyCallback* retorna um valor para as notificações de erro de exclusão. Para todas as outras notificações, *MyCallback* passa qualquer valor que a rotina de retorno de chamada de fila padrão retornada para a fila.

Esse fluxo de controle é ilustrado no diagrama a seguir.

![setas e caixas mostrando o fluxo de dados para a função de retorno de chamada personalizada](images/callback.png)

> [!IMPORTANT]
> Se a função de retorno de chamada personalizada chamar a rotina de retorno de chamada de fila padrão, ela deverá passar o ponteiro void retornado por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) para a rotina de retorno de chamada padrão.

 

 

 
