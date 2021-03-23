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
# <a name="subresources-direct3d-12-graphics"></a>Subrecursos (gráficos do Direct3D 12)

Descreve como um recurso é dividido em subrecursos e como fazer referência a uma única, várias ou fatia de subrecursos.

-   [Subrecursos de exemplo](#example-subresources)
    -   [Indexação de subrecurso](#subresource-indexing)
    -   [Fatia MIP](#mip-slice)
    -   [Fatia da matriz](#array-slice)
    -   [Fatia do plano](#plane-slice)
    -   [Vários subrecursos](#multiple-subresources)
-   [APIs de subrecurso](#subresource-apis)
-   [Tópicos relacionados](#related-topics)

## <a name="example-subresources"></a>Subrecursos de exemplo

Se um recurso contiver um buffer, ele simplesmente conterá um subrecurso com um índice de 0. Se o recurso contiver uma textura (ou matriz de textura), a referência aos subrecursos será mais complexa.

Algumas APIs acessam um recurso inteiro (como o método [**ID3D12GraphicsCommandList:: CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) ); outras pessoas acessam uma parte de um recurso (por exemplo, o método [**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ). Os métodos que acessam uma parte de um recurso geralmente usam uma descrição de exibição (como a estrutura [**\_ SRV da \_ matriz \_ D3D12 TEX2D**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) ) para especificar os subrecursos a serem acessados. Consulte a seção [APIs de subrecurso](#subresource-apis) para obter uma lista completa.

### <a name="subresource-indexing"></a>Indexação de subrecurso

Para indexar um determinado subrecurso, os níveis MIP são indexados primeiro à medida que cada entrada de matriz é indexada.

![indexação de subrecurso](images/subresource-index.png)

### <a name="mip-slice"></a>Fatia MIP

Uma fatia MIP inclui um nível de mipmap para cada textura em uma matriz, conforme mostrado na imagem a seguir.

![fatias MIP de subrecurso](images/subresource-mip-slice.png)

### <a name="array-slice"></a>Fatia da matriz

Dada uma matriz de texturas, cada textura com mipmaps, uma fatia de matriz inclui uma textura e todos os seus níveis de MIP, conforme mostrado na imagem a seguir.

![fatias de matriz de subrecurso](images/subresource-array-slices.png)

### <a name="plane-slice"></a>Fatia do plano

Normalmente, os formatos planar não são usados para armazenar dados RGBA, mas nos casos em que eles são (talvez 24bpp dados RGB), um plano poderia representar a imagem vermelha, um verde e uma imagem azul. Embora um plano não seja necessariamente uma cor, duas ou mais cores poderiam ser combinadas em um plano. Normalmente, os dados planar são usados para dados YCbCr Depth-Stencil e de subamostrados. Depth-Stencil é o único formato que dá suporte total a mipmaps, matrizes e vários planos (geralmente plano 0 para profundidade e plano 1 para o estêncil).

A indexação de subrecurso para uma matriz de duas imagens de Depth-Stencil, cada uma com três níveis de MIP, é mostrada abaixo.

![indexação do estêncil de profundidade](images/depth-stencil-indexing.png)

A subamostra YCbCr dá suporte a matrizes e tem planos, mas não oferece suporte a mipmaps. As imagens YCbCr têm dois planos, um para a luminância (Y) à qual o olho humano é mais sensível e outro para o crominância (CB e CR, intercalado) ao qual o olho humano é menos sensível. Esse formato permite a compactação dos valores de crominância para compactar uma imagem sem afetar a luminância e é um formato de compactação de vídeo comum por esse motivo, embora seja usado para compactar imagens ainda. A imagem abaixo mostra o formato NV12, observando que o crominância foi compactado para um quarto da resolução da luminância, o que significa que a largura de cada plano é idêntica e o plano de crominância é metade da altura do plano de luminância. Os planos seriam indexados como subrecursos de forma idêntica ao exemplo de Depth-Stencil acima.

![o formato NV12](images/ycbcr.png)

Os formatos planar existiam no Direct3D 11, mas os planos individuais não podiam ser resolvidos individualmente, digamos para operações de cópia ou mapeamento. Isso foi alterado no Direct3D 12 para que cada plano tenha recebido sua própria ID de subrecurso. Compare os dois métodos a seguir para calcular a ID do subrecurso.

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

A maioria dos hardwares pressupõe que a memória para o plano N sempre é imediatamente alocada após o plano N-1.

Uma alternativa ao uso de subrecursos é que um aplicativo pode alocar um recurso completamente separado por plano. Nesse caso, o aplicativo entende que os dados são planar e usa vários recursos para representá-los.

### <a name="multiple-subresources"></a>Vários subrecursos

Um modo de exibição de recurso de sombreador pode selecionar qualquer região retangular de subrecursos, usando uma das fatias descritas acima e criteriosamente o uso de campos nas estruturas de exibição (como [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), conforme mostrado na imagem.

![seleção múltipla de subrecurso](images/subresource-multiple.png)

Uma exibição de destino de renderização só pode usar um único subrecurso ou uma fatia MIP e não pode incluir subrecursos de mais de uma fatia MIP. Ou seja, todas as texturas em uma exibição de destino de renderização devem ter o mesmo tamanho. Um modo de exibição de recurso de sombreador pode selecionar qualquer região retangular de subrecurso, conforme mostrado na imagem.

## <a name="subresource-apis"></a>APIs de subrecurso

As seguintes referências de APIs e funcionam com os subrecursos:

Enumerações:

-   [**\_Tipo de \_ cópia de textura D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

As estruturas a seguir contêm índices *PlaneSlice* , a maioria contém índices *MipSlice* .

-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**\_Matriz D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ matriz \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**\_Matriz D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

As estruturas a seguir contêm índices *ArraySlice* , a maioria contém índices *MipSlice* .

-   [**\_DSV de \_ matriz D3D12 TEX1D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**\_DSV de \_ matriz D3D12 TEX2D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**\_DSV de \_ matriz D3D12 TEX2DMS \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**\_Matriz D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**\_Matriz D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**\_Matriz D3D12 \_ TEX2DMS \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX1D \_ matriz \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ matriz \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ matriz \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**\_Matriz D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**\_Matriz D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

As estruturas a seguir contêm índices *MipSlice* , mas nem índices *ArraySlice* nem *PlaneSlice* .

-   [**\_DSV D3D12 TEX1D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**\_DSV D3D12 TEX2D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

As seguintes estruturas também fazem referência a subrecursos:

-   [**D3D12 \_ \_Região de descarte**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : uma estrutura usada na preparação para descartar um recurso.
-   [**D3D12 \_ \_ \_ Superfície do SUBrecurso posicionado**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : Adiciona um deslocamento em um recurso à superfície básica.
-   [**D3D12 \_ \_ \_ Barreira de transição de recurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : descreve a transição de subrecursos entre diferentes usos (recurso de sombreador, destino de renderização, etc.).
-   [**D3D12 \_ \_Dados de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : os dados de subrecurso incluem os dados em si e a densidade da linha e da fatia.
-   [**D3D12 \_ \_Superfície de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : uma superfície inclui o formato, a largura, a altura, a profundidade e o tom de linha do subrecurso.
-   [**D3D12 \_ \_Informações de subrecurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contém o deslocamento, a densidade da linha e a densidade da profundidade do subrecurso.
-   [**D3D12 \_ Subrecurso \_ lado**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) a lado: descreve um volume de subrecurso com subdivisão (consulte [recursos do lado do volume](volume-tiled-resources.md)).
-   [**D3D12 \_ \_ \_ Local da cópia de textura**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : descreve uma parte de uma textura com a finalidade de copiar.
-   [**D3D12 \_ \_ \_ Coordenada de recurso por lado**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .: descreve as coordenadas de um recurso de lado.

Métodos:

-   [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : Obtém informações sobre um recurso, para permitir que uma cópia seja feita.
-   [**ID3D12Device:: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : Obtém informações sobre como um recurso de quebra-lado é dividido em blocos.
-   [**ID3D12GraphicsCommandList:: ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copia um subrecurso de várias amostras em um subrecurso sem várias amostras.
-   [**ID3D12Resource:: map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : retorna um ponteiro para os dados especificados no recurso e nega o acesso à GPU para o subrecurso.
-   [**ID3D12Resource:: ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : Copia dados de um subrecurso ou uma região retangular de um subrecurso.
-   [**ID3D12Resource:: remapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : cancela o mapeamento do intervalo de memória especificado e invalida o ponteiro para o recurso. Restabelece o acesso à GPU para o subrecurso.
-   [**ID3D12Resource:: WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : Copia dados para um subrecurso ou uma região retangular de um subrecurso.

As texturas devem estar no estado [**comum do \_ estado do recurso \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) para acesso de CPU por meio de [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) e [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) para serem legais; mas os buffers não. O acesso de CPU a um recurso normalmente é [**feito por meio**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)do / [**mapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)de mapeamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associação de recursos](resource-binding.md)
</dt> </dl>

 

 




