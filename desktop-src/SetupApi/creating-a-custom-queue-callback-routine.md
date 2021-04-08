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
# <a name="creating-a-custom-queue-callback-routine"></a><span data-ttu-id="787fb-103">Criando uma rotina de retorno de chamada de fila personalizada</span><span class="sxs-lookup"><span data-stu-id="787fb-103">Creating a Custom Queue Callback Routine</span></span>

<span data-ttu-id="787fb-104">Além de usar o retorno de chamada de fila padrão, você pode escrever uma rotina de retorno de chamada personalizada.</span><span class="sxs-lookup"><span data-stu-id="787fb-104">In addition to using the default queue callback, you can write a custom callback routine.</span></span> <span data-ttu-id="787fb-105">Essa função deve ter a mesma forma que [*filecallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="787fb-105">This function must have the same form as [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="787fb-106">Isso será útil se você precisar de uma rotina de retorno de chamada para manipular uma notificação de uma maneira diferente daquela fornecida pela rotina de retorno de chamada de fila padrão.</span><span class="sxs-lookup"><span data-stu-id="787fb-106">This is useful if you need a callback routine to handle a notification in a manner other than that provided by the default queue callback routine.</span></span>

<span data-ttu-id="787fb-107">Se apenas uma pequena parte do comportamento da rotina de retorno de chamada da fila padrão precisar ser alterada, você poderá criar uma rotina de retorno de chamada personalizada para filtrar as notificações, tratando apenas aquelas que exigem comportamento especial e chamando [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) para as outras.</span><span class="sxs-lookup"><span data-stu-id="787fb-107">If only a small portion of the default queue callback routine's behavior needs to be changed, you can create a custom callback routine to filter the notifications, handling only those that require special behavior and calling [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) for the others.</span></span>

<span data-ttu-id="787fb-108">Por exemplo, se você quisesse personalizar o identificador de erros de exclusão de arquivo, poderia criar uma função de retorno de chamada personalizada, *MyCallback*.</span><span class="sxs-lookup"><span data-stu-id="787fb-108">For example, if you wanted to custom-handle file delete errors, you could create a custom callback function, *MyCallback*.</span></span> <span data-ttu-id="787fb-109">Essa função interceptaria e processará notificações [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md) e chamaria a função de retorno de chamada de fila padrão para todas as outras notificações.</span><span class="sxs-lookup"><span data-stu-id="787fb-109">This function would intercept and process [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md) notifications, and call the default queue callback function for all other notifications.</span></span> <span data-ttu-id="787fb-110">*MyCallback* retorna um valor para as notificações de erro de exclusão.</span><span class="sxs-lookup"><span data-stu-id="787fb-110">*MyCallback* returns a value for the delete error notifications.</span></span> <span data-ttu-id="787fb-111">Para todas as outras notificações, *MyCallback* passa qualquer valor que a rotina de retorno de chamada de fila padrão retornada para a fila.</span><span class="sxs-lookup"><span data-stu-id="787fb-111">For all other notifications, *MyCallback* passes whatever value the default queue callback routine returned to the queue.</span></span>

<span data-ttu-id="787fb-112">Esse fluxo de controle é ilustrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="787fb-112">This flow of control is illustrated in the following diagram.</span></span>

![setas e caixas mostrando o fluxo de dados para a função de retorno de chamada personalizada](images/callback.png)

> [!IMPORTANT]
> <span data-ttu-id="787fb-114">Se a função de retorno de chamada personalizada chamar a rotina de retorno de chamada de fila padrão, ela deverá passar o ponteiro void retornado por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) para a rotina de retorno de chamada padrão.</span><span class="sxs-lookup"><span data-stu-id="787fb-114">If the custom callback function calls the default queue callback routine, it must pass the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) to the default callback routine.</span></span>

 

 

 
