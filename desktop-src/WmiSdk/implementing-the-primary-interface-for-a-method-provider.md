---
description: 'Um provedor de métodos deve implementar IWbemServices como a interface primária. No entanto, um provedor de método puro requer apenas que você implemente o método IWbemServices:: ExecMethodAsync.'
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementando a interface primária para um provedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196f87a6520d92bf18362be88f8cc40e5133dabe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764458"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a><span data-ttu-id="86830-104">Implementando a interface primária para um provedor de métodos</span><span class="sxs-lookup"><span data-stu-id="86830-104">Implementing the Primary Interface for a Method Provider</span></span>

<span data-ttu-id="86830-105">Um provedor de métodos deve implementar [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como a interface primária.</span><span class="sxs-lookup"><span data-stu-id="86830-105">A method provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="86830-106">No entanto, um provedor de método puro requer apenas que você implemente o método [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .</span><span class="sxs-lookup"><span data-stu-id="86830-106">However, a pure method provider requires only that you implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method.</span></span>

<span data-ttu-id="86830-107">Como outros provedores usam [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), a interface contém muitos métodos que são irrelevantes para um provedor de método puro.</span><span class="sxs-lookup"><span data-stu-id="86830-107">Because other providers use [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), the interface contains many methods that are irrelevant to a pure method provider.</span></span> <span data-ttu-id="86830-108">Seu provedor de método puro deve fornecer uma implementação de stub que retorne o \_ provedor WBEM E \_ \_ não \_ compatível com todos os outros métodos de **IWbemServices** além de [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span><span class="sxs-lookup"><span data-stu-id="86830-108">Your pure method provider should supply a stub implementation that returns WBEM\_E\_PROVIDER\_NOT\_CAPABLE for all of other **IWbemServices** methods besides [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span> <span data-ttu-id="86830-109">No entanto, muitos provedores de método também servem como provedores de instância ou classe.</span><span class="sxs-lookup"><span data-stu-id="86830-109">However, many method providers also serve as instance or class providers.</span></span> <span data-ttu-id="86830-110">Os provedores de método e instância de combinação devem dar suporte a mais dos métodos de **IWbemServices** .</span><span class="sxs-lookup"><span data-stu-id="86830-110">Combination method and instance providers must support more of the **IWbemServices** methods.</span></span>

 

 



