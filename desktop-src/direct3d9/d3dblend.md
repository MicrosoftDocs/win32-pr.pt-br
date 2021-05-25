---
description: Define o modo de combinação com suporte.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: Enumeração D3DBLEND (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 55edb432913720f58860d4f5cb87d8da9b9a8681
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343381"
---
# <a name="d3dblend-enumeration"></a><span data-ttu-id="4741c-103">Enumeração D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="4741c-103">D3DBLEND enumeration</span></span>

<span data-ttu-id="4741c-104">Define o modo de combinação com suporte.</span><span class="sxs-lookup"><span data-stu-id="4741c-104">Defines the supported blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="4741c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4741c-105">Syntax</span></span>


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a><span data-ttu-id="4741c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="4741c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4741c-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ ZERO**</span><span class="sxs-lookup"><span data-stu-id="4741c-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-108">O fator blend é (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="4741c-108">Blend factor is (0, 0, 0, 0).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ ONE**</span><span class="sxs-lookup"><span data-stu-id="4741c-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND\_ONE**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-110">O fator blend é (1, 1, 1, 1).</span><span class="sxs-lookup"><span data-stu-id="4741c-110">Blend factor is (1, 1, 1, 1).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ SRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4741c-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND\_SRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-112">O fator blend é (Rs, Gs, Bs, As).</span><span class="sxs-lookup"><span data-stu-id="4741c-112">Blend factor is (Rₛ, Gₛ, Bₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ INVSRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4741c-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND\_INVSRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-114">O fator blend é (1 - Rs, 1 - Gs, 1 - Bs, 1 - As).</span><span class="sxs-lookup"><span data-stu-id="4741c-114">Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ SRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="4741c-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND\_SRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-116">O fator blend é (As, As, As, As).</span><span class="sxs-lookup"><span data-stu-id="4741c-116">Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ INVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="4741c-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND\_INVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-118">O fator blend é ( 1 - As, 1 - As, 1 - As, 1 - As).</span><span class="sxs-lookup"><span data-stu-id="4741c-118">Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ DESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="4741c-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND\_DESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-120">O fator blend é (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="4741c-120">Blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ INVDESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="4741c-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND\_INVDESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-122">O fator blend é (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="4741c-122">Blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ DESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4741c-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND\_DESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-124">O fator de mistura é (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="4741c-124">Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ INVDESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4741c-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND\_INVDESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-126">O fator de mistura é (1-R<sub>d</sub>, 1-G<sub>d</sub>, 1-B<sub>d</sub>, 1-a<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="4741c-126">Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ SRCALPHASAT**</span><span class="sxs-lookup"><span data-stu-id="4741c-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND\_SRCALPHASAT**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-128">O fator de mistura é (f, f, f, 1); em que f = min (as, 1 a<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="4741c-128">Blend factor is (f, f, f, 1); where f = min(Aₛ, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ BOTHSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="4741c-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND\_BOTHSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-130">**Obsoleto**.</span><span class="sxs-lookup"><span data-stu-id="4741c-130">**Obsolete**.</span></span> <span data-ttu-id="4741c-131">A partir do DirectX 6, você pode obter o mesmo efeito definindo os fatores de mesclagem de origem e de destino como D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA em chamadas separadas.</span><span class="sxs-lookup"><span data-stu-id="4741c-131">Starting with DirectX 6, you can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span>

</dd> <dt>

<span data-ttu-id="4741c-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ BOTHINVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="4741c-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND\_BOTHINVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-133">**Obsoleto**.</span><span class="sxs-lookup"><span data-stu-id="4741c-133">**Obsolete**.</span></span> <span data-ttu-id="4741c-134">O fator de mistura de origem é (1-como, 1-como, 1-como, 1-como) e o fator de mesclagem de destino é (como, como, como, como); a seleção de mesclagem de destino é substituída.</span><span class="sxs-lookup"><span data-stu-id="4741c-134">Source blend factor is (1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), and destination blend factor is (Aₛ, Aₛ, Aₛ, Aₛ); the destination blend selection is overridden.</span></span> <span data-ttu-id="4741c-135">Esse modo de mesclagem tem suporte apenas para o \_ estado de RENDERIZAÇÃO D3DRS SRCBLEND.</span><span class="sxs-lookup"><span data-stu-id="4741c-135">This blend mode is supported only for the D3DRS\_SRCBLEND render state.</span></span>

</dd> <dt>

<span data-ttu-id="4741c-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="4741c-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-137">Fator de mistura de cor constante usado pelo misturador de buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="4741c-137">Constant color blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="4741c-138">Esse modo de mesclagem só terá suporte se D3DPBLENDCAPS \_ BLENDFACTOR estiver definido nos membros **SrcBlendCaps** ou **DestBlendCaps** de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="4741c-138">This blend mode is supported only if D3DPBLENDCAPS\_BLENDFACTOR is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ INVBLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="4741c-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND\_INVBLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-140">Fator de mistura de cor constante invertido usado pelo misturador de buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="4741c-140">Inverted constant color-blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="4741c-141">Esse modo de mesclagem só terá suporte se o \_ bit D3DPBLENDCAPS BLENDFACTOR for definido nos membros **SrcBlendCaps** ou **DestBlendCaps** de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="4741c-141">This blend mode is supported only if the D3DPBLENDCAPS\_BLENDFACTOR bit is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="4741c-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="4741c-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND\_SRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-143">O fator blend é (PSOutColor \[ 1 \] <sub>r,</sub>PSOutColor \[ 1 \] <sub>g,</sub>PSOutColor \[ 1 \] <sub>b</sub>, não usado).</span><span class="sxs-lookup"><span data-stu-id="4741c-143">Blend factor is (PSOutColor\[1\]<sub>r</sub>, PSOutColor\[1\]<sub>g</sub>, PSOutColor\[1\]<sub>b</sub>, not used).</span></span> <span data-ttu-id="4741c-144">Consulte [Renderizar mesclagem de destino.](#render-target-blending)</span><span class="sxs-lookup"><span data-stu-id="4741c-144">See [Render Target Blending](#render-target-blending).</span></span>

<span data-ttu-id="4741c-145">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="4741c-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="4741c-146">Esse sinalizador está disponível apenas no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="4741c-146">This flag is available in Direct3D 9Ex only.</span></span>



 

</dd> <dt>

<span data-ttu-id="4741c-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="4741c-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND\_INVSRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-148">O fator blend é (1 - PSOutColor \[ 1 \] <sub>r</sub>, 1 - PSOutColor \[ 1 \] <sub>g</sub>, 1 - PSOutColor \[ 1 \] <sub>b</sub>, não usado)).</span><span class="sxs-lookup"><span data-stu-id="4741c-148">Blend factor is (1 - PSOutColor\[1\]<sub>r</sub>, 1 - PSOutColor\[1\]<sub>g</sub>, 1 - PSOutColor\[1\]<sub>b</sub>, not used)).</span></span> <span data-ttu-id="4741c-149">Consulte [Renderizar mesclagem de destino.](#render-target-blending)</span><span class="sxs-lookup"><span data-stu-id="4741c-149">See [Render Target Blending](#render-target-blending).</span></span>


<span data-ttu-id="4741c-150">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="4741c-150">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="4741c-151">Esse sinalizador está disponível apenas no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="4741c-151">This flag is available in Direct3D 9Ex only.</span></span>



 

</dd> <dt>

<span data-ttu-id="4741c-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4741c-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4741c-153">Força essa enumeração a compilar para 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="4741c-153">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4741c-154">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4741c-154">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4741c-155">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="4741c-155">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4741c-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="4741c-156">Remarks</span></span>

<span data-ttu-id="4741c-157">Nas descrições do membro anterior, os valores RGBA da origem e do destino são indicados pelos subscritos s e d.</span><span class="sxs-lookup"><span data-stu-id="4741c-157">In the preceding member descriptions, the RGBA values of the source and destination are indicated by the s and d subscripts.</span></span>

<span data-ttu-id="4741c-158">Os valores nesse tipo enumerado são usados pelos seguintes estados de renderização:</span><span class="sxs-lookup"><span data-stu-id="4741c-158">The values in this enumerated type are used by the following render states:</span></span>

-   <span data-ttu-id="4741c-159">D3DRS \_ DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="4741c-159">D3DRS\_DESTBLEND</span></span>
-   <span data-ttu-id="4741c-160">D3DRS \_ SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="4741c-160">D3DRS\_SRCBLEND</span></span>
-   <span data-ttu-id="4741c-161">D3DRS \_ DESTBLENDALPHA</span><span class="sxs-lookup"><span data-stu-id="4741c-161">D3DRS\_DESTBLENDALPHA</span></span>
-   <span data-ttu-id="4741c-162">D3DRS \_ SRCBLENDALPHA</span><span class="sxs-lookup"><span data-stu-id="4741c-162">D3DRS\_SRCBLENDALPHA</span></span>

<span data-ttu-id="4741c-163">Consulte [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="4741c-163">See [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span></span>

### <a name="render-target-blending"></a><span data-ttu-id="4741c-164">Renderizar a mesclagem de destino</span><span class="sxs-lookup"><span data-stu-id="4741c-164">Render Target Blending</span></span>

<span data-ttu-id="4741c-165">O Direct3D 9Ex aprimorou os recursos de renderização de texto.</span><span class="sxs-lookup"><span data-stu-id="4741c-165">Direct3D 9Ex has improved text rendering capabilities.</span></span> <span data-ttu-id="4741c-166">A renderização de fontes de tipo limpar normalmente exigiria duas passagens.</span><span class="sxs-lookup"><span data-stu-id="4741c-166">Rendering clear-type fonts would normally require two passes.</span></span> <span data-ttu-id="4741c-167">Para eliminar a segunda passagem, um sombreador de pixel pode ser usado para produzir duas cores, que podemos chamar PSOutColor \[ 0 \] e PSOutColor \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="4741c-167">To eliminate the second pass, a pixel shader can be used to output two colors, which we can call PSOutColor\[0\] and PSOutColor\[1\].</span></span> <span data-ttu-id="4741c-168">A primeira cor conterá os componentes padrão de 3 cores (RGB).</span><span class="sxs-lookup"><span data-stu-id="4741c-168">The first color would contain the standard 3 color components (RGB).</span></span> <span data-ttu-id="4741c-169">A segunda cor conterá três componentes alfa (um para cada componente da primeira cor).</span><span class="sxs-lookup"><span data-stu-id="4741c-169">The second color would contain 3 alpha components (one for each component of the first color).</span></span>

<span data-ttu-id="4741c-170">Esses novos modos de mesclagem são usados apenas para renderização de texto no primeiro destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="4741c-170">These new blending modes are only used for text rendering on the first render target.</span></span>

## <a name="requirements"></a><span data-ttu-id="4741c-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4741c-171">Requirements</span></span>



| <span data-ttu-id="4741c-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="4741c-172">Requirement</span></span> | <span data-ttu-id="4741c-173">Valor</span><span class="sxs-lookup"><span data-stu-id="4741c-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4741c-174">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4741c-174">Header</span></span><br/> | <dl> <span data-ttu-id="4741c-175"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4741c-175"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4741c-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="4741c-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4741c-177">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="4741c-177">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
