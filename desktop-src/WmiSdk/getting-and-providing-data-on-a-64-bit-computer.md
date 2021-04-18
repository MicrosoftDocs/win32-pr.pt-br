---
description: Os aplicativos cliente e scripts que acessam provedores de 32 bits WMI padrão continuam a operar normalmente quando executados em um sistema operacional de 64 bits.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Obter e fornecer dados em um computador de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564093"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a><span data-ttu-id="82dd8-103">Obter e fornecer dados em um computador de 64 bits</span><span class="sxs-lookup"><span data-stu-id="82dd8-103">Getting and Providing Data on a 64-bit Computer</span></span>

<span data-ttu-id="82dd8-104">Os aplicativos cliente e scripts que acessam provedores de 32 bits WMI padrão continuam a operar normalmente quando executados em um sistema operacional de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="82dd8-104">Client applications and scripts that access standard WMI 32-bit providers continue to operate normally when running on a 64-bit operating system.</span></span> <span data-ttu-id="82dd8-105">Somente dois provedores pré-instalados, o provedor de [registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) e o [provedor de exibição](view-provider.md)têm versões de 64 bits que são executadas lado a lado com as versões de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="82dd8-105">Only two preinstalled providers, the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) and the [View provider](view-provider.md), have 64-bit versions which run side-by-side with the 32-bit versions.</span></span> <span data-ttu-id="82dd8-106">No entanto, um aplicativo de 32 bits que solicita instâncias de Windows Driver Model de 32 bits (WDM) recebe as instâncias de classe WDM de 64 bits padrão em um sistema operacional de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="82dd8-106">However, a 32-bit application that requests 32-bit Windows Driver Model (WDM) instances receives the default 64-bit WDM class instances on a 64-bit operating system.</span></span>

## <a name="accessing-default-and-nondefault-provider-data"></a><span data-ttu-id="82dd8-107">Acessando dados de provedor padrão e não padrão</span><span class="sxs-lookup"><span data-stu-id="82dd8-107">Accessing Default and Nondefault Provider Data</span></span>

<span data-ttu-id="82dd8-108">Em geral, os gravadores de provedor não incluem versões de 32 bits e 64 bits de um provedor no mesmo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="82dd8-108">Generally, provider writers do not include both 32-bit and 64-bit versions of a provider in the same operating system.</span></span> <span data-ttu-id="82dd8-109">Se nenhum provedor de 64 bits existir, um provedor de 32 bits poderá continuar executando os recursos do WOW64.</span><span class="sxs-lookup"><span data-stu-id="82dd8-109">If no 64-bit provider exists, a 32-bit provider can continue to run through the facilities of WOW64.</span></span> <span data-ttu-id="82dd8-110">O provedor de 64 bits pode, da mesma forma, fornecer dados para um aplicativo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="82dd8-110">A 64-bit provider can likewise supply data to a 32-bit application.</span></span> <span data-ttu-id="82dd8-111">Para obter mais informações, consulte [fornecendo dados do WMI em uma plataforma de 64 bits](providing-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="82dd8-111">For more information, see [Providing WMI Data on a 64-bit Platform](providing-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="82dd8-112">Se existirem duas versões, os aplicativos e scripts cliente poderão usar os parâmetros de contexto disponíveis na [API com](com-api-for-wmi.md) e a [API de script](scripting-api-for-wmi.md) para se conectar explicitamente a um provedor WMI não padrão específico, se estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="82dd8-112">If two versions exist, client applications and scripts can use the context parameters available in the [COM API](com-api-for-wmi.md) and the [Scripting API](scripting-api-for-wmi.md) to connect explicitly to a specific nondefault WMI provider, if it is available.</span></span> <span data-ttu-id="82dd8-113">Para obter mais informações, consulte [solicitando dados WMI em uma plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="82dd8-113">For more information, see [Requesting WMI Data on a 64-bit Platform](requesting-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="82dd8-114">O diagrama a seguir mostra as conexões padrão e não padrão, usando o registro como um exemplo para o qual dois provedores podem existir lado a lado em uma plataforma de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="82dd8-114">The following diagram shows the default and nondefault connections, using the registry as an example for which two providers can exist side-by-side on a 64-bit platform.</span></span>

![conexões padrão e não padrão em uma plataforma de 64 bits](images/32-64bit-registry.png)

## <a name="related-topics"></a><span data-ttu-id="82dd8-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82dd8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82dd8-117">Solicitando dados WMI em uma plataforma de 64 bits</span><span class="sxs-lookup"><span data-stu-id="82dd8-117">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="82dd8-118">Fornecendo dados do WMI em uma plataforma de 64 bits</span><span class="sxs-lookup"><span data-stu-id="82dd8-118">Providing WMI Data on a 64-bit Platform</span></span>](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
