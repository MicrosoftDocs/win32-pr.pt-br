---
description: Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas. Um valor de D3DX10 \_ padrão para qualquer um desses parâmetros fará com que o D3DX use automaticamente o valor do arquivo de origem.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: Estrutura de D3DX10_IMAGE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812374"
---
# <a name="d3dx10_image_load_info-structure"></a><span data-ttu-id="9de58-104">\_Estrutura de \_ informações de carregamento de imagem D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="9de58-104">D3DX10\_IMAGE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="9de58-105">Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas.</span><span class="sxs-lookup"><span data-stu-id="9de58-105">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="9de58-106">Um valor de D3DX10 \_ padrão para qualquer um desses parâmetros fará com que o D3DX use automaticamente o valor do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="9de58-106">A value of D3DX10\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9de58-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9de58-107">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="9de58-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9de58-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9de58-109">**Largura**</span><span class="sxs-lookup"><span data-stu-id="9de58-109">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de58-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-111">A largura de destino da textura.</span><span class="sxs-lookup"><span data-stu-id="9de58-111">The target width of the texture.</span></span> <span data-ttu-id="9de58-112">Se a largura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa largura de destino.</span><span class="sxs-lookup"><span data-stu-id="9de58-112">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="9de58-113">**Altura**</span><span class="sxs-lookup"><span data-stu-id="9de58-113">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de58-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-115">A altura de destino da textura.</span><span class="sxs-lookup"><span data-stu-id="9de58-115">The target height of the texture.</span></span> <span data-ttu-id="9de58-116">Se a altura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa altura de destino.</span><span class="sxs-lookup"><span data-stu-id="9de58-116">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="9de58-117">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="9de58-117">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de58-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-119">A profundidade da textura.</span><span class="sxs-lookup"><span data-stu-id="9de58-119">The depth of the texture.</span></span> <span data-ttu-id="9de58-120">Isso se aplica somente a texturas de volume.</span><span class="sxs-lookup"><span data-stu-id="9de58-120">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="9de58-121">**FirstMipLevel**</span><span class="sxs-lookup"><span data-stu-id="9de58-121">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de58-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-123">O nível de mipmap de resolução mais alto da textura.</span><span class="sxs-lookup"><span data-stu-id="9de58-123">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="9de58-124">Se for maior que 0, depois que a textura for carregada, FirstMipLevel será mapeado para o nível de mipmap 0.</span><span class="sxs-lookup"><span data-stu-id="9de58-124">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="9de58-125">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="9de58-125">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de58-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-127">O número máximo de níveis de mipmap que a textura terá.</span><span class="sxs-lookup"><span data-stu-id="9de58-127">The maximum number of mipmap levels that the texture will have.</span></span> <span data-ttu-id="9de58-128">Usar 0 ou D3DX10 \_ padrão fará com que uma cadeia de mipmap completa seja criada.</span><span class="sxs-lookup"><span data-stu-id="9de58-128">Using 0 or D3DX10\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="9de58-129">**Usage**</span><span class="sxs-lookup"><span data-stu-id="9de58-129">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-130">Tipo: **[ **\_ uso de d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span><span class="sxs-lookup"><span data-stu-id="9de58-130">Type: **[**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-131">A maneira como o recurso de textura deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="9de58-131">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="9de58-132">Consulte [**\_ uso de d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span><span class="sxs-lookup"><span data-stu-id="9de58-132">See [**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

</dd> <dt>

