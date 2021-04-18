---
title: Diretrizes gerais de programação
description: Diretrizes para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105761802"
---
# <a name="general-programming-guidelines"></a><span data-ttu-id="8fb68-103">Diretrizes gerais de programação</span><span class="sxs-lookup"><span data-stu-id="8fb68-103">General programming guidelines</span></span>

<span data-ttu-id="8fb68-104">As seções a seguir fornecem diretrizes gerais para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="8fb68-104">The following sections provide general guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8fb68-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8fb68-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="8fb68-106">Camada de compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="8fb68-106">Application compatibility layer</span></span>](application-compatibility-layer.md)
</dt> <dd>

<span data-ttu-id="8fb68-107">Para executar aplicativos herdados em um ambiente Serviços de Área de Trabalho Remota, você pode usar a camada de compatibilidade de aplicativos Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="8fb68-107">To run legacy applications in a Remote Desktop Services environment you can use the Remote Desktop Services Application Compatibility layer.</span></span>

</dd> <dt>

[<span data-ttu-id="8fb68-108">Diretrizes de aplicativo cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="8fb68-108">Client/Server application guidelines</span></span>](client-server-application-guidelines.md)
</dt> <dd>

<span data-ttu-id="8fb68-109">Aplicativos cliente/servidor não devem assumir que uma única conexão de computador é equivalente a uma única sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="8fb68-109">Client/server applications must not assume that a single computer connection is equivalent to a single user session.</span></span>

</dd> <dt>

[<span data-ttu-id="8fb68-110">Monitorando conexões de sessão e desconexões</span><span class="sxs-lookup"><span data-stu-id="8fb68-110">Monitoring session connections and disconnections</span></span>](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

<span data-ttu-id="8fb68-111">Para registrar um aplicativo com Serviços de Área de Trabalho Remota, armazene o nome do aplicativo de servidor do virtual Channel no registro adicionando uma subchave.</span><span class="sxs-lookup"><span data-stu-id="8fb68-111">To register an application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey.</span></span>

</dd> <dt>

[<span data-ttu-id="8fb68-112">Diretrizes de hardware periférico</span><span class="sxs-lookup"><span data-stu-id="8fb68-112">Peripheral hardware guidelines</span></span>](peripheral-hardware-guidelines.md)
</dt> <dd>

<span data-ttu-id="8fb68-113">Se o dispositivo de hardware não for projetado para funcionar em uma sessão remota, os fornecedores deverão garantir que o software do driver de dispositivo force a desabilitação do redirecionamento do dispositivo usando uma política do sistema ou uma política de grupo.</span><span class="sxs-lookup"><span data-stu-id="8fb68-113">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

</dd> <dt>

[<span data-ttu-id="8fb68-114">Vinculação de tempo de execução para Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="8fb68-114">Run-Time linking to Wtsapi32.dll</span></span>](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

<span data-ttu-id="8fb68-115">Seu aplicativo pode usar a API Serviços de Área de Trabalho Remota para vincular dinamicamente ao Wtsapi32.dll em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="8fb68-115">Your application can use the Remote Desktop Services API to dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="8fb68-116">Para fazer isso, seu aplicativo deve chamar a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="8fb68-116">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span>

</dd> </dl>

 

 