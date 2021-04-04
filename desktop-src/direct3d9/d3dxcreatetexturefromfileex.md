---
description: Cria uma textura a partir de um arquivo. Essa é uma função mais avançada do que D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: Função D3DXCreateTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4dba1424f98389a9282fdebf9dae55c7e1601f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837932"
---
# <a name="d3dxcreatetexturefromfileex-function"></a><span data-ttu-id="b4e81-104">Função D3DXCreateTextureFromFileEx</span><span class="sxs-lookup"><span data-stu-id="b4e81-104">D3DXCreateTextureFromFileEx function</span></span>

<span data-ttu-id="b4e81-105">Cria uma textura a partir de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4e81-105">Creates a texture from a file.</span></span> <span data-ttu-id="b4e81-106">Essa é uma função mais avançada do que [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="b4e81-106">This is a more advanced function than [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e81-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4e81-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="b4e81-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4e81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4e81-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b4e81-111">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="b4e81-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-112">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-113">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4e81-114">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4e81-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="b4e81-115">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b4e81-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b4e81-116">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b4e81-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="b4e81-117">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="b4e81-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-118">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4e81-120">Largura em pixels.</span><span class="sxs-lookup"><span data-stu-id="b4e81-120">Width in pixels.</span></span> <span data-ttu-id="b4e81-121">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo e arredondadas para uma potência de dois.</span><span class="sxs-lookup"><span data-stu-id="b4e81-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="b4e81-122">Se o dispositivo oferecer suporte a não potência de 2 texturas e [D3DX \_ padrão \_ NONPOW2](other-d3dx-constants.md) for especificado, o tamanho não será arredondado.</span><span class="sxs-lookup"><span data-stu-id="b4e81-122">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is specified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-123">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4e81-125">Altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="b4e81-125">Height, in pixels.</span></span> <span data-ttu-id="b4e81-126">Se esse valor for zero ou D3DX \_ padrão, as dimensões serão obtidas do arquivo e arredondadas para uma potência de dois.</span><span class="sxs-lookup"><span data-stu-id="b4e81-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="b4e81-127">Se o dispositivo der suporte a uma não potência de 2 texturas e [D3DX \_ \_ NONPOW2 padrão](other-d3dx-constants.md) for sepcified, o tamanho não será arredondado.</span><span class="sxs-lookup"><span data-stu-id="b4e81-127">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is sepcified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-128">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-128">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4e81-130">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="b4e81-130">Number of mip levels requested.</span></span> <span data-ttu-id="b4e81-131">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="b4e81-131">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="b4e81-132">Se D3DX \_ do \_ arquivo, o tamanho será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4e81-132">If D3DX\_FROM\_FILE, the size will be taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-133">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4e81-135">0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)ou **D3DUSAGE \_ Dynamic**.</span><span class="sxs-lookup"><span data-stu-id="b4e81-135">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="b4e81-136">Definir esse sinalizador como **D3DUSAGE \_ RENDERTARGET** indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="b4e81-136">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="b4e81-137">O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="b4e81-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="b4e81-138">Se **D3DUSAGE \_ RENDERTARGET** ou **D3DUSAGE \_ Dynamic** for especificado, o *pool* deverá ser definido como D3DPOOL \_ padrão e o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="b4e81-138">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="b4e81-139">**D3DUSAGE \_ DINÂMICO** indica que a superfície deve ser manipulada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="b4e81-139">**D3DUSAGE\_DYNAMIC** indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="b4e81-140">Consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="b4e81-140">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-141">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-142">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="b4e81-143">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura.</span><span class="sxs-lookup"><span data-stu-id="b4e81-143">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="b4e81-144">A textura retornada pode ter um formato diferente daquele especificado pelo *formato*.</span><span class="sxs-lookup"><span data-stu-id="b4e81-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="b4e81-145">Os aplicativos devem verificar o formato da textura retornada.</span><span class="sxs-lookup"><span data-stu-id="b4e81-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="b4e81-146">Se D3DFMT \_ desconhecido, o formato será extraído do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4e81-146">If D3DFMT\_UNKNOWN, the format is taken from the file.</span></span> <span data-ttu-id="b4e81-147">Se D3DFMT \_ do \_ arquivo, o formato será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4e81-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-148">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-149">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="b4e81-150">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="b4e81-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-151">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-152">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4e81-153">Uma combinação de uma ou mais constantes de [ \_ filtro D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="b4e81-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="b4e81-154">A especificação do [ \_ padrão D3DX](other-d3dx-constants.md) para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b4e81-154">Specifying [D3DX\_DEFAULT](other-d3dx-constants.md) for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-155">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4e81-157">Uma combinação de uma ou mais constantes de [ \_ filtro D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="b4e81-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="b4e81-158">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="b4e81-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="b4e81-159">Além disso, use o bits 27-31 para especificar o número de níveis MIP a serem ignorados (da parte superior da cadeia mipmap) quando uma textura. DDS for carregada na memória; Isso permite que você pule até 32 níveis.</span><span class="sxs-lookup"><span data-stu-id="b4e81-159">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-160">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-160">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-161">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-161">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="b4e81-162">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar a chave de cor.</span><span class="sxs-lookup"><span data-stu-id="b4e81-162">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the color key.</span></span> <span data-ttu-id="b4e81-163">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="b4e81-163">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="b4e81-164">Alfa é significativo e deve geralmente ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="b4e81-164">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="b4e81-165">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="b4e81-165">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-166">*pSrcInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-166">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-167">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4e81-167">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="b4e81-168">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b4e81-168">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-169">*pPalette* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-169">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-170">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="b4e81-170">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="b4e81-171">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , representando uma paleta de cor de 256 para preencher ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b4e81-171">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4e81-172">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b4e81-172">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e81-173">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="b4e81-173">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="b4e81-174">Endereço de um ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="b4e81-174">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4e81-175">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4e81-175">Return value</span></span>

