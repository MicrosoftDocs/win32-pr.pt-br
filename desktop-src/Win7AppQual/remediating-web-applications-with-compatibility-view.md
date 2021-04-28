---
description: Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116354"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a><span data-ttu-id="0a149-103">Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="0a149-103">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>

<span data-ttu-id="0a149-104">Esta seção descreve as etapas básicas de mitigação e como planejar a compatibilidade de aplicativos futuramente enquanto você está abordando quaisquer problemas agora.</span><span class="sxs-lookup"><span data-stu-id="0a149-104">This section describes basic mitigation steps and how to plan for future application compatibility while you are addressing any issues now.</span></span>

<span data-ttu-id="0a149-105">O Windows Internet Explorer dá suporte aos modelos herdados do Internet Explorer sempre que possível para que os sites que você desenvolve para eles continuem a se comportarem conforme o esperado nas versões mais recentes do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0a149-105">Windows Internet Explorer supports the legacy Internet Explorer models whenever feasible so that sites that you develop to them continue to behave as expected in newer versions of Internet Explorer.</span></span> <span data-ttu-id="0a149-106">A partir do Windows Internet Explorer 8, você pode optar por oferecer suporte a comportamentos herdados selecionando o modo de renderização página por página.</span><span class="sxs-lookup"><span data-stu-id="0a149-106">Starting with Windows Internet Explorer 8, you can choose to support legacy behaviors by selecting the rendering mode on a page-by-page basis.</span></span>

<span data-ttu-id="0a149-107">O Internet Explorer 8 inclui os seguintes modos de renderização que podem ser definidos usando o cabeçalho X-UA-Compatible.</span><span class="sxs-lookup"><span data-stu-id="0a149-107">Internet Explorer 8 includes the following rendering modes that you can set by using the X-UA-Compatible header.</span></span>



| <span data-ttu-id="0a149-108">Valor do conteúdo</span><span class="sxs-lookup"><span data-stu-id="0a149-108">Content value</span></span> | <span data-ttu-id="0a149-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a149-109">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a149-110">IE=5</span><span class="sxs-lookup"><span data-stu-id="0a149-110">IE=5</span></span>          | <span data-ttu-id="0a149-111">Use o modo peculiaridades.</span><span class="sxs-lookup"><span data-stu-id="0a149-111">Use quirks mode.</span></span>                                                                      |
| <span data-ttu-id="0a149-112">IE = 7</span><span class="sxs-lookup"><span data-stu-id="0a149-112">IE=7</span></span>          | <span data-ttu-id="0a149-113">Sempre use o modo do Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="0a149-113">Always use Windows Internet Explorer 7 mode.</span></span>                                          |
| <span data-ttu-id="0a149-114">IE=EmulateIE7</span><span class="sxs-lookup"><span data-stu-id="0a149-114">IE=EmulateIE7</span></span> | <span data-ttu-id="0a149-115">Exibir no modo do Internet Explorer 7, a menos que o site tenha o DOCTYPE de inpeculiars.</span><span class="sxs-lookup"><span data-stu-id="0a149-115">Display in Internet Explorer 7 mode unless the site has the quirks DOCTYPE.</span></span>           |
| <span data-ttu-id="0a149-116">IE = 8</span><span class="sxs-lookup"><span data-stu-id="0a149-116">IE=8</span></span>          | <span data-ttu-id="0a149-117">Sempre use o modo do Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="0a149-117">Always use Internet Explorer 8 mode.</span></span>                                                  |
| <span data-ttu-id="0a149-118">IE=EmulateIE8</span><span class="sxs-lookup"><span data-stu-id="0a149-118">IE=EmulateIE8</span></span> | <span data-ttu-id="0a149-119">Substitua a exibição de compatibilidade em computadores cliente e use o modo do Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="0a149-119">Override Compatibility View on client machines and use Internet Explorer 8 mode.</span></span>      |
| <span data-ttu-id="0a149-120">IE=Edge</span><span class="sxs-lookup"><span data-stu-id="0a149-120">IE=Edge</span></span>       | <span data-ttu-id="0a149-121">Exibir no modo mais recente.</span><span class="sxs-lookup"><span data-stu-id="0a149-121">Display in the latest mode.</span></span> <span data-ttu-id="0a149-122">No Internet Explorer 8, esse valor é equivalente ao IE = 8.</span><span class="sxs-lookup"><span data-stu-id="0a149-122">In Internet Explorer 8, this value is equivalent to IE=8.</span></span> |



 

<span data-ttu-id="0a149-123">Os tópicos a seguir descrevem como atualizar aplicativos Web usando o modo de exibição de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="0a149-123">The following topics describe how to update web applications by using Compatibility View.</span></span>



| <span data-ttu-id="0a149-124">Tópico</span><span class="sxs-lookup"><span data-stu-id="0a149-124">Topic</span></span>                                                                                                  | <span data-ttu-id="0a149-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a149-125">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="0a149-126">O que é o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="0a149-126">What Is Compatibility View</span></span>](what-is-compatibility-view-.md)                                          | <span data-ttu-id="0a149-127">Descreve o modo de exibição de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="0a149-127">Describes Compatibility View.</span></span>                                                  |
| [<span data-ttu-id="0a149-128">Por que você precisa do modo de exibição de compatibilidade?</span><span class="sxs-lookup"><span data-stu-id="0a149-128">Why Do You Need Compatibility View?</span></span>](why-do-you-need-compatibility-view-.md)                         | <span data-ttu-id="0a149-129">Descreve por que você deve usar o modo de exibição de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="0a149-129">Describes why you should use Compatibility View.</span></span>                               |
| [<span data-ttu-id="0a149-130">Use a marca meta para garantir a compatibilidade futura</span><span class="sxs-lookup"><span data-stu-id="0a149-130">Use the Meta Tag to Ensure Future Compatibility</span></span>](use-the-meta-tag-to-ensure-future-compatibility.md) | <span data-ttu-id="0a149-131">Descreve como você pode usar o elemento **meta** para garantir a compatibilidade futura.</span><span class="sxs-lookup"><span data-stu-id="0a149-131">Describes how you can use the **meta** element to ensure future compatibility.</span></span> |



 

 

 



