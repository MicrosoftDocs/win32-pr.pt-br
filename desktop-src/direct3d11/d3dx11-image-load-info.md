---
title: Estrutura de D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas. | Estrutura de D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- Estrutura D3DX11_IMAGE_LOAD_INFO Direct3D 11
- Ponteiro de estrutura LPD3DX11_IMAGE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968692"
---
# <a name="d3dx11_image_load_info-structure"></a><span data-ttu-id="96481-107">\_Estrutura de \_ informações de carregamento de imagem D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="96481-107">D3DX11\_IMAGE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="96481-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="96481-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="96481-109">Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas.</span><span class="sxs-lookup"><span data-stu-id="96481-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="96481-110">Um valor de D3DX11 \_ padrão para qualquer um desses parâmetros fará com que o D3DX use automaticamente o valor do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="96481-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="96481-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96481-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="96481-112">Membros</span><span class="sxs-lookup"><span data-stu-id="96481-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="96481-113">**Largura**</span><span class="sxs-lookup"><span data-stu-id="96481-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="96481-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96481-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-115">A largura de destino da textura.</span><span class="sxs-lookup"><span data-stu-id="96481-115">The target width of the texture.</span></span> <span data-ttu-id="96481-116">Se a largura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa largura de destino.</span><span class="sxs-lookup"><span data-stu-id="96481-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="96481-117">**Altura**</span><span class="sxs-lookup"><span data-stu-id="96481-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="96481-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96481-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-119">A altura de destino da textura.</span><span class="sxs-lookup"><span data-stu-id="96481-119">The target height of the texture.</span></span> <span data-ttu-id="96481-120">Se a altura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa altura de destino.</span><span class="sxs-lookup"><span data-stu-id="96481-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="96481-121">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="96481-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="96481-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96481-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-123">A profundidade da textura.</span><span class="sxs-lookup"><span data-stu-id="96481-123">The depth of the texture.</span></span> <span data-ttu-id="96481-124">Isso se aplica somente a texturas de volume.</span><span class="sxs-lookup"><span data-stu-id="96481-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="96481-125">**FirstMipLevel**</span><span class="sxs-lookup"><span data-stu-id="96481-125">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="96481-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96481-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-127">O nível de mipmap de resolução mais alto da textura.</span><span class="sxs-lookup"><span data-stu-id="96481-127">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="96481-128">Se for maior que 0, depois que a textura for carregada, FirstMipLevel será mapeado para o nível de mipmap 0.</span><span class="sxs-lookup"><span data-stu-id="96481-128">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="96481-129">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="96481-129">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="96481-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96481-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-131">O número máximo de níveis de mipmap na textura.</span><span class="sxs-lookup"><span data-stu-id="96481-131">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="96481-132">Consulte os comentários em [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="96481-132">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="96481-133">Usar 0 ou D3DX11 \_ padrão fará com que uma cadeia de mipmap completa seja criada.</span><span class="sxs-lookup"><span data-stu-id="96481-133">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="96481-134">**Usage**</span><span class="sxs-lookup"><span data-stu-id="96481-134">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="96481-135">Tipo: **[ **\_ uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span><span class="sxs-lookup"><span data-stu-id="96481-135">Type: **[**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-136">A maneira como o recurso de textura deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="96481-136">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="96481-137">Consulte [**\_ uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="96481-137">See [**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span>

</dd> <dt>

