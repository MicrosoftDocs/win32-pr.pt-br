---
title: Subrecursos (gráficos do Direct3D 11)
description: Este tópico descreve os subrecursos de textura ou partes de um recurso.
ms.assetid: 57444cb5-6c8b-4dac-8d6b-ca2b45eafac9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a432dbfbcbf08c4359ea436a3e8fa025c801d12
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008668"
---
# <a name="subresources-direct3d-11-graphics"></a><span data-ttu-id="13753-103">Subrecursos (gráficos do Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="13753-103">Subresources (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="13753-104">Este tópico descreve os subrecursos de textura ou partes de um recurso.</span><span class="sxs-lookup"><span data-stu-id="13753-104">This topic describes texture subresources, or portions of a resource.</span></span>

<span data-ttu-id="13753-105">O Direct3D pode fazer referência a um recurso inteiro ou pode fazer referência aos subconjuntos de um recurso.</span><span class="sxs-lookup"><span data-stu-id="13753-105">Direct3D can reference an entire resource or it can reference subsets of a resource.</span></span> <span data-ttu-id="13753-106">O termo sub-recurso refere-se ao subconjunto de um recurso.</span><span class="sxs-lookup"><span data-stu-id="13753-106">The term subresource refers to a subset of a resource.</span></span>

<span data-ttu-id="13753-107">Um buffer é definido como um sub-recurso único.</span><span class="sxs-lookup"><span data-stu-id="13753-107">A buffer is defined as a single subresource.</span></span> <span data-ttu-id="13753-108">As texturas são um pouco mais complicadas porque há vários tipos de textura diferentes (1D, 2D, etc.) que dão suporte a níveis de mipmap e/ou matrizes de textura.</span><span class="sxs-lookup"><span data-stu-id="13753-108">Textures are a little more complicated because there are several different texture types (1D, 2D, etc.) some of which support mipmap levels and/or texture arrays.</span></span> <span data-ttu-id="13753-109">Começando com o caso mais simples, uma textura 1D é definida como um sub-recurso único, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="13753-109">Beginning with the simplest case, a 1D texture is defined as a single subresource, as shown in the following illustration.</span></span>

![ilustração de uma textura 1D](images/d3d10-1d-texture.png)

<span data-ttu-id="13753-111">Isso significa que a matriz de texels que compõe uma textura 1D está contida em um único sub-recurso.</span><span class="sxs-lookup"><span data-stu-id="13753-111">This means that the array of texels that make up a 1D texture are contained in a single subresource.</span></span>

<span data-ttu-id="13753-112">Se você expandir uma textura 1D com três níveis de mipmap, ele poderá ser visualizado como a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="13753-112">If you expand a 1D texture with three mipmap levels, it can be visualized like the following illustration.</span></span>

![ilustração de uma textura 1D com três níveis de mipmap](images/d3d10-resource-texture1d.png)

<span data-ttu-id="13753-114">Imagine isso como uma única textura composta por três subrecursos.</span><span class="sxs-lookup"><span data-stu-id="13753-114">Think of this as a single texture that is made up of three subresources.</span></span> <span data-ttu-id="13753-115">Um subrecurso pode ser indexado usando o nível de detalhe (LOD) para uma única textura.</span><span class="sxs-lookup"><span data-stu-id="13753-115">A subresource can be indexed using the level-of-detail (LOD) for a single texture.</span></span> <span data-ttu-id="13753-116">Ao usar uma matriz de texturas, o acesso a um determinado subrecurso exige o LOD e a textura específica.</span><span class="sxs-lookup"><span data-stu-id="13753-116">When using an array of textures, accessing a particular subresource requires both the LOD and the particular texture.</span></span> <span data-ttu-id="13753-117">Como alternativa, a API combina essas duas informações em um único índice de subrecurso com base em zero, como mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="13753-117">Alternately, the API combines these two pieces of information into a single zero-based subresource index, as shown in the following illustration.</span></span>

