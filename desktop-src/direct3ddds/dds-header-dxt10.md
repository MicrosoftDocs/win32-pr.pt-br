---
title: Estrutura de DDS_HEADER_DXT10 (DDS. h)
description: Extensão de cabeçalho DDS para manipular matrizes de recursos, formatos de pixel DXGI que não mapeiam para as estruturas de formato de pixel do Microsoft DirectDraw herdado e metadados adicionais.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10 de estrutura DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764190"
---
# <a name="dds_header_dxt10-structure"></a><span data-ttu-id="befa2-104">Estrutura de DXT10 de \_ cabeçalho DDS \_</span><span class="sxs-lookup"><span data-stu-id="befa2-104">DDS\_HEADER\_DXT10 structure</span></span>

<span data-ttu-id="befa2-105">Extensão de cabeçalho DDS para manipular matrizes de recursos, formatos de pixel DXGI que não mapeiam para as estruturas de formato de pixel do Microsoft DirectDraw herdado e metadados adicionais.</span><span class="sxs-lookup"><span data-stu-id="befa2-105">DDS header extension to handle resource arrays, DXGI pixel formats that don't map to the legacy Microsoft DirectDraw pixel format structures, and additional metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="befa2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="befa2-106">Syntax</span></span>


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a><span data-ttu-id="befa2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="befa2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="befa2-108">**dxgiFormat**</span><span class="sxs-lookup"><span data-stu-id="befa2-108">**dxgiFormat**</span></span>
</dt> <dd>

