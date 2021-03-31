---
description: Cria uma textura de volume a partir de um recurso especificado por uma cadeia de caracteres. Essa é uma função mais avançada do que D3DXCreateVolumeTextureFromResource.
ms.assetid: 02f2cb9e-4750-4854-aa74-202426427af5
title: Função D3DXCreateVolumeTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44d842df2da1d5c3db374e838e0ffd2492683961
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930598"
---
# <a name="d3dxcreatevolumetexturefromresourceex-function"></a><span data-ttu-id="4948f-104">Função D3DXCreateVolumeTextureFromResourceEx</span><span class="sxs-lookup"><span data-stu-id="4948f-104">D3DXCreateVolumeTextureFromResourceEx function</span></span>

<span data-ttu-id="4948f-105">Cria uma textura de volume a partir de um recurso especificado por uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4948f-105">Creates a volume texture from a resource specified by a string.</span></span> <span data-ttu-id="4948f-106">Essa é uma função mais avançada do que [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="4948f-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4948f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4948f-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    HMODULE                  hSrcModule,
  _In_    LPCTSTR                  pSrcResource,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="4948f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4948f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4948f-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4948f-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4948f-111">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="4948f-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-112">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-113">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4948f-114">Manipule o módulo no qual o recurso está localizado ou **nulo** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="4948f-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-115">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4948f-117">Ponteiro para uma cadeia de caracteres que especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4948f-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="4948f-118">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="4948f-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4948f-119">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="4948f-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="4948f-120">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4948f-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-121">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4948f-123">Largura em pixels.</span><span class="sxs-lookup"><span data-stu-id="4948f-123">Width in pixels.</span></span> <span data-ttu-id="4948f-124">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4948f-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="4948f-125">A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="4948f-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="4948f-126">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-126">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4948f-128">Altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="4948f-128">Height, in pixels.</span></span> <span data-ttu-id="4948f-129">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4948f-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="4948f-130">A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="4948f-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="4948f-131">*Profundidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-131">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4948f-133">Profundidade, em pixels.</span><span class="sxs-lookup"><span data-stu-id="4948f-133">Depth, in pixels.</span></span> <span data-ttu-id="4948f-134">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4948f-134">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="4948f-135">A dimensão máxima à qual um driver dá suporte (para largura, altura e profundidade) pode ser encontrada em MaxVolumeExtent em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="4948f-135">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="4948f-136">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-136">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-137">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4948f-138">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="4948f-138">Number of mip levels requested.</span></span> <span data-ttu-id="4948f-139">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="4948f-139">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-140">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-140">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-141">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4948f-142">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="4948f-142">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="4948f-143">Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="4948f-143">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="4948f-144">O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="4948f-144">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="4948f-145">Se D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic for especificado, o *pool* deverá ser definido como D3DPOOL \_ padrão e o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="4948f-145">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="4948f-146">D3DUSAGE \_ Dynamic indica que a superfície deve ser manipulada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="4948f-146">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="4948f-147">Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="4948f-147">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="4948f-148">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-148">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-149">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-149">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="4948f-150">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura.</span><span class="sxs-lookup"><span data-stu-id="4948f-150">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="4948f-151">A textura retornada pode ter um formato diferente daquele especificado pelo *formato*.</span><span class="sxs-lookup"><span data-stu-id="4948f-151">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="4948f-152">Os aplicativos devem verificar o formato da textura retornada.</span><span class="sxs-lookup"><span data-stu-id="4948f-152">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="4948f-153">Se [D3DFMT \_ desconhecido](other-d3dx-constants.md), o formato será extraído do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4948f-153">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="4948f-154">Se D3DFMT \_ do \_ arquivo, o formato será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4948f-154">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-155">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-155">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-156">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-156">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="4948f-157">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="4948f-157">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-158">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-158">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-159">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-159">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4948f-160">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="4948f-160">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="4948f-161">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4948f-161">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-162">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-162">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-163">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-163">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4948f-164">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="4948f-164">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="4948f-165">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="4948f-165">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-166">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4948f-166">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-167">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="4948f-167">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="4948f-168">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="4948f-168">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="4948f-169">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="4948f-169">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="4948f-170">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="4948f-170">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="4948f-171">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="4948f-171">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-172">*pSrcInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4948f-172">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-173">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="4948f-173">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="4948f-174">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4948f-174">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-175">*pPalette* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4948f-175">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-176">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="4948f-176">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="4948f-177">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , representando uma paleta de cor de 256 para preencher ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4948f-177">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4948f-178">*ppVolumeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4948f-178">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4948f-179">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="4948f-179">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="4948f-180">Endereço de um ponteiro para uma interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="4948f-180">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4948f-181">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4948f-181">Return value</span></span>

<span data-ttu-id="4948f-182">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4948f-182">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4948f-183">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4948f-183">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4948f-184">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4948f-184">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4948f-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="4948f-185">Remarks</span></span>

<span data-ttu-id="4948f-186">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="4948f-186">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4948f-187">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateVolumeTextureFromResourceExW.</span><span class="sxs-lookup"><span data-stu-id="4948f-187">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceExW.</span></span> <span data-ttu-id="4948f-188">Caso contrário, a chamada de função é resolvida como D3DXCreateVolumeTextureFromResourceExA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="4948f-188">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="4948f-189">O recurso que está sendo carregado deve ser um recurso definido pelo aplicativo (RT \_ RCDATA).</span><span class="sxs-lookup"><span data-stu-id="4948f-189">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="4948f-190">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="4948f-190">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="4948f-191">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="4948f-191">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4948f-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4948f-192">Requirements</span></span>



| <span data-ttu-id="4948f-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="4948f-193">Requirement</span></span> | <span data-ttu-id="4948f-194">Valor</span><span class="sxs-lookup"><span data-stu-id="4948f-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4948f-195">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4948f-195">Header</span></span><br/>  | <dl> <span data-ttu-id="4948f-196"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4948f-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4948f-197">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4948f-197">Library</span></span><br/> | <dl> <span data-ttu-id="4948f-198"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4948f-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4948f-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="4948f-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4948f-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="4948f-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="4948f-201">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="4948f-201">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="4948f-202">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="4948f-202">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="4948f-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="4948f-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="4948f-204">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="4948f-204">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="4948f-205">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="4948f-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
