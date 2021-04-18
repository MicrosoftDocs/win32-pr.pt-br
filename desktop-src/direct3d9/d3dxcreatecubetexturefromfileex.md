---
description: Cria uma textura de cubo a partir de um arquivo. Essa é uma função mais avançada do que D3DXCreateCubeTextureFromFile.
ms.assetid: 77e64b33-9282-42fa-978c-a93fa9ba11fc
title: Função D3DXCreateCubeTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4f56ad3f8e314f7ceb5f4efb07562257efab5fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798294"
---
# <a name="d3dxcreatecubetexturefromfileex-function"></a><span data-ttu-id="2c690-104">Função D3DXCreateCubeTextureFromFileEx</span><span class="sxs-lookup"><span data-stu-id="2c690-104">D3DXCreateCubeTextureFromFileEx function</span></span>

<span data-ttu-id="2c690-105">Cria uma textura de cubo a partir de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2c690-105">Creates a cube texture from a file.</span></span> <span data-ttu-id="2c690-106">Essa é uma função mais avançada do que [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="2c690-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c690-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c690-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileEx(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _In_  DWORD                  Filter,
  _In_  DWORD                  MipFilter,
  _In_  D3DCOLOR               ColorKey,
  _Out_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_ PALETTEENTRY           *pPalette,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="2c690-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c690-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c690-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c690-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2c690-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2c690-111">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="2c690-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-112">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c690-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-113">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c690-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c690-114">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2c690-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="2c690-115">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="2c690-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2c690-116">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2c690-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="2c690-117">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="2c690-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-118">*Tamanho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c690-118">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c690-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c690-120">Largura e altura da textura do cubo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="2c690-120">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="2c690-121">Por exemplo, se a textura do cubo for de 8 pixels por cubo de 8 pixels, o valor desse parâmetro deverá ser 8.</span><span class="sxs-lookup"><span data-stu-id="2c690-121">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="2c690-122">Se esse valor for 0 ou D3DX \_ padrão, as dimensões serão obtidas do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2c690-122">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-123">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c690-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c690-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c690-125">Número de níveis de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="2c690-125">Number of mip levels requested.</span></span> <span data-ttu-id="2c690-126">Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada.</span><span class="sxs-lookup"><span data-stu-id="2c690-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-127">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2c690-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c690-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c690-129">0 ou D3DUSAGE \_ RENDERTARGET ou D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="2c690-129">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="2c690-130">Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="2c690-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="2c690-131">O recurso pode então ser passado para o parâmetro *pNewRenderTarget* do método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="2c690-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="2c690-132">Se D3DUSAGE \_ RENDERTARGET for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação [**chamando CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="2c690-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="2c690-133">D3DUSAGE \_ Dynamic indica que a superfície deve ser manipulada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="2c690-133">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="2c690-134">Para obter mais informações sobre como usar texturas dinâmicas, consulte [usando texturas dinâmicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="2c690-134">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c690-135">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c690-135">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-136">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2c690-136">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="2c690-137">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel solicitado para a textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="2c690-137">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="2c690-138">A textura do cubo retornado pode ter um formato diferente daquele especificado pelo *formato*.</span><span class="sxs-lookup"><span data-stu-id="2c690-138">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="2c690-139">Os aplicativos devem verificar o formato da textura do cubo retornado.</span><span class="sxs-lookup"><span data-stu-id="2c690-139">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="2c690-140">Se [D3DFMT \_ desconhecido](other-d3dx-constants.md), o formato será extraído do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2c690-140">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="2c690-141">Se D3DFMT \_ do \_ arquivo, o formato será levado exatamente como está no arquivo e a chamada falhará se isso violar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c690-141">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-142">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="2c690-142">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-143">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2c690-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="2c690-144">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura do cubo deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="2c690-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-145">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c690-145">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-146">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c690-146">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c690-147">Uma combinação de uma ou mais constantes de [ \_ filtro D3DX](d3dx-filter.md) , controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="2c690-147">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants, controlling how the image is filtered.</span></span> <span data-ttu-id="2c690-148">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2c690-148">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-149">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c690-149">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-150">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c690-150">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c690-151">Uma combinação de uma ou mais constantes de [ \_ filtro D3DX](d3dx-filter.md) controlando como a imagem é filtrada.</span><span class="sxs-lookup"><span data-stu-id="2c690-151">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="2c690-152">A especificação do \_ padrão D3DX para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="2c690-152">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="2c690-153">Além disso, use o bits 27-31 para especificar o número de níveis MIP a serem ignorados (da parte superior da cadeia mipmap) quando uma textura. DDS for carregada na memória; Isso permite que você pule até 32 níveis.</span><span class="sxs-lookup"><span data-stu-id="2c690-153">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-154">*COLORKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c690-154">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-155">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2c690-155">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="2c690-156">Valor [**D3DCOLOR**](d3dcolor.md) a ser substituído por preto transparente ou 0 para desabilitar o COLORKEY.</span><span class="sxs-lookup"><span data-stu-id="2c690-156">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="2c690-157">Essa é sempre uma cor ARGB de 32 bits, independente do formato de imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="2c690-157">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="2c690-158">Alfa é significativo e normalmente deve ser definido como FF para chaves de cor opacas.</span><span class="sxs-lookup"><span data-stu-id="2c690-158">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="2c690-159">Portanto, para preto opaco, o valor seria igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="2c690-159">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-160">*pSrcInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2c690-160">*pSrcInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-161">Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c690-161">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="2c690-162">Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com uma descrição dos dados no arquivo de imagem de origem, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2c690-162">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-163">*pPalette* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2c690-163">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-164">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="2c690-164">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="2c690-165">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , representando uma paleta de cor de 256 para preencher ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2c690-165">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2c690-166">*ppCubeTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2c690-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c690-167">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="2c690-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="2c690-168">Endereço de um ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , que representa o objeto de textura do cubo criado.</span><span class="sxs-lookup"><span data-stu-id="2c690-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c690-169">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c690-169">Return value</span></span>

<span data-ttu-id="2c690-170">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c690-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c690-171">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2c690-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2c690-172">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2c690-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c690-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c690-173">Remarks</span></span>

<span data-ttu-id="2c690-174">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="2c690-174">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2c690-175">Se o Unicode for definido, a chamada de função será resolvida como **D3DXCreateCubeTextureFromFileExW**.</span><span class="sxs-lookup"><span data-stu-id="2c690-175">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileExW**.</span></span> <span data-ttu-id="2c690-176">Caso contrário, a chamada de função é resolvida como **D3DXCreateCubeTextureFromFileExA** porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="2c690-176">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="2c690-177">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="2c690-177">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="2c690-178">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="2c690-178">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="2c690-179">Texturas de cubos diferem de outras superfícies em que são coleções de superfícies.</span><span class="sxs-lookup"><span data-stu-id="2c690-179">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="2c690-180">Para chamar [**SetRenderTarget**](/windows/desktop/api) com uma textura de cubo, você deve selecionar uma face individual usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passar a superfície resultante para **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="2c690-180">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="2c690-181">**D3DXCreateCubeTextureFromFileEx** usa o formato de arquivo de superfície do DIRECTDRAW (DDS).</span><span class="sxs-lookup"><span data-stu-id="2c690-181">**D3DXCreateCubeTextureFromFileEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="2c690-182">O editor de textura DirectX (Dxtex.exe) permite que você gere um mapa de cubo de outros formatos de arquivo e salve-o no formato de arquivo DDS.</span><span class="sxs-lookup"><span data-stu-id="2c690-182">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="2c690-183">Você pode obter Dxtex.exe e aprender sobre ele no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="2c690-183">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="2c690-184">Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="2c690-184">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="2c690-185">Ao ignorar os níveis de mipmap ao carregar um arquivo. DDS, use a \_ \_ macro D3DX \_ ignorar \_ os níveis de MIP do DDS para gerar o valor de MipFilter.</span><span class="sxs-lookup"><span data-stu-id="2c690-185">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="2c690-186">Essa macro usa o número de níveis a serem ignorados e o tipo de filtro e retorna o valor do filtro, que seria passado para o parâmetro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="2c690-186">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c690-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c690-187">Requirements</span></span>



| <span data-ttu-id="2c690-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c690-188">Requirement</span></span> | <span data-ttu-id="2c690-189">Valor</span><span class="sxs-lookup"><span data-stu-id="2c690-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c690-190">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c690-190">Header</span></span><br/>  | <dl> <span data-ttu-id="2c690-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c690-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2c690-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c690-192">Library</span></span><br/> | <dl> <span data-ttu-id="2c690-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c690-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2c690-194">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c690-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c690-195">**D3DXCreateCubeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="2c690-195">**D3DXCreateCubeTextureFromFile**</span></span>](d3dxcreatecubetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="2c690-196">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2c690-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
