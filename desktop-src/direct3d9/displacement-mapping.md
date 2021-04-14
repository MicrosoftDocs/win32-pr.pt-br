---
description: Os mapas de deslocamento são semelhantes aos mapas de textura, mas são acessados pelo mecanismo de vértice.
ms.assetid: d6f16ff2-5a66-48a3-82c4-523faaafa6ae
title: Mapeamento de deslocamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b687583b0109223d8c2dac807425e235ddf280e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456714"
---
# <a name="displacement-mapping-direct3d-9"></a>Mapeamento de deslocamento (Direct3D 9)

Os mapas de deslocamento são semelhantes aos mapas de textura, mas são acessados pelo mecanismo de vértice.

## <a name="block-diagram"></a>Diagrama de bloco

Um estágio de amostra adicional está presente na parte inicial do pipe de vértice, conforme mostrado no diagrama a seguir, que pode fazer uma amostragem de um mapa de deslocamento para fornecer dados de deslocamento de vértice.

![diagrama do estágio de amostra no pipe de vértice](images/tessellatordx9.png)

O estado de amostra do mapa de deslocamento pode ser definido pelo [**Setsamplestate**](/windows/desktop/api) usando o número de estágio 256, que é um novo número de estágio. A textura do mapa de deslocamento é definida por [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

O mapa pode ser de amostra ou não, o que significa que ele pode ser ordenado de uma maneira que permita a pesquisa dos valores de deslocamento sem filtragem.

-   Os mapas de deslocamento são análogos aos mapas de textura, mas são acessados pelo mecanismo de vértice.
-   Um estágio de amostra adicional está presente na parte inicial do pipe de vértice que pode fazer uma amostragem de um mapa de deslocamento. Esse estágio é acessado pela API setsamplestate usual, mas o número do estágio é D3DDMAPSAMPLER = 256.
-   O estado de amostra do mapa de deslocamento pode ser definido pelo setsamplestate (D3DDMAPSAMPLER,...) API.
-   A textura do mapa de deslocamento é definida pela API SetTexture (D3DDMAPSAMPLER, Texture).
-   O mapa pode ser previamente amostrado ou não. Isso significa que ele pode ser ordenado de uma maneira específica que permite a pesquisa dos valores de deslocamento sem filtragem.
-   As alterações na estrutura da declaração permitem a especificação da coordenada de textura usada para pesquisar o mapa de textura. Por exemplo, Stream0, offset, FLOAT2, pesquisa, valor de deslocamento \_ . Isso diz ao Tessellator para usar o vetor float 2D em stream0 em um determinado deslocamento como uma coordenada de textura para pesquisar o mapa de deslocamento e associar a \_ semântica de uso do valor de deslocamento a ele. A declaração de sombreador de vértice contém uma linha semelhante a {DCL \_ Texture0, V0} indicando que a semântica Texture0 deve ser associada ao registro de entrada V0. O valor de deslocamento procurado é copiado para o registro de entrada V0.
-   Há um tipo especial de mapeamento de deslocamento, quando o mapa de textura é previamente amostrado. O índice sequencial dos vértices gerados é usado como uma coordenada de textura para um mapa de textura. Por exemplo, 0, 0, (D3DDECLTYPE) 0, D3DDECLMETHOD \_ LOOKUPPRESAMPLED, Usage, UsageIndex.
-   A saída da pesquisa é 4 floats.
-   Há suporte para o mapeamento de deslocamento apenas com N-patches.
-   Os drivers precisam ignorar D3DDMAPSAMPLER em SetTextureStageState se não tratarem de mapas de substituição.
-   \_Não há suporte para o modo de filtro D3DTEXF ANISOTROPIC.
-   Quando D3DSAMP \_ MIPFILTER na amostra do mapa de deslocamento não for D3DTEXF \_ None, o nível de detalhe será calculado da seguinte maneira (Observe que o estado de mosaico adaptável será usado mesmo se D3DRS \_ ENABLEADAPTIVETESSELLATION for **false**): tmax = Process State D3DRS \_ MAXTESSELLATIONLEVEL
-   O te do nível de mosaico de computação para um vértice vi: (XI, Yi, Zi) da mesma maneira que descrito na seção "mosaico adaptável". Nível de detalhe L = log2 (tmax)-log2 (te).
-   As operações de filtragem e amostragem de textura seguem as mesmas regras que o pipeline de pixel (a tendência de nível de detalhe (LOD) é aplicada, etc.).
-   Nem todos os formatos podem ser usados como mapas de deslocamento, mas apenas aqueles que dão suporte ao D3DUSAGE \_ DMAP. O aplicativo pode consultar isso com o CheckDeviceFormat [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).
-   D3DUSAGE \_ DMAP deve ser especificado em [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) para notificar o driver de que essa textura deve ser usada como um mapa de deslocamento.
-   D3DUSAGE \_ DMAP só pode ser usado com texturas. Ele não pode ser usado com mapas ou volumes de cubo.
-   As texturas e os destinos de renderização criados com D3DUSAGE \_ DMAP podem ser definidos em estágios de amostra regulares e como destinos de renderização.
-   Os Estados de renderização para definir o modo de encapsulamento das coordenadas de textura são ignorados no mapeamento de deslocamento. Em geral, não há nenhum modo de encapsulamento para o mecanismo Tessellator.
-   Um amostra de mapa de deslocamento tem comportamento idêntico ao dos exemplos de textura de pixel. Se uma textura com menos de quatro canais (como R32f) for pesquisada, os valores de pesquisa irão para os canais apropriados do registro de destino (o registro de entrada do sombreador de vértice marcado com a \_ semântica de exemplo), enquanto os outros canais padrão são (1, 1, 1). Quando pesquisado, \_ o L8 D3DFMT Obtém a difusão nos canais R, G, B e um padrão como 1. O rasterizador de referência tem os detalhes da implementação completa.

## <a name="pre-sampled-displacement-mapping"></a>Mapeamento de deslocamento de amostra

-   Novo estado de amostra é introduzido: D3DSAMP \_ DMAPOFFSET (DWORD)-offset (em vértices) em um mapa de deslocamento de amostra.
-   O novo método de declaração foi introduzido: D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   O mosaico adaptável deve ser desabilitado.
-   As configurações de filtro de textura são ignoradas. A amostragem de ponto é feita. O filtro de textura MIP é considerado como D3DTEXF \_ nenhum. Todos os outros modos de filtro de textura são assumidos como \_ ponto D3DTEXF.
-   As coordenadas de textura são computadas como: U = (índice% TextureWidthInPixeles)/(float) (TextureWidthInPixeles) V = (index/TextureWidthInPixeles)/(float) (TextureHeightInPixeles), em que index é um índice sequencial de vértices gerados mais TSS D3DSAMP \[ \_ DMAPOFFSET \] . O índice sequencial é definido como zero no início de cada primitivo e aumenta após a geração de um vértice.

Essas são as alterações de API que dão suporte ao mapeamento de deslocamento.

-   Um único formato de canal adicionado, D3DFMT \_ L16.
-   Um novo sinalizador de uso, D3DUSAGE \_ DMAP.
-   Um estágio de textura especial, usado para definir uma textura de mapa de deslocamento, D3DDMAPSAMPLER.
-   Novos limites de hardware foram adicionados, D3DDEVCAPS2 \_ DMAPNPATCH e D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH. Consulte [D3DDEVCAPS2](d3ddevcaps2.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de vértice](vertex-pipeline.md)
</dt> </dl>

 

 
