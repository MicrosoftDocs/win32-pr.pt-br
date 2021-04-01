---
description: A interface IDirect3DDevice9 dá suporte ao processamento de vértice no software e no hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Processando dados de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825917"
---
# <a name="processing-vertex-data-direct3d-9"></a><span data-ttu-id="464f3-103">Processando dados de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="464f3-103">Processing Vertex Data (Direct3D 9)</span></span>

<span data-ttu-id="464f3-104">A interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) dá suporte ao processamento de vértice no software e no hardware.</span><span class="sxs-lookup"><span data-stu-id="464f3-104">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface supports vertex processing in both software and hardware.</span></span> <span data-ttu-id="464f3-105">Em geral, os recursos do dispositivo para o processamento de vértices de software e hardware não são idênticos.</span><span class="sxs-lookup"><span data-stu-id="464f3-105">In general, the device capabilities for software and hardware vertex processing are not identical.</span></span> <span data-ttu-id="464f3-106">Os recursos de hardware são variáveis, dependendo do adaptador de vídeo e do driver, enquanto os recursos de software são corrigidos.</span><span class="sxs-lookup"><span data-stu-id="464f3-106">Hardware capabilities are variable, depending on the display adapter and driver, while software capabilities are fixed.</span></span>

<span data-ttu-id="464f3-107">Os sinalizadores a seguir controlam o comportamento de processamento de vértice para a HAL (camada de abstração de hardware) e os dispositivos de referência.</span><span class="sxs-lookup"><span data-stu-id="464f3-107">The following flags control vertex processing behavior for the hardware abstraction layer (HAL) and reference devices.</span></span>

-   <span data-ttu-id="464f3-108">D3DCREATE \_ software \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="464f3-108">D3DCREATE\_SOFTWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="464f3-109">\_VERTEXPROCESSING de hardware D3DCREATE \_</span><span class="sxs-lookup"><span data-stu-id="464f3-109">D3DCREATE\_HARDWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="464f3-110">D3DCREATE \_ Misto \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="464f3-110">D3DCREATE\_MIXED\_VERTEXPROCESSING</span></span>