<span data-ttu-id="befa2-109">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="befa2-109">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="befa2-110">O formato de pixel de superfície (consulte o [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="befa2-110">The surface pixel format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span>

</dd> <dt>

<span data-ttu-id="befa2-111">**resourceDimension**</span><span class="sxs-lookup"><span data-stu-id="befa2-111">**resourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="befa2-112">Tipo: **[ **d3d10 \_ \_ dimensão de recurso**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="befa2-112">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="befa2-113">Identifica o tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="befa2-113">Identifies the type of resource.</span></span> <span data-ttu-id="befa2-114">Os valores a seguir para esse membro são um subconjunto dos valores na [**\_ \_ dimensão de recurso d3d10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) ou enumeração de [**\_ \_ dimensão de recurso D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) :</span><span class="sxs-lookup"><span data-stu-id="befa2-114">The following values for this member are a subset of the values in the [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) or [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) enumeration:</span></span>



| <span data-ttu-id="befa2-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="befa2-115">Type</span></span>                                                              | <span data-ttu-id="befa2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="befa2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="befa2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="befa2-117">Value</span></span> |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="befa2-118">DDS \_ Dimension \_ TEXTURE1D ( \_ TEXTURE1D de dimensão de recurso d3d10 \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="befa2-118">DDS\_DIMENSION\_TEXTURE1D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE1D)</span></span> | <span data-ttu-id="befa2-119">O recurso é uma [textura 1D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span><span class="sxs-lookup"><span data-stu-id="befa2-119">Resource is a [1D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span></span> <span data-ttu-id="befa2-120">O membro **dwWidth** do [**\_ cabeçalho DDS**](dds-header.md) especifica o tamanho da textura.</span><span class="sxs-lookup"><span data-stu-id="befa2-120">The **dwWidth** member of [**DDS\_HEADER**](dds-header.md) specifies the size of the texture.</span></span> <span data-ttu-id="befa2-121">Normalmente, você define o membro **dwHeight** do **\_ cabeçalho DDS** como 1; você também deve definir o \_ sinalizador de altura DDSD no membro **dwFlags** do **\_ cabeçalho DDS**.</span><span class="sxs-lookup"><span data-stu-id="befa2-121">Typically, you set the **dwHeight** member of **DDS\_HEADER** to 1; you also must set the DDSD\_HEIGHT flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                      | <span data-ttu-id="befa2-122">2</span><span class="sxs-lookup"><span data-stu-id="befa2-122">2</span></span>     |
| <span data-ttu-id="befa2-123">DDS \_ Dimension \_ TEXTURE2D ( \_ TEXTURE2D de dimensão de recurso d3d10 \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="befa2-123">DDS\_DIMENSION\_TEXTURE2D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE2D)</span></span> | <span data-ttu-id="befa2-124">O recurso é uma [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) com uma área especificada pelos membros **dwWidth** e **dwHeight** do [**\_ cabeçalho DDS**](dds-header.md).</span><span class="sxs-lookup"><span data-stu-id="befa2-124">Resource is a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with an area specified by the **dwWidth** and **dwHeight** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="befa2-125">Você também pode usar esse tipo para identificar uma textura de mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="befa2-125">You can also use this type to identify a cube-map texture.</span></span> <span data-ttu-id="befa2-126">Para obter mais informações sobre como identificar uma textura de mapa de cubo, consulte **miscFlag** e **Members** .</span><span class="sxs-lookup"><span data-stu-id="befa2-126">For more information about how to identify a cube-map texture, see **miscFlag** and **arraySize** members.</span></span> | <span data-ttu-id="befa2-127">3</span><span class="sxs-lookup"><span data-stu-id="befa2-127">3</span></span>     |
| <span data-ttu-id="befa2-128">DDS \_ Dimension \_ TEXTURE3D ( \_ TEXTURE3D de dimensão de recurso d3d10 \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="befa2-128">DDS\_DIMENSION\_TEXTURE3D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE3D)</span></span> | <span data-ttu-id="befa2-129">Recurso é uma [textura 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) com um volume especificado pelos membros **dwWidth**, **DwHeight** e **dwDepth** do [**\_ cabeçalho DDS**](dds-header.md).</span><span class="sxs-lookup"><span data-stu-id="befa2-129">Resource is a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with a volume specified by the **dwWidth**, **dwHeight**, and **dwDepth** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="befa2-130">Você também deve definir o \_ sinalizador de profundidade DDSD no membro **dwFlags** do **\_ cabeçalho do DDS**.</span><span class="sxs-lookup"><span data-stu-id="befa2-130">You also must set the DDSD\_DEPTH flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                                                                   | <span data-ttu-id="befa2-131">4</span><span class="sxs-lookup"><span data-stu-id="befa2-131">4</span></span>     |



 

</dd> <dt>

<span data-ttu-id="befa2-132">**miscFlag**</span><span class="sxs-lookup"><span data-stu-id="befa2-132">**miscFlag**</span></span>
</dt> <dd>

<span data-ttu-id="befa2-133">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="befa2-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="befa2-134">Identifica outras opções menos comuns para recursos.</span><span class="sxs-lookup"><span data-stu-id="befa2-134">Identifies other, less common options for resources.</span></span> <span data-ttu-id="befa2-135">O valor a seguir para esse membro é um subconjunto dos valores no [**\_ \_ \_ sinalizador diD3D10 do recurso**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) ou enumeração de [**\_ \_ \_ sinalizador variado do recurso D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) :</span><span class="sxs-lookup"><span data-stu-id="befa2-135">The following value for this member is a subset of the values in the [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) or [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration:</span></span>



| <span data-ttu-id="befa2-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="befa2-136">Type</span></span>                             | <span data-ttu-id="befa2-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="befa2-137">Description</span></span>                                                                                                  | <span data-ttu-id="befa2-138">Valor</span><span class="sxs-lookup"><span data-stu-id="befa2-138">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="befa2-139">\_TEXTURECUBE de recursos de DDS \_ \_</span><span class="sxs-lookup"><span data-stu-id="befa2-139">DDS\_RESOURCE\_MISC\_TEXTURECUBE</span></span> | <span data-ttu-id="befa2-140">Indica que uma [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) é uma textura de mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="befa2-140">Indicates a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) is a cube-map texture.</span></span> | <span data-ttu-id="befa2-141">0x4</span><span class="sxs-lookup"><span data-stu-id="befa2-141">0x4</span></span>   |



 

</dd> <dt>

<span data-ttu-id="befa2-142">**arraySize**</span><span class="sxs-lookup"><span data-stu-id="befa2-142">**arraySize**</span></span>
</dt> <dd>

<span data-ttu-id="befa2-143">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="befa2-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="befa2-144">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="befa2-144">The number of elements in the array.</span></span>

<span data-ttu-id="befa2-145">Para uma [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) que também é uma textura de mapa de cubo, esse número representa o número de cubos.</span><span class="sxs-lookup"><span data-stu-id="befa2-145">For a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) that is also a cube-map texture, this number represents the number of cubes.</span></span> <span data-ttu-id="befa2-146">Esse número é o mesmo que o número no membro **NumCubes** de [**d3d10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) ou [**D3D11 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span><span class="sxs-lookup"><span data-stu-id="befa2-146">This number is the same as the number in the **NumCubes** member of [**D3D10\_TEXCUBE\_ARRAY\_SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) or [**D3D11\_TEXCUBE\_ARRAY\_SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span></span> <span data-ttu-id="befa2-147">Nesse caso, o arquivo **DDS contém** \* 6 texturas 2D.</span><span class="sxs-lookup"><span data-stu-id="befa2-147">In this case, the DDS file contains **arraySize**\*6 2D textures.</span></span> <span data-ttu-id="befa2-148">Para obter mais informações sobre esse caso, consulte a descrição de **miscFlag** .</span><span class="sxs-lookup"><span data-stu-id="befa2-148">For more information about this case, see the **miscFlag** description.</span></span>

<span data-ttu-id="befa2-149">Para uma [textura 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), você deve definir esse número como 1.</span><span class="sxs-lookup"><span data-stu-id="befa2-149">For a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), you must set this number to 1.</span></span>

</dd> <dt>

<span data-ttu-id="befa2-150">**miscFlags2**</span><span class="sxs-lookup"><span data-stu-id="befa2-150">**miscFlags2**</span></span>
</dt> <dd>

<span data-ttu-id="befa2-151">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="befa2-151">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="befa2-152">Contém metadados adicionais (anteriormente reservado).</span><span class="sxs-lookup"><span data-stu-id="befa2-152">Contains additional metadata (formerly was reserved).</span></span> <span data-ttu-id="befa2-153">Os três bits inferiores indicam o modo alfa do recurso associado.</span><span class="sxs-lookup"><span data-stu-id="befa2-153">The lower 3 bits indicate the alpha mode of the associated resource.</span></span> <span data-ttu-id="befa2-154">Os 29 bits superiores são reservados e geralmente são 0.</span><span class="sxs-lookup"><span data-stu-id="befa2-154">The upper 29 bits are reserved and are typically 0.</span></span>



| <span data-ttu-id="befa2-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="befa2-155">Type</span></span>                            | <span data-ttu-id="befa2-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="befa2-156">Description</span></span>                                                                                                                              | <span data-ttu-id="befa2-157">Valor</span><span class="sxs-lookup"><span data-stu-id="befa2-157">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="befa2-158">\_modo alfa do DDS \_ \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="befa2-158">DDS\_ALPHA\_MODE\_UNKNOWN</span></span>       | <span data-ttu-id="befa2-159">O conteúdo do canal alfa é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="befa2-159">Alpha channel content is unknown.</span></span> <span data-ttu-id="befa2-160">Esse é o valor para arquivos herdados, que normalmente é considerado "reto" Alfa.</span><span class="sxs-lookup"><span data-stu-id="befa2-160">This is the value for legacy files, which typically is assumed to be 'straight' alpha.</span></span>                 | <span data-ttu-id="befa2-161">0x0</span><span class="sxs-lookup"><span data-stu-id="befa2-161">0x0</span></span>   |
| <span data-ttu-id="befa2-162">\_modo alfa do DDS \_ \_ reto</span><span class="sxs-lookup"><span data-stu-id="befa2-162">DDS\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="befa2-163">Todo o conteúdo do canal alfa é presumido usar alfa reto.</span><span class="sxs-lookup"><span data-stu-id="befa2-163">Any alpha channel content is presumed to use straight alpha.</span></span>                                                                             | <span data-ttu-id="befa2-164">0x1</span><span class="sxs-lookup"><span data-stu-id="befa2-164">0x1</span></span>   |
| <span data-ttu-id="befa2-165">modo alfa do DDS pré- \_ \_ \_ multiplicado</span><span class="sxs-lookup"><span data-stu-id="befa2-165">DDS\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="befa2-166">Qualquer conteúdo de canal alfa está usando alfa precalculado.</span><span class="sxs-lookup"><span data-stu-id="befa2-166">Any alpha channel content is using premultiplied alpha.</span></span> <span data-ttu-id="befa2-167">Os únicos formatos de arquivo herdados que indicam essas informações são ' DX2 ' e ' DX4 '.</span><span class="sxs-lookup"><span data-stu-id="befa2-167">The only legacy file formats that indicate this information are 'DX2' and 'DX4'.</span></span> | <span data-ttu-id="befa2-168">0x2</span><span class="sxs-lookup"><span data-stu-id="befa2-168">0x2</span></span>   |
| <span data-ttu-id="befa2-169">\_modo alfa do DDS \_ \_ opaco</span><span class="sxs-lookup"><span data-stu-id="befa2-169">DDS\_ALPHA\_MODE\_OPAQUE</span></span>        | <span data-ttu-id="befa2-170">Qualquer conteúdo do canal alfa é definido como totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="befa2-170">Any alpha channel content is all set to fully opaque.</span></span>                                                                                    | <span data-ttu-id="befa2-171">0x3</span><span class="sxs-lookup"><span data-stu-id="befa2-171">0x3</span></span>   |
| <span data-ttu-id="befa2-172">\_modo alfa do DDS \_ \_ personalizado</span><span class="sxs-lookup"><span data-stu-id="befa2-172">DDS\_ALPHA\_MODE\_CUSTOM</span></span>        | <span data-ttu-id="befa2-173">Qualquer conteúdo do canal alfa está sendo usado como um 4º Channel e não se destina a representar a transparência (reta ou premultiplicada).</span><span class="sxs-lookup"><span data-stu-id="befa2-173">Any alpha channel content is being used as a 4th channel and is not intended to represent transparency (straight or premultiplied).</span></span>      | <span data-ttu-id="befa2-174">0x4</span><span class="sxs-lookup"><span data-stu-id="befa2-174">0x4</span></span>   |



 

> [!Note]  
> <span data-ttu-id="befa2-175">As bibliotecas de utilitários herdadas D3DX 10 e [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) falharão ao carregar qualquer. O arquivo DDS com **miscFlags2** não é igual a zero.</span><span class="sxs-lookup"><span data-stu-id="befa2-175">The legacy D3DX 10 and [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) utility libraries will fail to load any .DDS file with **miscFlags2** not equal to zero.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="befa2-176">Comentários</span><span class="sxs-lookup"><span data-stu-id="befa2-176">Remarks</span></span>

<span data-ttu-id="befa2-177">Use essa estrutura junto com um [**\_ cabeçalho DDS**](dds-header.md) para armazenar uma matriz de recursos em um arquivo DDS.</span><span class="sxs-lookup"><span data-stu-id="befa2-177">Use this structure together with a [**DDS\_HEADER**](dds-header.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="befa2-178">Para obter mais informações, consulte [matrizes de textura](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="befa2-178">For more info, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="befa2-179">Esse cabeçalho estará presente se o membro **dwFourCC** da estrutura [**de \_ PIXELFORMAT do DDS**](dds-pixelformat.md) estiver definido como ' DX10 '.</span><span class="sxs-lookup"><span data-stu-id="befa2-179">This header is present if the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](dds-pixelformat.md) structure is set to 'DX10'.</span></span>

## <a name="requirements"></a><span data-ttu-id="befa2-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="befa2-180">Requirements</span></span>



| <span data-ttu-id="befa2-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="befa2-181">Requirement</span></span> | <span data-ttu-id="befa2-182">Valor</span><span class="sxs-lookup"><span data-stu-id="befa2-182">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="befa2-183">parâmetro</span><span class="sxs-lookup"><span data-stu-id="befa2-183">Header</span></span><br/> | <dl> <span data-ttu-id="befa2-184"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="befa2-184"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="befa2-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="befa2-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befa2-186">Referência para DDS</span><span class="sxs-lookup"><span data-stu-id="befa2-186">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

