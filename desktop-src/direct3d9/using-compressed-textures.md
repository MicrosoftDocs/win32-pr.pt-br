---
description: Usando texturas compactadas (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Usando texturas compactadas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646175"
---
# <a name="using-compressed-textures-direct3d-9"></a><span data-ttu-id="8856b-103">Usando texturas compactadas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8856b-103">Using Compressed Textures (Direct3D 9)</span></span>

## <a name="determining-support-for-compressed-textures"></a><span data-ttu-id="8856b-104">Determinando o suporte para texturas compactadas</span><span class="sxs-lookup"><span data-stu-id="8856b-104">Determining Support for Compressed Textures</span></span>

<span data-ttu-id="8856b-105">Para testar o adaptador, especifique qualquer formato de pixel que use DXT1, DXT2, DXT3, DXT4 ou DXT5.</span><span class="sxs-lookup"><span data-stu-id="8856b-105">To test the adapter, specify any pixel format that uses the DXT1, DXT2, DXT3, DXT4, or DXT5.</span></span> <span data-ttu-id="8856b-106">Se [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) retornar o D3D \_ OK, o dispositivo poderá criar textura diretamente de uma superfície de textura compactada que usa esse formato.</span><span class="sxs-lookup"><span data-stu-id="8856b-106">If [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) returns D3D\_OK, the device can create texture directly from a compressed texture surface that uses that format.</span></span> <span data-ttu-id="8856b-107">Nesse caso, você pode usar superfícies de textura compactadas diretamente com o Direct3D chamando o método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="8856b-107">If so, you can use compressed texture surfaces directly with Direct3D by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="8856b-108">O exemplo de código a seguir mostra como determinar se o adaptador dá suporte a um formato de textura compactada.</span><span class="sxs-lookup"><span data-stu-id="8856b-108">The following code example shows how to determine if the adapter supports a compressed texture format.</span></span>


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



<span data-ttu-id="8856b-109">Se o dispositivo não oferecer suporte a texturing de superfícies de textura compactadas, você ainda poderá armazenar dados de textura em uma superfície de formato compactado, mas deverá converter quaisquer texturas compactadas em um formato com suporte antes que possam ser usadas para texturing.</span><span class="sxs-lookup"><span data-stu-id="8856b-109">If the device does not support texturing from compressed texture surfaces, you can still store texture data in a compressed format surface, but you must convert any compressed textures to a supported format before they can be used for texturing.</span></span>

## <a name="creating-compressed-textures"></a><span data-ttu-id="8856b-110">Criando texturas compactadas</span><span class="sxs-lookup"><span data-stu-id="8856b-110">Creating Compressed Textures</span></span>

<span data-ttu-id="8856b-111">Depois de criar um dispositivo que dá suporte a um formato de textura compactada no adaptador, você pode criar um recurso de textura compactada.</span><span class="sxs-lookup"><span data-stu-id="8856b-111">After creating a device that supports a compressed texture format on the adapter, you can create a compressed texture resource.</span></span> <span data-ttu-id="8856b-112">Chame [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) e especifique um formato de textura compactada para o parâmetro format.</span><span class="sxs-lookup"><span data-stu-id="8856b-112">Call [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) and specify a compressed texture format for the Format parameter.</span></span>

<span data-ttu-id="8856b-113">Antes de carregar uma imagem em um objeto de textura, recupere um ponteiro para a superfície de textura chamando o método [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) .</span><span class="sxs-lookup"><span data-stu-id="8856b-113">Before loading an image into a texture object, retrieve a pointer to the texture surface by calling the [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) method.</span></span>

<span data-ttu-id="8856b-114">Agora você pode usar qualquer função D3DXLoadSurfacexxx para carregar uma imagem na superfície que foi recuperada usando [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span><span class="sxs-lookup"><span data-stu-id="8856b-114">Now you can use any D3DXLoadSurfacexxx function to load an image to the surface that was retrieved by using [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span></span> <span data-ttu-id="8856b-115">Essas funções manipulam a conversão de e para formatos de textura compactados.</span><span class="sxs-lookup"><span data-stu-id="8856b-115">These functions handle conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="8856b-116">Você pode criar e converter arquivos de textura compactada (DDS) usando o editor de textura DirectX (Dxtex.exe) fornecido com o SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="8856b-116">You can create and convert compressed texture (DDS) files using the DirectX Texture Editor (Dxtex.exe) supplied with the DirectX SDK.</span></span> <span data-ttu-id="8856b-117">Você pode obter Dxtex.exe e aprender sobre ele no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="8856b-117">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="8856b-118">Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="8856b-118">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="8856b-119">A vantagem desse comportamento é que um aplicativo pode copiar o conteúdo de uma superfície compactada para um arquivo sem calcular a quantidade de armazenamento necessária para uma superfície de uma largura e altura específicas no formato específico.</span><span class="sxs-lookup"><span data-stu-id="8856b-119">The advantage of this behavior is that an application can copy the contents of a compressed surface to a file without calculating how much storage is required for a surface of a particular width and height in the specific format.</span></span>

<span data-ttu-id="8856b-120">A tabela a seguir mostra os cinco tipos de texturas compactadas.</span><span class="sxs-lookup"><span data-stu-id="8856b-120">The following table shows the five types of compressed textures.</span></span> <span data-ttu-id="8856b-121">Para obter mais informações sobre como os dados são armazenados, consulte [formatos de textura compactados (Direct3D 9)](compressed-texture-formats.md).</span><span class="sxs-lookup"><span data-stu-id="8856b-121">For more information about how the data is stored, see [Compressed Texture Formats (Direct3D 9)](compressed-texture-formats.md).</span></span> <span data-ttu-id="8856b-122">Você só precisará dessas informações se estiver escrevendo suas próprias rotinas de compactação.</span><span class="sxs-lookup"><span data-stu-id="8856b-122">You only need this information if you are writing your own compression routines.</span></span>



| <span data-ttu-id="8856b-123">FOURCC</span><span class="sxs-lookup"><span data-stu-id="8856b-123">FOURCC</span></span> | <span data-ttu-id="8856b-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="8856b-124">Description</span></span>        | <span data-ttu-id="8856b-125">Alfa precalculado?</span><span class="sxs-lookup"><span data-stu-id="8856b-125">Alpha premultiplied?</span></span> |
|--------|--------------------|----------------------|
| <span data-ttu-id="8856b-126">DXT1</span><span class="sxs-lookup"><span data-stu-id="8856b-126">DXT1</span></span>   | <span data-ttu-id="8856b-127">Opaco/1 bit alfa</span><span class="sxs-lookup"><span data-stu-id="8856b-127">Opaque/1-bit alpha</span></span> | <span data-ttu-id="8856b-128">N/D</span><span class="sxs-lookup"><span data-stu-id="8856b-128">N/A</span></span>                  |
| <span data-ttu-id="8856b-129">DXT2</span><span class="sxs-lookup"><span data-stu-id="8856b-129">DXT2</span></span>   | <span data-ttu-id="8856b-130">Alfa explícito</span><span class="sxs-lookup"><span data-stu-id="8856b-130">Explicit alpha</span></span>     | <span data-ttu-id="8856b-131">Sim</span><span class="sxs-lookup"><span data-stu-id="8856b-131">Yes</span></span>                  |
| <span data-ttu-id="8856b-132">DXT3</span><span class="sxs-lookup"><span data-stu-id="8856b-132">DXT3</span></span>   | <span data-ttu-id="8856b-133">Alfa explícito</span><span class="sxs-lookup"><span data-stu-id="8856b-133">Explicit alpha</span></span>     | <span data-ttu-id="8856b-134">Não</span><span class="sxs-lookup"><span data-stu-id="8856b-134">No</span></span>                   |
| <span data-ttu-id="8856b-135">DXT4</span><span class="sxs-lookup"><span data-stu-id="8856b-135">DXT4</span></span>   | <span data-ttu-id="8856b-136">Alfa interpolado</span><span class="sxs-lookup"><span data-stu-id="8856b-136">Interpolated alpha</span></span> | <span data-ttu-id="8856b-137">Sim</span><span class="sxs-lookup"><span data-stu-id="8856b-137">Yes</span></span>                  |
| <span data-ttu-id="8856b-138">DXT5</span><span class="sxs-lookup"><span data-stu-id="8856b-138">DXT5</span></span>   | <span data-ttu-id="8856b-139">Alfa interpolado</span><span class="sxs-lookup"><span data-stu-id="8856b-139">Interpolated alpha</span></span> | <span data-ttu-id="8856b-140">Não</span><span class="sxs-lookup"><span data-stu-id="8856b-140">No</span></span>                   |



 

<span data-ttu-id="8856b-141">Quando você transfere dados de um formato nonpremultiplied para um formato premultiplicado, o Direct3D dimensiona as cores com base nos valores Alfa.</span><span class="sxs-lookup"><span data-stu-id="8856b-141">When you transfer data from a nonpremultiplied format to a premultiplied format, Direct3D scales the colors based on the alpha values.</span></span> <span data-ttu-id="8856b-142">Não há suporte para a transferência de dados de um formato premultiplicado para um formato nonpremultiplied.</span><span class="sxs-lookup"><span data-stu-id="8856b-142">Transferring data from a premultiplied format to a nonpremultiplied format is not supported.</span></span> <span data-ttu-id="8856b-143">Se você tentar transferir dados de uma fonte alfa contramultiplicada para um destino alfa nonpremultiplied, o método retornará D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8856b-143">If you try to transfer data from a premultiplied alpha source to a nonpremultiplied alpha destination, the method returns D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="8856b-144">Se você transferir dados de uma fonte alfa já multiplicada para um destino que não tem alfa, os componentes de cor de origem, que foram dimensionados por alfa, serão copiados como estão.</span><span class="sxs-lookup"><span data-stu-id="8856b-144">If you transfer data from a premultiplied alpha source to a destination that has no alpha, the source color components, which have been scaled by alpha, are copied as is.</span></span>

## <a name="decompressing-compressed-texture-surfaces"></a><span data-ttu-id="8856b-145">Descompactando superfícies de textura compactadas</span><span class="sxs-lookup"><span data-stu-id="8856b-145">Decompressing Compressed Texture Surfaces</span></span>

<span data-ttu-id="8856b-146">Assim como na compactação de uma superfície de textura, a descompactação de uma textura compactada é executada por meio de serviços de cópia de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8856b-146">As with compressing a texture surface, decompressing a compressed texture is performed through Direct3D copying services.</span></span>

<span data-ttu-id="8856b-147">Para copiar uma superfície de textura compactada para uma superfície de textura descompactada, use a função [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span><span class="sxs-lookup"><span data-stu-id="8856b-147">To copy a compressed texture surface to a uncompressed texture surface, use the function [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span></span> <span data-ttu-id="8856b-148">Essas funções manipulam a compactação de e para superfícies compactadas e descompactadas.</span><span class="sxs-lookup"><span data-stu-id="8856b-148">This functions handles compression to and from compressed and uncompressed surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8856b-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8856b-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8856b-150">Recursos de textura compactados</span><span class="sxs-lookup"><span data-stu-id="8856b-150">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 
