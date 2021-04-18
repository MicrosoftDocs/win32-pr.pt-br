---
description: Um bloco de estado pode ser usado para capturar todos os Estados do dispositivo (consulte o estado de salvar e restaurar dos blocos de estado (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Salvando todos os Estados do dispositivo com um StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105796406"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="8fc11-103">Salvando todos os Estados do dispositivo com um StateBlock (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8fc11-103">Saving All Device States with a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="8fc11-104">Um bloco de estado pode ser usado para capturar todos os Estados do dispositivo (consulte o [estado de salvar e restaurar dos blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="8fc11-104">A state block can be used to capture all device states (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="8fc11-105">Os seguintes elementos de estado estão incluídos no estado do dispositivo:</span><span class="sxs-lookup"><span data-stu-id="8fc11-105">The following state elements are included in the device state:</span></span>

-   <span data-ttu-id="8fc11-106">Estado do vértice (consulte [salvar Estados de vértice com um StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="8fc11-106">Vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="8fc11-107">Estado de pixel (consulte [economizando estado de pixel com um StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="8fc11-107">Pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="8fc11-108">Cada textura atribuída a uma amostra.</span><span class="sxs-lookup"><span data-stu-id="8fc11-108">Each texture assigned to a sampler.</span></span>
-   <span data-ttu-id="8fc11-109">Cada textura de vértice.</span><span class="sxs-lookup"><span data-stu-id="8fc11-109">Each vertex texture.</span></span>
-   <span data-ttu-id="8fc11-110">Cada textura de mapa de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="8fc11-110">Each displacement map texture.</span></span>
-   <span data-ttu-id="8fc11-111">A paleta de textura atual.</span><span class="sxs-lookup"><span data-stu-id="8fc11-111">The current texture palette.</span></span>
-   <span data-ttu-id="8fc11-112">Para cada fluxo de vértice: um ponteiro para o buffer de vértice, cada argumento de [**IDirect3DDevice9:: Setstreamname**](/windows/desktop/api)e o divisor (se houver) de [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="8fc11-112">For each vertex stream: a pointer to the vertex buffer, each argument from [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api), and the divider (if any) from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="8fc11-113">Um ponteiro para o buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="8fc11-113">A pointer to the index buffer.</span></span>
-   <span data-ttu-id="8fc11-114">O visor.</span><span class="sxs-lookup"><span data-stu-id="8fc11-114">The viewport.</span></span>
-   <span data-ttu-id="8fc11-115">O retângulo de tesoura.</span><span class="sxs-lookup"><span data-stu-id="8fc11-115">The scissors rectangle.</span></span>
-   <span data-ttu-id="8fc11-116">O mundo, a exibição e as matrizes de projeção.</span><span class="sxs-lookup"><span data-stu-id="8fc11-116">The world, view, and projection matrices.</span></span>
-   <span data-ttu-id="8fc11-117">A textura é transformada.</span><span class="sxs-lookup"><span data-stu-id="8fc11-117">The texture transforms.</span></span>
-   <span data-ttu-id="8fc11-118">Os planos de recorte (se houver).</span><span class="sxs-lookup"><span data-stu-id="8fc11-118">The clipping planes (if any).</span></span>
-   <span data-ttu-id="8fc11-119">O material atual.</span><span class="sxs-lookup"><span data-stu-id="8fc11-119">The current material.</span></span>

<span data-ttu-id="8fc11-120">Para capturar todos os Estados de dispositivo com um bloco de estado, especifique D3DSBT \_ All ao chamar [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span><span class="sxs-lookup"><span data-stu-id="8fc11-120">To capture all device states with a state block, specify D3DSBT\_ALL when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fc11-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8fc11-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fc11-122">Estado de salvamento e restauração de blocos de estado</span><span class="sxs-lookup"><span data-stu-id="8fc11-122">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