<span data-ttu-id="b4e81-176">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4e81-176">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4e81-177">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b4e81-177">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b4e81-178">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b4e81-178">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4e81-179">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4e81-179">Remarks</span></span>

<span data-ttu-id="b4e81-180">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="b4e81-180">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b4e81-181">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="b4e81-181">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileExW.</span></span> <span data-ttu-id="b4e81-182">Caso contrário, a chamada de função é resolvida como D3DXCreateTextureFromFileExA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="b4e81-182">Otherwise, the function call resolves to D3DXCreateTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="b4e81-183">Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) para determinar se o dispositivo pode dar suporte à textura dada o estado atual.</span><span class="sxs-lookup"><span data-stu-id="b4e81-183">Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to determine if your device can support the texture given the current state.</span></span>

<span data-ttu-id="b4e81-184">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="b4e81-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="b4e81-185">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="b4e81-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="b4e81-186">As texturas Mipmapped têm automaticamente cada nível preenchido com a textura carregada.</span><span class="sxs-lookup"><span data-stu-id="b4e81-186">Mipmapped textures automatically have each level filled with the loaded texture.</span></span> <span data-ttu-id="b4e81-187">Ao carregar imagens em texturas Mipmapped, alguns dispositivos não podem ir para uma imagem 1x1 e essa função falhará.</span><span class="sxs-lookup"><span data-stu-id="b4e81-187">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="b4e81-188">Se isso acontecer, as imagens precisarão ser carregadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="b4e81-188">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="b4e81-189">Para obter o melhor desempenho ao usar o **D3DXCreateTextureFromFileEx**:</span><span class="sxs-lookup"><span data-stu-id="b4e81-189">For the best performance when using **D3DXCreateTextureFromFileEx**:</span></span>

1.  <span data-ttu-id="b4e81-190">Fazer o dimensionamento de imagem e a conversão de formato no tempo de carregamento pode ser lento.</span><span class="sxs-lookup"><span data-stu-id="b4e81-190">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="b4e81-191">Armazene imagens no formato e na resolução que serão usadas.</span><span class="sxs-lookup"><span data-stu-id="b4e81-191">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="b4e81-192">Se o hardware de destino exigir a potência de 2 dimensões, crie e armazene imagens usando a potência de 2 dimensões.</span><span class="sxs-lookup"><span data-stu-id="b4e81-192">If the target hardware requires power of 2 dimensions, then create and store images using power of 2 dimensions.</span></span>
2.  <span data-ttu-id="b4e81-193">Para a criação da imagem mipmap no tempo de carregamento, filtre usando a [ \_ \_ caixa de filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b4e81-193">For mipmap image creation at load time, filter using [D3DX\_FILTER\_BOX](d3dx-filter.md).</span></span> <span data-ttu-id="b4e81-194">Um filtro de caixa é muito mais rápido do que outros tipos de filtro, como o \_ triângulo de filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="b4e81-194">A box filter is much faster than other filter types such as D3DX\_FILTER\_TRIANGLE.</span></span>
3.  <span data-ttu-id="b4e81-195">Considere o uso de arquivos DDS.</span><span class="sxs-lookup"><span data-stu-id="b4e81-195">Consider using DDS files.</span></span> <span data-ttu-id="b4e81-196">Como os arquivos DDS podem ser usados para representar qualquer formato de textura do Direct3D 9, eles são muito fáceis para a leitura de D3DX.</span><span class="sxs-lookup"><span data-stu-id="b4e81-196">Since DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="b4e81-197">Além disso, eles podem armazenar mipmaps, portanto, os algoritmos de geração de mipmap podem ser usados para criar as imagens.</span><span class="sxs-lookup"><span data-stu-id="b4e81-197">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

<span data-ttu-id="b4e81-198">Ao ignorar os níveis de mipmap ao carregar um arquivo. DDS, use a \_ \_ macro D3DX \_ ignorar \_ os níveis de MIP do DDS para gerar o valor de MipFilter.</span><span class="sxs-lookup"><span data-stu-id="b4e81-198">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="b4e81-199">Essa macro usa o número de níveis a serem ignorados e o tipo de filtro e retorna o valor do filtro, que seria passado para o parâmetro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="b4e81-199">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e81-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4e81-200">Requirements</span></span>



| <span data-ttu-id="b4e81-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4e81-201">Requirement</span></span> | <span data-ttu-id="b4e81-202">Valor</span><span class="sxs-lookup"><span data-stu-id="b4e81-202">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e81-203">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4e81-203">Header</span></span><br/>  | <dl> <span data-ttu-id="b4e81-204"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4e81-204"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b4e81-205">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4e81-205">Library</span></span><br/> | <dl> <span data-ttu-id="b4e81-206"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4e81-206"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b4e81-207">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4e81-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e81-208">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="b4e81-208">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="b4e81-209">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b4e81-209">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
