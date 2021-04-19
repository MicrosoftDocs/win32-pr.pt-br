---
description: A classe de provedores de MSFT \_ e as classes de solução de problemas de WMI são um grupo de classes de evento MSFT que são associadas a eventos de provedor WMI.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Configuração do provedor e classes de solução de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793694"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a><span data-ttu-id="32d46-103">Configuração do provedor e classes de solução de problemas</span><span class="sxs-lookup"><span data-stu-id="32d46-103">Provider Configuration and Troubleshooting Classes</span></span>

<span data-ttu-id="32d46-104">A classe de [**\_ provedores de MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) e as classes de solução de problemas de WMI são um grupo de [classes de evento MSFT](msft-classes.md) que são associadas a eventos de provedor WMI.</span><span class="sxs-lookup"><span data-stu-id="32d46-104">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class and the WMI troubleshooting classes are a group of the [MSFT event classes](msft-classes.md) coupled to WMI provider events.</span></span>

<span data-ttu-id="32d46-105">A classe de [**\_ provedores de MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) contém informações de configuração para provedores e inclui os seguintes métodos que permitem carregar e descarregar provedores, ou suspender e retomar operações do provedor:</span><span class="sxs-lookup"><span data-stu-id="32d46-105">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class contains configuration information for providers and includes the following methods that allow you to load and unload providers, or suspend and resume provider operations:</span></span>

-   [<span data-ttu-id="32d46-106">**Método Load da classe de \_ provedores MSFT**</span><span class="sxs-lookup"><span data-stu-id="32d46-106">**Load Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [<span data-ttu-id="32d46-107">**Método UnLoad da classe de \_ provedores MSFT**</span><span class="sxs-lookup"><span data-stu-id="32d46-107">**UnLoad Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [<span data-ttu-id="32d46-108">**Método resume da classe de \_ provedores MSFT**</span><span class="sxs-lookup"><span data-stu-id="32d46-108">**Resume Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [<span data-ttu-id="32d46-109">**Método Suspend da classe de \_ provedores MSFT**</span><span class="sxs-lookup"><span data-stu-id="32d46-109">**Suspend Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

<span data-ttu-id="32d46-110">As [classes de solução de problemas do WMI](wmi-troubleshooting-classes.md) são nomeadas para indicar se o evento é acionado antes ou depois de um evento de provedor.</span><span class="sxs-lookup"><span data-stu-id="32d46-110">The [WMI troubleshooting classes](wmi-troubleshooting-classes.md) are named to indicate whether the event is fired before or after a provider event.</span></span> <span data-ttu-id="32d46-111">Por exemplo, o objeto [**MSFT \_ WmiProvider \_ AccessCheck \_ pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) é gerado imediatamente antes de chamar a implementação do provedor de **IWbemEventSecurity:: AccessCheck**, enquanto o objeto de [**\_ \_ \_ postagem WmiProvider AccessCheck do MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) é chamado imediatamente após.</span><span class="sxs-lookup"><span data-stu-id="32d46-111">For example, the [**MSFT\_WmiProvider\_AccessCheck\_Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) object is generated immediately before calling the provider's implementation of **IWbemEventSecurity::AccessCheck**, while the [**MSFT\_WmiProvider\_AccessCheck\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) object is called immediately after.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32d46-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32d46-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32d46-113">Solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="32d46-113">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="32d46-114">Classes de solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="32d46-114">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
