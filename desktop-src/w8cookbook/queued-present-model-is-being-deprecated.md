---
title: O modelo presente na fila está sendo preterido
description: O modelo presente na fila está sendo preterido
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "105765617"
---
# <a name="queued-present-model-is-being-deprecated"></a><span data-ttu-id="87052-103">O modelo presente na fila está sendo preterido</span><span class="sxs-lookup"><span data-stu-id="87052-103">Queued present model is being deprecated</span></span>

## <a name="platforms"></a><span data-ttu-id="87052-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="87052-104">Platforms</span></span>

<span data-ttu-id="87052-105">**Clientes** – após o Windows 8</span><span class="sxs-lookup"><span data-stu-id="87052-105">**Clients** – After Windows 8</span></span>  
<span data-ttu-id="87052-106">**Servidores** – após o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="87052-106">**Servers** – After Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="87052-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="87052-107">Description</span></span>

<span data-ttu-id="87052-108">Na versão do Windows após o Windows 8, essas APIs retornarão E \_ NOTIMPL:</span><span class="sxs-lookup"><span data-stu-id="87052-108">In the Windows release after Windows 8, these APIs will return E\_NOTIMPL:</span></span>

-   <span data-ttu-id="87052-109">DwmSetPresentParameters</span><span class="sxs-lookup"><span data-stu-id="87052-109">DwmSetPresentParameters</span></span>
-   <span data-ttu-id="87052-110">DwmSetDxFrameDuration</span><span class="sxs-lookup"><span data-stu-id="87052-110">DwmSetDxFrameDuration</span></span>
-   <span data-ttu-id="87052-111">DwmModifyPreviousDxFrameDuration</span><span class="sxs-lookup"><span data-stu-id="87052-111">DwmModifyPreviousDxFrameDuration</span></span>

<span data-ttu-id="87052-112">Além disso, essa API só aceitará o valor nulo para o parâmetro hWnd:</span><span class="sxs-lookup"><span data-stu-id="87052-112">In addition, this API will only accept the NULL value for the hwnd parameter:</span></span>

-   <span data-ttu-id="87052-113">DwmGetCompositionTimingInfo</span><span class="sxs-lookup"><span data-stu-id="87052-113">DwmGetCompositionTimingInfo</span></span>

<span data-ttu-id="87052-114">Vamos parar de dar suporte a DwmGetCompositionTimingInfo com HWND! = NULL e remover a funcionalidade associada.</span><span class="sxs-lookup"><span data-stu-id="87052-114">We will stop supporting DwmGetCompositionTimingInfo with hwnd != NULL and remove associated functionality.</span></span> <span data-ttu-id="87052-115">Se um valor não nulo para HWND for especificado, essa API retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="87052-115">If non-NULL value for hwnd is specified, this API will return E\_INVALIDARG.</span></span>

<span data-ttu-id="87052-116">Também desencorajamos o uso da API DwmGetCompositionTimingInfo e sugerem que os desenvolvedores alternem para o modelo de flip-DXGI e a API de estatísticas do DX presente associado.</span><span class="sxs-lookup"><span data-stu-id="87052-116">We also discourage the use of DwmGetCompositionTimingInfo API and suggest that developers switch to the DXGI flip model and associated DX present statistics API.</span></span>

## <a name="manifestation"></a><span data-ttu-id="87052-117">Manifestação</span><span class="sxs-lookup"><span data-stu-id="87052-117">Manifestation</span></span>

<span data-ttu-id="87052-118">Os aplicativos que usam o modelo em fila no momento não funcionarão corretamente.</span><span class="sxs-lookup"><span data-stu-id="87052-118">Applications that use the queued present model will not function correctly.</span></span> <span data-ttu-id="87052-119">A manifestação exata depende do aplicativo específico, mas pode variar de tempo de apresentação incorreto para o aplicativo que está saindo inesperadamente).</span><span class="sxs-lookup"><span data-stu-id="87052-119">The exact manifestation depends on the particular application, but can range from incorrect presentation timing to the application exiting unexpectedly).</span></span> <span data-ttu-id="87052-120">Na prática, não esperamos ver muitos aplicativos (se houver) tais.</span><span class="sxs-lookup"><span data-stu-id="87052-120">In practice, we do not expect to see many (if any) such applications.</span></span> <span data-ttu-id="87052-121">Esse modelo foi usado pelo Media Player do vista, que não será usado no Windows 8 (e possivelmente no antigo Zune Player).</span><span class="sxs-lookup"><span data-stu-id="87052-121">This model was used by Vista media player, which will not be used on Windows 8 (and possibly the old Zune player).</span></span> <span data-ttu-id="87052-122">Neste momento, não temos informações sobre outros aplicativos que realmente usam esse modelo.</span><span class="sxs-lookup"><span data-stu-id="87052-122">At this time we don’t have info about any other applications actually using this model.</span></span>

## <a name="solution"></a><span data-ttu-id="87052-123">Solução</span><span class="sxs-lookup"><span data-stu-id="87052-123">Solution</span></span>

<span data-ttu-id="87052-124">Os desenvolvedores precisam usar o modo de apresentação de flip-DXGI em vez de estar na fila presente (disponível no tempo de execução do DX9 desde o Windows 7 e em tempos de execução DX10 e DX11 no Windows 8).</span><span class="sxs-lookup"><span data-stu-id="87052-124">Developers need to use the DXGI flip presentation mode instead of queued present (available in DX9 runtime since Windows 7, and on DX10 and DX11 runtimes in Windows 8).</span></span>

## <a name="tests"></a><span data-ttu-id="87052-125">Testes</span><span class="sxs-lookup"><span data-stu-id="87052-125">Tests</span></span>

<span data-ttu-id="87052-126">Execute testes gerais para garantir que os componentes do Windows da caixa de entrada e os principais produtos continuem a funcionar na próxima versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="87052-126">Run general tests to ensure that inbox Windows components and major products continue to work on the next version of Windows.</span></span>

 

 




