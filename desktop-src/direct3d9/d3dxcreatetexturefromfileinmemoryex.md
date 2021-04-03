---
description: Cria uma textura de um arquivo na memória. Essa é uma função mais avançada do que D3DXCreateTextureFromFileInMemory.
ms.assetid: e515697c-0e24-4d96-b58a-dc4f27683021
title: Função D3DXCreateTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da85af9e70a7971ba0bab1f76e9c3d30c3cc2884
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930602"
---
# <a name="d3dxcreatetexturefromfileinmemoryex-function"></a><span data-ttu-id="5110a-104">Função D3DXCreateTextureFromFileInMemoryEx</span><span class="sxs-lookup"><span data-stu-id="5110a-104">D3DXCreateTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="5110a-105">Cria uma textura de um arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="5110a-105">Creates a texture from a file in memory.</span></span> <span data-ttu-id="5110a-106">Essa é uma função mais avançada do que [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="5110a-106">This is a more advanced function than [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5110a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5110a-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCVOID            pSrcData,
  _In_    UINT               SrcDataSize,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="5110a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5110a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5110a-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5110a-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5110a-111">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="5110a-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-112">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-113">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5110a-114">Ponteiro para o arquivo na memória a partir da qual criar a textura.</span><span class="sxs-lookup"><span data-stu-id="5110a-114">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-115">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5110a-117">Tamanho do arquivo na memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5110a-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-118">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5110a-120">Largura em pixels.</span><span class="sxs-lookup"><span data-stu-id="5110a-120">Width in pixels.</span></span> <span data-ttu-id="5110a-121">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5110a-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-122">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-122">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5110a-124">Altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="5110a-124">Height, in pixels.</span></span> <span data-ttu-id="5110a-125">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5110a-125">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-126">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5110a-128">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="5110a-128">Number of mip levels requested.</span></span> <span data-ttu-id="5110a-129">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="5110a-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-130">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5110a-132">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="5110a-132">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="5110a-133">Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="5110a-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="5110a-134">O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="5110a-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="5110a-135">Se D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic for especificado, o *pool* deverá ser definido como D3DPOOL \_ padrão e o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="5110a-135">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="5110a-136">Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="5110a-136">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="5110a-137">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-137">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-138">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-138">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="5110a-139">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura.</span><span class="sxs-lookup"><span data-stu-id="5110a-139">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="5110a-140">A textura retornada pode ter um formato diferente daquele especificado pelo *formato*.</span><span class="sxs-lookup"><span data-stu-id="5110a-140">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="5110a-141">Os aplicativos devem verificar o formato da textura retornada.</span><span class="sxs-lookup"><span data-stu-id="5110a-141">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="5110a-142">Se [D3DFMT \_ desconhecido](other-d3dx-constants.md), o formato será extraído do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5110a-142">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="5110a-143">Se D3DFMT \_ do \_ arquivo, o formato será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5110a-143">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-144">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-144">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-145">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-145">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="5110a-146">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="5110a-146">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-147">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-147">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-148">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-148">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5110a-149">Combinação de um ou mais sinalizadores que controlam como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="5110a-149">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="5110a-150">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5110a-150">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="5110a-151">Cada filtro válido deve conter um dos sinalizadores no [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="5110a-151">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> <dt>

<span data-ttu-id="5110a-152">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-153">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5110a-154">Combinação de um ou mais sinalizadores que controlam como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="5110a-154">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="5110a-155">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="5110a-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="5110a-156">Cada filtro válido deve conter um dos sinalizadores no [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="5110a-156">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span> <span data-ttu-id="5110a-157">Além disso, use o bits 27-31 para especificar o número de níveis MIP a serem ignorados (da parte superior da cadeia mipmap) quando uma textura. DDS for carregada na memória; Isso permite que você pule até 32 níveis.</span><span class="sxs-lookup"><span data-stu-id="5110a-157">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-158">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5110a-158">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-159">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="5110a-159">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="5110a-160">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="5110a-160">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="5110a-161">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="5110a-161">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="5110a-162">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="5110a-162">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="5110a-163">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="5110a-163">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-164">*pSrcInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5110a-164">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-165">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="5110a-165">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="5110a-166">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5110a-166">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-167">*pPalette* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5110a-167">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-168">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="5110a-168">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="5110a-169">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , representando uma paleta de cor de 256 para preencher ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5110a-169">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="5110a-170">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="5110a-170">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5110a-171">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5110a-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5110a-172">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="5110a-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="5110a-173">Endereço de um ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="5110a-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5110a-174">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5110a-174">Return value</span></span>

<span data-ttu-id="5110a-175">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5110a-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5110a-176">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5110a-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5110a-177">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5110a-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5110a-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="5110a-178">Remarks</span></span>

<span data-ttu-id="5110a-179">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="5110a-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="5110a-180">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="5110a-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="5110a-181">Para obter detalhes sobre o [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), consulte o SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="5110a-181">For details about [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="5110a-182">Observe que, a partir do DirectX 8,0, o membro peFlags da estrutura **PaletteEntry** não funciona conforme documentado no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="5110a-182">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="5110a-183">O membro peFlags agora é o canal alfa para formatos de palettized de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="5110a-183">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="5110a-184">Ao ignorar os níveis de mipmap ao carregar um arquivo. DDS, use a \_ \_ macro D3DX \_ ignorar \_ os níveis de MIP do DDS para gerar o valor de MipFilter.</span><span class="sxs-lookup"><span data-stu-id="5110a-184">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="5110a-185">Essa macro usa o número de níveis a serem ignorados e o tipo de filtro e retorna o valor do filtro, que seria passado para o parâmetro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="5110a-185">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5110a-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5110a-186">Requirements</span></span>



| <span data-ttu-id="5110a-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="5110a-187">Requirement</span></span> | <span data-ttu-id="5110a-188">Valor</span><span class="sxs-lookup"><span data-stu-id="5110a-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5110a-189">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5110a-189">Header</span></span><br/>  | <dl> <span data-ttu-id="5110a-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5110a-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5110a-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5110a-191">Library</span></span><br/> | <dl> <span data-ttu-id="5110a-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5110a-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5110a-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="5110a-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5110a-194">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="5110a-194">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="5110a-195">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="5110a-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
