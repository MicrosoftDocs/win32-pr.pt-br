---
description: Define modos de filtragem de textura para um estágio de textura.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumeração D3DTEXTUREFILTERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 212fd05755ebf554c3c57e7ac45dcf8947f2d753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790379"
---
# <a name="d3dtexturefiltertype-enumeration"></a><span data-ttu-id="42f7b-103">Enumeração D3DTEXTUREFILTERTYPE</span><span class="sxs-lookup"><span data-stu-id="42f7b-103">D3DTEXTUREFILTERTYPE enumeration</span></span>

<span data-ttu-id="42f7b-104">Define modos de filtragem de textura para um estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="42f7b-104">Defines texture filtering modes for a texture stage.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f7b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42f7b-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a><span data-ttu-id="42f7b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="42f7b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="42f7b-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="42f7b-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="42f7b-108">Quando usado com [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md), desabilita o mipmapping.</span><span class="sxs-lookup"><span data-stu-id="42f7b-108">When used with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md), disables mipmapping.</span></span>

</dd> <dt>

<span data-ttu-id="42f7b-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**Ponto de D3DTEXF \_**</span><span class="sxs-lookup"><span data-stu-id="42f7b-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="42f7b-110">Quando usado com [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que a filtragem de ponto deve ser usada como o filtro de ampliação ou de minificação de textura, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="42f7b-110">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that point filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="42f7b-111">Quando usado com **D3DSAMP \_ MIPFILTER**, habilita mipmapping e especifica que o rasterizador escolhe a cor do Texel do nível de MIP mais próximo.</span><span class="sxs-lookup"><span data-stu-id="42f7b-111">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and specifies that the rasterizer chooses the color from the texel of the nearest mip level.</span></span>

</dd> <dt>

<span data-ttu-id="42f7b-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ linear**</span><span class="sxs-lookup"><span data-stu-id="42f7b-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="42f7b-113">Quando usado com [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que a filtragem linear deve ser usada como o filtro de ampliação ou de minificação de textura, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="42f7b-113">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that linear filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="42f7b-114">Quando usado com **D3DSAMP \_ MIPFILTER**, habilita a filtragem de mipmapping e trilineion; ele especifica que o rasterizador interpola entre os dois níveis MIP mais próximos.</span><span class="sxs-lookup"><span data-stu-id="42f7b-114">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and trilinear filtering; it specifies that the rasterizer interpolates between the two nearest mip levels.</span></span>

</dd> <dt>

<span data-ttu-id="42f7b-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ ANISOTROPIC**</span><span class="sxs-lookup"><span data-stu-id="42f7b-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF\_ANISOTROPIC**</span></span>
</dt> <dd>

<span data-ttu-id="42f7b-116">Quando usado com [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que a filtragem de textura anisotropic usada como um filtro de ampliação ou de minificação de textura, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="42f7b-116">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively.</span></span> <span data-ttu-id="42f7b-117">Compensa a distorção causada pela diferença em ângulo entre o polígono da textura e o plano da tela.</span><span class="sxs-lookup"><span data-stu-id="42f7b-117">Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen.</span></span> <span data-ttu-id="42f7b-118">Use with **D3DSAMP \_ MIPFILTER** é indefinido.</span><span class="sxs-lookup"><span data-stu-id="42f7b-118">Use with **D3DSAMP\_MIPFILTER** is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="42f7b-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**</span><span class="sxs-lookup"><span data-stu-id="42f7b-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF\_PYRAMIDALQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="42f7b-120">Um filtro de tipo tenda de 4 amostras usado como um filtro de ampliação ou minificação de textura.</span><span class="sxs-lookup"><span data-stu-id="42f7b-120">A 4-sample tent filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="42f7b-121">Use with [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) é indefinido.</span><span class="sxs-lookup"><span data-stu-id="42f7b-121">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="42f7b-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**</span><span class="sxs-lookup"><span data-stu-id="42f7b-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF\_GAUSSIANQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="42f7b-123">Um filtro gaussiano de 4 amostras usado como um filtro de ampliação ou minificação de textura.</span><span class="sxs-lookup"><span data-stu-id="42f7b-123">A 4-sample Gaussian filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="42f7b-124">Use with [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) é indefinido.</span><span class="sxs-lookup"><span data-stu-id="42f7b-124">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="42f7b-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**</span><span class="sxs-lookup"><span data-stu-id="42f7b-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF\_CONVOLUTIONMONO**</span></span>
</dt> <dd>

<span data-ttu-id="42f7b-126">Filtro de convolução para texturas monocromáticas.</span><span class="sxs-lookup"><span data-stu-id="42f7b-126">Convolution filter for monochrome textures.</span></span> <span data-ttu-id="42f7b-127">Consulte [D3DFMT \_ a1](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="42f7b-127">See [D3DFMT\_A1](d3dformat.md).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f7b-128">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="42f7b-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="42f7b-129">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="42f7b-129">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

<span data-ttu-id="42f7b-130">Use with [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) é indefinido.</span><span class="sxs-lookup"><span data-stu-id="42f7b-130">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="42f7b-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="42f7b-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="42f7b-132">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="42f7b-132">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="42f7b-133">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="42f7b-133">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="42f7b-134">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="42f7b-134">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42f7b-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="42f7b-135">Remarks</span></span>

<span data-ttu-id="42f7b-136">D3DTEXTUREFILTERTYPE é usado por [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) junto com [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) para definir modos de filtragem de textura para um estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="42f7b-136">D3DTEXTUREFILTERTYPE is used by [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) along with [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) to define texture filtering modes for a texture stage.</span></span>

<span data-ttu-id="42f7b-137">Para verificar se um formato dá suporte a tipos de filtro de textura diferentes do \_ ponto D3DTEXF (que sempre há suporte), chame [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) com \_ filtro de consulta D3DUSAGE \_ .</span><span class="sxs-lookup"><span data-stu-id="42f7b-137">To check if a format supports texture filter types other than D3DTEXF\_POINT (which is always supported), call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_FILTER.</span></span>

<span data-ttu-id="42f7b-138">Defina o filtro de ampliação de um estágio de textura chamando [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) com o \_ valor MAGFILTER D3DSAMP como o segundo parâmetro e um membro dessa enumeração como o terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="42f7b-138">Set a texture stage's magnification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="42f7b-139">Defina o filtro minificação de um estágio de textura chamando [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) com o \_ valor D3DSAMP MINFILTER como o segundo parâmetro e um membro dessa enumeração como o terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="42f7b-139">Set a texture stage's minification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="42f7b-140">Defina o filtro de textura para usar os níveis entre-mipmap chamando [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) com o \_ valor D3DSAMP MIPFILTER como o segundo parâmetro e um membro dessa enumeração como o terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="42f7b-140">Set the texture filter to use between-mipmap levels by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="42f7b-141">Nem todos os modos de filtragem válidos para um dispositivo serão aplicados aos mapas de volume.</span><span class="sxs-lookup"><span data-stu-id="42f7b-141">Not all valid filtering modes for a device will apply to volume maps.</span></span> <span data-ttu-id="42f7b-142">Em geral, os \_ \_ filtros de ampliação linear de ponto D3DTEXF e D3DTEXF terão suporte para mapas de volume.</span><span class="sxs-lookup"><span data-stu-id="42f7b-142">In general, D3DTEXF\_POINT and D3DTEXF\_LINEAR magnification filters will be supported for volume maps.</span></span> <span data-ttu-id="42f7b-143">Se D3DPTEXTURECAPS \_ MIPVOLUMEMAP for definido, o filtro de \_ MIPMAP do D3DTEXF Point e os \_ filtros D3DTEXF Point e D3DTEXF \_ line linear terão suporte para mapas de volume.</span><span class="sxs-lookup"><span data-stu-id="42f7b-143">If D3DPTEXTURECAPS\_MIPVOLUMEMAP is set, then the D3DTEXF\_POINT mipmap filter and D3DTEXF\_POINT and D3DTEXF\_LINEAR minification filters will be supported for volume maps.</span></span> <span data-ttu-id="42f7b-144">O dispositivo pode ou não dar suporte ao \_ filtro mipmap linear D3DTEXF para mapas de volume.</span><span class="sxs-lookup"><span data-stu-id="42f7b-144">The device may or may not support the D3DTEXF\_LINEAR mipmap filter for volume maps.</span></span> <span data-ttu-id="42f7b-145">Os dispositivos que dão suporte à filtragem de anisotropic para mapas 2D não necessariamente dão suporte à filtragem de anisotropic para mapas de volume.</span><span class="sxs-lookup"><span data-stu-id="42f7b-145">Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps.</span></span> <span data-ttu-id="42f7b-146">No entanto, os aplicativos que habilitam a filtragem de anisotropic receberão a melhor filtragem disponível (provavelmente linear) se não houver suporte para a filtragem de anisotropic.</span><span class="sxs-lookup"><span data-stu-id="42f7b-146">However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="42f7b-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42f7b-147">Requirements</span></span>



| <span data-ttu-id="42f7b-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="42f7b-148">Requirement</span></span> | <span data-ttu-id="42f7b-149">Valor</span><span class="sxs-lookup"><span data-stu-id="42f7b-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42f7b-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42f7b-150">Header</span></span><br/> | <dl> <span data-ttu-id="42f7b-151"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="42f7b-151"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f7b-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="42f7b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f7b-153">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="42f7b-153">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="42f7b-154">**ID3DXPatchMesh::GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="42f7b-154">**ID3DXPatchMesh::GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="42f7b-155">**ID3DXPatchMesh::SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="42f7b-155">**ID3DXPatchMesh::SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="42f7b-156">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="42f7b-156">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> <dt>

[<span data-ttu-id="42f7b-157">**IDirect3DDevice9::SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="42f7b-157">**IDirect3DDevice9::SetSamplerState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
