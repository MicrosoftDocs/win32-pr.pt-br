---
title: Interface IMsRdpInputSink
description: Coletor de entrada da área de trabalho remota.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpInputSink
- Serviços de Área de Trabalho Remota da interface IMsRdpInputSink, descrita
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918197"
---
# <a name="imsrdpinputsink-interface"></a><span data-ttu-id="31c75-105">Interface IMsRdpInputSink</span><span class="sxs-lookup"><span data-stu-id="31c75-105">IMsRdpInputSink interface</span></span>

<span data-ttu-id="31c75-106">Coletor de entrada da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="31c75-106">Remote desktop input sink.</span></span>

## <a name="members"></a><span data-ttu-id="31c75-107">Membros</span><span class="sxs-lookup"><span data-stu-id="31c75-107">Members</span></span>

<span data-ttu-id="31c75-108">A interface **IMsRdpInputSink** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="31c75-108">The **IMsRdpInputSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="31c75-109">**IMsRdpInputSink** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="31c75-109">**IMsRdpInputSink** also has these types of members:</span></span>

-   [<span data-ttu-id="31c75-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="31c75-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="31c75-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="31c75-111">Methods</span></span>

<span data-ttu-id="31c75-112">A interface **IMsRdpInputSink** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="31c75-112">The **IMsRdpInputSink** interface has these methods.</span></span>



| <span data-ttu-id="31c75-113">Método</span><span class="sxs-lookup"><span data-stu-id="31c75-113">Method</span></span>                                                               | <span data-ttu-id="31c75-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="31c75-114">Description</span></span>                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| <span data-ttu-id="31c75-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31c75-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span></span>               | <span data-ttu-id="31c75-116">Adiciona entrada por toque.</span><span class="sxs-lookup"><span data-stu-id="31c75-116">Adds touch input.</span></span><br/>         |
| <span data-ttu-id="31c75-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31c75-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span></span>           | <span data-ttu-id="31c75-118">Iniciar o quadro de toque.</span><span class="sxs-lookup"><span data-stu-id="31c75-118">Begin touch frame.</span></span><br/>        |
| <span data-ttu-id="31c75-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31c75-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span></span>               | <span data-ttu-id="31c75-120">Encerrar quadro de toque.</span><span class="sxs-lookup"><span data-stu-id="31c75-120">End touch frame.</span></span><br/>          |
| <span data-ttu-id="31c75-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31c75-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span></span>       | <span data-ttu-id="31c75-122">Envia o evento de teclado.</span><span class="sxs-lookup"><span data-stu-id="31c75-122">Sends keyboard event.</span></span><br/>     |
| <span data-ttu-id="31c75-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31c75-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span></span> | <span data-ttu-id="31c75-124">Envia o evento de botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="31c75-124">Sends mouse button event.</span></span><br/> |
| <span data-ttu-id="31c75-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31c75-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span></span>     | <span data-ttu-id="31c75-126">Envia o evento de movimentação do mouse.</span><span class="sxs-lookup"><span data-stu-id="31c75-126">Sends mouse move event.</span></span><br/>   |
| <span data-ttu-id="31c75-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31c75-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span></span>   | <span data-ttu-id="31c75-128">Envia o evento de roda do mouse.</span><span class="sxs-lookup"><span data-stu-id="31c75-128">Sends mouse wheel event.</span></span><br/>  |
| <span data-ttu-id="31c75-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31c75-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span></span>               | <span data-ttu-id="31c75-130">Envia o evento de sincronização.</span><span class="sxs-lookup"><span data-stu-id="31c75-130">Sends sync event.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="31c75-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31c75-131">Requirements</span></span>



| <span data-ttu-id="31c75-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="31c75-132">Requirement</span></span> | <span data-ttu-id="31c75-133">Valor</span><span class="sxs-lookup"><span data-stu-id="31c75-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31c75-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31c75-134">Minimum supported client</span></span><br/> | <span data-ttu-id="31c75-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="31c75-135">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="31c75-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31c75-136">Minimum supported server</span></span><br/> | <span data-ttu-id="31c75-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="31c75-137">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="31c75-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="31c75-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="31c75-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31c75-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="31c75-140">DLL</span><span class="sxs-lookup"><span data-stu-id="31c75-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31c75-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31c75-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="31c75-142">IID</span><span class="sxs-lookup"><span data-stu-id="31c75-142">IID</span></span><br/>                      | <span data-ttu-id="31c75-143">IID \_ IMsRdpInputSink é definido como 4606850E-76A7-4E28-A47E-C7174F619351</span><span class="sxs-lookup"><span data-stu-id="31c75-143">IID\_IMsRdpInputSink is defined as 4606850E-76A7-4E28-A47E-C7174F619351</span></span><br/>     |



 

