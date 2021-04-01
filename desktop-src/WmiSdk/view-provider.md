---
description: O provedor View é uma instância e um provedor de métodos que cria novas classes com base em instâncias de outras classes.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Exibir provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829261"
---
# <a name="view-provider"></a><span data-ttu-id="e5192-103">Exibir provedor</span><span class="sxs-lookup"><span data-stu-id="e5192-103">View Provider</span></span>

<span data-ttu-id="e5192-104">O provedor View é uma instância e um provedor de métodos que cria novas classes com base em instâncias de outras classes.</span><span class="sxs-lookup"><span data-stu-id="e5192-104">The View provider is an instance and method provider that creates new classes based on instances of other classes.</span></span> <span data-ttu-id="e5192-105">Você pode usar o provedor de exibição para obter propriedades de diferentes classes de origem, namespaces diferentes ou computadores diferentes e combinar as propriedades como uma única classe.</span><span class="sxs-lookup"><span data-stu-id="e5192-105">You can use the View provider to take properties from different source classes, different namespaces, or different computers and combine the properties as a single class.</span></span>

<span data-ttu-id="e5192-106">Como um provedor de método e instância, o provedor de exibição oferece suporte à interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) padrão e aos seguintes métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) :</span><span class="sxs-lookup"><span data-stu-id="e5192-106">As an instance and method provider, the View provider supports the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface and the following [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="e5192-107">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="e5192-107">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="e5192-108">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="e5192-108">**ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="e5192-109">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="e5192-109">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="e5192-110">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="e5192-110">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="e5192-111">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="e5192-111">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="e5192-112">Para obter mais informações sobre os qualificadores usados para definir as classes do provedor de exibição, consulte [qualificadores específicos para o provedor de exibição](qualifiers-specific-to-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e5192-112">For more information about the qualifiers use to define View provider classes, see [Qualifiers Specific to the View Provider](qualifiers-specific-to-the-view-provider.md).</span></span>

<span data-ttu-id="e5192-113">Para obter mais informações sobre exibições, consulte [vincular classes juntas](linking-classes-together.md).</span><span class="sxs-lookup"><span data-stu-id="e5192-113">For more information about views, see [Linking Classes Together](linking-classes-together.md).</span></span>

<span data-ttu-id="e5192-114">Duas versões do provedor de exibição estão disponíveis em plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e5192-114">Two versions of the View provider are available on 64-bit platforms.</span></span> <span data-ttu-id="e5192-115">Para obter mais informações, consulte [obter e fornecer dados em um computador de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).</span><span class="sxs-lookup"><span data-stu-id="e5192-115">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="e5192-116">O provedor de exibição é implementado no ViewProv.dll.</span><span class="sxs-lookup"><span data-stu-id="e5192-116">The View provider is implemented in ViewProv.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5192-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5192-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5192-118">Provedores de WMI</span><span class="sxs-lookup"><span data-stu-id="e5192-118">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



