---
title: Introdução às texturas no Direct3D 11
description: Um recurso de textura é uma coleção estruturada de dados projetada para armazenar texels.
ms.assetid: d745093e-2d51-4d45-a88a-caa0ca58b2ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fcafdfb9caf53a27e60956c8182ae3ef95008e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822771"
---
# <a name="introduction-to-textures-in-direct3d-11"></a>Introdução às texturas no Direct3D 11

Um recurso de textura é uma coleção estruturada de dados projetada para armazenar texels. Um texel representa a menor unidade de uma textura que pode ser lida ou gravada pelo pipeline. Diferente dos buffers, as texturas podem ser filtradas por amostras de texturas à medida que são lidas por unidades de sombreador. O tipo de textura afeta como a textura é filtrada. Cada Texel contém de 1 a 4 componentes, organizados em um dos formatos DXGI definidos pela enumeração de \_ formato dxgi.

As texturas são criadas como um recurso estruturado de tamanho conhecido. Entretanto, cada textura pode ter tipos ou não quando o recurso é criado, contanto que o tipo seja especificado usando um modo de exibição quando a textura está vinculada ao pipeline.

## <a name="texture-types"></a>Tipos de textura

Existem vários tipos de texturas: 1D, 2D, 3D, e cada uma pode ser criada com ou sem mipmaps. O Direct3D 11 também dá suporte a matrizes de textura e texturas com uma amostra.

-   [Texturas 1D](#1d-textures)
-   [Matrizes de textura 1D](#1d-texture-arrays)
-   [Texturas 2D e matrizes de textura 2D](#2d-textures-and-2d-texture-arrays)
-   [Texturas 3D](#3d-textures)

### <a name="1d-textures"></a>Texturas 1D

Uma textura 1D em sua forma mais simples contém dados de textura que podem ser tratados com uma coordenada de textura única; pode ser visualizada como uma matriz de texels, conforme mostrado na ilustração a seguir. as texturas 1D são representadas pela interface [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) .

![ilustração de uma textura 1D](images/d3d10-1d-texture.png)

Cada texel contém um número de componentes de cor dependendo do formato dos dados armazenados. Ao adicionar mais complexidade, você pode criar uma textura 1D com níveis de mipmap, conforme mostrado na ilustração a seguir.

![ilustração de uma textura 1D com níveis de mipmap](images/d3d10-resource-texture1d.png)

Um nível de mipmap é uma textura menor do que o nível superior por uma potência de dois. O nível superior é o mais detalhado, sendo que cada nível subsequente é menor. Para uma mipmap 1D, o menor nível contém um texel. Além disso, os níveis MIP sempre são reduzidos até 1:1. Quando mipmaps são gerados para uma textura de tamanho ímpar, o próximo nível inferior tem sempre o mesmo tamanho (exceto quando o nível mais baixo atinge 1). Por exemplo, o diagrama ilustra uma textura de 5 x 1, cujo próximo nível mais baixo é uma textura de 2 x 1, cujo próximo (e último) nível de mip é uma textura tamanho 1 x 1. Os níveis são identificados por um índice denominado LOD (nível de detalhe) utilizado para acessar a textura menor ao renderizar uma geometria que não está próxima da câmera.

### <a name="1d-texture-arrays"></a>Matrizes de textura 1D

O Direct3D 11 também dá suporte a matrizes de texturas. Uma matriz de textura 1D também é representada pela interface [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) . Uma matriz de texturas 1D conceitualmente parece com a ilustração a seguir.

![ilustração de uma matriz de texturas 1D](images/d3d10-resource-texture1darray.png)

Essa matriz de textura contém três texturas. Cada uma das três texturas tem uma largura de 5 (o número de elementos na primeira camada). Cada textura também contém uma mipmap de 3 camadas.

Todas as matrizes de textura no Direct3D são uma matriz homogênea de texturas; ou seja, cada textura em uma matriz de texturas deve ter o mesmo formato de dados e o tamanho (incluindo a largura de textura e o número de níveis de mipmap. Você pode criar matrizes de textura de diferentes tamanhos, contanto que todas as texturas em cada matriz correspondam em tamanho.

### <a name="2d-textures-and-2d-texture-arrays"></a>Texturas 2D e matrizes de textura 2D

Um recurso Texture2D contém uma grade 2D de texels. Cada texel é endereçável por um vetor u, v. Como é um recurso de textura, ele pode conter níveis de mipmap e sub-recursos. as texturas 2D são representadas pela interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) . Um recurso de textura 2D totalmente preenchida é semelhante à ilustração a seguir.

![ilustração de um recurso de textura 2D](images/d3d10-resource-texture2d.png)

Esse recurso de textura contém uma única textura 3 x 5 com três níveis de mipmap.

Um recurso de matriz de textura 2D é uma matriz homogênea de texturas 2D; ou seja, cada textura tem o mesmo formato de dados e dimensões (incluindo níveis de mipmap). Uma matriz de textura 2D também é representada pela interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) . Contém um layout semelhante ao da matriz de textura 1D, exceto que as texturas agora contêm dados 2D, como mostrado na ilustração a seguir.

![ilustração de uma matriz de texturas 2D](images/d3d10-resource-texture2darray.png)

Essa matriz de textura contém três texturas; cada uma de 3 x 5 com dois níveis de mipmap.

### <a name="using-a-2d-texture-array-as-a-texture-cube"></a>Usar uma matriz de textura 2D como um cubo de textura

Um cubo de textura é uma matriz de textura 2D com 6 texturas, uma para cada face do cubo. Um cubo de textura totalmente preenchida se parece com a ilustração a seguir.

![ilustração de uma matriz de texturas 2D que representa um cubo de textura](images/d3d10-resource-texturecube.png)

Uma matriz de textura 2D com 6 texturas pode ser lida nos sombreadores com as funções intrínsecas do mapa do cubo após a vinculação ao pipeline com um modo de exibição de textura de cubo. Os cubos de textura são endereçados do sombreador com um vetor 3D apontado para o centro do cubo de textura.

> [!Note]  
> Os dispositivos que você cria [**com \_ um nível de recurso de 10 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) e acima podem dar suporte a matrizes de cubos de textura em que o número de texturas é igual ao número de cubos de textura em uma matriz vezes seis. Os dispositivos que você cria [**com \_ nível de recurso de 10 0**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) dão suporte a apenas um único cubo de textura de seis faces. Além disso, o Direct3D 11 não oferece suporte a cubemaps parciais.

 

### <a name="3d-textures"></a>Texturas 3D

Um recurso de textura 3D (também conhecida como uma textura de volume) contém um volume 3D de texels. Como é um recurso de textura, ela pode conter níveis de mipmap. texturas 3D são representadas pela interface [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) . Uma textura 3D totalmente preenchida se parece com a ilustração a seguir.

![ilustração de um recurso de textura 3D](images/d3d10-resource-texture3d.png)

Quando uma fatia de mipmap da textura 3D é vinculada como uma saída de destino de renderização (com um modo de exibição de renderização de destino), a textura 3D se comporta de forma idêntica à matriz de textura 2D com n fatias. A fatia de renderização específica é escolhida no estágio Geometry-Shader, declarando um componente escalar de dados de saída como o \_ valor do sistema RENDERTARGETARRAYINDEX VA.

Não há nenhum conceito de matriz de textura 3D; portanto, um sub-recurso de textura 3D é um nível de mipmap único.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




