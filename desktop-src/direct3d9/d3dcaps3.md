---
description: Sinalizadores de capacidade do driver.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda81aa7f77dcaf03eb06b357ebfb91b4956f6d4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343361"
---
# <a name="d3dcaps3"></a><span data-ttu-id="71250-103">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="71250-103">D3DCAPS3</span></span>

<span data-ttu-id="71250-104">Sinalizadores de capacidade do driver.</span><span class="sxs-lookup"><span data-stu-id="71250-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71250-105">#definir</span><span class="sxs-lookup"><span data-stu-id="71250-105">#define</span></span></td>
<td><span data-ttu-id="71250-106">Valor</span><span class="sxs-lookup"><span data-stu-id="71250-106">Value</span></span></td>
<td><span data-ttu-id="71250-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="71250-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71250-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="71250-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="71250-109">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="71250-109">0x00000020L</span></span></td>
<td><span data-ttu-id="71250-110">Indica que o dispositivo pode respeitar o estado de renderização de D3DRS_ALPHABLENDENABLE no modo de tela inteira ao usar o efeito de permuta inverter ou descartar.</span><span class="sxs-lookup"><span data-stu-id="71250-110">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="71250-111">Isso só se aplica quando os Estados D3DRS_SRCBLEND ou D3DRS_DESTBLEND são definidos como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="71250-111">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="71250-112">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="71250-112">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="71250-113">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="71250-113">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="71250-114">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="71250-114">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="71250-115">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="71250-115">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71250-116">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="71250-116">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="71250-117">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="71250-117">0x00000100L</span></span></td>
<td><span data-ttu-id="71250-118">O dispositivo pode acelerar uma cópia de memória da memória do sistema para a memória de vídeo local.</span><span class="sxs-lookup"><span data-stu-id="71250-118">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="71250-119">Esse limite garante que as chamadas <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> e <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> serão aceleradas por hardware.</span><span class="sxs-lookup"><span data-stu-id="71250-119">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="71250-120">Se esse limite estiver ausente, essas chamadas terão sucesso, mas serão mais lentas.</span><span class="sxs-lookup"><span data-stu-id="71250-120">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71250-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="71250-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="71250-122">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="71250-122">0x00000200L</span></span></td>
<td><span data-ttu-id="71250-123">O dispositivo pode acelerar uma cópia de memória da memória de vídeo local para a memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="71250-123">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="71250-124">Esse limite garante que as <a href="/windows/desktop/api"><strong>chamadas GetRenderTargetData</strong></a> sejam aceleradas por hardware.</span><span class="sxs-lookup"><span data-stu-id="71250-124">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="71250-125">Se esse limite estiver ausente, essa chamada terá êxito, mas será mais lenta.</span><span class="sxs-lookup"><span data-stu-id="71250-125">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71250-126">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="71250-126">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="71250-127">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="71250-127">0x00000400L</span></span></td>
<td><span data-ttu-id="71250-128">O driver de exibição dá suporte à DDI DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="71250-128">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="71250-129">Para obter mais informações sobre dXVA-HD DDI, consulte <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span><span class="sxs-lookup"><span data-stu-id="71250-129">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71250-130">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="71250-130">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="71250-131">Esse sinalizador está disponível apenas no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="71250-131">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71250-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="71250-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="71250-133">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="71250-133">0x00000080L</span></span></td>
<td><span data-ttu-id="71250-134">Indica que o dispositivo pode executar a correção gama de um buffer de fundo com janelas (contendo conteúdo linear) para uma área de trabalho sRGB.</span><span class="sxs-lookup"><span data-stu-id="71250-134">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71250-135">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="71250-135">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="71250-136">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="71250-136">0x8000001fL</span></span></td>
<td><span data-ttu-id="71250-137">Reservado; não usado.</span><span class="sxs-lookup"><span data-stu-id="71250-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="71250-138">Essas constantes são usadas pelo membro D3CAPS3 [**de D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="71250-138">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="71250-139">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="71250-139">Constant Information</span></span>



|  <span data-ttu-id="71250-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="71250-140">Requirement</span></span>                        | <span data-ttu-id="71250-141">Valor</span><span class="sxs-lookup"><span data-stu-id="71250-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="71250-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71250-142">Header</span></span>                   | <span data-ttu-id="71250-143">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="71250-143">d3d9caps.h</span></span> |
| <span data-ttu-id="71250-144">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="71250-144">Minimum operating system</span></span> | <span data-ttu-id="71250-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="71250-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="71250-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71250-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71250-147">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="71250-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




