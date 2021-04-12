---
description: Cria uma textura de cubo a partir de um recurso especificado por uma cadeia de caracteres. Essa é uma função mais avançada do que D3DXCreateCubeTextureFromResource.
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: Função D3DXCreateCubeTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ed77556681e2ad43302b8608dc213b3ad0f0209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298784"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a><span data-ttu-id="223d2-104">Função D3DXCreateCubeTextureFromResourceEx</span><span class="sxs-lookup"><span data-stu-id="223d2-104">D3DXCreateCubeTextureFromResourceEx function</span></span>

<span data-ttu-id="223d2-105">Cria uma textura de cubo a partir de um recurso especificado por uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="223d2-105">Creates a cube texture from a resource specified by a string.</span></span> <span data-ttu-id="223d2-106">Essa é uma função mais avançada do que [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="223d2-106">This is a more advanced function than [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="223d2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="223d2-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="223d2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="223d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="223d2-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="223d2-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="223d2-111">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="223d2-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-112">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-113">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="223d2-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="223d2-114">Manipule para o módulo em que o recurso está localizado, ou **NULL** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="223d2-114">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-115">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="223d2-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="223d2-117">Ponteiro para uma cadeia de caracteres que especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="223d2-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="223d2-118">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="223d2-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="223d2-119">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="223d2-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="223d2-120">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="223d2-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-121">*Tamanho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-121">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="223d2-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="223d2-123">Largura e altura da textura do cubo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="223d2-123">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="223d2-124">Por exemplo, se a textura do cubo for de 8 pixels por cubo de 8 pixels, o valor desse parâmetro deverá ser 8.</span><span class="sxs-lookup"><span data-stu-id="223d2-124">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="223d2-125">Se esse valor for 0 ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="223d2-125">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-126">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="223d2-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="223d2-128">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="223d2-128">Number of mip levels requested.</span></span> <span data-ttu-id="223d2-129">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="223d2-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-130">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="223d2-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="223d2-132">0 ou D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="223d2-132">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="223d2-133">Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="223d2-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="223d2-134">O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="223d2-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="223d2-135">Se D3DUSAGE \_ RENDERTARGET for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação [**chamando CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="223d2-135">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="223d2-136">D3DUSAGE \_ Dynamic indica que a superfície deve ser manipulada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="223d2-136">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="223d2-137">Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="223d2-137">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="223d2-138">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-138">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-139">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="223d2-139">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="223d2-140">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="223d2-140">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="223d2-141">A textura do cubo retornado pode ter um formato diferente daquele especificado pelo *formato*.</span><span class="sxs-lookup"><span data-stu-id="223d2-141">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="223d2-142">Os aplicativos devem verificar o formato da textura do cubo retornado.</span><span class="sxs-lookup"><span data-stu-id="223d2-142">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="223d2-143">Se [D3DFMT \_ desconhecido](other-d3dx-constants.md), o formato será extraído do arquivo.</span><span class="sxs-lookup"><span data-stu-id="223d2-143">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="223d2-144">Se D3DFMT \_ do \_ arquivo, o formato será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="223d2-144">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-145">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-145">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-146">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="223d2-146">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="223d2-147">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura do cubo deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="223d2-147">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-148">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-148">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="223d2-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="223d2-150">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md), controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="223d2-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="223d2-151">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="223d2-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-152">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-153">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="223d2-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="223d2-154">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="223d2-154">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="223d2-155">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="223d2-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-156">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="223d2-156">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-157">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="223d2-157">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="223d2-158">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="223d2-158">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="223d2-159">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="223d2-159">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="223d2-160">Alfa é significativo e normalmente deve ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="223d2-160">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="223d2-161">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="223d2-161">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-162">*pSrcInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="223d2-162">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-163">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="223d2-163">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="223d2-164">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="223d2-164">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-165">*pPalette* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="223d2-165">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-166">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="223d2-166">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="223d2-167">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , representando uma paleta de cor de 256 para preencher ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="223d2-167">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="223d2-168">*ppCubeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="223d2-168">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="223d2-169">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="223d2-169">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="223d2-170">Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , que representa o objeto de textura do cubo criado.</span><span class="sxs-lookup"><span data-stu-id="223d2-170">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="223d2-171">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="223d2-171">Return value</span></span>

<span data-ttu-id="223d2-172">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="223d2-172">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="223d2-173">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="223d2-173">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="223d2-174">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="223d2-174">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="223d2-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="223d2-175">Remarks</span></span>

<span data-ttu-id="223d2-176">A configuração do compilador determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="223d2-176">The compiler setting determines the function version.</span></span> <span data-ttu-id="223d2-177">Se o Unicode for definido, a chamada de função será resolvida como **D3DXCreateCubeTextureFromResourceExW**.</span><span class="sxs-lookup"><span data-stu-id="223d2-177">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceExW**.</span></span> <span data-ttu-id="223d2-178">Caso contrário, a chamada de função é resolvida como **D3DXCreateCubeTextureFromResourceExA** porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="223d2-178">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="223d2-179">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="223d2-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="223d2-180">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="223d2-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="223d2-181">Texturas de cubos diferem de outras superfícies em que são coleções de superfícies.</span><span class="sxs-lookup"><span data-stu-id="223d2-181">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="223d2-182">Para chamar [**SetRenderTarget**](/windows/desktop/api) com uma textura de cubo, você deve selecionar uma face individual usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passar a superfície resultante para **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="223d2-182">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="223d2-183">**D3DXCreateCubeTextureFromResourceEx** usa o formato de arquivo de superfície do DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="223d2-183">**D3DXCreateCubeTextureFromResourceEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="223d2-184">O editor de textura DirectX (Dxtex.exe) permite que você gere um mapa de cubo de outros formatos de arquivo e salve-o no formato de arquivo DDS.</span><span class="sxs-lookup"><span data-stu-id="223d2-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="223d2-185">Você pode obter Dxtex.exe e aprender sobre ele no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="223d2-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="223d2-186">Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="223d2-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="223d2-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="223d2-187">Requirements</span></span>



| <span data-ttu-id="223d2-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="223d2-188">Requirement</span></span> | <span data-ttu-id="223d2-189">Valor</span><span class="sxs-lookup"><span data-stu-id="223d2-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="223d2-190">parâmetro</span><span class="sxs-lookup"><span data-stu-id="223d2-190">Header</span></span><br/>  | <dl> <span data-ttu-id="223d2-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="223d2-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="223d2-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="223d2-192">Library</span></span><br/> | <dl> <span data-ttu-id="223d2-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="223d2-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="223d2-194">Confira também</span><span class="sxs-lookup"><span data-stu-id="223d2-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223d2-195">**D3DXCreateCubeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="223d2-195">**D3DXCreateCubeTextureFromResource**</span></span>](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="223d2-196">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="223d2-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
