---
description: Cria uma textura a partir de um recurso. Essa é uma função mais avançada do que D3DXCreateTextureFromResource.
ms.assetid: 6015e2fa-9deb-4e6a-a401-f10fb05f40b7
title: Função D3DXCreateTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26298f8a63ccfde2171578c27e9208011c16dd28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506481"
---
# <a name="d3dxcreatetexturefromresourceex-function"></a><span data-ttu-id="cfe3c-104">Função D3DXCreateTextureFromResourceEx</span><span class="sxs-lookup"><span data-stu-id="cfe3c-104">D3DXCreateTextureFromResourceEx function</span></span>

<span data-ttu-id="cfe3c-105">Cria uma textura a partir de um recurso.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-105">Creates a texture from a resource.</span></span> <span data-ttu-id="cfe3c-106">Essa é uma função mais avançada do que [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="cfe3c-106">This is a more advanced function than [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe3c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfe3c-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    HMODULE            hSrcModule,
  _In_    LPCTSTR            pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="cfe3c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfe3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe3c-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cfe3c-111">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-112">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-113">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfe3c-114">Manipule o módulo no qual o recurso está localizado ou **nulo** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-115">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfe3c-117">Ponteiro para uma cadeia de caracteres que especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="cfe3c-118">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="cfe3c-119">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="cfe3c-120">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-121">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfe3c-123">Largura em pixels.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-123">Width in pixels.</span></span> <span data-ttu-id="cfe3c-124">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-125">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-125">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfe3c-127">Altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-127">Height, in pixels.</span></span> <span data-ttu-id="cfe3c-128">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-128">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-129">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-129">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfe3c-131">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-131">Number of mip levels requested.</span></span> <span data-ttu-id="cfe3c-132">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-132">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-133">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfe3c-135">0, D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-135">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="cfe3c-136">Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-136">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="cfe3c-137">O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="cfe3c-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="cfe3c-138">Se D3DUSAGE \_ RENDERTARGET ou D3DUSAGE for especificado, o *pool* deverá ser definido como D3DPOOL \_ padrão e o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="cfe3c-138">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="cfe3c-139">D3DUSAGE \_ Dynamic indica que a superfície deve ser manipulada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-139">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="cfe3c-140">Para obter mais informações sobre como usar texturas dinâmicas, consulte [otimizações de desempenho (Direct3D 9)](performance-optimizations.md)usando texturas dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-140">For more information about using dynamic textures, see [Performance Optimizations (Direct3D 9)](performance-optimizations.md)Using Dynamic Textures.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-141">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-142">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="cfe3c-143">Um membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-143">A member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="cfe3c-144">A textura retornada pode ter um formato diferente daquele especificado pelo *formato*.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="cfe3c-145">Os aplicativos devem verificar o formato da textura retornada.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="cfe3c-146">Se [D3DFMT \_ desconhecido](other-d3dx-constants.md), o formato será extraído do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-146">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="cfe3c-147">Se D3DFMT \_ do \_ arquivo, o formato será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-148">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-149">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="cfe3c-150">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-151">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-152">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfe3c-153">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="cfe3c-154">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cfe3c-154">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-155">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfe3c-157">Uma combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="cfe3c-158">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="cfe3c-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-159">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-159">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-160">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-160">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="cfe3c-161">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-161">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="cfe3c-162">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-162">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="cfe3c-163">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-163">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="cfe3c-164">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-164">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-165">*pSrcInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-165">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-166">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="cfe3c-166">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="cfe3c-167">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-167">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-168">*pPalette* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-168">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-169">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="cfe3c-169">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="cfe3c-170">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , representando uma paleta de cor de 256 para preencher ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-170">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cfe3c-171">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cfe3c-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe3c-172">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="cfe3c-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="cfe3c-173">Endereço de um ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe3c-174">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cfe3c-174">Return value</span></span>

<span data-ttu-id="cfe3c-175">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cfe3c-176">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cfe3c-177">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfe3c-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfe3c-178">Remarks</span></span>

<span data-ttu-id="cfe3c-179">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-179">The compiler setting also determines the function version.</span></span> <span data-ttu-id="cfe3c-180">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateTextureFromResourceExW.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-180">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceExW.</span></span> <span data-ttu-id="cfe3c-181">Caso contrário, a chamada de função é resolvida como D3DXCreateTextureFromResourceExA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-181">Otherwise, the function call resolves to D3DXCreateTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="cfe3c-182">O recurso que está sendo carregado deve ser do tipo \_ bitmap RT ou RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-182">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="cfe3c-183">O tipo de recurso RT \_ RCDATA é usado para carregar formatos diferentes de bitmaps (como. tga,. jpg e. DDS).</span><span class="sxs-lookup"><span data-stu-id="cfe3c-183">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="cfe3c-184">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="cfe3c-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="cfe3c-185">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="cfe3c-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe3c-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfe3c-186">Requirements</span></span>



| <span data-ttu-id="cfe3c-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe3c-187">Requirement</span></span> | <span data-ttu-id="cfe3c-188">Valor</span><span class="sxs-lookup"><span data-stu-id="cfe3c-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe3c-189">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cfe3c-189">Header</span></span><br/>  | <dl> <span data-ttu-id="cfe3c-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfe3c-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="cfe3c-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cfe3c-191">Library</span></span><br/> | <dl> <span data-ttu-id="cfe3c-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfe3c-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cfe3c-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfe3c-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe3c-194">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="cfe3c-194">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="cfe3c-195">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="cfe3c-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
