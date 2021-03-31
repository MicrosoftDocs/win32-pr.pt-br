---
description: Para usar a API do WUA (agente de Windows Update), primeiro crie uma instância de uma das interfaces criando o objeto da coclasse apropriada.
ms.assetid: b304971d-584a-4d0f-be5b-26f0ab315ec9
title: Usando a API do agente de Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b5d155a2354b68135d0742f765dffb01e7235f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647291"
---
# <a name="using-the-windows-update-agent-api"></a><span data-ttu-id="22a2e-103">Usando a API do agente de Windows Update</span><span class="sxs-lookup"><span data-stu-id="22a2e-103">Using the Windows Update Agent API</span></span>

<span data-ttu-id="22a2e-104">Para usar a API do WUA (agente de Windows Update), primeiro crie uma instância de uma das interfaces criando o objeto da coclasse apropriada.</span><span class="sxs-lookup"><span data-stu-id="22a2e-104">To use the Windows Update Agent (WUA) API, first create an instance of one of the interfaces by creating the object from the appropriate coclass.</span></span>

<span data-ttu-id="22a2e-105">Os tópicos a seguir descrevem como você pode usar a API do WUA:</span><span class="sxs-lookup"><span data-stu-id="22a2e-105">The following topics describe how you can use the WUA API:</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="22a2e-106">Esses scripts destinam-se a demonstrar o uso das APIs do agente de Windows Update e fornecem exemplos de como os desenvolvedores podem usar essas APIs para resolver problemas.</span><span class="sxs-lookup"><span data-stu-id="22a2e-106">These scripts are intended to demonstrate the use of the Windows Update Agent APIs, and provide examples of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="22a2e-107">Esses scripts não são pretendidos como código de produção, e os próprios scripts não têm suporte da Microsoft (embora as APIs de agente de Windows Update subjacentes sejam suportadas).</span><span class="sxs-lookup"><span data-stu-id="22a2e-107">These scripts are not intended as production code, and the scripts themselves are not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 

-   [<span data-ttu-id="22a2e-108">Modelo de objeto do agente Windows Update</span><span class="sxs-lookup"><span data-stu-id="22a2e-108">Windows Update Agent Object Model</span></span>](windows-update-agent-object-model.md)
-   [<span data-ttu-id="22a2e-109">Determinando a versão atual do WUA</span><span class="sxs-lookup"><span data-stu-id="22a2e-109">Determining the Current Version of WUA</span></span>](determining-the-current-version-of-wua.md)
-   [<span data-ttu-id="22a2e-110">Atualizando o agente de Windows Update</span><span class="sxs-lookup"><span data-stu-id="22a2e-110">Updating the Windows Update Agent</span></span>](updating-the-windows-update-agent.md)
-   [<span data-ttu-id="22a2e-111">Atualizando arquivos de cabeçalho do agente Windows Update</span><span class="sxs-lookup"><span data-stu-id="22a2e-111">Updating Windows Update Agent Header Files</span></span>](updating-windows-update-agent-header-files.md)
-   [<span data-ttu-id="22a2e-112">Usando o WUA para verificar se há atualizações offline</span><span class="sxs-lookup"><span data-stu-id="22a2e-112">Using WUA to Scan for Updates Offline</span></span>](using-wua-to-scan-for-updates-offline.md)
-   [<span data-ttu-id="22a2e-113">Métodos e propriedades protegidos na API do WUA</span><span class="sxs-lookup"><span data-stu-id="22a2e-113">Secured Methods and Properties in the WUA API</span></span>](secured-methods-and-properties-in-the-wua-api.md)
-   [<span data-ttu-id="22a2e-114">Pesquisando, baixando e instalando atualizações</span><span class="sxs-lookup"><span data-stu-id="22a2e-114">Searching, Downloading, and Installing Updates</span></span>](searching--downloading--and-installing-updates.md)
-   [<span data-ttu-id="22a2e-115">Pesquisando, baixando e instalando atualizações específicas</span><span class="sxs-lookup"><span data-stu-id="22a2e-115">Searching, Downloading, and Installing Specific Updates</span></span>](searching--downloading--and-installing-specific-updates.md)
-   [<span data-ttu-id="22a2e-116">Usando o WUA de um computador remoto</span><span class="sxs-lookup"><span data-stu-id="22a2e-116">Using WUA From a Remote Computer</span></span>](using-wua-from-a-remote-computer.md)
-   [<span data-ttu-id="22a2e-117">Diretrizes para operações assíncronas do WUA</span><span class="sxs-lookup"><span data-stu-id="22a2e-117">Guidelines for Asynchronous WUA Operations</span></span>](guidelines-for-asynchronous-wua-operations.md)
-   [<span data-ttu-id="22a2e-118">Usando o WUA de um processo de logon secundário (executar como)</span><span class="sxs-lookup"><span data-stu-id="22a2e-118">Using WUA from a Secondary Logon (Run As) Process</span></span>](using-wua-from-a-secondary-logon--run-as--process.md)
-   [<span data-ttu-id="22a2e-119">Códigos de erro e de êxito do WUA</span><span class="sxs-lookup"><span data-stu-id="22a2e-119">WUA Success and Error Codes</span></span>](wua-success-and-error-codes-.md)
-   [<span data-ttu-id="22a2e-120">Códigos de erro de rede do WUA</span><span class="sxs-lookup"><span data-stu-id="22a2e-120">WUA Networking Error Codes</span></span>](wua-networking-error-codes-.md)

 

 



