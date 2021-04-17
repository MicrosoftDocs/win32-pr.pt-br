---
title: Alterações no suporte de hardware herdado DX9
description: Alterações no suporte de hardware herdado DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105813447"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a><span data-ttu-id="09dec-103">Alterações no suporte de hardware herdado DX9</span><span class="sxs-lookup"><span data-stu-id="09dec-103">Changes in DX9 legacy hardware support</span></span>

## <a name="platform"></a><span data-ttu-id="09dec-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="09dec-104">Platform</span></span>

<span data-ttu-id="09dec-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="09dec-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="09dec-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="09dec-106">Description</span></span>

<span data-ttu-id="09dec-107">A Intel e a AMD/ATI não suportam mais suas partes gráficas DX9 e não estarão Atualizando Drivers para esses dispositivos para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="09dec-107">Intel and AMD/ATI no longer support their DX9 graphics parts and will not be updating drivers for these devices for Windows 8.</span></span> <span data-ttu-id="09dec-108">Além disso, esses dispositivos não são abordados na caixa para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="09dec-108">Furthermore, these devices are not covered in-box for Windows 8.</span></span> <span data-ttu-id="09dec-109">Os últimos drivers para esses dispositivos estão disponíveis no WU e nos sites do OEM/IHV; muitas datas do vista e muitos desses drivers de versão final apresentam problemas no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="09dec-109">The last drivers for these devices are those available on WU and on the OEM/IHV’s websites; many date from Vista, and many of these final version drivers exhibit problems on Windows 8.</span></span> <span data-ttu-id="09dec-110">Além disso, o nVidia afirmou recentemente que eles não oferecerão suporte às suas peças de DX9 (vista e mais antigas) móveis (Notebook) para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="09dec-110">In addition, nVidia has recently stated that they will not support their DX9 (Vista and older) mobile (notebook) parts for Windows 8.</span></span> <span data-ttu-id="09dec-111">Eles continuam a dar suporte às suas partes de desktop DX9.</span><span class="sxs-lookup"><span data-stu-id="09dec-111">They continue to support their desktop DX9 parts.</span></span>

<span data-ttu-id="09dec-112">Todas essas combinações de driver/parte estão na lista de fallback de software do Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="09dec-112">All of these driver/part combinations are on the Internet Explorer 9 software fallback list.</span></span> <span data-ttu-id="09dec-113">Isso significa que, para fins de desempenho ou estabilidade, o Internet Explorer 9 usa a renderização de software nesses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="09dec-113">This means that for either performance or stability reasons, Internet Explorer 9 uses software rendering on these devices.</span></span> <span data-ttu-id="09dec-114">Essa é uma boa indicação de que a experiência com aplicativos da Windows Store não será satisfatória nesses drivers e partes.</span><span class="sxs-lookup"><span data-stu-id="09dec-114">This is a good indication that the experience with Windows Store apps will not be satisfactory on these drivers and parts.</span></span>

## <a name="manifestation"></a><span data-ttu-id="09dec-115">Manifestação</span><span class="sxs-lookup"><span data-stu-id="09dec-115">Manifestation</span></span>

<span data-ttu-id="09dec-116">Como não há nenhum suporte na caixa para esses dispositivos, muitos usuários com essas partes serão executados no driver de vídeo básico da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09dec-116">As there is no in-box support for these devices, many users with these parts will wind up running on the Microsoft Basic Display Driver.</span></span> <span data-ttu-id="09dec-117">Trata-se de uma GPU de software WDDM 1,2 baseada em distorção e é, na verdade, mais rápida do que algumas das partes desta classe, por exemplo, a série GMA500 da Intel.</span><span class="sxs-lookup"><span data-stu-id="09dec-117">This is a WARP-based WDDM 1.2 software GPU, and is actually faster than some of the parts in this class, for example, the Intel GMA500 series).</span></span> <span data-ttu-id="09dec-118">Ele dá suporte ao Aero-Glass e ao DWM e pode executar aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="09dec-118">It supports aero-glass and DWM, and can run Windows Store apps.</span></span>

<span data-ttu-id="09dec-119">No entanto, ele tem algumas limitações importantes:</span><span class="sxs-lookup"><span data-stu-id="09dec-119">However, it has some important limitations:</span></span>

-   <span data-ttu-id="09dec-120">Ele não dá suporte a vários monitores ou projeção</span><span class="sxs-lookup"><span data-stu-id="09dec-120">It doesn’t support multiple monitors or projection</span></span>
-   <span data-ttu-id="09dec-121">Ele não dá suporte à suspensão, embora ofereça suporte à hibernação</span><span class="sxs-lookup"><span data-stu-id="09dec-121">It doesn’t support sleep, though it does support hibernation</span></span>
-   <span data-ttu-id="09dec-122">Geralmente, não permitirá a alteração da resolução da tela</span><span class="sxs-lookup"><span data-stu-id="09dec-122">It often will not allow changing screen resolution</span></span>

## <a name="mitigation"></a><span data-ttu-id="09dec-123">Atenuação</span><span class="sxs-lookup"><span data-stu-id="09dec-123">Mitigation</span></span>

<span data-ttu-id="09dec-124">Se, após o teste, você descobrir que a experiência do usuário não é aceitável, poderá optar por definir os requisitos de hardware para seus produtos que excluem essas partes mais antigas do DX9 Intel e AMD.</span><span class="sxs-lookup"><span data-stu-id="09dec-124">If after testing, you find that the user experience is not acceptable, you may choose to set hardware requirements for their products that exclude these older DX9 Intel and AMD parts.</span></span> <span data-ttu-id="09dec-125">Você também pode optar por alertar seus clientes de que eles podem ter uma experiência inaceitável nessas partes.</span><span class="sxs-lookup"><span data-stu-id="09dec-125">You may also choose to alert your customers that they may have an unacceptable experience on these parts.</span></span>

## <a name="tests"></a><span data-ttu-id="09dec-126">Testes</span><span class="sxs-lookup"><span data-stu-id="09dec-126">Tests</span></span>

<span data-ttu-id="09dec-127">Avalie o desempenho e a experiência nesses dispositivos:</span><span class="sxs-lookup"><span data-stu-id="09dec-127">Evaluate the performance and experience on these devices:</span></span>

-   <span data-ttu-id="09dec-128">Qual é a experiência como na versão final do driver disponível?</span><span class="sxs-lookup"><span data-stu-id="09dec-128">What is the experience like on the final driver version available?</span></span>
-   <span data-ttu-id="09dec-129">Qual é a experiência como no MSBDD?</span><span class="sxs-lookup"><span data-stu-id="09dec-129">What is the experience like on the MSBDD?</span></span>

 

 




