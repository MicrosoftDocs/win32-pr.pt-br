---
description: Você pode usar qualquer um dos métodos a seguir para depurar seu serviço.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Depurar um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646974"
---
# <a name="debugging-a-service"></a><span data-ttu-id="7e0a7-103">Depurar um serviço</span><span class="sxs-lookup"><span data-stu-id="7e0a7-103">Debugging a Service</span></span>

<span data-ttu-id="7e0a7-104">Você pode usar qualquer um dos métodos a seguir para depurar seu serviço.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-104">You can use any one of the following methods to debug your service.</span></span>

-   <span data-ttu-id="7e0a7-105">Use o depurador para depurar o serviço enquanto ele estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-105">Use your debugger to debug the service while it is running.</span></span> <span data-ttu-id="7e0a7-106">Primeiro, obtenha o identificador do processo (PID) do processo de serviço.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-106">First, obtain the process identifier (PID) of the service process.</span></span> <span data-ttu-id="7e0a7-107">Depois de obter a PID, anexe ao processo em execução.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-107">After you have obtained the PID, attach to the running process.</span></span> <span data-ttu-id="7e0a7-108">Para obter informações de sintaxe, consulte a documentação incluída com o depurador.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-108">For syntax information, see the documentation included with your debugger.</span></span>
-   <span data-ttu-id="7e0a7-109">Chame a função [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) para invocar o depurador para depuração Just-in-time.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-109">Call the [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) function to invoke the debugger for just-in-time debugging.</span></span>
-   <span data-ttu-id="7e0a7-110">Especifique um depurador a ser usado ao iniciar um programa.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-110">Specify a debugger to use when starting a program.</span></span> <span data-ttu-id="7e0a7-111">Para fazer isso, crie uma chave chamada **Opções de execução de arquivo de imagem** no seguinte local do registro:</span><span class="sxs-lookup"><span data-stu-id="7e0a7-111">To do so, create a key called **Image File Execution Options** in the following registry location:</span></span>

    <span data-ttu-id="7e0a7-112">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="7e0a7-112">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>

    <span data-ttu-id="7e0a7-113">Crie uma subchave com o mesmo nome que o seu serviço (por exemplo, MYSERV.EXE).</span><span class="sxs-lookup"><span data-stu-id="7e0a7-113">Create a subkey with the same name as your service (for example, MYSERV.EXE).</span></span> <span data-ttu-id="7e0a7-114">Para essa subchave, adicione um valor do tipo **reg \_ sz**, chamado **Debugger**.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-114">To this subkey, add a value of type **REG\_SZ**, named **Debugger**.</span></span> <span data-ttu-id="7e0a7-115">Use o caminho completo para o depurador como o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-115">Use the full path to the debugger as the string value.</span></span> <span data-ttu-id="7e0a7-116">No miniaplicativo do painel de controle de serviços, selecione seu serviço, clique em **inicialização** e marque **permitir que o serviço interaja com a área de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-116">In the Services control panel applet, select your service, click **Startup** and check **Allow Service to Interact with Desktop**.</span></span> <span data-ttu-id="7e0a7-117">O serviço deve ser um serviço interativo ou, caso contrário, o depurador não poderá ser executado na área de trabalho padrão.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-117">The service must be an interactive service, or else the debugger cannot run on the default desktop.</span></span> <span data-ttu-id="7e0a7-118">Observe que essa técnica não tem mais suporte do Windows Vista porque todos os serviços são executados na sessão que é reservada exclusivamente para serviços e não oferece suporte à exibição de uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-118">Note that this technique is no longer supported as of Windows Vista because all services are run in session that is reserved exclusively for services and does not support displaying a user interface.</span></span>

-   <span data-ttu-id="7e0a7-119">Use o [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) para registrar informações.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-119">Use [Event Tracing](/windows/desktop/ETW/event-tracing-portal) to log information.</span></span>

<span data-ttu-id="7e0a7-120">Para depurar o código de inicialização de um serviço de início automático, você precisará instalar e executar temporariamente o serviço como um serviço de início de demanda.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-120">To debug the initialization code of an auto-start service, you will have to temporarily install and run the service as a demand-start service.</span></span>

<span data-ttu-id="7e0a7-121">Às vezes, pode ser necessário executar um serviço como um aplicativo de console para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-121">At times, it may be necessary to run a service as a console application for debugging purposes.</span></span> <span data-ttu-id="7e0a7-122">Nesse cenário, a função [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) retornará **erro \_ falha na \_ conexão do \_ controlador \_ de serviço**.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-122">In this scenario, the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function will return **ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**.</span></span> <span data-ttu-id="7e0a7-123">Portanto, não se esqueça de estruturar seu código de modo que o código específico do serviço não seja chamado quando esse erro for retornado.</span><span class="sxs-lookup"><span data-stu-id="7e0a7-123">Therefore, be sure to structure your code such that service-specific code is not called when this error is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e0a7-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e0a7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e0a7-125">Depurando um aplicativo de serviço</span><span class="sxs-lookup"><span data-stu-id="7e0a7-125">Debugging a Service Application</span></span>](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[<span data-ttu-id="7e0a7-126">Ferramentas de Depuração para Windows</span><span class="sxs-lookup"><span data-stu-id="7e0a7-126">Debugging Tools for Windows</span></span>](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
