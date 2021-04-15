---
description: O sistema usa as informações de configuração para determinar como iniciar o serviço.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Configuração de Serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501579"
---
# <a name="service-configuration"></a><span data-ttu-id="bf143-103">Configuração de Serviço</span><span class="sxs-lookup"><span data-stu-id="bf143-103">Service Configuration</span></span>

<span data-ttu-id="bf143-104">O sistema usa as informações de configuração para determinar como iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="bf143-104">The system uses the configuration information to determine how to start the service.</span></span> <span data-ttu-id="bf143-105">As informações de configuração também incluem o nome de exibição do serviço e sua descrição.</span><span class="sxs-lookup"><span data-stu-id="bf143-105">The configuration information also includes the service display name and its description.</span></span> <span data-ttu-id="bf143-106">Por exemplo, para o serviço DHCP, você pode usar o nome de exibição "serviço de protocolo de configuração de host dinâmico" e a descrição "fornece endereços de Internet para o computador em sua rede".</span><span class="sxs-lookup"><span data-stu-id="bf143-106">For example, for the DHCP service, you could use the display name "Dynamic Host Configuration Protocol Service" and the description "Provides internet addresses for computer on your network."</span></span>

<span data-ttu-id="bf143-107">Para modificar as informações de configuração de um objeto de serviço, um programa de configuração usa a função [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ou [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="bf143-107">To modify the configuration information for a service object, a configuration program uses the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function.</span></span> <span data-ttu-id="bf143-108">Para obter um exemplo, consulte [alterando uma configuração de serviço](changing-a-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="bf143-108">For an example, see [Changing a Service Configuration](changing-a-service-configuration.md).</span></span>

<span data-ttu-id="bf143-109">Para recuperar as informações de configuração de um objeto de serviço, o programa de configuração usa a função [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) ou [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="bf143-109">To retrieve the configuration information for a service object, the configuration program uses the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) or [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) function.</span></span> <span data-ttu-id="bf143-110">Para obter um exemplo, consulte [consultando a configuração de um serviço](querying-a-service-s-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="bf143-110">For an example, see [Querying a Service's Configuration](querying-a-service-s-configuration.md).</span></span>

<span data-ttu-id="bf143-111">As funções de configuração do serviço [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) dão suporte ao uso de gatilhos para controlar o início do serviço.</span><span class="sxs-lookup"><span data-stu-id="bf143-111">The [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) service configuration functions support the use of triggers to control service start.</span></span>

<span data-ttu-id="bf143-112">Para modificar o descritor de segurança para um objeto SCManager ou um objeto de serviço, um programa de configuração usa a função [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="bf143-112">To modify the security descriptor for either an SCManager object or a service object, a configuration program uses the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function.</span></span> <span data-ttu-id="bf143-113">Para recuperar uma cópia do descritor de segurança, o programa de configuração usa a função [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="bf143-113">To retrieve a copy of the security descriptor, the configuration program uses the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf143-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf143-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf143-115">Configurando um serviço usando SC</span><span class="sxs-lookup"><span data-stu-id="bf143-115">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
