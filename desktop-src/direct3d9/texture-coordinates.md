---
description: A maioria das texturas, como bitmaps, é uma matriz bidimensional de valores de cores.
ms.assetid: vs|directx_sdk|~\texture_coordinates.htm
title: Coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff2c2c86eebac77d910b5dc6c583df380f0bbb2ccb3dca2fc65b9e929e7abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519782"
---
# <a name="texture-coordinates-direct3d-9"></a>Coordenadas de textura (Direct3D 9)

A maioria das texturas, como bitmaps, é uma matriz bidimensional de valores de cores. Texturas de mapa de ambiente cúbica são uma exceção. Para obter detalhes, consulte [Mapeamento de ambiente cúbica (Direct3D 9)](cubic-environment-mapping.md). Os valores de cor individuais são chamados de elemento de textura ou texel. Cada texel tem um endereço exclusivo na textura. O endereço pode ser pensado como uma coluna e um número de linha, que são rotulados como v e você, respectivamente, na ilustração a seguir.

![ilustração de um endereço texel como números de coluna e linha](images/uvcoordinates.jpg)

As coordenadas de textura estão no espaço de textura. Ou seja, eles são relativos ao local (0,0) na textura. Quando uma textura é aplicada a um primitivo no espaço 3D, seus endereços texel devem ser mapeados em coordenadas de objeto. Em seguida, eles devem ser convertidos em coordenadas de tela ou locais de pixel.

## <a name="mapping-texels-to-screen-space"></a>Mapeando o Texels para o Espaço na Tela

O Direct3D mapeia os texels no espaço de textura diretamente para pixels no espaço da tela, ignorando a etapa intermediária para maior eficiência. Esse processo de mapeamento é, na verdade, um mapeamento inverso. Ou seja, para cada pixel no espaço da tela, a posição de texel correspondente no espaço de textura é calculada. A cor da textura em ou ao redor desse ponto é amostrada. O processo de amostragem é chamado de filtragem de textura. Para obter mais informações, consulte [Filtragem de textura (Direct3D 9)](texture-filtering.md).

Cada texel em uma textura pode ser especificado por sua coordenada de texel. No entanto, para mapear os texels para primitivos, o Direct3D requer um intervalo de endereços uniforme para todos os texels em todas as texturas. Portanto, ele usa um esquema de endereçamento genérico no qual todos os endereços texel estão no intervalo de 0,0 a 1,0 inclusive. Os aplicativos Direct3D especificam coordenadas de textura em termos de valores de você, v, assim como coordenadas cartesianas 2D são especificadas em termos de coordenadas x,y. Tecnicamente, o sistema pode processar coordenadas de textura fora do intervalo de 0,0 e 1,0 e faz isso usando os parâmetros definidos para endereçamento de textura. Para obter mais informações, consulte [Modos de endereçamento de textura (Direct3D 9)](texture-addressing-modes.md).

Um resultado disso é que endereços de textura idênticos podem ser mapeado para diferentes coordenadas de texel em texturas diferentes. Na ilustração a seguir, o endereço de textura é (0,5,1.0). No entanto, como as texturas são de tamanhos diferentes, o endereço de textura é mapeado para diferentes texels. A textura 1, à esquerda, é 5x5. O endereço de textura (0,5,1.0) é mapeado para o texel (2,4). A textura 2, à direita, é 7x7. O endereço de textura (0,5,1.0) é mapeado para o texel (3,6).

![ilustração do mesmo mapeamento de endereço de textura para diferentes texels em texturas diferentes](images/texadr1.png)

Uma versão simplificada do processo de mapeamento de texel é mostrada na ilustração a seguir. Reconhecidamente, este exemplo é extremamente simples. Para obter informações mais detalhadas, consulte [Mapeando diretamente os Texels para Pixels (Direct3D 9)](directly-mapping-texels-to-pixels.md).

![ilustração de pixel (um quadrado de cor) mapeado para o espaço do objeto](images/texadr2.png)

