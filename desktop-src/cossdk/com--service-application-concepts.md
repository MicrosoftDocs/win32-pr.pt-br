---
description: Conceitos do aplicativo de serviço COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Conceitos do aplicativo de serviço COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456961"
---
# <a name="com-service-application-concepts"></a><span data-ttu-id="21011-103">Conceitos do aplicativo de serviço COM+</span><span class="sxs-lookup"><span data-stu-id="21011-103">COM+ Service Application Concepts</span></span>

<span data-ttu-id="21011-104">Você pode usar a ferramenta administrativa serviços de componentes para configurar um aplicativo de servidor do COM+ como um aplicativo de serviço.</span><span class="sxs-lookup"><span data-stu-id="21011-104">You can use the Component Services administrative tool to configure a COM+ server application as a service application.</span></span> <span data-ttu-id="21011-105">A execução de um aplicativo de servidor COM+ como um serviço oferece as seguintes vantagens:</span><span class="sxs-lookup"><span data-stu-id="21011-105">Running a COM+ server application as a service offers the following advantages:</span></span>

-   <span data-ttu-id="21011-106">Se seu aplicativo sempre precisar ser executado, os serviços de componentes podem, opcionalmente, fazer com que o servidor seja iniciado automaticamente e também poderá reiniciar o servidor se ele atingir o tempo limite. Por exemplo, se um computador executando componentes de ouvinte de componentes enfileirados for reinicializado, os ouvintes de componentes em fila poderão ser iniciados automaticamente se estiverem configurados como um serviço.</span><span class="sxs-lookup"><span data-stu-id="21011-106">If your application always needs to be running, Component Services can optionally have the server started automatically and can also restart the server if it times out. For example, if a computer running Queued Components listener components is rebooted, the Queued Components listeners can be started automatically if they are configured as a service.</span></span>
-   <span data-ttu-id="21011-107">Se seu aplicativo precisar executar operações privilegiadas, o aplicativo poderá ser executado como a conta do sistema local.</span><span class="sxs-lookup"><span data-stu-id="21011-107">If your application needs to perform privileged operations, the application can run as the local system account.</span></span> <span data-ttu-id="21011-108">Somente os serviços NT podem ser executados com esse nível de segurança.</span><span class="sxs-lookup"><span data-stu-id="21011-108">Only NT services are allowed to run with this level of security.</span></span> <span data-ttu-id="21011-109">O aplicativo será compatível com o Serviço de cluster do Windows, que gerencia os serviços durante o failover do sistema.</span><span class="sxs-lookup"><span data-stu-id="21011-109">The application will be compatible with the Windows Cluster service, which manages services during system failover.</span></span>
-   <span data-ttu-id="21011-110">Se outros serviços precisarem ser marcados como dependentes, os serviços de componentes fornecerão essa opção.</span><span class="sxs-lookup"><span data-stu-id="21011-110">If other services need to be marked as dependent, Component Services provides that option.</span></span> <span data-ttu-id="21011-111">Por exemplo, se seu aplicativo utiliza a funcionalidade fornecida por outro serviço, o serviço marcado como dependente será iniciado antes do aplicativo ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="21011-111">For example, if your application makes use of functionality provided by another service, the service marked as dependent will be started before your application starts.</span></span>

## <a name="starting-an-application-automatically"></a><span data-ttu-id="21011-112">Iniciando um aplicativo automaticamente</span><span class="sxs-lookup"><span data-stu-id="21011-112">Starting an Application Automatically</span></span>

<span data-ttu-id="21011-113">Quando o aplicativo do servidor COM+ é iniciado automaticamente, ele atua como um serviço, exigindo que o desenvolvedor gerencie o servidor usando a ferramenta administrativa serviços.</span><span class="sxs-lookup"><span data-stu-id="21011-113">When the COM+ server application is started automatically, it acts like a service, requiring the developer to manage the server using the Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="21011-114">A ferramenta administrativa serviços pode ser acessada iniciando a ferramenta administrativa serviços de componentes e clicando em **Serviços (local)**.</span><span class="sxs-lookup"><span data-stu-id="21011-114">The Services administrative tool can be accessed by launching the Component Services administrative tool and then clicking **Services (Local)**.</span></span>

 

