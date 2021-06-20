---
description: Consulte uma lista de sinalizadores de funcionalidade do driver D3DCAPS3. Inclui as definições, valores e descrições com links para APIs.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b28614b2b2ea3c20f828b39f2b8926cb484a88c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408259"
---
# <a name="d3dcaps3"></a><span data-ttu-id="7351a-104">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="7351a-104">D3DCAPS3</span></span>

<span data-ttu-id="7351a-105">Sinalizadores de funcionalidade do driver.</span><span class="sxs-lookup"><span data-stu-id="7351a-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7351a-106">#Definir</span><span class="sxs-lookup"><span data-stu-id="7351a-106">#define</span></span></td>
<td><span data-ttu-id="7351a-107">Valor</span><span class="sxs-lookup"><span data-stu-id="7351a-107">Value</span></span></td>
<td><span data-ttu-id="7351a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7351a-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7351a-109">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="7351a-109">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="7351a-110">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="7351a-110">0x00000020L</span></span></td>
<td><span data-ttu-id="7351a-111">Indica que o dispositivo pode respeitar o estado D3DRS_ALPHABLENDENABLE renderização no modo de tela inteira ao usar o efeito de troca FLIP ou DISCARD.</span><span class="sxs-lookup"><span data-stu-id="7351a-111">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="7351a-112">Isso só se aplica quando os D3DRS_SRCBLEND ou D3DRS_DESTBLEND estão definidos como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="7351a-112">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="7351a-113">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="7351a-113">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="7351a-114">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="7351a-114">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="7351a-115">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="7351a-115">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="7351a-116">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="7351a-116">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7351a-117">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="7351a-117">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="7351a-118">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="7351a-118">0x00000100L</span></span></td>
<td><span data-ttu-id="7351a-119">O dispositivo pode acelerar uma cópia de memória da memória do sistema para a memória de vídeo local.</span><span class="sxs-lookup"><span data-stu-id="7351a-119">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="7351a-120">Esse limite garante que <a href="/windows/desktop/api"><strong>as chamadas UpdateSurface</strong></a> e <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> sejam aceleradas por hardware.</span><span class="sxs-lookup"><span data-stu-id="7351a-120">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="7351a-121">Se esse limite estiver ausente, essas chamadas serão bem-sucedidas, mas serão mais lentas.</span><span class="sxs-lookup"><span data-stu-id="7351a-121">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7351a-122">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="7351a-122">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="7351a-123">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="7351a-123">0x00000200L</span></span></td>
<td><span data-ttu-id="7351a-124">O dispositivo pode acelerar uma cópia de memória da memória de vídeo local para a memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="7351a-124">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="7351a-125">Esse limite garante que as <a href="/windows/desktop/api"><strong>chamadas GetRenderTargetData</strong></a> sejam aceleradas por hardware.</span><span class="sxs-lookup"><span data-stu-id="7351a-125">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="7351a-126">Se esse limite estiver ausente, essa chamada terá êxito, mas será mais lenta.</span><span class="sxs-lookup"><span data-stu-id="7351a-126">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7351a-127">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="7351a-127">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="7351a-128">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="7351a-128">0x00000400L</span></span></td>
<td><span data-ttu-id="7351a-129">O driver de exibição dá suporte à DDI DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="7351a-129">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="7351a-130">Para obter mais informações sobre dXVA-HD DDI, consulte <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span><span class="sxs-lookup"><span data-stu-id="7351a-130">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7351a-131">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="7351a-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7351a-132">Esse sinalizador está disponível apenas no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="7351a-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7351a-133">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="7351a-133">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="7351a-134">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="7351a-134">0x00000080L</span></span></td>
<td><span data-ttu-id="7351a-135">Indica que o dispositivo pode executar a correção gama de um buffer de fundo com janelas (contendo conteúdo linear) para uma área de trabalho sRGB.</span><span class="sxs-lookup"><span data-stu-id="7351a-135">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7351a-136">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="7351a-136">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="7351a-137">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="7351a-137">0x8000001fL</span></span></td>
<td><span data-ttu-id="7351a-138">Reservado; não usado.</span><span class="sxs-lookup"><span data-stu-id="7351a-138">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7351a-139">Essas constantes são usadas pelo membro D3CAPS3 [**de D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="7351a-139">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="7351a-140">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="7351a-140">Constant Information</span></span>



|  <span data-ttu-id="7351a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7351a-141">Requirement</span></span>                        | <span data-ttu-id="7351a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="7351a-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="7351a-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7351a-143">Header</span></span>                   | <span data-ttu-id="7351a-144">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="7351a-144">d3d9caps.h</span></span> |
| <span data-ttu-id="7351a-145">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="7351a-145">Minimum operating system</span></span> | <span data-ttu-id="7351a-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7351a-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7351a-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7351a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7351a-148">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="7351a-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




