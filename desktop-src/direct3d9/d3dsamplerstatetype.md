---
description: Os Estados de amostra definem operações de amostragem de textura, como endereçamento de textura e filtragem de textura.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Enumeração D3DSAMPLERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802091"
---
# <a name="d3dsamplerstatetype-enumeration"></a><span data-ttu-id="a20ac-103">Enumeração D3DSAMPLERSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="a20ac-103">D3DSAMPLERSTATETYPE enumeration</span></span>

<span data-ttu-id="a20ac-104">Os Estados de amostra definem operações de amostragem de textura, como endereçamento de textura e filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="a20ac-104">Sampler states define texture sampling operations such as texture addressing and texture filtering.</span></span> <span data-ttu-id="a20ac-105">Alguns Estados de amostra configuram o processamento de vértice e algum processamento de pixel de configuração.</span><span class="sxs-lookup"><span data-stu-id="a20ac-105">Some sampler states set-up vertex processing, and some set-up pixel processing.</span></span> <span data-ttu-id="a20ac-106">Os Estados de amostra podem ser salvos e restaurados usando stateblocks (consulte [estado de salvamento e restauração de blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="a20ac-106">Sampler states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="a20ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a20ac-107">Syntax</span></span>


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="a20ac-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a20ac-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a20ac-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**Endereço de D3DSAMP \_**</span><span class="sxs-lookup"><span data-stu-id="a20ac-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP\_ADDRESSU**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-110">Textura – modo de endereço para a coordenada u.</span><span class="sxs-lookup"><span data-stu-id="a20ac-110">Texture-address mode for the u coordinate.</span></span> <span data-ttu-id="a20ac-111">O padrão é D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="a20ac-111">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="a20ac-112">Para obter mais informações, consulte [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="a20ac-112">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ ADDRESSV**</span><span class="sxs-lookup"><span data-stu-id="a20ac-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP\_ADDRESSV**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-114">Textura – modo de endereço para a coordenada v.</span><span class="sxs-lookup"><span data-stu-id="a20ac-114">Texture-address mode for the v coordinate.</span></span> <span data-ttu-id="a20ac-115">O padrão é D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="a20ac-115">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="a20ac-116">Para obter mais informações, consulte [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="a20ac-116">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ ADDRESSW**</span><span class="sxs-lookup"><span data-stu-id="a20ac-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP\_ADDRESSW**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-118">Textura – modo de endereço para a coordenada w.</span><span class="sxs-lookup"><span data-stu-id="a20ac-118">Texture-address mode for the w coordinate.</span></span> <span data-ttu-id="a20ac-119">O padrão é D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="a20ac-119">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="a20ac-120">Para obter mais informações, consulte [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="a20ac-120">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**\_BORDERCOLOR D3DSAMP**</span><span class="sxs-lookup"><span data-stu-id="a20ac-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP\_BORDERCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-122">Cor da borda ou tipo [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a20ac-122">Border color or type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="a20ac-123">A cor padrão é 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a20ac-123">The default color is 0x00000000.</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ MAGFILTER**</span><span class="sxs-lookup"><span data-stu-id="a20ac-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP\_MAGFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-125">Filtro de ampliação do tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="a20ac-125">Magnification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="a20ac-126">O valor padrão é D3DTEXF \_ Point.</span><span class="sxs-lookup"><span data-stu-id="a20ac-126">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MINFILTER**</span><span class="sxs-lookup"><span data-stu-id="a20ac-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP\_MINFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-128">Filtro minificação do tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="a20ac-128">Minification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="a20ac-129">O valor padrão é D3DTEXF \_ Point.</span><span class="sxs-lookup"><span data-stu-id="a20ac-129">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MIPFILTER**</span><span class="sxs-lookup"><span data-stu-id="a20ac-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP\_MIPFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-131">Filtro de mipmap a ser usado durante o minificação.</span><span class="sxs-lookup"><span data-stu-id="a20ac-131">Mipmap filter to use during minification.</span></span> <span data-ttu-id="a20ac-132">Consulte [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="a20ac-132">See [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="a20ac-133">O valor padrão é D3DTEXF \_ None.</span><span class="sxs-lookup"><span data-stu-id="a20ac-133">The default value is D3DTEXF\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ MIPMAPLODBIAS**</span><span class="sxs-lookup"><span data-stu-id="a20ac-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP\_MIPMAPLODBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-135">Mipmap de diferença de nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="a20ac-135">Mipmap level-of-detail bias.</span></span> <span data-ttu-id="a20ac-136">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="a20ac-136">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MAXMIPLEVEL**</span><span class="sxs-lookup"><span data-stu-id="a20ac-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP\_MAXMIPLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-138">índice de nível de detalhe do maior mapa a ser usado.</span><span class="sxs-lookup"><span data-stu-id="a20ac-138">level-of-detail index of largest map to use.</span></span> <span data-ttu-id="a20ac-139">Os valores variam de 0 a (n-1), em que 0 é o maior.</span><span class="sxs-lookup"><span data-stu-id="a20ac-139">Values range from 0 to (n - 1) where 0 is the largest.</span></span> <span data-ttu-id="a20ac-140">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="a20ac-140">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MAXANISOTROPY**</span><span class="sxs-lookup"><span data-stu-id="a20ac-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP\_MAXANISOTROPY**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-142">Anisotropy de máximo DWORD.</span><span class="sxs-lookup"><span data-stu-id="a20ac-142">DWORD maximum anisotropy.</span></span> <span data-ttu-id="a20ac-143">Os valores variam de 1 até o valor especificado no membro **MaxAnisotropy** da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="a20ac-143">Values range from 1 to the value that is specified in the **MaxAnisotropy** member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="a20ac-144">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="a20ac-144">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ SRGBTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="a20ac-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP\_SRGBTEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-146">Valor de correção gama.</span><span class="sxs-lookup"><span data-stu-id="a20ac-146">Gamma correction value.</span></span> <span data-ttu-id="a20ac-147">O valor padrão é 0, o que significa que o gama é 1,0 e nenhuma correção é necessária.</span><span class="sxs-lookup"><span data-stu-id="a20ac-147">The default value is 0, which means gamma is 1.0 and no correction is required.</span></span> <span data-ttu-id="a20ac-148">Caso contrário, esse valor significa que a amostra deve assumir o gama de 2,2 no conteúdo e convertê-lo em linear (gama 1,0) antes de apresentá-lo ao sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="a20ac-148">Otherwise, this value means that the sampler should assume gamma of 2.2 on the content and convert it to linear (gamma 1.0) before presenting it to the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ ELEMENTINDEX**</span><span class="sxs-lookup"><span data-stu-id="a20ac-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP\_ELEMENTINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-150">Quando uma textura Multielemento é atribuída à amostra, isso indica qual índice de elemento usar.</span><span class="sxs-lookup"><span data-stu-id="a20ac-150">When a multielement texture is assigned to the sampler, this indicates which element index to use.</span></span> <span data-ttu-id="a20ac-151">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a20ac-151">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ DMAPOFFSET**</span><span class="sxs-lookup"><span data-stu-id="a20ac-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP\_DMAPOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-153">Deslocamento de vértice no mapa de substituição de amostra.</span><span class="sxs-lookup"><span data-stu-id="a20ac-153">Vertex offset in the presampled displacement map.</span></span> <span data-ttu-id="a20ac-154">Essa é uma constante usada pelo Tessellator, seu valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a20ac-154">This is a constant used by the tessellator, its default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a20ac-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a20ac-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a20ac-156">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="a20ac-156">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a20ac-157">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a20ac-157">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a20ac-158">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="a20ac-158">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a20ac-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a20ac-159">Requirements</span></span>



| <span data-ttu-id="a20ac-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="a20ac-160">Requirement</span></span> | <span data-ttu-id="a20ac-161">Valor</span><span class="sxs-lookup"><span data-stu-id="a20ac-161">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a20ac-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a20ac-162">Header</span></span><br/> | <dl> <span data-ttu-id="a20ac-163"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a20ac-163"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a20ac-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="a20ac-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a20ac-165">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="a20ac-165">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