## <a name="starting-an-application-manually"></a><span data-ttu-id="21011-115">Iniciando um aplicativo manualmente</span><span class="sxs-lookup"><span data-stu-id="21011-115">Starting an Application Manually</span></span>

<span data-ttu-id="21011-116">Quando o aplicativo do servidor COM+ é iniciado manualmente, ele atua como um host DLL com as configurações de segurança de um serviço.</span><span class="sxs-lookup"><span data-stu-id="21011-116">When the COM+ server application is started manually, it acts like a DLL host with the security settings of a service.</span></span> <span data-ttu-id="21011-117">O serviço será iniciado manualmente quando for ativado e desligado automaticamente quando atingir o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="21011-117">The service will be started up manually when activated and shut down automatically when it times out.</span></span>

## <a name="service-configurations"></a><span data-ttu-id="21011-118">Configurações de Serviço</span><span class="sxs-lookup"><span data-stu-id="21011-118">Service Configurations</span></span>

<span data-ttu-id="21011-119">Independentemente do tipo de inicialização, o aplicativo pode ser configurado para ser executado como uma conta do sistema local ou atribuído a uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="21011-119">Regardless of the startup type, the application can be configured to run as a local system account or assigned to a user account.</span></span> <span data-ttu-id="21011-120">O sistema local e a conta de usuário podem ser configurados no momento da criação do serviço.</span><span class="sxs-lookup"><span data-stu-id="21011-120">The local system and user account can be configured at the time of creating the service.</span></span> <span data-ttu-id="21011-121">Para definir as configurações de segurança, a ferramenta administrativa serviços precisará ser usada.</span><span class="sxs-lookup"><span data-stu-id="21011-121">To configure the security settings, the Services administrative tool will have to be used.</span></span> <span data-ttu-id="21011-122">As dependências também podem ser definidas para o serviço.</span><span class="sxs-lookup"><span data-stu-id="21011-122">Dependencies can also be set for the service.</span></span>

<span data-ttu-id="21011-123">O aplicativo também pode ser iniciado em qualquer ordem específica, selecionando dependências de uma lista de outros serviços do sistema.</span><span class="sxs-lookup"><span data-stu-id="21011-123">The application can also be started in any particular order by selecting dependencies from a list of other system services.</span></span> <span data-ttu-id="21011-124">Por exemplo, os serviços do sistema podem ser marcados como dependentes e não iniciarão o aplicativo até que os serviços do sistema tenham sido iniciados na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="21011-124">For example, the system services can be marked as dependent and will not start the application until the system services have been started in the specified order.</span></span> <span data-ttu-id="21011-125">Isso inicializará corretamente o aplicativo de serviço antes de ser usado.</span><span class="sxs-lookup"><span data-stu-id="21011-125">This will properly initialize the service application before it is used.</span></span>

<span data-ttu-id="21011-126">Para obter instruções passo a passo sobre como configurar um aplicativo COM+ para ser executado como um serviço, consulte [Configurando um aplicativo de servidor com+ como um aplicativo de serviço](configuring-a-com--server-application-as-a-service-application.md).</span><span class="sxs-lookup"><span data-stu-id="21011-126">For a step-by-step instruction on how to configure a COM+ application to run as a service, see [Configuring a COM+ Server Application as a Service Application](configuring-a-com--server-application-as-a-service-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="21011-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="21011-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21011-128">Tarefas do aplicativo de serviço COM+</span><span class="sxs-lookup"><span data-stu-id="21011-128">COM+ Service Application Tasks</span></span>](com--service-application-tasks.md)
</dt> </dl>

 

 



