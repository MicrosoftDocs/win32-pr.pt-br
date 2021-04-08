---
description: Um aplicativo em execução como um usuário padrão se comunica com um serviço em execução como sistema usando RPC (chamada de procedimento remoto).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Modelo de serviço do sistema operacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce545c60da8e480247c8fc8b02cfc01e4487340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922120"
---
# <a name="operating-system-service-model"></a><span data-ttu-id="f66bd-103">Modelo de serviço do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="f66bd-103">Operating System Service Model</span></span>

<span data-ttu-id="f66bd-104">No modelo de serviço do sistema operacional, um aplicativo em execução como um usuário padrão se comunica com um serviço em execução como **sistema** usando RPC ( [chamada de procedimento remoto](/windows/desktop/Rpc/rpc-start-page) ).</span><span class="sxs-lookup"><span data-stu-id="f66bd-104">In the operating system service model, an application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>

<span data-ttu-id="f66bd-105">O aplicativo de usuário padrão é marcado no manifesto do aplicativo com um **requestedExecutionLevel** de **asInvoker**.</span><span class="sxs-lookup"><span data-stu-id="f66bd-105">The standard user application is marked in the application manifest with a **requestedExecutionLevel** of **asInvoker**.</span></span> <span data-ttu-id="f66bd-106">Para executar uma operação que exige privilégio de administrador, o aplicativo de usuário padrão faz uma solicitação ao serviço.</span><span class="sxs-lookup"><span data-stu-id="f66bd-106">To perform an operation that requires administrator privilege, the standard user application makes a request to the service.</span></span>

<span data-ttu-id="f66bd-107">Um uso para o modelo de serviço do sistema operacional é gerenciar aplicativos que podem afetar o sistema, como antivírus ou outros softwares indesejados e spyware.</span><span class="sxs-lookup"><span data-stu-id="f66bd-107">One use for the operating system service model is to manage applications that could impact the system, such as antivirus or other unwanted software and spyware.</span></span> <span data-ttu-id="f66bd-108">O aplicativo de usuário padrão permite que o usuário conectado controle alguns aspectos do serviço.</span><span class="sxs-lookup"><span data-stu-id="f66bd-108">The standard user application allows the logged on user to control some aspects of the service.</span></span> <span data-ttu-id="f66bd-109">O serviço é responsável por determinar quais operações ele executa para um aplicativo de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="f66bd-109">The service is responsible for determining which operations it performs for a standard user application.</span></span> <span data-ttu-id="f66bd-110">Por exemplo, um serviço antivírus pode permitir que um usuário padrão inicie uma verificação do sistema, mas pode não permitir que um usuário padrão desabilite a verificação de vírus em tempo real.</span><span class="sxs-lookup"><span data-stu-id="f66bd-110">For example, an antivirus service might allow a standard user to start a scan of the system, but it might not allow a standard user to disable real-time virus checking.</span></span>

<span data-ttu-id="f66bd-111">Uma grande vantagem de usar o modelo de serviço do sistema operacional é que não é necessária nenhuma solicitação de elevação.</span><span class="sxs-lookup"><span data-stu-id="f66bd-111">A major benefit of using the operating system service model is that no elevation prompting is required.</span></span>

<span data-ttu-id="f66bd-112">Uma desvantagem de usar o modelo de serviço do sistema operacional é que um serviço em execução no sistema usa mais recursos do que uma tarefa, e um serviço não pode ser interrompido por um usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="f66bd-112">One drawback of using the operating system service model is that a service running on the system uses more resources than a task, and a service cannot be stopped by a standard user.</span></span> <span data-ttu-id="f66bd-113">Considere usar o [modelo de tarefa elevada](elevated-task-model.md) se for suficiente.</span><span class="sxs-lookup"><span data-stu-id="f66bd-113">Consider using the [Elevated Task Model](elevated-task-model.md) if it suffices.</span></span>

<span data-ttu-id="f66bd-114">Para implementar o modelo de serviço do sistema operacional, crie um aplicativo cliente de usuário padrão e um serviço do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f66bd-114">To implement the operating system service model, create a standard user client application and an operating system service.</span></span> <span data-ttu-id="f66bd-115">Instale o serviço no sistema operacional durante o tempo de instalação do produto.</span><span class="sxs-lookup"><span data-stu-id="f66bd-115">Install the service in the operating system during product installation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f66bd-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f66bd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f66bd-117">Desenvolvendo aplicativos que exigem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="f66bd-117">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="f66bd-118">Modelo de agente do administrador</span><span class="sxs-lookup"><span data-stu-id="f66bd-118">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="f66bd-119">Modelo de objeto COM do administrador</span><span class="sxs-lookup"><span data-stu-id="f66bd-119">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="f66bd-120">Modelo de tarefa elevada</span><span class="sxs-lookup"><span data-stu-id="f66bd-120">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