![ilustração de um índice de sub-recurso baseado em zero](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a><span data-ttu-id="13753-119">Selecionando sub-recursos</span><span class="sxs-lookup"><span data-stu-id="13753-119">Selecting Subresources</span></span>

<span data-ttu-id="13753-120">Algumas APIs acessam um recurso inteiro (por exemplo, o método [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ), outras acessam uma parte de um recurso (por exemplo, o método [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) ou o método [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) ).</span><span class="sxs-lookup"><span data-stu-id="13753-120">Some APIs access an entire resource (for example the [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) method), others access a portion of a resource (for example the [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) method or the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method).</span></span> <span data-ttu-id="13753-121">Os métodos que acessam uma parte de um recurso geralmente usam uma descrição de exibição (como a estrutura [**\_ DSV de \_ matriz \_ D3D11 TEX2D**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) ) para especificar os subrecursos a serem acessados.</span><span class="sxs-lookup"><span data-stu-id="13753-121">The methods that access a portion of a resource generally use a view description (such as the [**D3D11\_TEX2D\_ARRAY\_DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) structure) to specify the subresources to access.</span></span>

<span data-ttu-id="13753-122">As ilustrações nas seções a seguir mostram os termos usados por uma descrição de exibição ao acessar uma matriz de texturas.</span><span class="sxs-lookup"><span data-stu-id="13753-122">The illustrations in the following sections show the terms used by a view description when accessing an array of textures.</span></span>

### <a name="array-slice"></a><span data-ttu-id="13753-123">Fatia de matriz</span><span class="sxs-lookup"><span data-stu-id="13753-123">Array Slice</span></span>

<span data-ttu-id="13753-124">Dada uma matriz de texturas, cada textura com mipmaps, uma *fatia de matriz* (representada pelo retângulo branco) inclui uma textura e todos os seus subrecursos, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="13753-124">Given an array of textures, each texture with mipmaps, an *array slice* (represented by the white rectangle) includes one texture and all of its subresources, as shown in the following illustration.</span></span>

![ilustração de uma fatia de matriz](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a><span data-ttu-id="13753-126">Tamanho de MIP</span><span class="sxs-lookup"><span data-stu-id="13753-126">Mip Slice</span></span>

<span data-ttu-id="13753-127">Uma *fatia MIP* (representada pelo retângulo branco) inclui um nível de mipmap para cada textura em uma matriz, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="13753-127">A *mip slice* (represented by the white rectangle) includes one mipmap level for every texture in an array, as shown in the following illustration.</span></span>

![ilustração de uma fatia MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a><span data-ttu-id="13753-129">Selecionando um sub-recurso único</span><span class="sxs-lookup"><span data-stu-id="13753-129">Selecting a Single Subresource</span></span>

<span data-ttu-id="13753-130">Você pode usar esses dois tipos de fatias para escolher um sub-recurso único, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="13753-130">You can use these two types of slices to choose a single subresource, as shown in the following illustration.</span></span>

![ilustração de escolher um subrecurso usando uma fatia de matriz e uma fatia MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a><span data-ttu-id="13753-132">Selecionando vários sub-recursos</span><span class="sxs-lookup"><span data-stu-id="13753-132">Selecting Multiple Subresources</span></span>

<span data-ttu-id="13753-133">Ou você pode usar esses dois tipos de fatias com o número de níveis mipmap e/ou número de texturas, para escolher vários subrecursos, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="13753-133">Or you can use these two types of slices with the number of mipmap levels and/or number of textures, to choose multiple subresources, as shown in the following illustration.</span></span>

![ilustração de escolher vários subrecursos](images/d3d10-resource-subresources-2.png)

> [!Note]  
> <span data-ttu-id="13753-135">Uma [**exibição de destino de renderização**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) só pode usar um único subrecurso ou uma fatia MIP e não pode incluir subrecursos de mais de uma fatia MIP.</span><span class="sxs-lookup"><span data-stu-id="13753-135">A [**render-target view**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="13753-136">Ou seja, todas as texturas em uma exibição de destino de renderização devem ter o mesmo tamanho.</span><span class="sxs-lookup"><span data-stu-id="13753-136">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="13753-137">Um [**modo de exibição de recurso de sombreador**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) pode selecionar qualquer região retangular de subrecurso, conforme mostrado na figura.</span><span class="sxs-lookup"><span data-stu-id="13753-137">A [**shader-resource view**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) can select any rectangular region of subresources, as shown in the figure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="13753-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13753-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13753-139">Recursos</span><span class="sxs-lookup"><span data-stu-id="13753-139">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




