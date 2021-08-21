---
title: VRS (sombreamento de taxa variável)
description: Sombreamento de taxa variável ou sombreamento de pixels altos é um mecanismo que permite alocar desempenho/potência de renderização em taxas que variam em toda &mdash; &mdash; a imagem renderizada.
ms.localizationpriority: high
ms.topic: article
ms.date: 04/08/2019
ms.openlocfilehash: b26d2d67a6e4a5f7b599a9fc65f324b301346fde3170262e80235a25f8cfb88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045267"
---
# <a name="variable-rate-shading-vrs"></a>VRS (sombreamento de taxa variável)

## <a name="the-motivation-for-vrs"></a>A motivação para VRS
Devido a restrições de desempenho, um renderador de gráficos nem sempre pode oferecer o mesmo nível de qualidade a cada parte de sua imagem de saída. Sombreamento de taxa variável ou sombreamento de pixels altos é um mecanismo que permite alocar desempenho/potência de renderização em taxas que variam em toda &mdash; &mdash; a imagem renderizada.

Em alguns casos, a taxa de sombreamento pode ser reduzida com pouca ou nenhuma redução na qualidade de saída perceptível; levando a uma melhoria de desempenho que é essencialmente gratuita.

## <a name="without-vrsmdashmulti-sample-anti-aliasing-with-supersampling"></a>Sem a suavização de vários exemplos de VRS &mdash; com a superampling
Sem sombreamento de taxa variável, o único meio de controlar a taxa de sombreamento é com MSAA (suavização de várias amostras) com execução baseada em exemplo (também conhecida como supersampling).

A MSAA é um mecanismo para reduzir o alias geométrico e melhorar a qualidade de renderização de uma imagem em comparação com o não uso da MSAA. A contagem de exemploSAA, que pode ser 1x, 2x, 4x, 8x ou 16x, rege o número de amostras alocadas por pixel de destino de renderização. A contagem de exemploSAA deve ser conhecida antes quando o destino é alocado e não pode ser alterada posteriormente.

A superamplagem faz com que o sombreador de pixel seja invocado uma vez por amostra, com uma qualidade mais alta, mas também um custo de desempenho mais alto em comparação com a execução por pixel.

Seu aplicativo pode controlar sua taxa de sombreamento escolhendo entre a execução baseada em pixel ou MSAA com supersampling. Essas duas opções não fornecem um controle muito bom. Além disso, talvez você queira uma taxa de sombreamento mais baixa para uma determinada classe de objetos em comparação com o restante da imagem. Esses objetos podem incluir um objeto por trás de um elemento MOTION ou uma transparência, um desfoque (profundidade do campo, movimento etc.) ou uma distorção óptica devido à métrica de VR. Mas isso não seria possível, porque a qualidade e os custos de sombreamento são corrigidos em toda a imagem.

## <a name="with-variable-rate-shading-vrs"></a>Com VRS (sombreamento de taxa variável)
O modelo vrS (sombreamento de taxa variável) estende a direção de supersampling-with-MSAA na direção oposta, "pixel alto", adicionando o conceito de sombreamento abstrato. É aí que o sombreamento pode ser executado em uma frequência mais alta do que um pixel. Em outras palavras, um grupo de pixels pode ser sombreado como uma única unidade e, em seguida, o resultado é transmitido para todos os exemplos no grupo.

Uma API de sombreamento asserção permite que seu aplicativo especifique o número de pixels que pertencem a um grupo sombreado ou pixel *alto.* Você pode variar o tamanho de pixel grande depois de alocar o destino de renderização. Portanto, diferentes partes da tela ou diferentes passagens de desenho podem ter taxas de sombreamento diferentes.

Aqui está uma tabela que descreve qual nível de MSAA tem suporte com qual tamanho de pixel alto. Não há suporte para alguns em nenhuma plataforma; enquanto outros estão habilitados condicionalmente com base em um recurso (*AdditionalShadingRatesSupported*), indicado por "Cap".

![A tabela mostra o tamanho de pixel alto para níveis de MS A A.](images/CoarsePixelSizeSupport.PNG "Tamanhos de pixels grossos")

Para as camadas de recursos discutidas na próxima seção, não há nenhuma combinação de tamanho de pixel e contagem de exemplos, em que o hardware precisa acompanhar mais de 16 exemplos por invocação de sombreador de pixel. Essas combinações são sombreadas por meio tom na tabela acima.

## <a name="feature-tiers"></a>Camadas de recursos
Há duas camadas para a implementação de VRS e duas funcionalidades que você pode consultar. Cada camada é descrita em mais detalhes após a tabela.

![A tabela mostra os recursos disponíveis nas Camadas 1 e 2.](images/Tiers.PNG "Camadas VRS")

### <a name="tier-1"></a>Camada 1
- A taxa de sombreamento pode ser especificada somente por desenho; não mais granular do que isso.
- A taxa de sombreamento aplica-se uniformemente ao que é desenhado independentemente de onde ele está dentro do destino de renderização.

### <a name="tier-2"></a>Camada 2
- A taxa de sombreamento pode ser especificada por desenho, como na Camada 1. Ele também pode ser especificado por uma combinação de base por desenho e de:
  - Semântica de cada vértice de provocação e
  - uma imagem de espaço na tela.