<span data-ttu-id="464f3-111">Especifique um dos sinalizadores de comportamento de processamento de vértice ao chamar [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span><span class="sxs-lookup"><span data-stu-id="464f3-111">Specify one of the vertex processing behavior flags when calling [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span> <span data-ttu-id="464f3-112">O sinalizador de modo misto permite que o dispositivo execute o processamento de vértice de software e hardware.</span><span class="sxs-lookup"><span data-stu-id="464f3-112">The mixed-mode flag enables the device to perform both software and hardware vertex processing.</span></span> <span data-ttu-id="464f3-113">Somente um sinalizador de processamento de vértice pode ser definido para um dispositivo a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="464f3-113">Only one vertex processing flag may be set for a device at any one time.</span></span> <span data-ttu-id="464f3-114">Observe que o sinalizador D3DCREATE de \_ hardware \_ VERTEXPROCESSING deve ser definido ao criar um dispositivo puro (D3DCREATE \_ PUREDEVICE).</span><span class="sxs-lookup"><span data-stu-id="464f3-114">Note that the D3DCREATE\_HARDWARE\_VERTEXPROCESSING flag is required to be set when creating a pure device (D3DCREATE\_PUREDEVICE).</span></span>

<span data-ttu-id="464f3-115">Para evitar funcionalidades de processamento de vértice duplo em um único dispositivo, somente os recursos de processamento de vértice de hardware podem ser consultados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="464f3-115">To avoid dual vertex processing capabilities on a single device, only the hardware vertex processing capabilities can be queried at run time.</span></span> <span data-ttu-id="464f3-116">Os recursos de processamento de vértice de software são fixos e não podem ser consultados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="464f3-116">Software vertex processing capabilities are fixed and cannot be queried at run time.</span></span>

<span data-ttu-id="464f3-117">O membro VertexProcessingCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) determina os recursos de processamento de vértice de hardware do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="464f3-117">The VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure determines the hardware vertex processing capabilities of the device.</span></span>

<span data-ttu-id="464f3-118">Para o processamento de vértice de software, há suporte para os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="464f3-118">For software vertex processing the following capabilities are supported.</span></span>

-   <span data-ttu-id="464f3-119">o \_ membro D3DVTXPCAPS DIRECTIONALLIGHTS da [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="464f3-119">the D3DVTXPCAPS\_DIRECTIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="464f3-120">o \_ membro D3DVTXPCAPS LOCALVIEWER da [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="464f3-120">the D3DVTXPCAPS\_LOCALVIEWER member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="464f3-121">o \_ membro D3DVTXPCAPS MATERIALSOURCE7 da [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="464f3-121">the D3DVTXPCAPS\_MATERIALSOURCE7 member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="464f3-122">o \_ membro D3DVTXPCAPS POSITIONALLIGHTS da [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="464f3-122">the D3DVTXPCAPS\_POSITIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="464f3-123">o \_ membro D3DVTXPCAPS TEXGEN da [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="464f3-123">the D3DVTXPCAPS\_TEXGEN member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="464f3-124">o \_ membro de interpolação D3DVTXPCAPS de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="464f3-124">the D3DVTXPCAPS\_TWEENING member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>

<span data-ttu-id="464f3-125">Além disso, a tabela a seguir lista os valores que são definidos para membros da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) de um dispositivo no modo de processamento de vértice de software.</span><span class="sxs-lookup"><span data-stu-id="464f3-125">In addition, the following table lists the values that are set for members of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for a device in software vertex processing mode.</span></span>



| <span data-ttu-id="464f3-126">Membro</span><span class="sxs-lookup"><span data-stu-id="464f3-126">Member</span></span>                 | <span data-ttu-id="464f3-127">Recursos de processamento de vértice de software</span><span class="sxs-lookup"><span data-stu-id="464f3-127">Software vertex processing capabilities</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="464f3-128">MaxActiveLights</span><span class="sxs-lookup"><span data-stu-id="464f3-128">MaxActiveLights</span></span>        | <span data-ttu-id="464f3-129">Ilimitado</span><span class="sxs-lookup"><span data-stu-id="464f3-129">Unlimited</span></span>                               |
| <span data-ttu-id="464f3-130">MaxUserClipPlanes</span><span class="sxs-lookup"><span data-stu-id="464f3-130">MaxUserClipPlanes</span></span>      | <span data-ttu-id="464f3-131">6</span><span class="sxs-lookup"><span data-stu-id="464f3-131">6</span></span>                                       |
| <span data-ttu-id="464f3-132">MaxVertexBlendMatrices</span><span class="sxs-lookup"><span data-stu-id="464f3-132">MaxVertexBlendMatrices</span></span> | <span data-ttu-id="464f3-133">4</span><span class="sxs-lookup"><span data-stu-id="464f3-133">4</span></span>                                       |
| <span data-ttu-id="464f3-134">MaxStreams</span><span class="sxs-lookup"><span data-stu-id="464f3-134">MaxStreams</span></span>             | <span data-ttu-id="464f3-135">16</span><span class="sxs-lookup"><span data-stu-id="464f3-135">16</span></span>                                      |
| <span data-ttu-id="464f3-136">MaxVertexIndex</span><span class="sxs-lookup"><span data-stu-id="464f3-136">MaxVertexIndex</span></span>         | <span data-ttu-id="464f3-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="464f3-137">0xFFFFFFFF</span></span>                              |



 

<span data-ttu-id="464f3-138">Em geral, qualquer aplicativo que esteja associado ao processamento de vértice deve usar um dispositivo HAL.</span><span class="sxs-lookup"><span data-stu-id="464f3-138">In general, any application that is vertex processing bound should use a HAL device.</span></span> <span data-ttu-id="464f3-139">O processamento de vértices de software fornece um conjunto garantido de recursos de processamento de vértice, incluindo um número de luzes não associadas e suporte completo para sombreadores de vértice programáveis.</span><span class="sxs-lookup"><span data-stu-id="464f3-139">Software vertex processing provides a guaranteed set of vertex processing capabilities, including an unbounded number of lights and full support for programmable vertex shaders.</span></span> <span data-ttu-id="464f3-140">Você pode alternar entre o processamento de vértice de software e hardware a qualquer momento ao usar o dispositivo HAL (que é o único tipo de dispositivo que dá suporte ao processamento de vértice de hardware e software).</span><span class="sxs-lookup"><span data-stu-id="464f3-140">You can toggle between software and hardware vertex processing at any time when using the HAL device (which is the only device type that supports both hardware and software vertex processing).</span></span> <span data-ttu-id="464f3-141">O único requisito é que os buffers de vértice usados para o processamento de vértice de software devem ser alocados na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="464f3-141">The only requirement is that vertex buffers used for software vertex processing must be allocated in system memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="464f3-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="464f3-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="464f3-143">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="464f3-143">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
