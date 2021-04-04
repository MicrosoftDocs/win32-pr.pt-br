---
title: Funções DirectComposition
description: Esta seção descreve as funções fornecidas pelo Microsoft DirectComposition \ 32; API.
ms.assetid: 750FDFD5-ADD5-43B3-A596-ECDB82C2EF73
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934e0b7e32f22faaefdf625e0af2a42a03e469d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084631"
---
# <a name="directcomposition-functions"></a><span data-ttu-id="e08c5-103">Funções DirectComposition</span><span class="sxs-lookup"><span data-stu-id="e08c5-103">DirectComposition functions</span></span>

<span data-ttu-id="e08c5-104">Esta seção descreve as funções fornecidas pela API do Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="e08c5-104">This section describes the functions provided by the Microsoft DirectComposition API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e08c5-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e08c5-105">In this section</span></span>



| <span data-ttu-id="e08c5-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="e08c5-106">Topic</span></span>                                                                                       | <span data-ttu-id="e08c5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e08c5-107">Description</span></span>                                                                                                                                          |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e08c5-108">**DCompositionAttachMouseDragToHwnd**</span><span class="sxs-lookup"><span data-stu-id="e08c5-108">**DCompositionAttachMouseDragToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousedragtohwnd)<br/>   | <span data-ttu-id="e08c5-109">Cria uma interação/InputSink para rotear o botão do mouse para baixo e quaisquer eventos move e up subsequentes para o HWND fornecido.</span><span class="sxs-lookup"><span data-stu-id="e08c5-109">Creates an Interaction/InputSink to route mouse button down and any subsequent move and up events to the given HWND.</span></span><br/>                      |
| [<span data-ttu-id="e08c5-110">**DCompositionAttachMouseWheelToHwnd**</span><span class="sxs-lookup"><span data-stu-id="e08c5-110">**DCompositionAttachMouseWheelToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousewheeltohwnd)<br/> | <span data-ttu-id="e08c5-111">Cria uma interação/InputSink para rotear mensagens de roda do mouse para o HWND fornecido.</span><span class="sxs-lookup"><span data-stu-id="e08c5-111">Creates an Interaction/InputSink to route mouse wheel messages to the given HWND.</span></span> <br/>                                                        |
| [<span data-ttu-id="e08c5-112">**DCompositionCreateDevice**</span><span class="sxs-lookup"><span data-stu-id="e08c5-112">**DCompositionCreateDevice**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)<br/>                     | <span data-ttu-id="e08c5-113">Cria um novo objeto de dispositivo que pode ser usado para criar outros objetos DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="e08c5-113">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="e08c5-114">**DCompositionCreateDevice2**</span><span class="sxs-lookup"><span data-stu-id="e08c5-114">**DCompositionCreateDevice2**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice2)<br/>                   | <span data-ttu-id="e08c5-115">Cria um novo objeto de dispositivo que pode ser usado para criar outros objetos DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="e08c5-115">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="e08c5-116">**DCompositionCreateDevice3**</span><span class="sxs-lookup"><span data-stu-id="e08c5-116">**DCompositionCreateDevice3**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatedevice3)<br/>                   | <span data-ttu-id="e08c5-117">Cria um novo objeto de dispositivo DirectComposition, que pode ser usado para criar outros objetos DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="e08c5-117">Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.</span></span><br/>                               |
| [<span data-ttu-id="e08c5-118">**DCompositionCreateSurfaceHandle**</span><span class="sxs-lookup"><span data-stu-id="e08c5-118">**DCompositionCreateSurfaceHandle**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatesurfacehandle)<br/>       | <span data-ttu-id="e08c5-119">Cria um novo objeto de superfície de composição que pode ser associado a uma cadeia de permuta do Microsoft DirectX ou ao buffer de permuta e associado a um Visual.</span><span class="sxs-lookup"><span data-stu-id="e08c5-119">Creates a new composition surface object that can be bound to a Microsoft DirectX swap chain or swap buffer and associated with a visual.</span></span><br/> |
| <span data-ttu-id="e08c5-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e08c5-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span></span><br/>         | <span data-ttu-id="e08c5-121">Recupera informações de estatísticas de composição.</span><span class="sxs-lookup"><span data-stu-id="e08c5-121">Retrieves composition statistics information.</span></span><br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="e08c5-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e08c5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e08c5-123">Referência de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="e08c5-123">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

