---
description: Cria uma textura de volume a partir de um arquivo.
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: Função D3DXCreateVolumeTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d63377394dc123defac565cd11a0d40324a28a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298629"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a><span data-ttu-id="7c00a-103">Função D3DXCreateVolumeTextureFromFileEx</span><span class="sxs-lookup"><span data-stu-id="7c00a-103">D3DXCreateVolumeTextureFromFileEx function</span></span>

<span data-ttu-id="7c00a-104">Cria uma textura de volume a partir de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c00a-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c00a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c00a-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCTSTR                  pSrcFile,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
          D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="7c00a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c00a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c00a-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7c00a-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="7c00a-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-110">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c00a-112">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c00a-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="7c00a-113">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="7c00a-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7c00a-114">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="7c00a-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="7c00a-115">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="7c00a-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-116">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-116">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c00a-118">Largura em pixels.</span><span class="sxs-lookup"><span data-stu-id="7c00a-118">Width in pixels.</span></span> <span data-ttu-id="7c00a-119">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c00a-119">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="7c00a-120">A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="7c00a-120">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-121">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-121">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c00a-123">Altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="7c00a-123">Height, in pixels.</span></span> <span data-ttu-id="7c00a-124">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c00a-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="7c00a-125">A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="7c00a-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-126">*Profundidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-126">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c00a-128">Profundidade, em pixels.</span><span class="sxs-lookup"><span data-stu-id="7c00a-128">Depth, in pixels.</span></span> <span data-ttu-id="7c00a-129">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c00a-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="7c00a-130">A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="7c00a-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-131">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-131">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c00a-133">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="7c00a-133">Number of mip levels requested.</span></span> <span data-ttu-id="7c00a-134">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="7c00a-134">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-135">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-135">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-136">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-136">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c00a-137">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="7c00a-137">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="7c00a-138">Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="7c00a-138">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="7c00a-139">O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="7c00a-139">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="7c00a-140">Se D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic for especificado, o *pool* deverá ser definido como D3DPOOL \_ padrão e o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="7c00a-140">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="7c00a-141">D3DUSAGE \_ Dynamic indica que a superfície deve ser manipulada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="7c00a-141">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="7c00a-142">Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="7c00a-142">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-143">*Formato*</span><span class="sxs-lookup"><span data-stu-id="7c00a-143">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="7c00a-144">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-144">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="7c00a-145">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura.</span><span class="sxs-lookup"><span data-stu-id="7c00a-145">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="7c00a-146">A textura retornada pode ter um formato diferente daquele especificado pelo *formato*.</span><span class="sxs-lookup"><span data-stu-id="7c00a-146">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="7c00a-147">Os aplicativos devem verificar o formato da textura retornada.</span><span class="sxs-lookup"><span data-stu-id="7c00a-147">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="7c00a-148">Se [D3DFMT \_ desconhecido](other-d3dx-constants.md), o formato será extraído do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c00a-148">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="7c00a-149">Se D3DFMT \_ do \_ arquivo, o formato será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c00a-149">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-150">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-150">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-151">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-151">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="7c00a-152">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="7c00a-152">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-153">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-153">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c00a-155">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="7c00a-155">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="7c00a-156">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7c00a-156">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-157">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-157">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-158">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-158">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c00a-159">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="7c00a-159">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="7c00a-160">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="7c00a-160">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="7c00a-161">Além disso, use o bits 27-31 para especificar o número de níveis MIP a serem ignorados (da parte superior da cadeia mipmap) quando uma textura. DDS for carregada na memória; Isso permite que você pule até 32 níveis.</span><span class="sxs-lookup"><span data-stu-id="7c00a-161">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-162">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-162">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-163">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-163">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="7c00a-164">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="7c00a-164">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="7c00a-165">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="7c00a-165">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="7c00a-166">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="7c00a-166">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="7c00a-167">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="7c00a-167">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-168">*pSrcInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-168">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-169">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c00a-169">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="7c00a-170">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7c00a-170">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-171">*pPalette* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-171">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-172">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="7c00a-172">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="7c00a-173">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , representando uma paleta de cor de 256 para preencher ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7c00a-173">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7c00a-174">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7c00a-174">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c00a-175">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="7c00a-175">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="7c00a-176">Endereço de um ponteiro para uma interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="7c00a-176">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c00a-177">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c00a-177">Return value</span></span>

<span data-ttu-id="7c00a-178">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c00a-178">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c00a-179">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c00a-179">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7c00a-180">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7c00a-180">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c00a-181">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c00a-181">Remarks</span></span>

<span data-ttu-id="7c00a-182">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="7c00a-182">The compiler setting also determines the function version.</span></span> <span data-ttu-id="7c00a-183">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateVolumeTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="7c00a-183">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileExW.</span></span> <span data-ttu-id="7c00a-184">Caso contrário, a chamada de função é resolvida como D3DXCreateVolumeTextureFromFileExA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="7c00a-184">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="7c00a-185">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="7c00a-185">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="7c00a-186">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="7c00a-186">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="7c00a-187">As texturas Mipmapped têm automaticamente cada nível preenchido com a textura do volume carregado.</span><span class="sxs-lookup"><span data-stu-id="7c00a-187">Mipmapped textures automatically have each level filled with the loaded volume texture.</span></span> <span data-ttu-id="7c00a-188">Ao carregar imagens em texturas Mipmapped, alguns dispositivos não podem ir para uma imagem 1x1 e essa função falhará.</span><span class="sxs-lookup"><span data-stu-id="7c00a-188">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="7c00a-189">Se isso acontecer, as imagens precisarão ser carregadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="7c00a-189">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="7c00a-190">Ao ignorar os níveis de mipmap ao carregar um arquivo. DDS, use a \_ \_ macro D3DX \_ ignorar \_ os níveis de MIP do DDS para gerar o valor de *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="7c00a-190">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="7c00a-191">Essa macro usa o número de níveis a serem ignorados e o tipo de filtro e retorna o valor do filtro, que seria passado para o parâmetro *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="7c00a-191">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c00a-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c00a-192">Requirements</span></span>



| <span data-ttu-id="7c00a-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c00a-193">Requirement</span></span> | <span data-ttu-id="7c00a-194">Valor</span><span class="sxs-lookup"><span data-stu-id="7c00a-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c00a-195">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c00a-195">Header</span></span><br/>  | <dl> <span data-ttu-id="7c00a-196"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c00a-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7c00a-197">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c00a-197">Library</span></span><br/> | <dl> <span data-ttu-id="7c00a-198"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c00a-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7c00a-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c00a-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c00a-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="7c00a-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="7c00a-201">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="7c00a-201">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="7c00a-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="7c00a-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="7c00a-203">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="7c00a-203">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="7c00a-204">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="7c00a-204">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="7c00a-205">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="7c00a-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