<span data-ttu-id="9de58-133">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="9de58-133">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-134">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de58-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-135">Os estágios de pipeline aos quais a textura terá permissão de associação.</span><span class="sxs-lookup"><span data-stu-id="9de58-135">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="9de58-136">Consulte [**\_ \_ sinalizador de ligação d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="9de58-136">See [**D3D10\_BIND\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="9de58-137">**CpuAccessFlags**</span><span class="sxs-lookup"><span data-stu-id="9de58-137">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-138">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de58-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-139">As permissões de acesso que a CPU terá para o recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="9de58-139">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="9de58-140">Consulte [**\_ sinalizador de \_ acesso \_ de CPU d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="9de58-140">See [**D3D10\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="9de58-141">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="9de58-141">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-142">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de58-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-143">Propriedades de recurso diversas ( [**consulte \_ \_ \_ sinalizador d3d10 do recurso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="9de58-143">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="9de58-144">**Formato**</span><span class="sxs-lookup"><span data-stu-id="9de58-144">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-145">Tipo: **[ **\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="9de58-145">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-146">O formato em que a textura estará depois de ser carregada.</span><span class="sxs-lookup"><span data-stu-id="9de58-146">The format the texture will be in after it is loaded.</span></span> <span data-ttu-id="9de58-147">Consulte [**o \_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="9de58-147">See [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="9de58-148">**Filter**</span><span class="sxs-lookup"><span data-stu-id="9de58-148">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-149">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de58-149">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-150">Filtre a textura usando o filtro especificado (somente ao reamostrar).</span><span class="sxs-lookup"><span data-stu-id="9de58-150">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="9de58-151">Consulte [**\_ \_ sinalizador de filtro D3DX10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="9de58-151">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="9de58-152">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="9de58-152">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-153">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9de58-153">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9de58-154">Filtre os níveis de MIP de textura usando o filtro especificado (somente se estiver gerando mipmaps).</span><span class="sxs-lookup"><span data-stu-id="9de58-154">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="9de58-155">Os valores válidos são \_ filtro D3DX10 \_ nenhum, \_ ponto de filtro D3DX10 \_ , filtro de D3DX10 \_ \_ linear ou triângulo de filtro de D3DX10 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9de58-155">Valid values are D3DX10\_FILTER\_NONE, D3DX10\_FILTER\_POINT, D3DX10\_FILTER\_LINEAR, or D3DX10\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="9de58-156">Consulte [**\_ \_ sinalizador de filtro D3DX10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="9de58-156">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="9de58-157">**pSrcInfo**</span><span class="sxs-lookup"><span data-stu-id="9de58-157">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="9de58-158">Tipo: **[ **D3DX10 \_ Image \_ info**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="9de58-158">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="9de58-159">Informações sobre a imagem original.</span><span class="sxs-lookup"><span data-stu-id="9de58-159">Information about the original image.</span></span> <span data-ttu-id="9de58-160">Consulte [**D3DX10 \_ Image \_ info**](d3dx10-image-info.md).</span><span class="sxs-lookup"><span data-stu-id="9de58-160">See [**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md).</span></span> <span data-ttu-id="9de58-161">Pode ser obtido com [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)ou [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="9de58-161">Can be obtained with [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md), or [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9de58-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="9de58-162">Remarks</span></span>

<span data-ttu-id="9de58-163">Ao inicializar a estrutura, você pode definir qualquer membro como D3DX10 \_ padrão e D3DX irá inicializá-lo com um valor padrão da textura de origem quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="9de58-163">When initializing the structure, you may set any member to D3DX10\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="9de58-164">Essa estrutura pode ser usada por APIs que:</span><span class="sxs-lookup"><span data-stu-id="9de58-164">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="9de58-165">Crie recursos, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="9de58-165">Create resources, such as [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="9de58-166">Crie processadores de dados, como [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) ou [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="9de58-166">Create data processors, such as [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) or [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9de58-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9de58-167">Requirements</span></span>



| <span data-ttu-id="9de58-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="9de58-168">Requirement</span></span> | <span data-ttu-id="9de58-169">Valor</span><span class="sxs-lookup"><span data-stu-id="9de58-169">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9de58-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9de58-170">Header</span></span><br/> | <dl> <span data-ttu-id="9de58-171"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9de58-171"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de58-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="9de58-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de58-173">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="9de58-173">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
