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
# <a name="subresources-direct3d-11-graphics"></a>Subrecursos (gráficos do Direct3D 11)

Este tópico descreve os subrecursos de textura ou partes de um recurso.

O Direct3D pode fazer referência a um recurso inteiro ou pode fazer referência aos subconjuntos de um recurso. O termo sub-recurso refere-se ao subconjunto de um recurso.

Um buffer é definido como um sub-recurso único. As texturas são um pouco mais complicadas porque há vários tipos de textura diferentes (1D, 2D, etc.) que dão suporte a níveis de mipmap e/ou matrizes de textura. Começando com o caso mais simples, uma textura 1D é definida como um sub-recurso único, conforme mostrado na ilustração a seguir.

![ilustração de uma textura 1D](images/d3d10-1d-texture.png)

Isso significa que a matriz de texels que compõe uma textura 1D está contida em um único sub-recurso.

Se você expandir uma textura 1D com três níveis de mipmap, ele poderá ser visualizado como a ilustração a seguir.

![ilustração de uma textura 1D com três níveis de mipmap](images/d3d10-resource-texture1d.png)

Imagine isso como uma única textura composta por três subrecursos. Um subrecurso pode ser indexado usando o nível de detalhe (LOD) para uma única textura. Ao usar uma matriz de texturas, o acesso a um determinado subrecurso exige o LOD e a textura específica. Como alternativa, a API combina essas duas informações em um único índice de subrecurso com base em zero, como mostrado na ilustração a seguir.

![ilustração de um índice de sub-recurso baseado em zero](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a>Selecionando sub-recursos

Algumas APIs acessam um recurso inteiro (por exemplo, o método [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ), outras acessam uma parte de um recurso (por exemplo, o método [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) ou o método [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) ). Os métodos que acessam uma parte de um recurso geralmente usam uma descrição de exibição (como a estrutura [**\_ DSV de \_ matriz \_ D3D11 TEX2D**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) ) para especificar os subrecursos a serem acessados.

As ilustrações nas seções a seguir mostram os termos usados por uma descrição de exibição ao acessar uma matriz de texturas.

### <a name="array-slice"></a>Fatia de matriz

Dada uma matriz de texturas, cada textura com mipmaps, uma *fatia de matriz* (representada pelo retângulo branco) inclui uma textura e todos os seus subrecursos, conforme mostrado na ilustração a seguir.

![ilustração de uma fatia de matriz](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Tamanho de MIP

Uma *fatia MIP* (representada pelo retângulo branco) inclui um nível de mipmap para cada textura em uma matriz, conforme mostrado na ilustração a seguir.

![ilustração de uma fatia MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Selecionando um sub-recurso único

Você pode usar esses dois tipos de fatias para escolher um sub-recurso único, conforme mostrado na ilustração a seguir.

![ilustração de escolher um subrecurso usando uma fatia de matriz e uma fatia MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Selecionando vários sub-recursos

Ou você pode usar esses dois tipos de fatias com o número de níveis mipmap e/ou número de texturas, para escolher vários subrecursos, conforme mostrado na ilustração a seguir.

![ilustração de escolher vários subrecursos](images/d3d10-resource-subresources-2.png)

> [!Note]  
> Uma [**exibição de destino de renderização**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) só pode usar um único subrecurso ou uma fatia MIP e não pode incluir subrecursos de mais de uma fatia MIP. Ou seja, todas as texturas em uma exibição de destino de renderização devem ter o mesmo tamanho. Um [**modo de exibição de recurso de sombreador**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) pode selecionar qualquer região retangular de subrecurso, conforme mostrado na figura.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