- As taxas de sombreamento das três fontes são combinadas usando um conjunto de combinadores.
- O tamanho do lado do lado da imagem de espaço na tela é 16x16 ou menor.
- A taxa de sombreamento solicitada pelo aplicativo tem a garantia de ser entregue exatamente (para precisão de filtros temporais e outros filtros de reconstrução).
- SV_ShadingRate entrada PS tem suporte.
- A taxa de sombreamento por vértice de provocação (também conhecida como por primitivo), é válida quando um viewport é usado e `SV_ViewportArrayIndex` não é gravado.
- A taxa de vértice por ataque pode ser usada com mais de um viewport se a funcionalidade *SupportsPerVertexShadingRateWithMultipleViewports* estiver definida como `true` . Além disso, nesse caso, essa taxa pode ser usada quando `SV_ViewportArrayIndex` é gravado.

### <a name="list-of-capabilities"></a>List of capabilities
- *AdditionalShadingRatesSupported*
  - Tipo booliana.
  - Indica se os tamanhos de pixel 2x4, 4x2 e 4x4 são suportados para renderização de amostra única; e se o tamanho de pixel 2x4 é suportado para 2x MSAA.
- *SupportsPerVertexShadingRateWithMultipleViewports*
  - Tipo booliana.
  - Indica se mais de um viewport pode ser usado com a taxa de sombreamento por vértice (também conhecida como por primitivo).

## <a name="specifying-shading-rate"></a>Especificando a taxa de sombreamento
Para flexibilidade em aplicativos, há uma variedade de mecanismos fornecidos para controlar a taxa de sombreamento. Mecanismos diferentes estão disponíveis dependendo da camada de recursos de hardware.

### <a name="command-list"></a>Lista de comandos
Esse é o mecanismo mais simples para definir a taxa de sombreamento. Ele está disponível em todas as camadas.

Seu aplicativo pode especificar um tamanho de pixel alta usando o [ **método ID3D12GraphicsCommandList5::RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate). Essa API aceita um único argumento de enum. A API fornece um controle geral do nível de qualidade para renderizar a capacidade de definir a taxa de sombreamento &mdash; por desenho.

Os valores para esse estado são expressos por meio [**da enumeração D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) dados.

#### <a name="coarse-pixel-size-support"></a>Suporte a tamanho de pixels de grosseria
As taxas de sombreamento 1x1, 1x2, 2x2 e 2x2 têm suporte em todas as camadas.

Há uma funcionalidade, *AdditionalShadingRatesSupported,* para indicar se há suporte para 2x4, 4x2 e 4x4 no dispositivo.

### <a name="screen-space-image-image-based"></a>Imagem de espaço na tela (baseada em imagem)
Na Camada 2 e superior, você pode especificar a taxa de sombreamento de pixel com uma imagem de espaço na tela.

A imagem de espaço na tela permite que seu aplicativo crie uma imagem de "máscara LOD (nível de detalhe) indicando regiões de qualidade variável, como áreas que serão cobertas por desfoque de movimento, desfoque de profundidade do campo, objetos transparentes ou elementos de interface do usuário DO MOTION. A resolução da imagem está em macroblocks; não está na resolução do destino de renderização. Em outras palavras, os dados de taxa de sombreamento são especificados em uma granularidade de blocos de 8x8 ou 16 x 16 pixels, conforme indicado pelo tamanho do bloco VRS.

#### <a name="tile-size"></a>Tamanho de bloco
Seu aplicativo pode consultar uma API para recuperar o tamanho do lado do vrs com suporte para seu dispositivo.

Os blocos são quadrados e o tamanho refere-se à largura ou à altura do bloco em texels.

Se o hardware não dá suporte ao sombreamento de taxa variável da Camada 2, a consulta de funcionalidade para o tamanho do seu arquivo retornará 0.

Se o hardware *dá suporte* ao sombreamento de taxa variável de Camada 2, o tamanho do lado é um desses valores.

- 8
- 16
- 32

#### <a name="screen-space-image-size"></a>Tamanho da imagem de espaço na tela
Para um destino de renderização de tamanho {rtWidth, rtHeight}, usando um determinado tamanho de bloco chamado **VRSTileSize**, a imagem de espaço na tela que a cobrirá é dessas dimensões.

```cpp
{ ceil((float)rtWidth / VRSTileSize), ceil((float)rtHeight / VRSTileSize) }
```

A parte superior esquerda da imagem de espaço na tela (0, 0) é bloqueada na parte superior esquerda do destino de renderização (0, 0).

Para procurar a coordenada (x,y) de um peças que corresponde a um local específico no destino de renderização, divida as coordenadas de espaço de janela de (x, y) pelo tamanho do peças, ignorando os bits fracionados.

Se a imagem de espaço na tela for maior do que precisa ser para um determinado destino de renderização, as partes extras à direita e/ou inferior não serão usadas.

Se a imagem de espaço na tela for muito pequena para um determinado destino de renderização, qualquer tentativa de leitura da imagem além de suas extensão reais produzirá uma taxa de sombreamento padrão de 1x1. Isso porque a parte superior esquerda da imagem de espaço na tela (0, 0) está bloqueada na parte superior esquerda do destino de renderização (0, 0) e "leitura além das extensão de destino de renderização" significa ler muito grandes valores para x e y.

