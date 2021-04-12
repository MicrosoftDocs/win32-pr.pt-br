---
description: Cria uma textura a partir de um arquivo.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: Função D3DXCreateTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19453986405ee4d46a3e72145c2117bb113663bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370955"
---
# <a name="d3dxcreatetexturefromfile-function"></a><span data-ttu-id="c73b3-103">Função D3DXCreateTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="c73b3-103">D3DXCreateTextureFromFile function</span></span>

<span data-ttu-id="c73b3-104">Cria uma textura a partir de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c73b3-104">Creates a texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c73b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c73b3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="c73b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c73b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c73b3-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c73b3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c73b3-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c73b3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c73b3-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="c73b3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="c73b3-110">*pSrcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c73b3-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c73b3-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c73b3-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c73b3-112">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c73b3-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="c73b3-113">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="c73b3-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c73b3-114">Caso contrário, o tipo de dados String será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c73b3-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="c73b3-115">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="c73b3-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c73b3-116">*ppTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c73b3-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c73b3-117">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="c73b3-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="c73b3-118">Endereço de um ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , que representa o objeto de textura criado.</span><span class="sxs-lookup"><span data-stu-id="c73b3-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c73b3-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c73b3-119">Return value</span></span>

<span data-ttu-id="c73b3-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c73b3-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c73b3-121">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c73b3-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c73b3-122">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c73b3-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c73b3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c73b3-123">Remarks</span></span>

<span data-ttu-id="c73b3-124">A configuração do compilador também determina a versão da função.</span><span class="sxs-lookup"><span data-stu-id="c73b3-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="c73b3-125">Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateTextureFromFileW.</span><span class="sxs-lookup"><span data-stu-id="c73b3-125">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileW.</span></span> <span data-ttu-id="c73b3-126">Caso contrário, a chamada de função é resolvida como D3DXCreateTextureFromFileA porque as cadeias de caracteres ANSI estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="c73b3-126">Otherwise, the function call resolves to D3DXCreateTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="c73b3-127">Essa função dá suporte aos seguintes formatos de arquivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="c73b3-127">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="c73b3-128">Consulte [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="c73b3-128">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="c73b3-129">A função é equivalente a D3DXCreateTextureFromFileEx (pDevice, pSrcFile, D3DX \_ padrão, D3DX padrão \_ , D3DX padrão \_ , 0, D3DFMT \_ desconhecido, D3DPOOL \_ gerenciado, D3DX \_ padrão, D3DX \_ Default, 0, **NULL**, **null**, ppTexture).</span><span class="sxs-lookup"><span data-stu-id="c73b3-129">The function is equivalent to D3DXCreateTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="c73b3-130">As texturas Mipmapped têm automaticamente cada nível preenchido com a textura carregada.</span><span class="sxs-lookup"><span data-stu-id="c73b3-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="c73b3-131">Ao carregar imagens em texturas Mipmapped, alguns dispositivos não podem ir para uma imagem 1x1 e essa função falhará.</span><span class="sxs-lookup"><span data-stu-id="c73b3-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="c73b3-132">Se isso acontecer, as imagens precisarão ser carregadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="c73b3-132">If this happens, the images need to be loaded manually.</span></span>

<span data-ttu-id="c73b3-133">Observe que um recurso criado com essa função será colocado na classe de memória denotada por D3DPOOL \_ gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c73b3-133">Note that a resource created with this function will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span>

<span data-ttu-id="c73b3-134">A filtragem é aplicada automaticamente a uma textura criada usando esse método.</span><span class="sxs-lookup"><span data-stu-id="c73b3-134">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="c73b3-135">A filtragem é equivalente ao D3DX \_ Filter \_ triângulo \| D3DX \_ Filter \_ pontilhado [no \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="c73b3-135">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="c73b3-136">Para obter o melhor desempenho ao usar o **D3DXCreateTextureFromFile**:</span><span class="sxs-lookup"><span data-stu-id="c73b3-136">For the best performance when using **D3DXCreateTextureFromFile**:</span></span>

1.  <span data-ttu-id="c73b3-137">Fazer o dimensionamento de imagem e a conversão de formato no tempo de carregamento pode ser lento.</span><span class="sxs-lookup"><span data-stu-id="c73b3-137">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="c73b3-138">Armazene imagens no formato e na resolução que serão usadas.</span><span class="sxs-lookup"><span data-stu-id="c73b3-138">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="c73b3-139">Se o hardware de destino exigir uma potência de duas dimensões, crie e armazene imagens usando a potência de duas dimensões.</span><span class="sxs-lookup"><span data-stu-id="c73b3-139">If the target hardware requires power of two dimensions, create and store images using power of two dimensions.</span></span>
2.  <span data-ttu-id="c73b3-140">Considere o uso de arquivos de superfície do DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="c73b3-140">Consider using DirectDraw surface (DDS) files.</span></span> <span data-ttu-id="c73b3-141">Como os arquivos DDS podem ser usados para representar qualquer formato de textura do Direct3D 9, eles são muito fáceis para a leitura de D3DX.</span><span class="sxs-lookup"><span data-stu-id="c73b3-141">Because DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="c73b3-142">Além disso, eles podem armazenar mipmaps, portanto, os algoritmos de geração de mipmap podem ser usados para criar as imagens.</span><span class="sxs-lookup"><span data-stu-id="c73b3-142">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

## <a name="requirements"></a><span data-ttu-id="c73b3-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c73b3-143">Requirements</span></span>



| <span data-ttu-id="c73b3-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c73b3-144">Requirement</span></span> | <span data-ttu-id="c73b3-145">Valor</span><span class="sxs-lookup"><span data-stu-id="c73b3-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c73b3-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c73b3-146">Header</span></span><br/>  | <dl> <span data-ttu-id="c73b3-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c73b3-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c73b3-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c73b3-148">Library</span></span><br/> | <dl> <span data-ttu-id="c73b3-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c73b3-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c73b3-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="c73b3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c73b3-151">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="c73b3-151">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="c73b3-152">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c73b3-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
