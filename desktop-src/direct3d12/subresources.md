---
title: Sub-recursos (elementos gráficos do Direct3D 12)
description: Descreve como um recurso é dividido em sub-recursos e como referenciar uma única, várias ou fatias de sub-recursos.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fc4478e71bbafb8a21897f838ee8091592024a4e3c761280911e395f8ae491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911950"
---
# <a name="subresources-direct3d-12-graphics"></a>Sub-recursos (elementos gráficos do Direct3D 12)

Descreve como um recurso é dividido em sub-recursos e como referenciar uma única, várias ou fatias de sub-recursos.

-   [Sub-recursos de exemplo](#example-subresources)
    -   [Indexação de sub-recursos](#subresource-indexing)
    -   [Fatia da Mip](#mip-slice)
    -   [Fatia da matriz](#array-slice)
    -   [Fatia do plano](#plane-slice)
    -   [Várias sub-fontes](#multiple-subresources)
-   [APIs de sub-recursos](#subresource-apis)
-   [Tópicos relacionados](#related-topics)

## <a name="example-subresources"></a>Sub-recursos de exemplo

Se um recurso contiver um buffer, ele simplesmente conterá uma sub-fonte com um índice de 0. Se o recurso contiver uma textura (ou matriz de textura), a referência às sub-fontes será mais complexa.

Algumas APIs acessam um recurso inteiro (como o método [**ID3D12GraphicsCommandList::CopyResource),**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) outras acessam uma parte de um recurso (por exemplo, o método [**ID3D12Resource::ReadFromSubresource).**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) Os métodos que acessam uma parte de um recurso geralmente usam uma descrição de exibição (como a estrutura [**SRV D3D12 \_ TEX2D \_ ARRAY) \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) para especificar as sub-fontes a acessar. Consulte a [seção APIs de sub-recursos](#subresource-apis) para ver uma lista completa.

### <a name="subresource-indexing"></a>Indexação de sub-recursos

Para indexar uma sub-fonte específica, os níveis mip são indexados primeiro à medida que cada entrada de matriz é indexada.

![indexação de sub-recursos](images/subresource-index.png)

### <a name="mip-slice"></a>Fatia da Mip

Uma fatia mip inclui um nível de mipmap para cada textura em uma matriz, conforme mostrado na imagem a seguir.

![subresource mip slices](images/subresource-mip-slice.png)

### <a name="array-slice"></a>Fatia da matriz

Dada uma matriz de texturas, cada textura com mipmaps, uma fatia de matriz inclui uma textura e todos os seus níveis de mip, conforme mostrado na imagem a seguir.

![fatias de matriz de sub-recursos](images/subresource-array-slices.png)

### <a name="plane-slice"></a>Fatia do plano

Normalmente, os formatos planares não são usados para armazenar dados RGBA, mas nos casos em que estão (talvez 24bpp de dados RGB), um plano pode representar a imagem vermelha, uma verde e outra a imagem azul. No entanto, um plano não é necessariamente uma cor, duas ou mais cores podem ser combinadas em um plano. Normalmente, os dados mais planários são usados para dados YCbCr e Depth-Stencil subempreso. Depth-Stencil é o único formato que dá suporte total a mipmaps, matrizes e vários planos (geralmente plano 0 para Profundidade e plano 1 para Estêncil).

A indexação de sub-recursos para uma matriz de duas imagens Depth-Stencil, cada uma com três níveis de mip, é mostrada abaixo.

![indexação de estêncil de profundidade](images/depth-stencil-indexing.png)

O YCbCr de sub amostra dá suporte a matrizes e tem planos, mas não dá suporte a mipmaps. As imagens YCbCr têm dois planos, um para a luminância (Y) à qual o olho humano é mais sensível e outro para acromática (Cb e Cr, intercalada) à qual o olho humano é menos sensível. Esse formato permite a compactação dos valores de chrominance para compactar uma imagem sem afetar a luminância e é um formato comum de compactação de vídeo por esse motivo, embora seja usado para compactar imagens ainda. A imagem abaixo mostra o formato NV12, indicando que acromática foi compactada para um quarto da resolução da luminância, o que significa que a largura de cada plano é idêntica e o plano decromática é metade da altura do plano de luminância. Os planos seriam indexados como sub-recursos de maneira idêntica ao Depth-Stencil exemplo acima.

![o formato nv12](images/ycbcr.png)

Os formatos planar existiam no Direct3D 11, mas planos individuais não podiam ser resolvidos individualmente, digamos, para operações de cópia ou mapeamento. Isso foi alterado no Direct3D 12 para que cada plano recebe sua própria ID de sub-fonte. Compare os dois métodos a seguir para calcular a ID da sub-fonte.

Direct3D 11

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

Direct3D 12

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

A maioria dos hardwares supõe que a memória do plano N seja sempre alocada imediatamente após o plano N-1.

Uma alternativa ao uso de sub-recursos é que um aplicativo pode alocar um recurso completamente separado por plano. Nesse caso, o aplicativo entende que os dados são planares e usa vários recursos para representá-los.

### <a name="multiple-subresources"></a>Várias sub-fontes

Uma exibição de sombreador-recurso pode selecionar qualquer região retangular de sub-fontes, usando uma das fatias descritas acima e o uso criterioso de campos nas estruturas de exibição (como [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), conforme mostrado na imagem.

![seleção de várias sub-fontes](images/subresource-multiple.png)

Uma exibição de destino de renderização só pode usar uma única sub-fonte ou fatia mip e não pode incluir sub-recursos de mais de uma fatia mip. Ou seja, cada textura em uma exibição de destino de renderização deve ter o mesmo tamanho. Uma exibição de sombreador-recurso pode selecionar qualquer região retangular de sub-fontes, conforme mostrado na imagem.

## <a name="subresource-apis"></a>APIs de sub-recursos

As apIs a seguir referenciam e funcionam com sub-recursos:

Enumerações:

-   [**TIPO DE CÓPIA DE TEXTURA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

As estruturas a seguir *contêm índices PlaneSlice,* a maioria contém *índices MipSlice.*

-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEXAS2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

As estruturas a seguir *contêm índices ArraySlice,* a maioria contém *índices MipSlice.*

-   [**D3D12 \_ TEX1D \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX1D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ ARRAY \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

As estruturas a seguir *contêm índices MipSlice,* mas nem *índices ArraySlice* nem *PlaneSlice.*

-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ UAV DO TEX3D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

As seguintes estruturas também referenciam sub-recursos:

-   [**D3D12 \_ DISCARD \_ REGION:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) uma estrutura usada na preparação para descartar um recurso.
-   [**D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) adiciona um deslocamento em um recurso ao espaço básico.
-   [**D3D12 \_ RESOURCE \_ TRANSITION \_ BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : descreve a transição de sub-recursos entre diferentes usos (recurso de sombreador, destino de renderização etc.).
-   [**D3D12 \_ SUBRESOURCE \_ DATA:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) os dados de sub-fonte incluem os dados em si e a linha e a fatia.
-   [**D3D12 \_ SUBRESOURCE \_ FOOTPRINT:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) uma área de trabalho inclui o formato, largura, altura, profundidade e tom de linha da sub-fonte.
-   [**D3D12 \_ SUBRESOURCE \_ INFO:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) contém o deslocamento, a inclinação da linha e a profundidade da sub-fonte.
-   [**D3D12 \_ SUBRESOURCE \_ TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : descreve um volume de sub-fonte lado a lado (consulte [Volume Tiled Resources](volume-tiled-resources.md)).
-   [**D3D12 \_ TEXTURE \_ COPY \_ LOCATION:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) descreve uma parte de uma textura para fins de cópia.
-   [**D3D12 \_ TILED \_ RESOURCE \_ COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : descreve as coordenadas de um recurso lado a lado.

Métodos:

-   [**ID3D12Device::GetCopyablePrints:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) obtém informações sobre um recurso para permitir que uma cópia seja feita.
-   [**ID3D12Device::GetResourceTiling:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) obtém informações sobre como um recurso lado a lado é dividido em blocos.
-   [**ID3D12GraphicsCommandList::ResolveSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) copia uma sub-fonte com várias amostras em uma sub-fonte que não tem várias amostras.
-   [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : retorna um ponteiro para os dados especificados no recurso e nega o acesso de GPU à sub-fonte.
-   [**ID3D12Resource::ReadFromSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) copia dados de uma sub-fonte ou de uma região retangular de uma sub-fonte.
-   [**ID3D12Resource:: remapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : cancela o mapeamento do intervalo de memória especificado e invalida o ponteiro para o recurso. Restabelece o acesso à GPU para o subrecurso.
-   [**ID3D12Resource:: WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : Copia dados para um subrecurso ou uma região retangular de um subrecurso.

As texturas devem estar no estado [**comum do \_ estado do recurso \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) para acesso de CPU por meio de [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) e [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) para serem legais; mas os buffers não. O acesso de CPU a um recurso normalmente é [**feito por meio**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)do / [**mapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)de mapeamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associação de recursos](resource-binding.md)
</dt> </dl>

 

 