#### <a name="format-layout-resource-properties"></a>Formato, layout, propriedades do recurso
O formato dessa superfície é uma superfície de 8 bits de canal único ([**DXGI_FORMAT_R8_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

O recurso é a **dimensão TEXTURE2D.**

Ele não pode ser matriz ou mipped. Ele deve ter explicitamente um nível mip.

Ele tem a contagem de exemplo 1 e a qualidade de exemplo 0.

Ele tem layout de textura **DESCONHECIDO.** Implicitamente, ele não pode ser um layout de linha principal, porque o adaptador cruzado não é permitido.

A maneira esperada na qual os dados de imagem de espaço na tela são preenchidos é
1. Gravar os dados usando um sombreador de computação; a imagem de espaço na tela é vinculada como um UAV ou
2. Copie os dados para a imagem de espaço na tela.

Ao criar a imagem de espaço na tela, esses sinalizadores são permitidos.

- Nenhuma
- ALLOW_UNORDERED_ACCESS
- DENY_SHADER_RESOURCE

Esses sinalizadores não são permitidos.

- ALLOW_RENDER_TARGET
- ALLOW_DEPTH_STENCIL
- ALLOW_CROSS_ADAPTER
- ALLOW_SIMULTANEOUS_ACCESS
- VIDEO_DECODE_REFERENCE_ONLY

O tipo de heap do recurso não pode ser carregado nem READBACK.

O recurso não pode ser SIMULTANEOUS_ACCESS. O recurso não pode ser entre adaptadores.

#### <a name="data"></a>Dados
Cada byte da imagem de espaço na tela corresponde a um valor da enumeração [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)  .

#### <a name="resource-state"></a>Estado do recurso
Um recurso precisa ser transferido para um estado somente leitura quando usado como uma imagem de espaço na tela. Um estado somente leitura, [**D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states), é definido para essa finalidade.

O recurso de imagem é transferido para fora desse Estado para se tornar gravável novamente.

#### <a name="setting-the-image"></a>Configurando a imagem
A imagem de espaço de tela para especificar a taxa do sombreador é definida na lista de comandos.

Um recurso que foi definido como uma fonte de taxa de sombreamento não pode ser lido ou gravado em nenhum estágio do sombreador.

Uma `null` imagem de espaço na tela pode ser definida para especificar a taxa do sombreador. Isso tem o efeito de 1x1 ser usado consistentemente como a contribuição da imagem de espaço na tela. Inicialmente, a imagem de espaço na tela pode ser considerada definida como `null` .

#### <a name="promotion-and-decay"></a>Promoção e decaimento
Um recurso de imagem de espaço na tela não tem nenhuma implicação especial em relação à promoção ou decaimento.

### <a name="per-primitive-attribute"></a>Atributo por primitivo
Um atributo por primitivo adiciona a capacidade de especificar um termo de taxa de sombreamento como um atributo de um vértice provocativa. Esse atributo é sombreado &mdash; , ou seja, é propagado para todos os pixels no triângulo atual ou na linha primitiva. O uso de um atributo por primitivo pode permitir um controle mais refinado da qualidade da imagem em comparação com os outros especificadores de taxa de sombreamento.

O atributo por primitivo é uma semântica configurável chamada `SV_ShadingRate` . `SV_ShadingRate` existe como parte do [modelo de sombreador HLSL 6,4](/windows/desktop/direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12).

Se um conjunto de VS ou GS `SV_ShadingRate` , mas VRS não estiver habilitado, a configuração semântica não terá nenhum efeito. Se nenhum valor para `SV_ShadingRate` for especificado por primitivo, um valor de taxa de sombreamento de 1x1 será considerado como a contribuição por primitiva.

### <a name="combining-shading-rate-factors"></a>Combinando fatores de taxa de sombreamento
As várias fontes de taxa de sombreamento são aplicadas em sequência usando este diagrama.

![O diagrama mostra um estado de pipeline, rotulado como, com a taxa de sombreamento de vértice provocativa, rotulada como B, aplicada a um combinador, a taxa de sombreamento baseada em imagem, rotulada B, aplicada a um combinador.](images/Combiners.PNG "Combinadores de sombreamento")

Cada par de A e B é combinado usando um combinador.

\* Ao especificar uma taxa de sombreador por atributo de vértice.

- Se um sombreador de geometria for usado, a taxa de sombreamento poderá ser especificada por meio dele.
- Se um sombreador de geometria não for usado, a taxa de sombreamento será especificada pelo vértice provocativa.

#### <a name="list-of-combiners"></a>Lista de combinadores
Há suporte para os seguintes combinadores. Usando um combinador (C) e duas entradas (A e B).

- **Passagem**. C. XY = A. XY.
- **Substituir**. C. XY = B. XY.
- **Maior qualidade**. C. XY = min (A. XY, B. XY).
- **Qualidade inferior**. C. XY = Max (A. XY, B. XY).
- **Aplique o custo B em relação A um**. C. XY = min (maxRate, A. XY + B. XY).

em que `maxRate` é a maior dimensão permitida de pixel grosso no dispositivo. Isso seria

- **D3D12_AXIS_SHADING_RATE_2X** (ou seja, um valor de 1), se AdditionalShadingRatesSupported for `false` .
- **D3D12_AXIS_SHADING_RATE_4X** (ou seja, um valor de 2), se AdditionalShadingRatesSupported for `true` .

A escolha do combinador para sombreamento de taxa variável é definida na lista de comandos por meio de [**ID3D12GraphicsCommandList5:: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate).

Se nenhum combinado for definido, então ele permanecerá no padrão, que é passagem.

Se a origem para um combinador for um [**D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate), o que não é permitido na tabela de suporte, a entrada será corrigida para uma taxa de sombreamento *com suporte.*

Se a saída de um combinador não corresponder a uma taxa de sombreamento com suporte na plataforma, o resultado será corrigido para uma *taxa de sombreamento com suporte.*

### <a name="default-state-and-state-clearing"></a>Estado padrão e limpeza de estado
Todas as fontes de taxa de sombreamento, a saber

- a taxa especificada do estado do pipeline (especificada na lista de comandos),
- a taxa especificada da imagem de espaço de tela e
- o atributo por primitivo

ter um padrão de **D3D12_SHADING_RATE_1X1**. Os combinadores padrão são {PASSTHROUGH, PASSTHROUGH}.

Se nenhuma imagem de espaço de tela for especificada, uma taxa de sombreamento de 1x1 será inferida da origem.

Se nenhum atributo por primitivo for especificado, uma taxa de sombreamento de 1x1 será inferida da origem.

[ID3D12CommandList:: clearstate](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate) redefine a taxa especificada pelo estado do pipeline para o padrão e a seleção da imagem de espaço da tela para o padrão "nenhuma imagem de espaço na tela".

## <a name="querying-shading-rate-by-using-sv_shadingrate"></a>Consultando a taxa de sombreamento usando SV_ShadingRate
É útil saber qual taxa de sombreamento foi selecionada pelo hardware em qualquer invocação de sombreador de pixel fornecida. Isso pode permitir uma variedade de otimizações em seu código do PS. Uma variável de sistema somente PS, `SV_ShadingRate` , fornece informações sobre a taxa de sombreamento.

### <a name="type"></a>Tipo
O tipo dessa semântica é uint.

### <a name="data-interpretation"></a>Interpretação de dados
Os dados são interpretados como um valor da enumeração [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) .

### <a name="if-vrs-is-not-being-used"></a>Se VRS não estiver sendo usado
Se o sombreamento de pixel grosso não estiver sendo usado, `SV_ShadingRate` será lido novamente como um valor de 1x1, indicando pixels finos.

### <a name="behavior-under-sample-based-execution"></a>Comportamento na execução baseada em amostra
Um sombreador de pixel falha na compilação se ele insere `SV_ShadingRate` e também usa a execução baseada em exemplo &mdash; , por exemplo, inserindo `SV_SampleIndex` ou usando a palavra-chave de interpolação de exemplo.

> ### <a name="remarks-on-deferred-shading"></a>Comentários sobre o sombreamento adiado
>
> As passagens de iluminação de um aplicativo de sombreamento adiado podem precisar saber qual taxa de sombreamento foi usada para qual área da tela. Isso é para que os despachos de passagem de iluminação possam ser iniciados com uma taxa mais grosseira. A `SV_ShadingRate` variável pode ser usada para fazer isso se for gravada no gbuffer.

## <a name="depth-and-stencil"></a>Profundidade e estêncil
Quando o sombreamento de pixels grossos é usado, a profundidade e o estêncil e a cobertura são sempre computados e emitidos na resolução de exemplo completa.

## <a name="using-the-shading-rate-requested"></a>Usando a taxa de sombreamento solicitada
Para todas as camadas, espera-se que se uma taxa de sombreamento seja solicitada e tenha suporte na combinação de nível de dispositivo e MSAA, essa é a taxa de sombreamento entregue pelo hardware.

Uma taxa de sombreamento solicitada significa uma taxa de sombreamento calculada como uma saída dos combinadores (consulte a seção [combinando fatores de taxa de sombreamento](#combining-shading-rate-factors) neste tópico).

Uma taxa de sombreamento com suporte é 1x1, 1x2, 2x1 ou 2x2 em uma operação de renderização em que a contagem de amostra é menor ou igual a quatro. Se o recurso *AdditionalShadingRatesSupported* for `true` , os 2x4, 4x e 4x4 também serão taxas de sombreamento com suporte para algumas contagens de amostra (consulte a tabela na seção [with VRS (sombreamento de taxa variável)](#with-variable-rate-shading-vrs) neste tópico).

## <a name="screen-space-derivatives"></a>Derivações de espaço na tela
Os cálculos de gradientes de pixel para adjacentes são afetados por sombreamento de pixel grosso. Por exemplo, quando forem usados pixels grossos 2x2, um gradiente será o dobro do tamanho em comparação quando não forem usados pixels grossos. Seu aplicativo pode desejar ajustar os sombreadores para compensar isso &mdash; ou não, dependendo da funcionalidade desejada.

Como os MIPS são escolhidos com base em uma derivação de espaço de tela, o uso de sombreamento de pixels grossos afeta a seleção MIP. O uso de sombreamento de pixels finos faz com que mips menos detalhados sejam selecionados em comparação com quando pixels mais finos não são usados.

## <a name="attribute-interpolation"></a>Interpolação de atributo
Entradas para um sombreador de pixel podem ser interpoladas com base em seus vértices de origem. Como o sombreamento de taxa variável afeta as áreas do destino gravado por cada invocação do sombreador de pixel, ele interage com a interpolação de atributo. Os três tipos de interpolação são center, centroid e sample.

### <a name="center"></a>Centro
O local de interpolação central para um pixel de grosseria é o centro geométrico da área de pixels inteiramente grosseira. `SV_Position` é sempre interpolado no centro da região de pixels grosseiras.

### <a name="centroid"></a>Centróide
Quando o sombreamento de pixels alto é usado com MSAA, para cada pixel fino, ainda haverá gravações no número completo de amostras alocadas para o nível de MSAA do destino. Portanto, o local de interpolação de centroide considerará todos os exemplos de pixels finos em pixels finos. Dito isso, o local de interpolação de centroide é definido como o primeiro exemplo abordado, em ordem crescente de índice de exemplo. A cobertura efetiva do exemplo é AND-ed com o bit correspondente do sampleMask de estado do rasterizador.

> [!NOTE]
> Quando o sombreamento de pixels alto é usado na Camada 1, SampleMask é sempre uma máscara completa. Se SampleMask estiver configurado para não ser uma máscara completa, o sombreamento de pixels está desabilitado na Camada 1.

### <a name="sample-based-execution"></a>Execução baseada em exemplo
A execução baseada em exemplo ou a *supersamplagem,* que é causada pelo uso do recurso de interpolação de exemplo, pode ser usada com sombreamento de pixels e faz com que o sombreador de pixel seja invocado por &mdash; &mdash; exemplo. Para destinos da contagem de exemplo N, o sombreador de pixel é invocado N vezes por pixel fino.

### <a name="evaluateattributesnapped"></a>EvaluateAttributeS sistemat
Intrínsecos de modelo de pull não são compatíveis com sombreamento de pixels finos na Camada 1. Se houver uma tentativa de usar intrínsecos de modelo de pull com sombreamento de pixel alto na Camada 1, o sombreamento de pixels alto será desabilitado automaticamente.

O `EvaluateAttributeSnapped` intrínseco pode ser usado com sombreamento de pixels alto na Camada 2. Sua sintaxe é a mesma que sempre foi.

```hlsl
numeric EvaluateAttributeSnapped(   
    in attrib numeric value, 
    in int2 offset);
```

Para contexto, `EvaluateAttributeSnapped` tem um parâmetro offset com dois campos. Quando usado sem sombreamento de pixels, apenas os quatro bits de ordem inferior do total de 32 são usados. Esses quatro bits representam o intervalo [-8, 7]. Esse intervalo abrange uma grade 16x16 dentro de um pixel. O intervalo é tal que as bordas superior e esquerda do pixel são incluídas e as bordas inferior e direita não são. O deslocamento (-8, -8) está no canto superior esquerdo e o deslocamento (7, 7) é no canto inferior direito. Deslocamento (0, 0) é o centro do pixel.

Quando usado com sombreamento de pixels altos, o parâmetro offset de é capaz `EvaluateAttributeSnapped` de especificar um intervalo maior de locais. O parâmetro offset seleciona uma grade 16x16 para cada pixel fino e há vários pixels finos. O intervalo expressível e o número consequente de bits usados depende do tamanho de pixel alto. As bordas superior e esquerda do pixel alto estão incluídas e as bordas inferior e direita não estão.

A tabela a seguir descreve a interpretação do `EvaluateAttributeSnapped` parâmetro offset de para cada tamanho de pixel alta.

#### <a name="evaluateattributesnappeds-offset-range"></a>Intervalo de deslocamento de EvaluateAttributeS offset

|Tamanho de pixel muito grande  |Intervalo indexável             |Tamanho do intervalo representável  |Número de bits necessários {x, y}  |Máscara binária de bits usáveis          |    
|------------------:|---------------------------:|-------------------------:|-----------------------------:|-----------------------------------:|    
|1x1 (bom)         |{ \[ -8, 7 \] , \[ -8, 7 \] }      |{16, 16}                  |{4, 4}                        |{00000000000xxxx, 0000000000xxxx}|    
|1x2                |{ \[ -8, 7 \] , \[ -16, 15 \] }    |{16, 32}                  |{4, 5}                        |{00000000000xxxx, 0000000000xxxx}|    
|2x1                |{ \[ -16, 15 \] , \[ -8, 7 \] }    |{32, 16}                  |{5, 4}                        |{0000000000xxxxx, 00000000000xxxx}|    
|2x2                |{ \[ -16, 15 \] , \[ -16, 15 \] }  |{32, 32}                  |{5, 5}                        |{0000000000xxxxx, 0000000000xxxx}|    
|2x4                |{ \[ -16, 15 \] , \[ -32, 31 \] }  |{32, 64}                  |{5, 6}                        |{0000000000xxxxx, 000000000xxxxxx}|    
|4x2                |{ \[ -32, 31 \] , \[ -16, 15 \] }  |{64, 32}                  |{6, 5}                        |{000000000xxxxxx, 0000000000xxxx}|    
|4x4                |{ \[ -32, 31 \] , \[ -32, 31 \] }  |{64, 64}                  |{6, 6}                        |{000000000xxxxxx, 000000000xxxxxx}|   

As tabelas a seguir são um guia para conversão do ponto fixo em representação decimal e fracionada. O primeiro bit acessível na máscara binária é o bit de sinal e o restante da máscara binária consiste na parte numérica.

O esquema de número para valores de quatro bits passados para `EvaluateAttributeSnapped` não é específico para sombreamento de taxa variável. Ele é rebaixado aqui para a conclusão.

Para valores de quatro bits.

| Valor binário | Decimal  | Fracionário |
|-------------:|---------:|-----------:|
|         1000 |-0,5f     |-8 / 16     |
|         1001 |-0,4375f  |-7 / 16|    |
|         1010 |-0,375f   |-6 / 16|    |
|         1011 |-0,3125f  |-5 / 16     |
|         1100 |-0,25f    |-4 / 16     |
|         1101 |-0,1875f  |-3 / 16     |
|         1110 |-0,125f   |-2 / 16     |
|         1111 |-0,0625f  |-1 /16      |
|         0000 |0.0f      |0 / 16      |
|         0001 |-0,0625f  |1 / 16      |
|         0010 |-0,125f   |2 / 16      |
|         0011 |-0,1875f  |3 / 16      |
|         0100 |-0,25f    |4 / 16      |
|         0101 |-0,3125f  |5 / 16      |
|         0110 |-0,375f   |6 / 16      |
|         0111 |-0,4375f  |7 / 16      |

Para valores de cinco bits.

| Valor binário | Decimal  | Fracionário |
|-------------:|---------:|-----------:|
|        10000 |-1        |-16 / 16    |
|        10001 |-0.9375   |-15 / 16    |
|        10010 |-0.875    |-14 / 16    |
|        10011 |-0.8125   |-13 / 16    |
|        10100 |-0.75     |-12 / 16    |
|        10101 |-0.6875   |-11 / 16    |
|        10110 |-0.625    |-10 / 16    |
|        10111 |-0.5625   |-9 / 16     |
|        11000 |-0,5      |-8 / 16     |
|        11001 |-0.4375   |-7 / 16     |
|        11010 |-0.375    |-6 / 16     |
|        11011 |-0.3125   |-5 / 16     |
|        11100 |-0.25     |-4 / 16     |
|        11101 |-0.1875   |-3 / 16     |
|        11110 |-0.125    |-2 / 16     |
|        11111 |-0.0625   |-1 / 16     |
|        00000 |0         |0 / 16      |
|        00001 |0.0625    |1 / 16      |
|        00010 |0,125     |2 / 16      |
|        00011 |0.1875    |3 / 16      |
|        00100 |0,25      |4 / 16      |
|        00101 |0.3125    |5 / 16      |
|        00110 |0.375     |6 / 16      |
|        00111 |0.4375    |7 / 16      |
|        01000 |0,5       |8 / 16      |
|        01001 |0.5625    |9 / 16      |
|        01010 |0.625     |10 / 16     |
|        01011 |0.6875    |11 / 16     |
|        01100 |0,75      |12 / 16     |
|        01101 |0.8125    |13 / 16     |
|        01110 |0.875     |14 / 16     |
|        01111 |0.9375    |15 / 16     |

Para valores de seis bits.

| Valor binário | Decimal  | Fracionário |
|-------------:|---------:|-----------:|
|       100000 |-2        |-32 / 16    |
|       100001 |-1.9375   |-31 / 16    |
|       100010 |-1.875    |-30 / 16    |
|       100011 |-1.8125   |-29 / 16    |
|       100100 |-1.75     |-28 / 16    |
|       100101 |-1.6875   |-27 / 16    |
|       100110 |-1.625    |-26 / 16    |
|       100111 |-1.5625   |-25 / 16    |
|       101000 |-1.5      |-24 / 16    |
|       101001 |-1.4375   |-23 / 16    |
|       101010 |-1.375    |-22 / 16    |
|       101011 |-1.3125   |-21 / 16    |
|       101100 |-1.25     |-20 / 16    |
|       101101 |-1.1875   |-19 / 16    |
|       101110 |-1.125    |-18 / 16    |
|       101111 |-1.0625   |-17 / 16    |
|       110000 |-1        |-16 / 16    |
|       110001 |-0.9375   |-15 / 16    |
|       110010 |-0.875    |-14 / 16    |
|       110011 |-0.8125   |-13 / 16    |
|       110100 |-0.75     |-12 / 16    |
|       110101 |-0.6875   |-11 / 16    |
|       110110 |-0.625    |-10 / 16    |
|       110111 |-0.5625   |-9 / 16     |
|       111000 |-0,5      |-8 / 16     |
|       111001 |-0.4375   |-7 / 16     |
|       111010 |-0.375    |-6 / 16     |
|       111011 |-0.3125   |-5 / 16     |
|       111100 |-0.25     |-4 / 16     |
|       111101 |-0.1875   |-3 / 16     |
|       111110 |-0.125    |-2 / 16     |
|       111111 |-0.0625   |-1 / 16     |
|       000000 |0         |0 / 16      |
|       000001 |0.0625    |1 / 16      |
|       000010 |0,125     |2 / 16      |
|       000011 |0.1875    |3 / 16      |
|       000100 |0,25      |4 / 16      |
|       000101 |0.3125    |5 / 16      |
|       000110 |0.375     |6 / 16      |
|       000111 |0.4375    |7 / 16      |
|       001000 |0,5       |8 / 16      |
|       001001 |0.5625    |9 / 16      |
|       001010 |0.625     |10 / 16     |
|       001011 |0.6875    |11 / 16     |
|       001100 |0,75      |12 / 16     |
|       001101 |0.8125    |13 / 16     |
|       001110 |0.875     |14 / 16     |
|       001111 |0.9375    |15 / 16     |
|       010000 |1         |16 / 16     |
|       010001 |1.0625    |17 / 16     |
|       010010 |1.125     |18 / 16     |
|       010011 |1.1875    |19 / 16     |
|       010100 |1,25      |20 / 16     |
|       010101 |1.3125    |21 / 16     |
|       010110 |1.375     |22 / 16     |
|       010111 |1,4375    |23 / 16     |
|       011000 |1.5       |24 / 16     |
|       011001 |1,5625    |25 / 16     |
|       011010 |1.625     |26 / 16     |
|       011011 |1,6875    |27 / 16     |
|       011100 |1,75      |28 / 16     |
|       011101 |1,8125    |29 / 16     |
|       011110 |1,875     |30 / 16     |
|       011111 |1,9375    |31 / 16     |

Da mesma maneira que com os pixels finos, a `EvaluateAttributeSnapped` grade de locais avaliáveis é centralizada no nível de pixel grande ao usar sombreamento de pixels grossos.

## <a name="setsamplepositions"></a>SetSamplePositions
Quando a API [**ID3D12GraphicsCommandList1:: SetSamplePositions**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) é usada com sombreamento grosso, a API define as posições de exemplo para pixels finos.

## <a name="sv_coverage"></a>SV_Coverage
Se `SV_Coverage` é declarado como uma entrada de sombreador ou saída na camada 1, o sombreamento de pixel grosso é desabilitado.

Você pode usar a `SV_Coverage` semântica com sombreamento de pixel grosso na camada 2 e reflete quais exemplos de um destino MSAA estão sendo gravados.

Quando o sombreamento de pixel grosso é usado, permitindo que vários pixels de origem componham &mdash; um bloco, &mdash; a máscara de cobertura representa todos os exemplos provenientes desse bloco.

Dada a compatibilidade de sombreamento de pixel grosso com MSAA, o número de bits de cobertura necessários para ser especificado pode variar. Por exemplo, com um recurso de MSAA de 4x usando [**D3D12_SHADING_RATE_2x2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate), cada pixel grosso grava em quatro pixels finos e cada pixel fino tem quatro amostras. Isso significa que cada pixel grosso grava em um total de 4 * 4 = 16 amostras.

### <a name="number-of-coverage-bits-needed"></a>Número de bits de cobertura necessários
A tabela a seguir indica quantos bits de cobertura são necessários para cada combinação de tamanho de pixel grosso e nível de MSAA.

![A tabela mostra o tamanho de pixel grosso, o número de pixels finos e M A um nível A.](images/NumberOfCoverageBits.PNG "Bits de cobertura")

Conforme indicado na tabela, não é possível usar pixels grossos para gravar mais de 16 amostras por vez usando o recurso de sombreamento de taxa variável exposto por meio do Direct3D 12. Essa restrição ocorre devido a restrições do Direct3D 12 sobre quais níveis de MSAA são permitidos com o tamanho de pixel grosso (consulte a tabela na seção [with VRS (sombreamento de taxa variável)](#with-variable-rate-shading-vrs) neste tópico).

### <a name="ordering-and-format-of-bits-in-the-coverage-mask"></a>Ordenação e formato de bits na máscara de cobertura
Os bits da máscara de cobertura aderem a uma ordem bem definida. A máscara consiste em coberturas de pixels da esquerda para a direita e, em seguida, da ordem superior para a inferior (coluna-principal). Os bits de cobertura são os bits de ordem inferior da semântica de cobertura e são condensados em conjunto.

A tabela a seguir mostra o formato de máscara de cobertura para combinações com suporte de tamanho de pixels e nível de MSAA.

![A tabela mostra um tamanho de pixel grosso, um diagrama de pixel grande e 1 x M S um bits de cobertura.](images/Coverage1x.PNG "Cobertura em 1x")

A tabela a seguir retrata 2x pixels de MSAA, em que cada pixel tem dois exemplos de índices 0 e 1.

O posicionamento dos rótulos de exemplos nos pixels é para fins ilustrativos e não transmite necessariamente os locais de exemplos {X, Y} de amostras nesse pixel; especialmente, Considerando que as posições de exemplo podem ser alteradas de forma programática. Os exemplos são referenciados por seu índice baseado em 0.

![A tabela mostra um tamanho de pixel grosso, um diagrama de pixel grande e 2 x M um bits de cobertura.](images/Coverage2x.PNG "Cobertura em 2x")

A tabela a seguir mostra 4x pixels de MSAA, em que cada pixel tem quatro amostras de índices 0, 1, 2 e 3.

![A tabela mostra um tamanho de pixel grosso, um diagrama de pixel grande e 4 x M S um bits de cobertura.](images/Coverage4x.PNG "Cobertura em 4x")

## <a name="discard"></a>Descartar
Quando a semântica HLSL `discard` é usada com sombreamento de pixel grosso, os pixels grossos são descartados.

## <a name="target-independent-rasterization-tir"></a>Rasterização independente de destino (TIR)
Não há suporte para TIR quando sombreamento de pixel grosso é usado.

## <a name="raster-order-views-rovs"></a>Exibições de ordem de rasterização (ROVs)
Os interbloqueios ROV são especificados como operando em granularidade de pixel fino. Se o sombreamento for executado por amostra, os interbloqueios estarão operando na granularidade de exemplo.

## <a name="conservative-rasterization"></a>Rasterização conservadora
Você pode usar a rasterização conservadora com sombreamento de taxa variável. Quando a rasterização conservadora é usada com sombreamento de pixel grosso, os pixels finos dentro de pixels grossos são rerasterizados de forma conservadora por meio da cobertura completa.

### <a name="coverage"></a>Cobertura
Quando a rasterização conservadora é usada, a semântica de cobertura contém máscaras completas para pixels finos que são abordados e 0 para pixels finos que não são cobertos.

## <a name="bundles"></a>Pacotes
Você pode chamar APIs de sombreamento de taxa variável em um pacote.

## <a name="render-passes"></a>Passagens de renderização
Você pode chamar APIs de sombreamento de taxa variável em uma [passagem de renderização](/windows/desktop/direct3d12/direct3d-12-render-passes).

## <a name="calling-the-vrs-apis"></a>Chamando as APIs VRS
Esta próxima seção descreve a maneira como o sombreamento de taxa variável é acessível para seu aplicativo por meio do Direct3D 12.

### <a name="capability-querying"></a>Consulta de funcionalidade

Para consultar o recurso de sombreamento de taxa variável do adaptador, chame [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) com [**D3D12_FEATURE::D 3D12_FEATURE_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)e forneça uma estrutura de [ **D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) para que a função seja preenchida para você. A estrutura de **D3D12_FEATURE_DATA_D3D12_OPTIONS6** contém vários membros, incluindo um que seja do tipo enumerado [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) (D3D12_FEATURE_DATA_D3D12_OPTIONS6:: VariableShadingRateTier) e outro que indica se há suporte para o processamento em segundo plano (D3D12_FEATURE_DATA_D3D12_OPTIONS6:: BackgroundProcessingSupported).

Para consultar o recurso de camada 1, por exemplo, você pode fazer isso.

```cpp
D3D12_FEATURE_DATA_D3D12_OPTIONS6 options;
return 
    SUCCEEDED(m_device->CheckFeatureSupport(
        D3D12_FEATURE_D3D12_OPTIONS6, 
        &options, 
        sizeof(options))) && 
    options.ShadingRateTier == D3D12_VARIABLE_SHADING_RATE_TIER_1;
```

### <a name="shading-rates"></a>Taxas de sombreamento

Os valores na enumeração [ **D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) são organizados de forma que as taxas de sombreamento sejam facilmente descombináveis em dois eixos, em que os valores de cada eixo são representados compactamente em um espaço logarítmica de acordo com a [enumeração **D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate).

Você pode criar uma macro para compor duas taxas de sombreamento de eixo em uma taxa de sombreamento como esta.

```cpp
#define D3D12_MAKE_COARSE_SHADING_RATE(x,y) ((x) << 2 | (y))
D3D12_MAKE_COARSE_SHADING_RATE(
    D3D12_AXIS_SHADING_RATE_2X, 
    D3D12_AXIS_SHADING_RATE_1X)
```

A plataforma também fornece essas macros, definidas em `d3d12.h` .

```cpp
#define D3D12_GET_COARSE_SHADING_RATE_X_AXIS(x) ((x) >> 2 )
#define D3D12_GET_COARSE_SHADING_RATE_Y_AXIS(y) ((y) & 3 )
```

Eles podem ser usados para dissecar e entender `SV_ShaderRate` .

> [!NOTE]
> Essa interpretação de dados é voltada para descrever a imagem de espaço na tela, que pode ser manipulada por sombreadores. Isso é abordado mais adiante nas seções acima. Mas não há motivo para não ter uma definição consistente dos tamanhos de pixel grossos a serem usados em todos os lugares, incluindo ao definir a taxa de sombreamento de nível de comando.

### <a name="setting-command-level-shading-rate-and-combiners"></a>Definindo taxas e combinadores de sombreamento de nível de comando
A taxa de sombreamento e, opcionalmente, os combinadores são especificados por meio do método [**ID3D12GraphicsCommandList5:: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate) . Você passa um valor [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) para a taxa de sombreamento base e uma matriz opcional de valores de [D3D12_SHADING_RATE_COMBINER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner) .

### <a name="preparing-the-screen-space-image"></a>Preparando a imagem de espaço na tela
O estado do recurso somente leitura que designa uma imagem de taxa de sombreamento utilizável é definido como [D3D12_RESOURCE_STATES::D 3D12_RESOURCE_STATE_SHADING_RATE_SOURCE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### <a name="setting-the-screen-space-image"></a>Configurando a imagem de espaço na tela
Você especifica a imagem de espaço de tela por meio do método [**ID3D12GraphicsCommandList5:: RSSetShadingRateImage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrateimage) .

```cpp
m_commandList->RSSetShadingRateImage(screenSpaceImage);
```

### <a name="querying-the-tile-size"></a>Consultando o tamanho do bloco
Você pode consultar o tamanho do bloco do membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS6:: ShadingRateImageTileSize**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) . Consulte as [consultas de funcionalidade](#capability-querying) acima.

Uma dimensão é recuperada, pois as dimensões horizontal e vertical são sempre as mesmas. Se o recurso do sistema for [**D3D12_SHADING_RATE_TIER_NOT_SUPPORTED**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier), o tamanho do bloco retornado será 0.
