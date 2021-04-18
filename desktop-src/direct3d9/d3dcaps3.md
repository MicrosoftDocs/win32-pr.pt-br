---
description: Sinalizadores de capacidade do driver.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a165ff1d550612ba302c94a0b8181affe040921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105802082"
---
# <a name="d3dcaps3"></a><span data-ttu-id="93bef-103">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="93bef-103">D3DCAPS3</span></span>

<span data-ttu-id="93bef-104">Sinalizadores de capacidade do driver.</span><span class="sxs-lookup"><span data-stu-id="93bef-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93bef-105">#definir</span><span class="sxs-lookup"><span data-stu-id="93bef-105">#define</span></span></td>
<td><span data-ttu-id="93bef-106">Valor</span><span class="sxs-lookup"><span data-stu-id="93bef-106">Value</span></span></td>
<td><span data-ttu-id="93bef-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="93bef-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93bef-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="93bef-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="93bef-109">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="93bef-109">0x00000020L</span></span></td>
<td><span data-ttu-id="93bef-110">Indica que o dispositivo pode respeitar o estado de renderização de D3DRS_ALPHABLENDENABLE no modo de tela inteira ao usar o efeito de permuta inverter ou descartar.</span><span class="sxs-lookup"><span data-stu-id="93bef-110">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="93bef-111">Isso só se aplica quando os Estados D3DRS_SRCBLEND ou D3DRS_DESTBLEND são definidos como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="93bef-111">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="93bef-112">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="93bef-112">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="93bef-113">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="93bef-113">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="93bef-114">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="93bef-114">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="93bef-115">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="93bef-115">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93bef-116">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="93bef-116">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="93bef-117">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="93bef-117">0x00000100L</span></span></td>
<td><span data-ttu-id="93bef-118">O dispositivo pode acelerar uma cópia de memória da memória do sistema para a memória de vídeo local.</span><span class="sxs-lookup"><span data-stu-id="93bef-118">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="93bef-119">Esse limite garante que as chamadas <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> e <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> serão aceleradas por hardware.</span><span class="sxs-lookup"><span data-stu-id="93bef-119">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="93bef-120">Se esse limite estiver ausente, essas chamadas terão sucesso, mas serão mais lentas.</span><span class="sxs-lookup"><span data-stu-id="93bef-120">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93bef-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="93bef-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="93bef-122">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="93bef-122">0x00000200L</span></span></td>
<td><span data-ttu-id="93bef-123">O dispositivo pode acelerar uma cópia de memória da memória de vídeo local para a memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="93bef-123">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="93bef-124">Esse limite garante que as chamadas de <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> serão aceleradas por hardware.</span><span class="sxs-lookup"><span data-stu-id="93bef-124">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="93bef-125">Se esse limite estiver ausente, essa chamada terá sucesso, mas será mais lenta.</span><span class="sxs-lookup"><span data-stu-id="93bef-125">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93bef-126">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="93bef-126">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="93bef-127">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="93bef-127">0x00000400L</span></span></td>
<td><span data-ttu-id="93bef-128">O driver de vídeo dá suporte à DDI DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="93bef-128">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="93bef-129">Para obter mais informações sobre a DDI DXVA-HD, consulte <a href="https://msdn.microsoft.com/library/dd835176.aspx">processamento High-Definition vídeo</a>.</span><span class="sxs-lookup"><span data-stu-id="93bef-129">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93bef-130">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="93bef-130">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="93bef-131">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="93bef-131">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93bef-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="93bef-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="93bef-133">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="93bef-133">0x00000080L</span></span></td>
<td><span data-ttu-id="93bef-134">Indica que o dispositivo pode executar a correção gama de um buffer de fundo em janela (que contém conteúdo linear) para uma área de trabalho sRGB.</span><span class="sxs-lookup"><span data-stu-id="93bef-134">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93bef-135">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="93bef-135">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="93bef-136">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="93bef-136">0x8000001fL</span></span></td>
<td><span data-ttu-id="93bef-137">Reservado Não usado.</span><span class="sxs-lookup"><span data-stu-id="93bef-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="93bef-138">Essas constantes são usadas pelo membro D3CAPS3 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="93bef-138">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="93bef-139">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="93bef-139">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="93bef-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93bef-140">Header</span></span>                   | <span data-ttu-id="93bef-141">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="93bef-141">d3d9caps.h</span></span> |
| <span data-ttu-id="93bef-142">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="93bef-142">Minimum operating system</span></span> | <span data-ttu-id="93bef-143">Windows 98</span><span class="sxs-lookup"><span data-stu-id="93bef-143">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="93bef-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93bef-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93bef-145">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="93bef-145">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




