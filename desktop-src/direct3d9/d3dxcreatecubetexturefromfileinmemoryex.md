---
description: Cria uma textura de cubo a partir de um arquivo na memória. Essa é uma função mais avançada do que D3DXCreateCubeTextureFromFileInMemory.
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: Função D3DXCreateCubeTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7813d4532bbde18a5fc7fd7d1d090dc72eccd61f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012160"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a><span data-ttu-id="906f0-104">Função D3DXCreateCubeTextureFromFileInMemoryEx</span><span class="sxs-lookup"><span data-stu-id="906f0-104">D3DXCreateCubeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="906f0-105">Cria uma textura de cubo a partir de um arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="906f0-105">Creates a cube texture from a file in memory.</span></span> <span data-ttu-id="906f0-106">Essa é uma função mais avançada do que [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="906f0-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="906f0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="906f0-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="906f0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="906f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="906f0-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="906f0-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="906f0-111">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="906f0-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-112">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-113">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="906f0-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="906f0-114">Ponteiro para o arquivo na memória a partir da qual criar a textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="906f0-114">Pointer to the file in memory from which to create the cube texture.</span></span> <span data-ttu-id="906f0-115">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="906f0-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-116">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-116">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="906f0-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="906f0-118">Tamanho do arquivo na memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="906f0-118">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-119">*Tamanho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-119">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="906f0-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="906f0-121">Largura (ou altura) em pixels.</span><span class="sxs-lookup"><span data-stu-id="906f0-121">Width (or height) in pixels.</span></span> <span data-ttu-id="906f0-122">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="906f0-122">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-123">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="906f0-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="906f0-125">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="906f0-125">Number of mip levels requested.</span></span> <span data-ttu-id="906f0-126">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="906f0-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-127">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="906f0-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="906f0-129">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="906f0-129">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="906f0-130">Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="906f0-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="906f0-131">O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="906f0-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="906f0-132">Se D3DUSAGE \_ RENDERTARGET for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação [**chamando CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="906f0-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="906f0-133">Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="906f0-133">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="906f0-134">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-134">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-135">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="906f0-135">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="906f0-136">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="906f0-136">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="906f0-137">A textura retornada pode ter um formato diferente daquele especificado pelo *formato*.</span><span class="sxs-lookup"><span data-stu-id="906f0-137">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="906f0-138">Os aplicativos devem verificar o formato da textura retornada.</span><span class="sxs-lookup"><span data-stu-id="906f0-138">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="906f0-139">Se [D3DFMT \_ desconhecido](other-d3dx-constants.md), o formato será extraído do arquivo.</span><span class="sxs-lookup"><span data-stu-id="906f0-139">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="906f0-140">Se D3DFMT \_ do \_ arquivo, o formato será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="906f0-140">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-141">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-141">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-142">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="906f0-142">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="906f0-143">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura do cubo deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="906f0-143">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-144">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-144">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-145">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="906f0-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="906f0-146">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="906f0-146">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="906f0-147">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="906f0-147">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-148">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-148">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="906f0-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="906f0-150">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="906f0-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="906f0-151">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="906f0-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="906f0-152">Além disso, use o bits 27-31 para especificar o número de níveis MIP a serem ignorados (da parte superior da cadeia mipmap) quando uma textura. DDS for carregada na memória; Isso permite que você pule até 32 níveis.</span><span class="sxs-lookup"><span data-stu-id="906f0-152">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-153">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="906f0-153">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-154">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="906f0-154">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="906f0-155">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="906f0-155">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="906f0-156">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="906f0-156">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="906f0-157">Alfa é significativo e normalmente deve ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="906f0-157">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="906f0-158">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="906f0-158">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-159">*pSrcInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="906f0-159">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-160">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="906f0-160">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="906f0-161">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="906f0-161">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-162">*pPalette* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="906f0-162">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-163">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="906f0-163">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="906f0-164">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , representando uma paleta de cor de 256 para preencher ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="906f0-164">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="906f0-165">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="906f0-165">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="906f0-166">*ppCubeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="906f0-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="906f0-167">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="906f0-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="906f0-168">Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , que representa o objeto de textura do cubo criado.</span><span class="sxs-lookup"><span data-stu-id="906f0-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="906f0-169">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="906f0-169">Return value</span></span>

<span data-ttu-id="906f0-170">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="906f0-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="906f0-171">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="906f0-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="906f0-172">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="906f0-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="906f0-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="906f0-173">Remarks</span></span>

<span data-ttu-id="906f0-174">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="906f0-174">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="906f0-175">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="906f0-175">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="906f0-176">Texturas de cubos diferem de outras superfícies em que são coleções de superfícies.</span><span class="sxs-lookup"><span data-stu-id="906f0-176">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="906f0-177">Para chamar [**SetRenderTarget**](/windows/desktop/api) com uma textura de cubo, você deve selecionar uma face individual usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passar a superfície resultante para **SetRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="906f0-177">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget** .</span></span>

<span data-ttu-id="906f0-178">Esse método foi projetado para ser usado para carregar arquivos de imagem armazenados como RT \_ RCDATA, que é um recurso definido pelo aplicativo (dados brutos).</span><span class="sxs-lookup"><span data-stu-id="906f0-178">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="906f0-179">Caso contrário, esse método falhará.</span><span class="sxs-lookup"><span data-stu-id="906f0-179">Otherwise this method will fail.</span></span>

<span data-ttu-id="906f0-180">Para obter detalhes sobre o [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), consulte o SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="906f0-180">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="906f0-181">Observe que, a partir do DirectX 8,0, o membro peFlags da estrutura **PaletteEntry** não funciona conforme documentado no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="906f0-181">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="906f0-182">O membro peFlags agora é o canal alfa para formatos de palettized de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="906f0-182">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="906f0-183">**D3DXCreateCubeTextureFromFileInMemoryEx** usa o formato de arquivo de superfície do DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="906f0-183">**D3DXCreateCubeTextureFromFileInMemoryEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="906f0-184">O editor de textura DirectX (Dxtex.exe) permite que você gere um mapa de cubo de outros formatos de arquivo e salve-o no formato de arquivo DDS.</span><span class="sxs-lookup"><span data-stu-id="906f0-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="906f0-185">Você pode obter Dxtex.exe e aprender sobre ele no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="906f0-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="906f0-186">Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="906f0-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="906f0-187">Ao ignorar os níveis de mipmap ao carregar um arquivo. DDS, use a \_ \_ macro D3DX \_ ignorar \_ os níveis de MIP do DDS para gerar o valor de MipFilter.</span><span class="sxs-lookup"><span data-stu-id="906f0-187">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="906f0-188">Essa macro usa o número de níveis a serem ignorados e o tipo de filtro e retorna o valor do filtro, que seria passado para o parâmetro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="906f0-188">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="906f0-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="906f0-189">Requirements</span></span>



| <span data-ttu-id="906f0-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="906f0-190">Requirement</span></span> | <span data-ttu-id="906f0-191">Valor</span><span class="sxs-lookup"><span data-stu-id="906f0-191">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="906f0-192">parâmetro</span><span class="sxs-lookup"><span data-stu-id="906f0-192">Header</span></span><br/>  | <dl> <span data-ttu-id="906f0-193"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="906f0-193"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="906f0-194">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="906f0-194">Library</span></span><br/> | <dl> <span data-ttu-id="906f0-195"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="906f0-195"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="906f0-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="906f0-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="906f0-197">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="906f0-197">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
