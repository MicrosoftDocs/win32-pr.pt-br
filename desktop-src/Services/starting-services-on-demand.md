---
description: O usuário pode iniciar um serviço com o utilitário do painel de controle de serviços. O usuário pode especificar argumentos para o serviço no campo Iniciar parâmetros. Um programa de controle de serviço pode iniciar um serviço e especificar seus argumentos com a função StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Iniciando serviços sob demanda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751070"
---
# <a name="starting-services-on-demand"></a><span data-ttu-id="10ee5-105">Iniciando serviços sob demanda</span><span class="sxs-lookup"><span data-stu-id="10ee5-105">Starting Services on Demand</span></span>

<span data-ttu-id="10ee5-106">O usuário pode iniciar um serviço com o utilitário do painel de controle de serviços.</span><span class="sxs-lookup"><span data-stu-id="10ee5-106">The user can start a service with the Services control panel utility.</span></span> <span data-ttu-id="10ee5-107">O usuário pode especificar argumentos para o serviço no campo **Iniciar parâmetros** .</span><span class="sxs-lookup"><span data-stu-id="10ee5-107">The user can specify arguments for the service in the **Start parameters** field.</span></span> <span data-ttu-id="10ee5-108">Um programa de controle de serviço pode iniciar um serviço e especificar seus argumentos com a função [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="10ee5-108">A service control program can start a service and specify its arguments with the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function.</span></span>

<span data-ttu-id="10ee5-109">Quando o serviço é iniciado, o SCM executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="10ee5-109">When the service is started, the SCM performs the following steps:</span></span>

-   <span data-ttu-id="10ee5-110">Recupere as informações de conta armazenadas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="10ee5-110">Retrieve the account information stored in the database.</span></span>
-   <span data-ttu-id="10ee5-111">Faça logon na conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="10ee5-111">Log on the service account.</span></span>
-   <span data-ttu-id="10ee5-112">Carregue o perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="10ee5-112">Load the user profile.</span></span>
-   <span data-ttu-id="10ee5-113">Crie o serviço no estado suspenso.</span><span class="sxs-lookup"><span data-stu-id="10ee5-113">Create the service in the suspended state.</span></span>
-   <span data-ttu-id="10ee5-114">Atribua o token de logon ao processo.</span><span class="sxs-lookup"><span data-stu-id="10ee5-114">Assign the logon token to the process.</span></span>
-   <span data-ttu-id="10ee5-115">Permitir que o processo seja executado.</span><span class="sxs-lookup"><span data-stu-id="10ee5-115">Allow the process to execute.</span></span>

 

 