Para este exemplo, um pixel, mostrado à esquerda da ilustração, é cortado em um quadrado de cor. Os endereços dos quatro cantos do pixel são mapeados para o primitivo 3D no espaço do objeto. A forma do pixel geralmente é distorcida devido à forma do primitivo no espaço 3D e devido ao ângulo de exibição. Os cantos da área da superfície no primitivo que correspondem aos cantos do pixel são mapeados para o espaço de textura. O processo de mapeamento distorce a forma do pixel novamente, o que é comum. O valor de cor final do pixel é calculado dos texels na região para a qual o pixel é mapeado. Você determina o método usado pelo Direct3D para chegar à cor do pixel ao definir o método de filtragem de textura. Para obter mais informações, consulte [Filtragem de textura (Direct3D 9)](texture-filtering.md).

Seu aplicativo pode atribuir coordenadas de textura diretamente aos vértices. Essa funcionalidade fornece controle sobre qual parte de uma textura é mapeada em um primitivo. Por exemplo, suponha que você crie um primitivo retangular exatamente do mesmo tamanho que a textura na ilustração a seguir. Neste exemplo, você deseja que seu aplicativo mapeie toda a textura para a parede inteira. As coordenadas de textura que seu aplicativo atribui aos vértices do primitivo são (0.0,0.0), (1.0,0.0), (1.0,1.0) e (0.0,1.0).

![ilustração de uma parede mapeada em textura](images/texadr3.png)

Se você decidir diminuir a altura da parede em uma metade, poderá distorcer a textura para caber na parede menor ou atribuir coordenadas de textura que causam o Direct3D a usar a metade inferior da textura.

Se você decidir distorcer ou dimensionar a textura para se ajustar à parede menor, o método de filtragem de textura usado influenciará a qualidade da imagem. Para obter mais informações, consulte [Filtragem de textura (Direct3D 9)](texture-filtering.md).

Se, em vez disso, você decidir atribuir coordenadas de textura para fazer com que o Direct3D use a metade inferior da textura para a parede menor, as coordenadas de textura que seu aplicativo atribui aos vértices do primitivo neste exemplo serão (0,0,0,0,5), (1,0,0,5), (1.0,1.0) e (0,0,1.0). O Direct3D aplica a metade inferior da textura à parede.

É possível que as coordenadas de textura de um vértice sejam maiores que 1,0. Ao atribuir coordenadas de textura a um vértice que não está no intervalo de 0,0 a 1,0, inclusive, você também deve definir o modo de endereçamento de textura. Para obter mais informações, consulte [Modos de endereçamento de textura (Direct3D 9)](texture-addressing-modes.md).

## <a name="texture-coordinates-and-texture-stages"></a>Coordenadas de textura e estágios de textura

As coordenadas de textura são associadas a texturas por meio de estágios de textura. As texturas são atribuídas a estágios de textura com SetTexture(stageIndex, pTexture). Consulte [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

Um código FVF (Formato de Vértice Flexível) pode definir até oito conjuntos de coordenadas de textura. Os dados de coordenadas de textura são fornecidos pelo usuário nos dados de vértice. Os dados são referenciados com um índice baseado em zero: 0 a 7. Há até oito estágios de mesclagem de textura. Uma textura é associada a um estágio específico usando SetTexture( stageIndex, pTexture).

Depois que isso for feito, qualquer conjunto de coordenadas de textura poderá ser usado por qualquer estágio. Cada conjunto de coordenadas é associado a um estágio usando SetTextureStageState( stageIndex, D3DTSS \_ TEXCOORDINDEX, textureCoordinateIndex ). Consulte [**IDirect3DDevice9::SetTextureStageState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) Dessa forma, os estágios de mesclagem podem ser definidos para usar qualquer textura e qualquer coordenada de textura. Mais de um estágio pode usar as mesmas texturas ou coordenadas de textura.

Informações adicionais estão contidas nos tópicos a seguir.

-   [Formatos de coordenada de textura (Direct3D 9)](texture-coordinate-formats.md)
-   [Processamento de coordenadas de textura (Direct3D 9)](texture-coordinate-processing.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
