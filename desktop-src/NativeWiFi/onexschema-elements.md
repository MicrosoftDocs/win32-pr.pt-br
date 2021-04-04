---
description: Um perfil 802.1 X contém os seguintes elementos de esquema.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Elementos de esquema OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662141"
---
# <a name="onex-schema-elements"></a><span data-ttu-id="fd51b-103">Elementos de esquema OneX</span><span class="sxs-lookup"><span data-stu-id="fd51b-103">OneX Schema Elements</span></span>

<span data-ttu-id="fd51b-104">Um perfil 802.1 X contém os seguintes elementos de esquema.</span><span class="sxs-lookup"><span data-stu-id="fd51b-104">An 802.1X profile contains the following schema elements.</span></span> <span data-ttu-id="fd51b-105">Todos os elementos de esquema de OneX se aplicam a perfis com e sem fio.</span><span class="sxs-lookup"><span data-stu-id="fd51b-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="fd51b-106">A maioria dos elementos nomeados está no namespace `https://www.microsoft.com/networking/OneX/v1` , com exceção de [**EAPConfig (Onex)**](onexschema-eapconfig-onex-element.md) , que está no namespace `https://www.microsoft.com/provisioning/EapHostConfig` .</span><span class="sxs-lookup"><span data-stu-id="fd51b-106">Most of the named elements are in the namespace `https://www.microsoft.com/networking/OneX/v1`, except for [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md) which is in the namespace `https://www.microsoft.com/provisioning/EapHostConfig`.</span></span>

<span data-ttu-id="fd51b-107">A lista a seguir mostra os elementos definidos na ordem em que os elementos aparecem em um perfil.</span><span class="sxs-lookup"><span data-stu-id="fd51b-107">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="fd51b-108">A ordem dos elementos é imposta.</span><span class="sxs-lookup"><span data-stu-id="fd51b-108">The ordering of elements is enforced.</span></span> <span data-ttu-id="fd51b-109">Nem todos os elementos estão em todos os perfis, pois alguns elementos são opcionais.</span><span class="sxs-lookup"><span data-stu-id="fd51b-109">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="fd51b-110">Essa lista não mostra todos os elementos possíveis que podem aparecer em um perfil, pois elementos podem ser adicionados em **xs: qualquer** ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="fd51b-110">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="fd51b-111">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="fd51b-111">**OneX**</span></span>](onexschema-onex-element.md)
    -   [<span data-ttu-id="fd51b-112">**cacheUserData (OneX)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-112">**cacheUserData (OneX)**</span></span>](onexschema-cacheuserdata-onex-element.md)
    -   [<span data-ttu-id="fd51b-113">**heldPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-113">**heldPeriod (OneX)**</span></span>](onexschema-heldperiod-onex-element.md)
    -   [<span data-ttu-id="fd51b-114">**authPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-114">**authPeriod (OneX)**</span></span>](onexschema-authperiod-onex-element.md)
    -   [<span data-ttu-id="fd51b-115">**startPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-115">**startPeriod (OneX)**</span></span>](onexschema-startperiod-onex-element.md)
    -   [<span data-ttu-id="fd51b-116">**maxStart (OneX)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-116">**maxStart (OneX)**</span></span>](onexschema-maxstart-onex-element.md)
    -   [<span data-ttu-id="fd51b-117">**maxAuthFailures (OneX)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-117">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
    -   [<span data-ttu-id="fd51b-118">**suplicante (OneX)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-118">**supplicantMode (OneX)**</span></span>](onexschema-supplicantmode-onex-element.md)
    -   [<span data-ttu-id="fd51b-119">**AuthMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-119">**authMode (OneX)**</span></span>](onexschema-authmode-onex-element.md)
    -   [<span data-ttu-id="fd51b-120">**Logon único (OneX)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
        -   [<span data-ttu-id="fd51b-121">**tipo (logon único)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-121">**type (singleSignOn)**</span></span>](onexschema-type-singlesignon-element.md)
        -   [<span data-ttu-id="fd51b-122">**maxDelay (logon único)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-122">**maxDelay (singleSignOn)**</span></span>](onexschema-maxdelay-singlesignon-element.md)
        -   [<span data-ttu-id="fd51b-123">**userBasedVirtualLan (logon único)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-123">**userBasedVirtualLan (singleSignOn)**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [<span data-ttu-id="fd51b-124">**EAPConfig (OneX)**</span><span class="sxs-lookup"><span data-stu-id="fd51b-124">**EAPConfig (OneX)**</span></span>](onexschema-eapconfig-onex-element.md)

 

 