<span data-ttu-id="96481-138">**BindFlags**</span><span class="sxs-lookup"><span data-stu-id="96481-138">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="96481-139">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96481-139">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-140">Os estágios de pipeline aos quais a textura terá permissão de associação.</span><span class="sxs-lookup"><span data-stu-id="96481-140">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="96481-141">Consulte [**\_ \_ sinalizador de ligação D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="96481-141">See [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="96481-142">**CpuAccessFlags**</span><span class="sxs-lookup"><span data-stu-id="96481-142">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="96481-143">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96481-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-144">As permissões de acesso que a CPU terá para o recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="96481-144">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="96481-145">Consulte [**\_ sinalizador de \_ acesso \_ de CPU D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="96481-145">See [**D3D11\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="96481-146">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="96481-146">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="96481-147">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96481-147">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-148">Propriedades de recurso diversas ( [**consulte \_ \_ \_ sinalizador D3D11 do recurso**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="96481-148">Miscellaneous resource properties (see [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="96481-149">**Formato**</span><span class="sxs-lookup"><span data-stu-id="96481-149">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="96481-150">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="96481-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-151">Uma enumeração de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) que indica o formato em que a textura estará depois de ser carregada.</span><span class="sxs-lookup"><span data-stu-id="96481-151">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration indicating the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="96481-152">**Filter**</span><span class="sxs-lookup"><span data-stu-id="96481-152">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="96481-153">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96481-153">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-154">Filtre a textura usando o filtro especificado (somente ao reamostrar).</span><span class="sxs-lookup"><span data-stu-id="96481-154">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="96481-155">Consulte [**\_ \_ sinalizador de filtro D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="96481-155">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="96481-156">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="96481-156">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="96481-157">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96481-157">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="96481-158">Filtre os níveis de MIP de textura usando o filtro especificado (somente se estiver gerando mipmaps).</span><span class="sxs-lookup"><span data-stu-id="96481-158">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="96481-159">Os valores válidos são \_ filtro D3DX11 \_ nenhum, \_ ponto de filtro D3DX11 \_ , filtro de D3DX11 \_ \_ linear ou triângulo de filtro de D3DX11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="96481-159">Valid values are D3DX11\_FILTER\_NONE, D3DX11\_FILTER\_POINT, D3DX11\_FILTER\_LINEAR, or D3DX11\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="96481-160">Consulte [**\_ \_ sinalizador de filtro D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="96481-160">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="96481-161">**pSrcInfo**</span><span class="sxs-lookup"><span data-stu-id="96481-161">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="96481-162">Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="96481-162">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="96481-163">Informações sobre a imagem original.</span><span class="sxs-lookup"><span data-stu-id="96481-163">Information about the original image.</span></span> <span data-ttu-id="96481-164">Consulte [**D3DX11 \_ Image \_ info**](d3dx11-image-info.md).</span><span class="sxs-lookup"><span data-stu-id="96481-164">See [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md).</span></span> <span data-ttu-id="96481-165">Pode ser obtido com [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)ou [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="96481-165">Can be obtained with [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96481-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="96481-166">Remarks</span></span>

<span data-ttu-id="96481-167">Ao inicializar a estrutura, você pode definir qualquer membro como D3DX11 \_ padrão e D3DX irá inicializá-lo com um valor padrão da textura de origem quando a textura for carregada.</span><span class="sxs-lookup"><span data-stu-id="96481-167">When initializing the structure, you may set any member to D3DX11\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="96481-168">Essa estrutura pode ser usada por APIs que:</span><span class="sxs-lookup"><span data-stu-id="96481-168">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="96481-169">Crie recursos, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="96481-169">Create resources, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="96481-170">Crie processadores de dados, como [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) ou [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="96481-170">Create data processors, such as [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) or [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span></span>

<span data-ttu-id="96481-171">Os valores padrão são:</span><span class="sxs-lookup"><span data-stu-id="96481-171">The default values are:</span></span>


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



<span data-ttu-id="96481-172">Aqui está um breve exemplo que usa essa estrutura para fornecer o formato de pixel ao carregar uma textura.</span><span class="sxs-lookup"><span data-stu-id="96481-172">Here is a brief example that uses this structure to supply the pixel format when loading a texture.</span></span> <span data-ttu-id="96481-173">Para obter o código completo, consulte HDRFormats10. cpp no [exemplo de HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="96481-173">For the complete code, see HDRFormats10.cpp in [HDRToneMappingCS11 Sample](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span></span>


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a><span data-ttu-id="96481-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96481-174">Requirements</span></span>



| <span data-ttu-id="96481-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="96481-175">Requirement</span></span> | <span data-ttu-id="96481-176">Valor</span><span class="sxs-lookup"><span data-stu-id="96481-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96481-177">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96481-177">Header</span></span><br/> | <dl> <span data-ttu-id="96481-178"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="96481-178"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96481-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="96481-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96481-180">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="96481-180">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

