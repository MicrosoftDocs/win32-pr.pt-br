---
title: Mapeamento de textura padrão
description: O uso de mapeamento de textura padrão reduz a cópia e o uso de memória ao compartilhar dados de imagem entre a GPU e a CPU.
ms.assetid: 77AF4BFA-09B5-4181-9408-002764F2A923
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc81fc1bf59a974f9bd901fc96d43afc16019edce68fbaabfbf3259c0d4a3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752286"
---
# <a name="default-texture-mapping"></a>Mapeamento de textura padrão

O uso de mapeamento de textura padrão reduz a cópia e o uso de memória ao compartilhar dados de imagem entre a GPU e a CPU. No entanto, ele só deve ser usado em situações específicas. O layout swizzle padrão evita copiar ou swizzling dados em vários layouts.

-   [Visão geral](#overview)
-   [APIs do D3D 11.3](#d3d113-apis)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

O mapeamento de texturas padrão não deve ser a primeira opção para os desenvolvedores. Os desenvolvedores devem codificar em uma forma amigável de GPU discreta primeiro (ou seja, não têm nenhum acesso de CPU para a maioria das texturas e carregar com [**CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)). Mas, para determinados casos, a CPU e a GPU podem interagir com tanta frequência nos mesmos dados, que o mapeamento de texturas padrão se torna útil para economizar energia ou para acelerar um design específico em adaptadores ou arquiteturas específicos. Os aplicativos devem detectar esses casos e otimizar as cópias desnecessárias.

No D3D 11.3, as texturas criadas \_ com \_ o layout de textura D3D11 \_ não são definidas (um membro da enumeração de [**\_ \_ layout de textura D3D11**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) ) e nenhum acesso de CPU é o mais eficiente para a renderização e a amostragem de GPU frequentes. Quando o teste de desempenho, essas texturas devem ser comparadas \_ \_ com o layout de textura D3D11 \_ indefinido com acesso à CPU e o \_ layout de textura D3D11 \_ \_ 64K \_ Standard \_ SWIZZLE com acesso à CPU e a \_ \_ \_ linha de layout de textura D3D11 \_ principal para suporte entre adaptadores.

O uso \_ \_ do layout \_ de textura D3D11 indefinido com acesso à CPU permite que os métodos [**WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource), [**ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource), [**mapeie**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) (impedindo o acesso do aplicativo ao ponteiro) e o [**cancelem**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap), mas possam sacrificar a eficiência do acesso à GPU. Usando \_ \_ o layout de textura D3D11 \_ 64K \_ Standard \_ SWIZZLE com acesso à CPU habilita **WriteToSubresource**, **ReadFromSubresource**, **MAP** (que retorna um ponteiro válido para o aplicativo) e o **mapeamento**. Ele também pode sacrificar a eficiência de acesso de GPU mais do que o \_ layout de textura D3D11 \_ \_ indefinido com acesso à CPU.

Em geral, os aplicativos devem criar a maioria das texturas como acessíveis somente à GPU e com o \_ layout de textura D3D11 \_ \_ indefinido.

Antes do recurso de mapeamento de texturas padrão, havia apenas um layout padronizado para dados multidimensionais: "linear", também conhecido como "linha-principal". Os aplicativos devem evitar o uso da \_ preparação e do uso de \_ texturas dinâmicas quando o padrão do mapa estiver disponível. As \_ \_ texturas dinâmicas de uso e preparo usam o layout linear.

O D3D 11.3 (e D3D12) introduz um layout de dados multidimensional padrão. Isso é feito para permitir que várias unidades de processamento operem nos mesmos dados sem copiar os dados ou swizzling os dados entre vários layouts. Um layout padronizado permite ganhos de eficiência por meio de efeitos de rede e permite que os algoritmos façam pequenos cortes, supondo um padrão específico.

No entanto, observe que esse swizzle padrão é um recurso de hardware e pode não ter suporte de todas as GPUs.

## <a name="d3d113-apis"></a>APIs do D3D 11.3

Ao contrário do D3D12, o D3D 11.3 não dá suporte ao mapeamento de textura por padrão, portanto, você precisa consultar [**\_ os dados do recurso D3D11 \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2). O padrão swizzle também precisará ser consultado com uma chamada para [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) e verificar o `StandardSwizzle64KBSupported` campo dos **dados do \_ recurso D3D11 D3D11 \_ \_ \_ OPTIONS2**.

As seguintes APIs referenciam o mapeamento de textura:

Enumerações

-   [**D3D11 \_ \_Layout de textura**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout) : controla o padrão swizzle de texturas padrão e habilita o suporte de mapa em texturas padrão.
-   [**D3D11 \_ RECURSO**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) : referencia [**\_ os dados de recurso D3D11 \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2).
-   [**D3D11 \_ \_ \_ Sinalizador de cópia do bloco**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : contém sinalizadores para copiar os recursos de lado do swizzled para e de buffers lineares.

Estruturas

-   [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1) : descreve uma textura 2D. Observe a \_ \_ estrutura auxiliar CD3D11 TEXTURE2D DESC1.
-   [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1) : descreve uma textura 3D. Observe a \_ \_ estrutura auxiliar CD3D11 TEXTURE3D DESC1.

Métodos

-   [**ID3D11Device3:: CreateTexture2D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture2d1) : cria uma matriz de texturas 2D.
-   [**ID3D11Device3:: CreateTexture3D1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11device3-createtexture3d1) : cria uma única textura 3D.
-   [**ID3D11Device3:: WriteToSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-writetosubresource) : Copia dados em uma \_ textura padrão de uso de D3D11 \_ que foi mapeada usando o [**mapa**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11Device3:: ReadFromSubresource**](/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-readfromsubresource) : Copia dados de uma \_ textura padrão de uso de D3D11 \_ que foi mapeada usando o [**mapa**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
-   [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) : Obtém um ponteiro para os dados contidos em um subrecurso e nega o acesso GPU a esse subrecurso.
-   [**ID3D11DeviceContext:: inmapeamento**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) : invalida o ponteiro para um recurso e reabilita o acesso da GPU a esse recurso.
-   [**ID3D11Texture2D1:: GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture2d1-getdesc1) : Obtém as propriedades de um recurso de textura 2D.
-   [**ID3D11Texture3D1:: GetDesc1**](/windows/desktop/api/D3D11_3/nf-d3d11_3-id3d11texture3d1-getdesc1) : Obtém as propriedades de um recurso de textura 3D.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




