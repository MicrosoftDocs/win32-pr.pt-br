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
# <a name="using-the-default-queue-callback-routine"></a><span data-ttu-id="e6144-103">Usando a rotina de retorno de chamada de fila padrão</span><span class="sxs-lookup"><span data-stu-id="e6144-103">Using the Default Queue Callback Routine</span></span>

<span data-ttu-id="e6144-104">A rotina de retorno de chamada de fila padrão pode ser especificada para lidar com notificações enviadas pelo [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)ou pode ser chamada por uma rotina de retorno de chamada personalizada que se baseia na funcionalidade da rotina de retorno de chamada de fila padrão.</span><span class="sxs-lookup"><span data-stu-id="e6144-104">The default queue callback routine can be specified to handle notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), or it can be called by a custom callback routine that builds on the functionality of the default queue callback routine.</span></span>

<span data-ttu-id="e6144-105">As seções a seguir explicam como inicializar e encerrar o contexto usado por uma rotina de retorno de chamada de fila padrão.</span><span class="sxs-lookup"><span data-stu-id="e6144-105">The following sections explain how to initialize and terminate the context used by a default queue callback routine.</span></span> <span data-ttu-id="e6144-106">As seções também descrevem como usar a rotina de retorno de chamada de fila padrão com [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) ou uma rotina de retorno de chamada personalizada.</span><span class="sxs-lookup"><span data-stu-id="e6144-106">The sections also describe how to use the default queue callback routine with [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) or a custom callback routine.</span></span>

-   [<span data-ttu-id="e6144-107">Inicializando e encerrando o contexto de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="e6144-107">Initializing and Terminating the Callback Context</span></span>](initializing-and-terminating-the-callback-context.md)
-   [<span data-ttu-id="e6144-108">Chamando a rotina de retorno de chamada de fila padrão</span><span class="sxs-lookup"><span data-stu-id="e6144-108">Calling the Default Queue Callback Routine</span></span>](calling-the-default-queue-callback-routine.md)

 

 



