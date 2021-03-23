---
title: Subrecursos (gráficos do Direct3D 12)
description: Descreve como um recurso é dividido em subrecursos e como fazer referência a uma única, várias ou fatia de subrecursos.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548264"
---
# <a name="subresources-direct3d-12-graphics"></a><span data-ttu-id="e29da-103">Subrecursos (gráficos do Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="e29da-103">Subresources (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="e29da-104">Descreve como um recurso é dividido em subrecursos e como fazer referência a uma única, várias ou fatia de subrecursos.</span><span class="sxs-lookup"><span data-stu-id="e29da-104">Describes how a resource is divided into subresources, and how to reference a single, multiple or slice of subresources.</span></span>

-   [<span data-ttu-id="e29da-105">Subrecursos de exemplo</span><span class="sxs-lookup"><span data-stu-id="e29da-105">Example subresources</span></span>](#example-subresources)
    -   [<span data-ttu-id="e29da-106">Indexação de subrecurso</span><span class="sxs-lookup"><span data-stu-id="e29da-106">Subresource indexing</span></span>](#subresource-indexing)
    -   [<span data-ttu-id="e29da-107">Fatia MIP</span><span class="sxs-lookup"><span data-stu-id="e29da-107">Mip slice</span></span>](#mip-slice)
    -   [<span data-ttu-id="e29da-108">Fatia da matriz</span><span class="sxs-lookup"><span data-stu-id="e29da-108">Array slice</span></span>](#array-slice)
    -   [<span data-ttu-id="e29da-109">Fatia do plano</span><span class="sxs-lookup"><span data-stu-id="e29da-109">Plane slice</span></span>](#plane-slice)
    -   [<span data-ttu-id="e29da-110">Vários subrecursos</span><span class="sxs-lookup"><span data-stu-id="e29da-110">Multiple subresources</span></span>](#multiple-subresources)
-   [<span data-ttu-id="e29da-111">APIs de subrecurso</span><span class="sxs-lookup"><span data-stu-id="e29da-111">Subresource APIs</span></span>](#subresource-apis)
-   [<span data-ttu-id="e29da-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e29da-112">Related topics</span></span>](#related-topics)

## <a name="example-subresources"></a><span data-ttu-id="e29da-113">Subrecursos de exemplo</span><span class="sxs-lookup"><span data-stu-id="e29da-113">Example subresources</span></span>

<span data-ttu-id="e29da-114">Se um recurso contiver um buffer, ele simplesmente conterá um subrecurso com um índice de 0.</span><span class="sxs-lookup"><span data-stu-id="e29da-114">If a resource contains a buffer, then it simply contains one subresource with an index of 0.</span></span> <span data-ttu-id="e29da-115">Se o recurso contiver uma textura (ou matriz de textura), a referência aos subrecursos será mais complexa.</span><span class="sxs-lookup"><span data-stu-id="e29da-115">If the resource contains a texture (or texture array), then referencing the subresources is more complex.</span></span>

<span data-ttu-id="e29da-116">Algumas APIs acessam um recurso inteiro (como o método [**ID3D12GraphicsCommandList:: CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) ); outras pessoas acessam uma parte de um recurso (por exemplo, o método [**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ).</span><span class="sxs-lookup"><span data-stu-id="e29da-116">Some APIs access an entire resource (such as the [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) method), others access a portion of a resource (for example the [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) method).</span></span> <span data-ttu-id="e29da-117">Os métodos que acessam uma parte de um recurso geralmente usam uma descrição de exibição (como a estrutura [**\_ SRV da \_ matriz \_ D3D12 TEX2D**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) ) para especificar os subrecursos a serem acessados.</span><span class="sxs-lookup"><span data-stu-id="e29da-117">The methods that access a portion of a resource generally use a view description (such as the [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) structure) to specify the subresources to access.</span></span> <span data-ttu-id="e29da-118">Consulte a seção [APIs de subrecurso](#subresource-apis) para obter uma lista completa.</span><span class="sxs-lookup"><span data-stu-id="e29da-118">Refer to the [Subresource APIs](#subresource-apis) section for a complete list.</span></span>

### <a name="subresource-indexing"></a><span data-ttu-id="e29da-119">Indexação de subrecurso</span><span class="sxs-lookup"><span data-stu-id="e29da-119">Subresource indexing</span></span>

<span data-ttu-id="e29da-120">Para indexar um determinado subrecurso, os níveis MIP são indexados primeiro à medida que cada entrada de matriz é indexada.</span><span class="sxs-lookup"><span data-stu-id="e29da-120">To index a particular subresource, the mip levels are indexed first as each array entry is indexed.</span></span>

![indexação de subrecurso](images/subresource-index.png)

### <a name="mip-slice"></a><span data-ttu-id="e29da-122">Fatia MIP</span><span class="sxs-lookup"><span data-stu-id="e29da-122">Mip slice</span></span>

<span data-ttu-id="e29da-123">Uma fatia MIP inclui um nível de mipmap para cada textura em uma matriz, conforme mostrado na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="e29da-123">A mip slice includes one mipmap level for every texture in an array, as shown in the following image.</span></span>

![fatias MIP de subrecurso](images/subresource-mip-slice.png)

### <a name="array-slice"></a><span data-ttu-id="e29da-125">Fatia da matriz</span><span class="sxs-lookup"><span data-stu-id="e29da-125">Array slice</span></span>

<span data-ttu-id="e29da-126">Dada uma matriz de texturas, cada textura com mipmaps, uma fatia de matriz inclui uma textura e todos os seus níveis de MIP, conforme mostrado na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="e29da-126">Given an array of textures, each texture with mipmaps, an array slice includes one texture and all of its mip levels, as shown in the following image.</span></span>

![fatias de matriz de subrecurso](images/subresource-array-slices.png)

### <a name="plane-slice"></a><span data-ttu-id="e29da-128">Fatia do plano</span><span class="sxs-lookup"><span data-stu-id="e29da-128">Plane slice</span></span>

<span data-ttu-id="e29da-129">Normalmente, os formatos planar não são usados para armazenar dados RGBA, mas nos casos em que eles são (talvez 24bpp dados RGB), um plano poderia representar a imagem vermelha, um verde e uma imagem azul.</span><span class="sxs-lookup"><span data-stu-id="e29da-129">Typically planar formats are not used to store RGBA data, but in the cases where it is (perhaps 24bpp RGB data), one plane could represent the red image, one the green, and one the blue image.</span></span> <span data-ttu-id="e29da-130">Embora um plano não seja necessariamente uma cor, duas ou mais cores poderiam ser combinadas em um plano.</span><span class="sxs-lookup"><span data-stu-id="e29da-130">One plane though is not necessarily one color, two or more colors could be combined into one plane.</span></span> <span data-ttu-id="e29da-131">Normalmente, os dados planar são usados para dados YCbCr Depth-Stencil e de subamostrados.</span><span class="sxs-lookup"><span data-stu-id="e29da-131">More typically planar data is used for sub-sampled YCbCr and Depth-Stencil data.</span></span> <span data-ttu-id="e29da-132">Depth-Stencil é o único formato que dá suporte total a mipmaps, matrizes e vários planos (geralmente plano 0 para profundidade e plano 1 para o estêncil).</span><span class="sxs-lookup"><span data-stu-id="e29da-132">Depth-Stencil is the only format that fully supports mipmaps, arrays, and multiple planes (often plane 0 for Depth and plane 1 for Stencil).</span></span>

<span data-ttu-id="e29da-133">A indexação de subrecurso para uma matriz de duas imagens de Depth-Stencil, cada uma com três níveis de MIP, é mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="e29da-133">The subresource indexing for an array of two Depth-Stencil images, each with three mip levels, is shown below.</span></span>

![indexação do estêncil de profundidade](images/depth-stencil-indexing.png)

<span data-ttu-id="e29da-135">A subamostra YCbCr dá suporte a matrizes e tem planos, mas não oferece suporte a mipmaps.</span><span class="sxs-lookup"><span data-stu-id="e29da-135">Sub-sampled YCbCr supports arrays and has planes, but does not support mipmaps.</span></span> <span data-ttu-id="e29da-136">As imagens YCbCr têm dois planos, um para a luminância (Y) à qual o olho humano é mais sensível e outro para o crominância (CB e CR, intercalado) ao qual o olho humano é menos sensível.</span><span class="sxs-lookup"><span data-stu-id="e29da-136">YCbCr images have two planes, one for the luminance (Y) that the human eye is most sensitive to, and one for the chrominance (both Cb, and Cr, interleaved) which the human eye is less sensitive to.</span></span> <span data-ttu-id="e29da-137">Esse formato permite a compactação dos valores de crominância para compactar uma imagem sem afetar a luminância e é um formato de compactação de vídeo comum por esse motivo, embora seja usado para compactar imagens ainda.</span><span class="sxs-lookup"><span data-stu-id="e29da-137">This format enables compression of the chrominance values in order to compress an image without affecting the luminance, and is a common video compression format for that reason, although it is used to compress still images.</span></span> <span data-ttu-id="e29da-138">A imagem abaixo mostra o formato NV12, observando que o crominância foi compactado para um quarto da resolução da luminância, o que significa que a largura de cada plano é idêntica e o plano de crominância é metade da altura do plano de luminância.</span><span class="sxs-lookup"><span data-stu-id="e29da-138">The image below shows the NV12 format, noting the chrominance has been compressed to one quarter of the resolution of the luminance, meaning the width of each plane is identical, and the chrominance plane is half the height of the luminance plane.</span></span> <span data-ttu-id="e29da-139">Os planos seriam indexados como subrecursos de forma idêntica ao exemplo de Depth-Stencil acima.</span><span class="sxs-lookup"><span data-stu-id="e29da-139">The planes would be indexed as subresources in an identical way to the Depth-Stencil example above.</span></span>

![o formato NV12](images/ycbcr.png)

<span data-ttu-id="e29da-141">Os formatos planar existiam no Direct3D 11, mas os planos individuais não podiam ser resolvidos individualmente, digamos para operações de cópia ou mapeamento.</span><span class="sxs-lookup"><span data-stu-id="e29da-141">Planar formats existed in Direct3D 11, but individual planes could not be addressed individually, say for copy or mapping operations.</span></span> <span data-ttu-id="e29da-142">Isso foi alterado no Direct3D 12 para que cada plano tenha recebido sua própria ID de subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e29da-142">This was changed in Direct3D 12 so that each plane received its own subresource ID.</span></span> <span data-ttu-id="e29da-143">Compare os dois métodos a seguir para calcular a ID do subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e29da-143">Compare the following two methods for calculating the subresource ID.</span></span>

<span data-ttu-id="e29da-144">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e29da-144">Direct3D 11</span></span>

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

<span data-ttu-id="e29da-145">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e29da-145">Direct3D 12</span></span>

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

<span data-ttu-id="e29da-146">A maioria dos hardwares pressupõe que a memória para o plano N sempre é imediatamente alocada após o plano N-1.</span><span class="sxs-lookup"><span data-stu-id="e29da-146">Most hardware assumes that the memory for plane N is always immediately allocated after plane N-1.</span></span>

<span data-ttu-id="e29da-147">Uma alternativa ao uso de subrecursos é que um aplicativo pode alocar um recurso completamente separado por plano.</span><span class="sxs-lookup"><span data-stu-id="e29da-147">An alternative to using subresources is that an app could allocate a completely separate resource per plane.</span></span> <span data-ttu-id="e29da-148">Nesse caso, o aplicativo entende que os dados são planar e usa vários recursos para representá-los.</span><span class="sxs-lookup"><span data-stu-id="e29da-148">In this case, the application understands the data is planar and uses multiple resources to represent it.</span></span>

### <a name="multiple-subresources"></a><span data-ttu-id="e29da-149">Vários subrecursos</span><span class="sxs-lookup"><span data-stu-id="e29da-149">Multiple subresources</span></span>

<span data-ttu-id="e29da-150">Um modo de exibição de recurso de sombreador pode selecionar qualquer região retangular de subrecursos, usando uma das fatias descritas acima e criteriosamente o uso de campos nas estruturas de exibição (como [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), conforme mostrado na imagem.</span><span class="sxs-lookup"><span data-stu-id="e29da-150">A shader-resource view can select any rectangular region of subresources, using one of the slices described above and judicious use of fields in the view structures (such as [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), as shown in the image.</span></span>

![seleção múltipla de subrecurso](images/subresource-multiple.png)

<span data-ttu-id="e29da-152">Uma exibição de destino de renderização só pode usar um único subrecurso ou uma fatia MIP e não pode incluir subrecursos de mais de uma fatia MIP.</span><span class="sxs-lookup"><span data-stu-id="e29da-152">A render-target view can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="e29da-153">Ou seja, todas as texturas em uma exibição de destino de renderização devem ter o mesmo tamanho.</span><span class="sxs-lookup"><span data-stu-id="e29da-153">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="e29da-154">Um modo de exibição de recurso de sombreador pode selecionar qualquer região retangular de subrecurso, conforme mostrado na imagem.</span><span class="sxs-lookup"><span data-stu-id="e29da-154">A shader-resource view can select any rectangular region of subresources, as shown in the image.</span></span>

## <a name="subresource-apis"></a><span data-ttu-id="e29da-155">APIs de subrecurso</span><span class="sxs-lookup"><span data-stu-id="e29da-155">Subresource APIs</span></span>

<span data-ttu-id="e29da-156">As seguintes referências de APIs e funcionam com os subrecursos:</span><span class="sxs-lookup"><span data-stu-id="e29da-156">The following APIs reference and work with subresources:</span></span>

<span data-ttu-id="e29da-157">Enumerações:</span><span class="sxs-lookup"><span data-stu-id="e29da-157">Enumerations:</span></span>

-   [<span data-ttu-id="e29da-158">**\_Tipo de \_ cópia de textura D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="e29da-158">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

<span data-ttu-id="e29da-159">As estruturas a seguir contêm índices *PlaneSlice* , a maioria contém índices *MipSlice* .</span><span class="sxs-lookup"><span data-stu-id="e29da-159">The following structures contain *PlaneSlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="e29da-160">**D3D12 \_ TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="e29da-160">**D3D12\_TEX2D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [<span data-ttu-id="e29da-161">**\_Matriz D3D12 \_ TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="e29da-161">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="e29da-162">**D3D12 \_ TEX2D \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="e29da-162">**D3D12\_TEX2D\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [<span data-ttu-id="e29da-163">**D3D12 \_ TEX2D \_ matriz \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="e29da-163">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="e29da-164">**D3D12 \_ TEX2D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="e29da-164">**D3D12\_TEX2D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [<span data-ttu-id="e29da-165">**\_Matriz D3D12 \_ TEX2D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="e29da-165">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="e29da-166">As estruturas a seguir contêm índices *ArraySlice* , a maioria contém índices *MipSlice* .</span><span class="sxs-lookup"><span data-stu-id="e29da-166">The following structures contain *ArraySlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="e29da-167">**\_DSV de \_ matriz D3D12 TEX1D \_**</span><span class="sxs-lookup"><span data-stu-id="e29da-167">**D3D12\_TEX1D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [<span data-ttu-id="e29da-168">**\_DSV de \_ matriz D3D12 TEX2D \_**</span><span class="sxs-lookup"><span data-stu-id="e29da-168">**D3D12\_TEX2D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [<span data-ttu-id="e29da-169">**\_DSV de \_ matriz D3D12 TEX2DMS \_**</span><span class="sxs-lookup"><span data-stu-id="e29da-169">**D3D12\_TEX2DMS\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [<span data-ttu-id="e29da-170">**\_Matriz D3D12 \_ TEX1D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="e29da-170">**D3D12\_TEX1D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [<span data-ttu-id="e29da-171">**\_Matriz D3D12 \_ TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="e29da-171">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="e29da-172">**\_Matriz D3D12 \_ TEX2DMS \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="e29da-172">**D3D12\_TEX2DMS\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [<span data-ttu-id="e29da-173">**D3D12 \_ TEX1D \_ matriz \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="e29da-173">**D3D12\_TEX1D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [<span data-ttu-id="e29da-174">**D3D12 \_ TEX2D \_ matriz \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="e29da-174">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="e29da-175">**D3D12 \_ TEX2DMS \_ matriz \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="e29da-175">**D3D12\_TEX2DMS\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [<span data-ttu-id="e29da-176">**\_Matriz D3D12 \_ TEX1D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="e29da-176">**D3D12\_TEX1D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [<span data-ttu-id="e29da-177">**\_Matriz D3D12 \_ TEX2D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="e29da-177">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="e29da-178">As estruturas a seguir contêm índices *MipSlice* , mas nem índices *ArraySlice* nem *PlaneSlice* .</span><span class="sxs-lookup"><span data-stu-id="e29da-178">The following structures contain *MipSlice* indexes, but neither *ArraySlice* nor *PlaneSlice* indexes.</span></span>

-   [<span data-ttu-id="e29da-179">**\_DSV D3D12 TEX1D \_**</span><span class="sxs-lookup"><span data-stu-id="e29da-179">**D3D12\_TEX1D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [<span data-ttu-id="e29da-180">**\_DSV D3D12 TEX2D \_**</span><span class="sxs-lookup"><span data-stu-id="e29da-180">**D3D12\_TEX2D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [<span data-ttu-id="e29da-181">**D3D12 \_ TEX1D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="e29da-181">**D3D12\_TEX1D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [<span data-ttu-id="e29da-182">**D3D12 \_ TEX3D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="e29da-182">**D3D12\_TEX3D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [<span data-ttu-id="e29da-183">**D3D12 \_ TEX1D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="e29da-183">**D3D12\_TEX1D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [<span data-ttu-id="e29da-184">**D3D12 \_ TEX3D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="e29da-184">**D3D12\_TEX3D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

<span data-ttu-id="e29da-185">As seguintes estruturas também fazem referência a subrecursos:</span><span class="sxs-lookup"><span data-stu-id="e29da-185">The following structures also reference subresources:</span></span>

-   <span data-ttu-id="e29da-186">[**D3D12 \_ \_Região de descarte**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : uma estrutura usada na preparação para descartar um recurso.</span><span class="sxs-lookup"><span data-stu-id="e29da-186">[**D3D12\_DISCARD\_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : a structure used in preparation for discarding a resource.</span></span>
-   <span data-ttu-id="e29da-187">[**D3D12 \_ \_ \_ Superfície do SUBrecurso posicionado**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : Adiciona um deslocamento em um recurso à superfície básica.</span><span class="sxs-lookup"><span data-stu-id="e29da-187">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : adds an offset into a resource to the basic footprint.</span></span>
-   <span data-ttu-id="e29da-188">[**D3D12 \_ \_ \_ Barreira de transição de recurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : descreve a transição de subrecursos entre diferentes usos (recurso de sombreador, destino de renderização, etc.).</span><span class="sxs-lookup"><span data-stu-id="e29da-188">[**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : describes the transition of subresources between different usages (shader resource, render target, etc.).</span></span>
-   <span data-ttu-id="e29da-189">[**D3D12 \_ \_Dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : os dados de subrecurso incluem os dados em si e a densidade da linha e da fatia.</span><span class="sxs-lookup"><span data-stu-id="e29da-189">[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : subresource data includes the data itself, and the row and slice pitch.</span></span>
-   <span data-ttu-id="e29da-190">[**D3D12 \_ \_Superfície de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : uma superfície inclui o formato, a largura, a altura, a profundidade e o tom de linha do subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e29da-190">[**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : a footprint includes the format, width, height, depth and row-pitch of the subresource.</span></span>
-   <span data-ttu-id="e29da-191">[**D3D12 \_ \_Informações de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contém o deslocamento, a densidade da linha e a densidade da profundidade do subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e29da-191">[**D3D12\_SUBRESOURCE\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contains the offset, row pitch and depth pitch of the subresource.</span></span>
-   <span data-ttu-id="e29da-192">[**D3D12 \_ Subrecurso \_ lado**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) a lado: descreve um volume de subrecurso com subdivisão (consulte [recursos do lado do volume](volume-tiled-resources.md)).</span><span class="sxs-lookup"><span data-stu-id="e29da-192">[**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : describes a tiled subresource volume (refer to [Volume Tiled Resources](volume-tiled-resources.md)).</span></span>
-   <span data-ttu-id="e29da-193">[**D3D12 \_ \_ \_ Local da cópia de textura**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : descreve uma parte de uma textura com a finalidade de copiar.</span><span class="sxs-lookup"><span data-stu-id="e29da-193">[**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : describes a portion of a texture for the purpose of copying.</span></span>
-   <span data-ttu-id="e29da-194">[**D3D12 \_ \_ \_ Coordenada de recurso por lado**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .: descreve as coordenadas de um recurso de lado.</span><span class="sxs-lookup"><span data-stu-id="e29da-194">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : describes the coordinates of a tiled resource.</span></span>

<span data-ttu-id="e29da-195">Métodos:</span><span class="sxs-lookup"><span data-stu-id="e29da-195">Methods:</span></span>

-   <span data-ttu-id="e29da-196">[**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : Obtém informações sobre um recurso, para permitir que uma cópia seja feita.</span><span class="sxs-lookup"><span data-stu-id="e29da-196">[**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : gets information on a resource, to enable a copy to be made.</span></span>
-   <span data-ttu-id="e29da-197">[**ID3D12Device:: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : Obtém informações sobre como um recurso de quebra-lado é dividido em blocos.</span><span class="sxs-lookup"><span data-stu-id="e29da-197">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>
-   <span data-ttu-id="e29da-198">[**ID3D12GraphicsCommandList:: ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copia um subrecurso de várias amostras em um subrecurso sem várias amostras.</span><span class="sxs-lookup"><span data-stu-id="e29da-198">[**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copies a multi-sampled subresource into a non-multi-sampled subresource.</span></span>
-   <span data-ttu-id="e29da-199">[**ID3D12Resource:: map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : retorna um ponteiro para os dados especificados no recurso e nega o acesso à GPU para o subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e29da-199">[**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : returns a pointer to the specified data in the resource, and denies the GPU access to the subresource.</span></span>
-   <span data-ttu-id="e29da-200">[**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : Copia dados de um subrecurso ou uma região retangular de um subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e29da-200">[**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copies data from a subresource, or a rectangular region of a subresource.</span></span>
-   <span data-ttu-id="e29da-201">[**ID3D12Resource:: remapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : cancela o mapeamento do intervalo de memória especificado e invalida o ponteiro para o recurso.</span><span class="sxs-lookup"><span data-stu-id="e29da-201">[**ID3D12Resource::Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : unmaps the specified range of memory and invalidates the pointer to the resource.</span></span> <span data-ttu-id="e29da-202">Restabelece o acesso à GPU para o subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e29da-202">Reinstates GPU access to the subresource.</span></span>
-   <span data-ttu-id="e29da-203">[**ID3D12Resource:: WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : Copia dados para um subrecurso ou uma região retangular de um subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e29da-203">[**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copies data to a subresource, or a rectangular region of a subresource.</span></span>

<span data-ttu-id="e29da-204">As texturas devem estar no estado [**comum do \_ estado do recurso \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) para acesso de CPU por meio de [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) e [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) para serem legais; mas os buffers não.</span><span class="sxs-lookup"><span data-stu-id="e29da-204">Textures must be in the [**D3D12\_RESOURCE\_STATE\_COMMON**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) state for CPU access through [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) and [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) to be legal; but buffers do not.</span></span> <span data-ttu-id="e29da-205">O acesso de CPU a um recurso normalmente é [**feito por meio**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)do / [**mapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="e29da-205">CPU access to a resource is typically done through [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)/[**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e29da-206">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e29da-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e29da-207">Associação de recursos</span><span class="sxs-lookup"><span data-stu-id="e29da-207">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 




