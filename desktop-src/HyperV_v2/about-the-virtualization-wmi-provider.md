---
description: O provedor WMI para Hyper-V permite que desenvolvedores e criadores de scripts criem rapidamente ferramentas, utilitários e aprimoramentos personalizados para a plataforma de virtualização. As interfaces WMI podem gerenciar todos os aspectos dos serviços do Hyper-V.
ms.assetid: 773BB141-7B9C-4015-81A0-BD17B8233CCD
title: Sobre o provedor WMI do Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c30b329f7e8a3fd3ae65b49f8467a8f712707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754678"
---
# <a name="about-the-hyper-v-wmi-provider"></a><span data-ttu-id="88881-104">Sobre o provedor WMI do Hyper-V</span><span class="sxs-lookup"><span data-stu-id="88881-104">About the Hyper-V WMI provider</span></span>

<span data-ttu-id="88881-105">O provedor WMI para Hyper-V permite que desenvolvedores e criadores de scripts criem rapidamente ferramentas, utilitários e aprimoramentos personalizados para a plataforma de virtualização.</span><span class="sxs-lookup"><span data-stu-id="88881-105">The WMI provider for Hyper-V enable developers, and scripters, to quickly build custom tools, utilities, and enhancements for the virtualization platform.</span></span> <span data-ttu-id="88881-106">As interfaces WMI podem gerenciar todos os aspectos dos serviços do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="88881-106">The WMI interfaces can manage all aspects of the Hyper-V services.</span></span>

## <a name="about-microsoft-windows-server-2008-r2-hyper-v"></a><span data-ttu-id="88881-107">Sobre o Microsoft Windows Server 2008 R2 Hyper-V</span><span class="sxs-lookup"><span data-stu-id="88881-107">About Microsoft Windows Server 2008 R2 Hyper-V</span></span>

<span data-ttu-id="88881-108">O Microsoft Windows Server 2008 R2 Hyper-V permite que os administradores de sistema consolidem servidores de hardware separados em um único servidor que executa o Microsoft Windows Server 2008 R2 como o sistema operacional do host.</span><span class="sxs-lookup"><span data-stu-id="88881-108">Microsoft Windows Server 2008 R2 Hyper-V allows system administrators to consolidate separate hardware servers on to a single server running Microsoft Windows Server 2008 R2 as the host operating system.</span></span>

<span data-ttu-id="88881-109">Cada uma das máquinas virtuais hospedadas é executada em seu próprio ambiente virtual separado e isolado.</span><span class="sxs-lookup"><span data-stu-id="88881-109">Each of the hosted virtual machines runs in its own separate and isolated virtual environment.</span></span> <span data-ttu-id="88881-110">Isso permite que o administrador gerencie, forneça e mantenha um grande número de máquinas virtuais com facilidade, reduzindo a necessidade de executar várias soluções de hardware para usar vários produtos e sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="88881-110">This allows the administrator to easily manage, provide for, and maintain large numbers of virtual machines while reducing the need to run multiple hardware solutions to use various products and operating systems.</span></span>

<span data-ttu-id="88881-111">Outra vantagem do ambiente de máquina virtual é o teste e o suporte.</span><span class="sxs-lookup"><span data-stu-id="88881-111">Another advantage of the virtual machine environment is in test and support.</span></span> <span data-ttu-id="88881-112">Novas configurações de servidor e sistema podem ser implantadas e testadas em paralelo com o sistema existente sem exigir um tempo de inatividade dispendioso durante a fase de distribuição.</span><span class="sxs-lookup"><span data-stu-id="88881-112">New server and system configurations can be deployed and tested in parallel with the existing system without requiring costly downtime during the rollout phase.</span></span> <span data-ttu-id="88881-113">Cada máquina virtual pode ser configurada para usar diferentes configurações durante a execução em uma plataforma padrão para produzir melhores resultados de teste.</span><span class="sxs-lookup"><span data-stu-id="88881-113">Each virtual machine can be setup to use varying configurations while running on a standard platform to produce better test results.</span></span> <span data-ttu-id="88881-114">Com suporte para sistemas operacionais anteriores, um pode dar suporte e testar hardware, sistemas e aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="88881-114">With support for earlier operating systems, one can support and test legacy hardware, systems and applications.</span></span> <span data-ttu-id="88881-115">O suporte a instantâneos permite tirar um instantâneo do estado de uma máquina virtual para que você possa retornar a um evento anterior, se necessário.</span><span class="sxs-lookup"><span data-stu-id="88881-115">Snapshot support allows you to take a snapshot of a virtual machine's state so you can return to a prior event if needed.</span></span>

<span data-ttu-id="88881-116">O Hyper-V expõe uma interface rica que permite ao usuário monitorar e controlar o ambiente de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="88881-116">Hyper-V exposes a rich interface which permits the user to monitor and control the virtual machine environment.</span></span> <span data-ttu-id="88881-117">A maior parte do Hyper-V pode ser controlada usando o provedor de WMI, que permite uma personalização fácil, mas eficiente, das máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="88881-117">Most of Hyper-V can be controlled by using the WMI provider, which allows easy, yet powerful customization of the virtual machines.</span></span> <span data-ttu-id="88881-118">Para obter mais informações sobre o que pode ser controlado com o provedor WMI, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="88881-118">For more information about what can be controlled with the WMI provider, see the following topics:</span></span>

-   [<span data-ttu-id="88881-119">Serviço de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="88881-119">Virtual system management service</span></span>](virtual-system-management-service.md)
-   [<span data-ttu-id="88881-120">Serviço de rede</span><span class="sxs-lookup"><span data-stu-id="88881-120">Networking service</span></span>](networking-service.md)
-   [<span data-ttu-id="88881-121">Serviço de gerenciamento de recursos</span><span class="sxs-lookup"><span data-stu-id="88881-121">Resource management service</span></span>](resource-management-service.md)
-   [<span data-ttu-id="88881-122">O que há de novo no provedor WMI do Hyper-V</span><span class="sxs-lookup"><span data-stu-id="88881-122">What's new in Hyper-V WMI provider</span></span>](what-s-new-in-hyper-v.md)

 

 



