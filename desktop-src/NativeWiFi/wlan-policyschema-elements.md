---
description: Um perfil de política de WLAN (rede local sem fio) nativo do wifi é composto pelos seguintes elementos de esquema.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: Elementos do esquema de WLAN_policy
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501559"
---
# <a name="wlan_policy-schema-elements"></a><span data-ttu-id="9cd08-103">Elementos do esquema de política de WLAN \_</span><span class="sxs-lookup"><span data-stu-id="9cd08-103">WLAN\_policy Schema Elements</span></span>

<span data-ttu-id="9cd08-104">Um perfil de política de WLAN (rede local sem fio) nativo do wifi é composto pelos seguintes elementos de esquema.</span><span class="sxs-lookup"><span data-stu-id="9cd08-104">A Native Wifi wireless LAN (WLAN) policy profile is composed of the following schema elements.</span></span> <span data-ttu-id="9cd08-105">Todos os elementos nomeados estão no namespace `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="9cd08-105">All of the named elements are in the namespace `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

<span data-ttu-id="9cd08-106">A lista a seguir mostra os elementos definidos na ordem em que os elementos aparecem em um perfil.</span><span class="sxs-lookup"><span data-stu-id="9cd08-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="9cd08-107">A ordem dos elementos é imposta.</span><span class="sxs-lookup"><span data-stu-id="9cd08-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="9cd08-108">Nem todos os elementos estão em todos os perfis, pois alguns elementos são opcionais.</span><span class="sxs-lookup"><span data-stu-id="9cd08-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="9cd08-109">Essa lista não mostra todos os elementos possíveis que podem aparecer em um perfil, pois elementos podem ser adicionados em **xs: qualquer** ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="9cd08-109">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="9cd08-110">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="9cd08-110">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
    -   [<span data-ttu-id="9cd08-111">**nome (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-111">**name (WLANPolicy)**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)
    -   [<span data-ttu-id="9cd08-112">**Descrição (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-112">**description (WLANPolicy)**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)
    -   [<span data-ttu-id="9cd08-113">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-113">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [<span data-ttu-id="9cd08-114">**enableAutoConfig (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-114">**enableAutoConfig (globalFlags)**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [<span data-ttu-id="9cd08-115">**showDeniedNetwork (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-115">**showDeniedNetwork (globalFlags)**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [<span data-ttu-id="9cd08-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [<span data-ttu-id="9cd08-117">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-117">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [<span data-ttu-id="9cd08-118">**permitirlist (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [<span data-ttu-id="9cd08-119">**rede (permitirlist)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-119">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
                -   [<span data-ttu-id="9cd08-120">**NetworkName (networkitemtype)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-120">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="9cd08-121">**NetworkType (networkitemtype)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-121">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="9cd08-122">**Blocklist (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-122">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [<span data-ttu-id="9cd08-123">**rede (bloquearlist)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-123">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
                -   [<span data-ttu-id="9cd08-124">**NetworkName (networkitemtype)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-124">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="9cd08-125">**NetworkType (networkitemtype)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-125">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="9cd08-126">**denyAllIBSS (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-126">**denyAllIBSS (networkFilter)**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [<span data-ttu-id="9cd08-127">**denyAllESS (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-127">**denyAllESS (networkFilter)**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [<span data-ttu-id="9cd08-128">**ProfileList (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="9cd08-128">**profileList (WLANPolicy)**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



