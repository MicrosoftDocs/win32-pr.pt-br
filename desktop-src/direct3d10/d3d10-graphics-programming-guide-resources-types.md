---
description: 'Todos os recursos usados pelo pipeline Direct3D derivam de dois tipos de recurso básicos: buffers e texturas. Um buffer é uma coleção de dados brutos (elementos); uma textura é uma coleção de texels (elementos de textura).'
ms.assetid: c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69
title: Tipos de recurso (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0f757eac93fac8c0ffd49641441fa4570824670dfcca9c3d271f954054548b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120044"
---
# <a name="resource-types-direct3d-10"></a>Tipos de recurso (Direct3D 10)

Todos os recursos usados pelo pipeline Direct3D derivam de dois tipos de recurso básicos: [buffers](#buffer-resources) e [texturas](#texture-resources). Um buffer é uma coleção de dados brutos (elementos); uma textura é uma coleção de texels (elementos de textura).

-   [Recursos de buffer](#buffer-resources)
    -   [Tipos de buffer](#buffer-types)
-   [Recursos de textura](#texture-resources)
    -   [Tipos de textura](#texture-types)
    -   [Sub-recursos](#subresources)
    -   [Tipo forte versus fraco](#strong-vs-weak-typing)
-   [Tópicos relacionados](#related-topics)

Há duas maneiras de especificar totalmente o layout (ou volume de memória) de um recurso:



| Item                                                                                                 | Descrição                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="Typed"></span><span id="typed"></span><span id="TYPED"></span>Automaticamente<br/>             | Especifique totalmente o tipo quando o recurso é criado.<br/>               |
| <span id="Typeless"></span><span id="typeless"></span><span id="TYPELESS"></span>Sem especificação<br/> | Especifique totalmente o tipo quando o recurso é vinculado ao pipeline.<br/> |



 

## <a name="buffer-resources"></a>Recursos de buffer

Um recurso de buffer é uma coleção de dados completamente tipados; internamente, um buffer contém elementos. Um elemento é composto de 1 a 4 componentes. Exemplos de tipos de dados de elemento incluem: um valor de dados compactados (como R8G8B8A8), um único inteiro de 8 bits, quatro valores flutuantes de 32 bits. Esses tipos de dados são usados para armazenar dados, como um vetor de posição, um vetor normal, uma coordenada de textura em um buffer de vértice, um índice em um buffer de índice ou o estado do dispositivo.

Um buffer é criado como um recurso não estruturado. Como ele não é estruturado, um buffer não pode conter níveis de mipmap, não é filtrado quando lido e não pode conter várias amostras.

### <a name="buffer-types"></a>Tipos de buffer

-   [Buffer de vértice](#vertex-buffer)
-   [Buffer de índice](#index-buffer)
-   [Buffer de constantes](#constant-buffer)

### <a name="vertex-buffer"></a>Buffer de vértice

Um buffer é uma coleção de elementos; um buffer de vértices contém dados por vértice. O exemplo mais simples é um buffer de vértices que contém um tipo de dado, como dados de posição. Ele pode ser visualizado como na ilustração a seguir.

![ilustração de um buffer de vértices que contém dados de posição](images/d3d10-resources-single-element-vb2.png)

Com mais frequência, um buffer de vértices contém todos os dados necessários para especificar totalmente vértices 3D. Um exemplo disso pode ser um buffer de vértices que contém coordenadas de posição, normais e de textura por vértice. Esses dados geralmente são organizados como conjuntos de elementos por vértice, conforme mostrado na ilustração a seguir.

![ilustração de um buffer de vértices que contém dados de posição, normais e de textura](images/d3d10-vertex-buffer-element.png)

Esse buffer de vértices contém dados por vértice para oito vértices; cada vértice armazena três elementos (coordenadas de posição, normais e de textura). A posição e o normal são cada um normalmente especificado usando floats de 3 32 bits ( \_ float do formato dxgi \_ R32G32B32 \_ ) e as coordenadas de textura usando floats de 2 32 bits ( \_ formato dxgi \_ R32G32 \_ float).

Para acessar dados de um buffer de vértices, você precisa saber qual vértice acessar e estes outros parâmetros de buffer:

-   Deslocamento -o número de bytes desde o início do buffer para os dados para o primeiro vértice. O deslocamento é fornecido para [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers).
-   BaseVertexLocation-o número de bytes do deslocamento para o primeiro vértice usado pela chamada Draw apropriada (consulte os [métodos Draw](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).

Antes de criar um buffer de vértice, você precisa definir seu layout criando um [**objeto de layout de entrada**](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout); Isso é feito chamando [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout). Depois que o objeto de layout de entrada for criado, associe-o ao estágio de Assembler de entrada chamando [**IASetInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetinputlayout).

Para criar um buffer de vértice, chame [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer).

### <a name="index-buffer"></a>Buffer de índice

Um buffer de índice contém um conjunto sequencial de índices de 16 ou 32 bits; cada índice é usado para identificar um vértice em um buffer de vértices. Indexação é usar um buffer de índice com um ou mais buffers de vértices para fornecer dados ao estágio de IA. Um buffer de índice pode ser visualizado como na ilustração a seguir.

![ilustração de um buffer de índice](images/d3d10-index-buffer.png)

Os índices sequenciais armazenados em um buffer de índice estão localizados com os seguintes parâmetros:

-   Deslocamento -o número de bytes desde o início do buffer ao primeiro índice. O deslocamento é fornecido para [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer).
-   StartIndexLocation-o número de bytes do deslocamento para o primeiro vértice usado pela chamada Draw apropriada (consulte os [métodos Draw](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).
-   IndexCount -o número de índices para renderizar.

Para criar um buffer de índice, chame [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer).

Um buffer de índice pode unir várias [faixas de linha ou de triângulo](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) separando cada uma com um índice de corte de faixa. Um índice de recorte de faixa permite várias faixas de linhas ou de triângulos serem desenhadas com uma chamada de desenho único. Um índice de corte de faixa é simplesmente o valor máximo possível para o índice (0xFFFF para um índice de 16 bits, 0xFFFFFFFF para um índice de 32 bits). O índice de recorte de faixa redefine o sentido de giro em primitivos indexados e pode ser usado para eliminar a necessidade de triângulos degenerados que caso contrário, seriam necessários para manter o sentido correto de giro em uma faixa de triângulo. A ilustração a seguir mostra um exemplo de índice de recorte de faixa.

![ilustração de um índice de recorte de faixa](images/d3d10-ia-strips-cut-value.png)

### <a name="constant-buffer"></a>Buffer constante

O Direct3D 10 introduziu um novo buffer para fornecer constantes de sombreador chamado buffer de constante de sombreador ou simplesmente um buffer de constante. Conceitualmente, ele se parece com um buffer de vértice de elemento único, como mostrado na ilustração a seguir.

![ilustração de um buffer constante de sombreador](images/d3d10-shader-resource-buffer.png)

Cada elemento armazena uma constante de 1 a 4 componentes determinada pelo formato dos dados armazenados.

Buffers constantes reduzem a largura de banda necessária para atualizar constantes de sombreador, permitindo que as constantes de sombreador sejam agrupadas e confirmadas ao mesmo tempo em vez de fazer chamadas individuais para confirmar cada constante separadamente.

Para criar um buffer de sombreador-constante, chame [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) e especifique o buffer constante de associação d3d10 do sinalizador de associação de buffer de constantes \_ \_ \_ (consulte o [**\_ \_ sinalizador de ligação d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)).

Para associar um buffer de sombreador-constante ao pipeline, chame um destes métodos: [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers)ou [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers).

Observe que, ao usar a interface de [**interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , o processo de criação, associação e confirmação de um buffer constante é manipulado pela instância da **interface ID3D10Effect** . Nesse caso, só nescesary obter a variável do efeito com um dos métodos getvariance, como [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) , e atualizar a variável com um dos métodos SetVariable, como [**setmatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix). Para obter um exemplo de como usar a **interface ID3D10Effect** para gerenciar um buffer de constantes, consulte o [tutorial 07](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

Um sombreador continua a ler variáveis em um buffer constante diretamente pelo nome de variável da mesma maneira que são lidas variáveis que não fazem parte de um buffer constante.

Cada estágio de sombreador permite até 15 buffers constantes de sombreador; cada buffer pode manter até 4.096 constantes.

Use um buffer constante para armazenar os resultados da fase de fluxo de saída.

Consulte [Constantes de sombreador (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-constants.md) para obter um exemplo de declaração de um buffer constante em um sombreador.

## <a name="texture-resources"></a>Recursos de textura

Um recurso de textura é uma coleção estruturada de dados projetada para armazenar texels. Diferente dos buffers, as texturas podem ser filtradas por amostras de texturas à medida que são lidas por unidades de sombreador. O tipo de textura afeta como a textura é filtrada. Um texel representa a menor unidade de uma textura que pode ser lida ou gravada pelo pipeline. Cada Texel contém de 1 a 4 componentes, organizados em um dos formatos DXGI (consulte [**o \_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).

Texturas são criadas como um recurso estruturado para que seu tamanho seja conhecido. No entanto, cada textura pode ser digitada ou ter um tipo menor no momento da criação do recurso, desde que o tipo seja totalmente especificado usando uma exibição quando a textura estiver associada ao pipeline.

-   [Tipos de textura](#texture-types)
-   [Sub-recursos](#subresources)
-   [Tipo forte versus fraco](#strong-vs-weak-typing)

### <a name="texture-types"></a>Tipos de textura

Existem vários tipos de texturas: 1D, 2D, 3D, e cada uma pode ser criada com ou sem mipmaps. O Direct3D 10 também dá suporte a matrizes de textura e texturas com uma amostra.

-   [Textura 1D](#1d-texture)
-   [Matriz de textura 1D](#1d-texture-array)
-   [Textura 2D e matriz de textura 2D](#2d-texture-and-2d-texture-array)
-   [Textura 3D](#3d-texture)

### <a name="1d-texture"></a>Textura 1D

Uma textura 1D em sua forma mais simples contém dados de textura que podem ser tratados com uma coordenada de textura única; pode ser visualizada como uma matriz de texels, conforme mostrado na ilustração a seguir.

![ilustração de uma textura 1D](images/d3d10-1d-texture.png)

Cada texel contém um número de componentes de cor dependendo do formato dos dados armazenados. Ao adicionar mais complexidade, você pode criar uma textura 1D com níveis de mipmap, conforme mostrado na ilustração a seguir.

![ilustração de uma textura 1D com níveis de mipmap](images/d3d10-resource-texture1d.png)

Um nível de mipmap é uma textura menor do que o nível superior por uma potência de dois. O nível mais alto contém o máximo de detalhes, cada nível subsequente é menor; para mipmap 1D, o menor nível contém um texel. Os diferentes níveis são identificados por um índice chamado LOD (nível de detalhes); você pode usar o LOD para acessar uma textura menor na renderização de uma geometria que não está tão próxima da câmera.

### <a name="1d-texture-array"></a>Matriz de textura 1D

Direct3D 10 também tem uma nova estrutura de dados para uma matriz de texturas. Uma matriz de texturas 1D conceitualmente parece com a ilustração a seguir.

![ilustração de uma matriz de textura 1D](images/d3d10-resource-texture1darray.png)

Essa matriz de textura contém três texturas. Cada uma das três texturas tem uma largura de 5 (o número de elementos na primeira camada). Cada textura também contém uma mipmap de 3 camadas.

Todas as matrizes de textura no Direct3D são uma matriz homogênea de texturas; ou seja, cada textura em uma matriz de texturas deve ter o mesmo formato de dados e o tamanho (incluindo a largura de textura e o número de níveis de mipmap. Você pode criar matrizes de textura de diferentes tamanhos, contanto que todas as texturas em cada matriz correspondam em tamanho.

### <a name="2d-texture-and-2d-texture-array"></a>Textura 2D e matriz de textura 2D

Um recurso Texture2D contém uma grade 2D de texels. Cada texel é endereçável por um vetor u, v. Como é um recurso de textura, ele pode conter níveis de mipmap e sub-recursos. Um recurso de textura 2D totalmente preenchida é semelhante à ilustração a seguir.

![ilustração de um recurso de textura 2D](images/d3d10-resource-texture2d.png)

Esse recurso de textura contém uma única textura 3 x 5 com três níveis de mipmap.

Um recurso Texture2DArray é uma matriz homogênea de texturas 2D; ou seja, cada textura tem o mesmo formato de dados e dimensões (incluindo níveis de mipmap). Ele tem um layout semelhante ao da matriz de textura 1D, exceto que as texturas agora contêm dados 2D e, portanto, têm a aparência da ilustração a seguir.

![ilustração de uma matriz de recursos de textura 2D](images/d3d10-resource-texture2darray.png)

Essa matriz de textura contém três texturas; cada uma de 3 x 5 com dois níveis de mipmap.

### <a name="using-a-texture2darray-as-a-texture-cube"></a>Usar Texture2DArray como um cubo de textura

Um cubo de textura é uma matriz de textura 2D com 6 texturas, uma para cada face do cubo. Um cubo de textura totalmente preenchida se parece com a ilustração a seguir.

![ilustração de uma matriz de recursos de textura 2D que representa um cubo de textura](images/d3d10-resource-texturecube.png)

Uma matriz de textura 2D com 6 texturas pode ser lida nos sombreadores com as funções intrínsecas do mapa do cubo após a vinculação ao pipeline com um modo de exibição de textura de cubo. Os cubos de textura são endereçados do sombreador com um vetor 3D apontado para o centro do cubo de textura.

### <a name="3d-texture"></a>Textura 3D

Um recurso Texture3D (também conhecido como textura de volume) contém um volume 3D de texels. Como é um recurso de textura, pode conter níveis de mipmap. Uma textura [**3D totalmente preenchida se**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) parece com a ilustração a seguir.

![ilustração de um recurso de textura 3D](images/d3d10-resource-texture3d.png)

Quando uma fatia de mipmap da textura 3D é vinculada como uma saída de destino de renderização (com um modo de exibição de renderização de destino), a textura 3D se comporta de forma idêntica à matriz de textura 2D com n fatias. A fatia de renderização específica é escolhida no estágio geometry-shader, declarando um componente escalar dos dados de saída como o valor do sistema \_ RenderTargetArrayIndex do SV.

Não há nenhum conceito de matriz de textura 3D; portanto, um sub-recurso de textura 3D é um nível de mipmap único.

### <a name="subresources"></a>Sub-recursos

A API do Direct3D 10 faz referência a recursos inteiros ou subconjunto de recursos. Para especificar uma parte dos recursos, o Direct3D cunhou o termo sub-recursos, o que significa um subconjunto de um recurso.

Um buffer é definido como um sub-recurso único. Texturas são um pouco mais complicadas, já que existem vários tipos diferentes de textura (1D, 2D, etc), e algumas suportam níveis de mipmap e/ou matrizes de textura. Começando com o caso mais simples, uma textura 1D é definida como um sub-recurso único, conforme mostrado na ilustração a seguir.

![ilustração de uma textura 1D](images/d3d10-1d-texture.png)

Isso significa que a matriz de texels que compõe uma textura 1D está contida em um único sub-recurso.

Se você expandir uma textura 1D com três níveis de mipmap, ela poderá ser visualizada da seguinte forma.

![ilustração de uma textura 1D com níveis de mipmap](images/d3d10-resource-texture1d.png)

Pense nisso como uma textura única composta por três subtexturas. Cada subtextura conta como um sub-recurso, portanto, essa textura 1D contém 3 sub-recursos. Uma subtextura (ou sub-recurso) pode ser indexada usando o nível de detalhe (LOD) para uma única textura. Ao usar uma matriz de texturas, acessar uma determinada subtextura exige o LOD e a textura específica. Ou então, a API combina essas duas partes de informações em um índice de sub-recurso único baseado em zero, conforme mostrado aqui.

![ilustração de um índice de sub-recurso baseado em zero](images/d3d10-resource-texture1darray-sub-indexing.png)

### <a name="selecting-subresources"></a>Selecionando sub-recursos

Algumas APIs acessam um recurso inteiro (por [**exemplo, CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)), outras acessam uma parte de um recurso (por [**exemplo, UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource) ou [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)). As APIs que acessam uma parte de um recurso geralmente usam uma descrição de exibição (como [**D3D10 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)) para especificar as sub-fontes a acessar.

Essas figuras ilustram os termos usados por uma descrição do modo de exibição ao acessar uma matriz de texturas.

### <a name="array-slice"></a>Fatia de matriz

Dada uma matriz de texturas, cada textura com mipmaps, uma fatia de matriz (representada pelo retângulo branco) inclui uma textura e todas as suas subtexturas, conforme mostrado na ilustração a seguir.

![ilustração de uma fatia de matriz](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Tamanho de MIP

Um tamanho de MIP (representado pelo retângulo branco) inclui um nível de mipmap para cada textura em uma matriz, conforme mostrado na ilustração a seguir.

![ilustração de um tamanho de MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Selecionando um sub-recurso único

Você pode usar esses dois tipos de fatias para escolher um sub-recurso único, conforme mostrado na ilustração a seguir.

![ilustração da escolha de um sub-recurso usando uma fatia de matriz e um tamanho de MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Selecionando vários sub-recursos

Ou você pode usar esses dois tipos de fatias com o número de níveis de mipmap e/ou número de texturas para escolher vários sub-recursos.

![ilustração de escolha de vários sub-recursos](images/d3d10-resource-subresources-2.png)

Independentemente do tipo de textura que você está usando, com ou sem mipmaps, com ou sem uma matriz de textura, você pode usar a função [**auxiliar, D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource), para calcular o índice de uma sub-fonte específica.

### <a name="strong-vs-weak-typing"></a>Tipo forte versus fraco

Criar um recurso totalmente com tipo restringe o recurso ao formato com o qual ele foi criado. Isso permite que o runtime otimize o acesso, especialmente se o recurso for criado com sinalizadores indicando que ele não pode [ser mapeado](d3d10-graphics-programming-guide-resources-mapping.md) pelo aplicativo. Recursos criados com um tipo específico não podem ser reinterpretados usando o mecanismo de exibição.

Em um recurso de tipo menor, o tipo de dados é desconhecido quando o recurso é criado pela primeira vez. O aplicativo deve escolher entre os formatos sem tipo disponíveis (consulte [**FORMATO DXGI \_**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Você deve especificar o tamanho da memória a alocar e se o tempo de execução precisará gerar as subtexturas em mipmap. No entanto, o formato exato dos dados (seja a memória interpretada como inteiros, valores de ponto flutuante, inteiros não atribuídos, etc.) não é determinado até que o recurso seja associado ao pipeline com um modo de exibição. Como o formato de textura permanece flexível até a textura ser associada ao pipeline, o recurso será referido como armazenamento com tipo fraco. O armazenamento com tipo fraco tem a vantagem de poder ser reutilizado ou reinterpretado (em outro formato), desde que o bit de componente do novo formato corresponda à contagem de bit do formato antigo.

Um recurso único pode ser vinculado a vários estágios de pipeline, desde que cada um tenha um modo de exibição exclusivo que qualifique totalmente os formatos em cada local. Por exemplo, um recurso criado com o formato DXGI \_ FORMAT \_ R32G32B32A32 TYPELESS pode ser usado como um \_ FORMATO DXGI \_ \_ R32G32B32A32 FLOAT e um \_ UINT DXGI \_ FORMAT \_ R32G32B32A32 \_ em diferentes locais no pipeline simultaneamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
