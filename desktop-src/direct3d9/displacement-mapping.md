---
description: Os mapas de deslocamento são semelhantes aos mapas de textura, mas são acessados pelo mecanismo de vértice.
ms.assetid: d6f16ff2-5a66-48a3-82c4-523faaafa6ae
title: Mapeamento de deslocamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87b559c2c4758b773c48c0b556b6d61af54549f1b30e5c2693a24c4c27856c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523756"
---
# <a name="displacement-mapping-direct3d-9"></a>Mapeamento de deslocamento (Direct3D 9)

Os mapas de deslocamento são semelhantes aos mapas de textura, mas são acessados pelo mecanismo de vértice.

## <a name="block-diagram"></a>Diagrama de bloco

Um estágio de amostra adicional está presente na parte inicial do pipe de vértice, conforme mostrado no diagrama a seguir, que pode amostrar um mapa de deslocamento para fornecer dados de deslocamento de vértice.

![diagrama do estágio de amostra no pipe de vértice](images/tessellatordx9.png)

O estado de amostra do mapa de deslocamento pode ser definido pelo [**SetSamplerState**](/windows/desktop/api) usando o número de estágio 256, que é um novo número de estágio. A textura do mapa de deslocamento é definida [**por SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)

O mapa pode ser pré-prempled ou não, o que significa que ele pode ser ordenado de uma maneira que habilita a procurar os valores de deslocamento sem filtragem.

-   Os mapas de deslocamento são análogos aos mapas de textura, mas são acessados pelo mecanismo de vértice.
-   Um estágio de amostra adicional está presente na parte inicial do pipe de vértice que pode amostrar um mapa de deslocamento. Esse estágio é acessado pela API SetSamplerState normal, mas o número do estágio é D3DDMAPSAMPLER = 256.
-   O estado do amostrador do mapa de deslocamento pode ser definido pelo SetSamplerState(D3DDMAPSAMPLER, ...) Api.
-   A textura do mapa de deslocamento é definida pela API SetTexture(D3DDMAPSAMPLER, textura).
-   O mapa pode ser previamente amostrado ou não. Isso significa que ele pode ser ordenado de uma maneira específica que habilita a procurar os valores de deslocamento sem filtragem.
-   As alterações na estrutura de declaração permitem a especificação da coordenada de textura usada para procurar o mapa de textura. Por exemplo, Stream0, Offset, FLOAT2, LOOKUP, Valor de \_ deslocamento. Isso informa ao mosaico para usar o vetor float 2D em stream0 em um determinado deslocamento como uma coordenada de textura para procurar o mapa de deslocamento e associar a semântica uso de valor de deslocamento a \_ ele. A declaração do sombreador de vtex conteria uma linha semelhante a {dcl texture0, v0} indicando que a semântica texture0 deve ser associada ao registro de entrada \_ v0. O valor de deslocamento procurado é copiado para o registro de entrada v0.
-   Há um tipo especial de mapeamento de deslocamento, quando o mapa de textura é pré-amostrado. O índice sequencial de vértices gerados é usado como uma coordenada de textura para um mapa de textura. Por exemplo, 0,0,(D3DDECLTYPE)0,D3DDECLMETHOD \_ LOOKUPPRESAMPLED, Usage, UsageIndex.
-   A saída da lookup é 4 floats.
-   O mapeamento de deslocamento só tem suporte com N patches.
-   Os drivers precisarão ignorar D3DDMAPSAMPLER em SetTextureStageState se não tratarem mapas de deslocamento.
-   Não há suporte para o \_ modo de filtro ANIS LTDA D3DTEXF.
-   Quando D3DSAMP MIPFILTER no amostrador de mapa de deslocamento não é D3DTEXF NONE, o nível de detalhe é calculado da seguinte forma (observe que o estado de mosaico adaptável é usado mesmo se \_ \_ o D3DRS \_ ENABLEADAPTIVETESSELLATION for **FALSE**): Tmax = renderizar estado D3DRS \_ MAXTESSELLATIONLEVEL
-   Nível de mosaico de computação Te para um vértice Vi: (Xi, Xi, Zi) da mesma maneira descrita na seção "Mosaico adaptável". Nível de detalhes L = log2(Tmax) – log2 (Te).
-   As operações de filtragem e amostragem de textura seguem as mesmas regras que o desvio de pipeline de pixel (LOD (nível de detalhe) é aplicado etc.).
-   Nem todos os formatos podem ser usados como mapas de deslocamento, mas apenas aqueles que suportam o \_ DMAP D3DUSAGE. O aplicativo pode consultar isso com CheckDeviceFormat [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).
-   D3DUSAGE DMAP deve ser especificado em CreateTexture para notificar o driver de que essa textura deve ser usada como \_ um mapa de deslocamento. [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   D3DUSAGE \_ DMAP só pode ser usado com texturas. Ele não pode ser usado com mapas de cubo ou volumes.
-   Texturas e destinos de renderização criados com DMAP D3DUSAGE podem ser definidos em estágios regulares de amostra e \_ como destinos de renderização.
-   Os estados de renderização para definir o modo de quebra para as coordenadas de textura são ignorados no mapeamento de deslocamento. Em geral, não há modos de wrap para o mecanismo de mosaico.
-   Um exemplo de mapa de deslocamento tem um comportamento idêntico ao dos amostradores de textura de pixel. Se uma textura com menos de quatro canais (como R32f) for procurada, os valores de procura vão para os canais apropriados do registro de destino (o registro de entrada do sombreador de vértice marcado com a semântica de exemplo), enquanto os outros canais assumem \_ como padrão (1, 1, 1). Quando procurado, d3DFMT L8 é transmitido para os canais \_ R, G, B e A assume como padrão 1. O rasterizador de referência tem os detalhes completos da implementação.

## <a name="pre-sampled-displacement-mapping"></a>Mapeamento de deslocamento pré-amostrado

-   O novo estado de amostra foi introduzido: \_ DMAPOFFSET DMAPOFFSET (DMAPOFFSET) D3DSAMP – deslocamento (em vértices) em um mapa de deslocamento pré-amostrado.
-   Novo método de declaração foi introduzido: D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   O mosaico adaptável deve ser desabilitado.
-   As configurações de filtro de textura são ignoradas. A amostragem de ponto é feita. Presume-se que o filtro de textura mip seja D3DTEXF \_ NONE. Todos os outros modos de filtro de textura são presumidos como D3DTEXF \_ POINT.
-   As coordenadas de textura são computadas como: U = (Index % TextureWidthInPixeles) / (float)(TextureWidthInPixeles) V = (Index /TextureWidthInPixeles) / (float)(TextureHeightInPixeles) em que Index é um índice sequencial de vértices gerados mais TSS \[ D3DSAMP \_ DMAPOFFSET \] . O índice sequencial é definido como zero no início de cada primitivo e é aumentado depois que um vértice é gerado.

Essas são as alterações de API que suportam mapeamento de deslocamento.

-   Um único formato de canal adicionado, D3DFMT \_ L16.
-   Um novo sinalizador de uso, D3DUSAGE \_ DMAP.
-   Um estágio de textura especial, usado para definir uma textura de mapa de deslocamento, D3DDMAPSAMPLER.
-   Novos limites de hardware foram adicionados, D3DDEVCAPS2 \_ DMAPNPATCH e D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH. Consulte [D3DDEVCAPS2](d3ddevcaps2.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de vértice](vertex-pipeline.md)
</dt> </dl>

 

 
