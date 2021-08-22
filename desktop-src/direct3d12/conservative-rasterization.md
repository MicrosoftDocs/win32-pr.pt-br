---
title: Rasterização de Direct3D 12 conservador
description: A rasterização conservadora adiciona alguma certeza à renderização de pixels, que é útil em particular aos algoritmos de detecção de colisão.
ms.assetid: 081199AD-1702-4EC8-95AD-B1148C676199
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bb5893e944c5d495cf91fdb334bd6ab5f755b7f1e200648242cb46b281f695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045747"
---
# <a name="direct3d-12-conservative-rasterization"></a>Rasterização de Direct3D 12 conservador

A rasterização conservadora adiciona alguma certeza à renderização de pixels, que é útil em particular aos algoritmos de detecção de colisão.

-   [Visão geral](#overview)
-   [Interações com o pipeline](#interactions-with-the-pipeline)
    -   [Interação de regras de rasterização](#rasterization-rules-interaction)
    -   [Interação de multiamostrar](#multisampling-interaction)
    -   [Interação SampleMask](#samplemask-interaction)
    -   [Interação de teste de profundidade/estêncil](#depthstencil-test-interaction)
    -   [Interação do pixel do auxiliar](#helper-pixel-interaction)
    -   [Interação de cobertura de saída](#output-coverage-interaction)
    -   [Interação InputCoverage](#inputcoverage-interaction)
    -   [Interação InnerCoverage](#innercoverage-interaction)
    -   [Interação de interpolação de atributo](#attribute-interpolation-interaction)
    -   [Interação de recorte](#clipping-interaction)
    -   [Interação de distância do clipe](#clip-distance-interaction)
    -   [Interação de rasterização independente de destino](#target-independent-rasterization-interaction)
    -   [Interação da topologia primitiva de IA](#ia-primitive-topology-interaction)
    -   [Interação de consulta](#query-interaction)
    -   [Seleção de interação de estado](#cull-state-interaction)
    -   [Interação IsFrontFace](#isfrontface-interaction)
    -   [Interação dos modos de preenchimento](#fill-modes-interaction)
-   [Detalhes de implementação](#implementation-details)
-   [Resumo da API](#api-summary)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

A rasterização conservadora significa que todos os pixels que estão pelo menos parcialmente cobertos por um primitivo renderizado são rasterizados, o que significa que o sombreador de pixel é invocado. O comportamento normal é a amostragem, que não é usada se a rasterização conservadora estiver habilitada.

A rasterização conservadora é útil em várias situações, incluindo para ter certeza na detecção de colisão, na remoção de oclusão e na renderização de ladrilhos.

Por exemplo, a figura a seguir mostra um triângulo verde renderizado usando a rasterização conservadora, como apareceria no rasterizador (ou seja, usando as coordenadas de vértice de ponto fixo 16,8). A área Brown é conhecida como "região incerteza" – uma região conceitual que representa os limites estendidos do triângulo, necessários para garantir que o primitivo no rasterizador seja conservador em relação às coordenadas do vértice do ponto flutuante original. Os quadrados vermelhos em cada vértice mostram como a região de incertezas é calculada: como um quadrado removido.

Os quadrados cinzas grandes mostram os pixels que serão renderizados. Os quadrados rosa mostram pixels renderizados usando a "regra de cima para a esquerda", que entra em cena, pois a borda do triângulo cruza a borda dos pixels. Pode haver falsos positivos (conjunto de pixels que não deveriam ter sido) que o sistema normalmente, mas nem sempre irá fazer a seleção.

![a regra superior esquerda](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interações com o pipeline

### <a name="rasterization-rules-interaction"></a>Interação de regras de rasterização

No modo de rasterização conservadora, as regras de rasterização se aplicam da mesma maneira que quando o modo de rasterização conservador não está habilitado com exceções para a regra de Top-Left, descrita acima e cobertura de pixel. 16,8 a precisão do rasterizador Fixed-Point deve ser usada.

Pixels que não seriam abordados se o hardware estivesse usando coordenadas de vértice de ponto flutuante completo só pode ser incluído se estiverem dentro de uma região de incertezas que não tenham uma metade maior de um pixel no domínio de ponto fixo. Espera-se que o hardware futuro atinja a região de incertezas rígida especificada na camada 2. Observe que esse requisito impede que os triângulos prata estendam além do necessário.

Uma região de incerteza válida semelhante também se aplica a `InnerCoverage` , mas é mais rígida porque nenhuma implementação requer uma região de incerteza maior para esse caso. Consulte a [interação do InnerCoverage](#innercoverage-interaction) para obter mais detalhes.

As regiões de incerteza internas e externas devem ser maiores ou iguais ao tamanho da metade da grade de subpixel, ou 1/512 de um pixel, no domínio de ponto fixo. Esta é a região mínima de incerteza válida. 1/512 vem da representação de coordenada do rasterizador de ponto fixo 16,8 e a regra de ida e volta mais próxima que se aplica ao converter coordenadas de vértice de ponto flutuante para 16,8 coordenadas de ponto fixo. 1/512 poderá alterar se a precisão do rasterizador for alterada. Se uma implementação implementar essa região de incerteza mínima, ela deverá seguir a regra de Top-Left quando uma borda ou canto da região incerteza estiver ao longo da borda ou do canto de um pixel. As bordas recortadas da região incerteza devem ser tratadas como o vértice mais próximo, o que significa que ela conta como duas bordas: as duas que ingressam no vértice associado. Top-Left regra é necessária quando a região de incerteza mínima é usada porque, se não for, uma implementação de rasterização conservadora falhará ao rasterizar os pixels que poderiam ser cobertos quando o modo de rasterização conservador estiver desabilitado.

O diagrama a seguir ilustra uma região de incerteza externa válida produzida por meio da varredura de um quadrado em volta das bordas do primitivo no domínio de ponto fixo (ou seja, os vértices foram quantificados pela representação de ponto fixo 16,8). As dimensões desse quadrado se baseiam no tamanho de região de incerteza externa válido: para 1/2 de um pixel, o quadrado é de 1 pixel em largura e altura, para 1/512 de um pixel, o quadrado é 1/256 de um pixel em largura e altura. O triângulo verde representa um determinado primitivo, a linha vermelha pontilhada representa o limite na rasterização conservadora estimada, os quadrados pretos sólidos representam o quadrado removido ao longo das bordas primitivas e a área quadriculada azul é a região de incerteza externa:

![região de incerteza externa.](images/outercoverage.jpg)

### <a name="multisampling-interaction"></a>Interação de multiamostrar

Independentemente do número de amostras em superfícies **renderTarget** / **DepthStencil** (ou se o *ForcedSampleCount* está sendo usado ou não), todos os exemplos são cobertos por pixels rasterizados pela rasterização conservadora. Os locais de exemplo individuais não são testados para se eles se enquadram no primitivo ou não.

### <a name="samplemask-interaction"></a>Interação SampleMask

O estado do rasterizador *SampleMask* se aplica da mesma maneira que quando a rasterização conservadora não está habilitada para `InputCoverage` , mas não afeta `InnerCoverage` (ou seja, não está AND'ed em uma entrada declarada com `InnerCoverage` ). Isso ocorre porque `InnerCoverage` o não está relacionado a se os exemplos de MSAA são mascarados: 0 `InnerCoverage` apenas significa que não há garantia de que o pixel seja totalmente coberto, não que nenhum exemplo seja atualizado.

### <a name="depthstencil-test-interaction"></a>Interação de teste de profundidade/estêncil

O teste de profundidade/estêncil prossegue para um pixel com rasterização conservadora da mesma forma como se todas as amostras forem cobertas quando a rasterização conservadora não estiver habilitada.

Continuar com todos os exemplos cobertos pode causar extrapolação de profundidade, que é válida e deve ser clampedda ao visor, conforme especificado quando a rasterização conservadora não está habilitada. Isso é semelhante a quando os modos de interpolação de frequência de pixel são usados em um **renderTarget** com contagem de amostra maior que 1, embora no caso de uma rasterização conservadora, é o valor de profundidade que vai para o teste de profundidade de função fixa que pode ser extrapolado.

O comportamento de remoção de profundidade antecipada com extrapolação de profundidade é indefinido. Isso ocorre porque alguma profundidade antecipada que escolhe o hardware não pode dar suporte adequado a valores de profundidade extrapolados. No entanto, o comportamento de remoção de profundidade antecipada na presença da extrapolação de profundidade é problemática até mesmo com hardware que pode dar suporte a valores de profundidade extrapolados. Esse problema pode ser solucionado por fixação MSS a profundidade de entrada do sombreador de pixel para os valores de profundidade mín. e máx. do primitivo que está sendo rasterizado e grava esse valor em `oDepth` (o registro de profundidade de saída do sombreador de pixel). As implementações são necessárias para desabilitar a remoção de profundidade inicial nesse caso, devido à `oDepth` gravação.

### <a name="helper-pixel-interaction"></a>Interação do pixel do auxiliar

As regras de pixel do auxiliar se aplicam da mesma maneira que quando a rasterização conservadora não está habilitada. Como parte disso, todos os pixels, incluindo os pixels auxiliares, devem relatar `InputCoverage` precisamente conforme especificado na `InputCoverage` seção de interação. Portanto, os pixels totalmente não cobertos pelo relatório 0 de cobertura.

### <a name="output-coverage-interaction"></a>Interação de cobertura de saída

A cobertura de saída ( `oMask` ) se comporta para um pixel com rasterização conservadora como faz quando a rasterização conservadora não está habilitada com todos os exemplos cobertos.

### <a name="inputcoverage-interaction"></a>Interação InputCoverage

No modo de rasterização conservador, esse registro de entrada é preenchido como se todas as amostras forem cobertas quando a rasterização conservadora não estiver habilitada para um determinado pixel rasterizado conservadoramente. Isso significa que todas as interações existentes se aplicam (por exemplo, *SampleMask* é aplicado) e os primeiros n bits de `InputCoverage` de LSB são definidos como 1 para um pixel com rasterização conservadora, dada uma amostra n por pixel **renderTarget** e/ou **DepthStencil** buffer associado na **fusão de saída** ou um *ForcedSampleCount* de exemplo n. O restante dos bits é 0.

Essa entrada está disponível em um sombreador independentemente do uso de uma rasterização conservadora, embora a rasterização conservadora altere seu comportamento para mostrar apenas todos os exemplos cobertos (ou nenhum para pixels auxiliares).

### <a name="innercoverage-interaction"></a>Interação InnerCoverage

Esse recurso é exigido pelo, e só está disponível no, camada 3. O tempo de execução falhará na criação de sombreador para sombreadores que usam esse modo quando uma implementação dá suporte a uma camada menor que a camada 3.

O sombreador de pixel tem um sistema inteiro escalar de 32 bits que gera o valor disponível: `InnerCoverage` . Esse é um campo de bits que tem um bit 0 do LSB definido como 1 para um determinado pixel rasterizado conservadoramente, somente quando esse pixel tem a garantia de estar inteiramente dentro do primitivo atual. Todos os outros bits de registro de entrada devem ser definidos como 0 quando o bit 0 não está definido, mas não é definido quando o bit 0 é definido como 1 (essencialmente, esse campo de bits representa um valor booliano em que false deve ser exatamente 0, mas true pode ser um valor diferente de zero (ou seja, 0)). Essa entrada é usada para informações de rasterização conservadora subestimadas. Ele informa o sombreador de pixel se o pixel atual está completamente dentro da geometria.

Isso deve considerar o erro de encaixe em resoluções maiores ou iguais à resolução na qual o empate atual está operando. Não deve haver falsos positivos (Configurando `InnerCoverage` bits quando o pixel não é totalmente coberto para qualquer erro de encaixe em resoluções maiores ou iguais à resolução na qual o empate atual está operando), mas falsos negativos são permitidos. Em resumo, a implementação não deve identificar incorretamente os pixels como totalmente cobertos que não seriam com coordenadas completas de vértice de ponto flutuante no rasterizador.

Os pixels que seriam totalmente cobertos se o hardware estivesse usando coordenadas de vértice de ponto flutuante completo só podem ser omitidos se interceptarem a região de incerteza interna, que não deve ser maior que o tamanho da grade de subpixel ou 1/256 de um pixel no domínio de ponto fixo. Dito outra forma, os pixels totalmente dentro do limite interno da região de incerteza interna devem ser marcados como totalmente cobertos. O limite interno da região incerteza é ilustrado no diagrama abaixo da linha pontilhada preta em negrito. 1/256 vem da representação de coordenada do rasterizador de ponto fixo 16,8, que pode ser alterada se a precisão do rasterizador for alterada. Essa região de incerteza é suficiente para considerar o erro de ajuste causado pela conversão de coordenadas de vértice de ponto flutuante para coordenadas de vértice de ponto fixo no rasterizador.

Os mesmos requisitos de região de incerteza mínima de 1/512 definidos na interação de regras de rasterização também se aplicam aqui.

O diagrama a seguir ilustra uma região de incerteza interna válida produzida por meio da varredura de um quadrado em volta das bordas do primitivo no domínio de ponto fixo (ou seja, os vértices foram quantificados pela representação de ponto fixo 16,8). As dimensões desse quadrado se baseiam no tamanho de região de incerteza interna válido: para 1/256 de um pixel, o quadrado é 1/128 de um pixel em largura e altura. O triângulo verde representa um determinado primitivo, a linha pontilhada preta em negrito representa o limite da região de incerteza interna, os quadrados pretos sólidos representam o quadrado removidodo ao longo das bordas primitivas, e a área quadriculada laranja é a região de incerteza interna:

![incerteza interna reqion.](images/innercoverage.jpg)

O uso de não `InnerCoverage` afeta se um pixel é rasterizado de forma conservadora, ou seja, usar um desses `InputCoverage` modos não afeta quais pixels são rasterizados quando o modo de rasterização conservador está habilitado. Portanto, quando `InnerCoverage` é usado e o sombreador de pixel está processando um pixel que não é totalmente coberto pela geometria, seu valor será 0, mas a invocação do sombreador de pixel terá amostras atualizadas. Isso é diferente de quando `InputCoverage` é 0, o que significa que nenhuma amostra será atualizada.

Esta entrada é mutuamente exclusiva com `InputCoverage` : as duas não podem ser usadas.

Para acessar `InnerCoverage` o, ele deve ser declarado como um único componente de um dos registros de entrada do sombreador de pixel. O modo de interpolação na declaração deve ser constante (interpolação não se aplica).

O `InnerCoverage` campo de bits não é afetado por testes de profundidade/estêncil, nem ANDed com o estado do rasterizador *SampleMask* .

Essa entrada só é válida no modo de rasterização conservadora. Quando a rasterização conservadora não está habilitada, `InnerCoverage` o produz um valor indefinido.

Invocações de sombreador de pixel causadas pela necessidade de pixels auxiliares, mas de outra forma não cobertas pelo primitivo, devem ter o `InnerCoverage` registro definido como 0.

### <a name="attribute-interpolation-interaction"></a>Interação de interpolação de atributo

Os modos de interpolação de atributo são inalterados e prosseguem da mesma maneira que quando a rasterização conservadora não está habilitada, onde os vértices de escala de visor e de ponto fixo são usados. Como todos os exemplos em um pixel rasterizado conservadormente são considerados cobertos, é válido que os valores sejam extrapolados, semelhante a quando os modos de interpolação de frequência de pixels são usados em um **renderTarget** com contagem de exemplo maior que 1. Os modos de interpolação de centróide produzem resultados idênticos ao modo de interpolação não-centróide correspondente; a noção de centróide não faz sentido nesse cenário, em que a cobertura de amostra é apenas completa ou 0.

A rasterização conservadora permite que triângulos de degeneração gerem invocações de sombreador de pixel, portanto, os triângulos de degeneração devem usar os valores atribuídos ao vértice 0 para todos os valores interpolados.

### <a name="clipping-interaction"></a>Interação de recorte

Quando o modo de rasterização conservador estiver habilitado e o clipe de profundidade estiver desabilitado (quando o estado do rasterizador *DepthClipEnable* for definido como false), pode haver variações na interpolação de atributo para segmentos de um primitivo que se enquadram fora do intervalo de 0 <= z <= w, dependendo da implementação: os valores constantes são usados de um ponto em que a primitiva intersecciona o plano relevante (próximo ou longe) ou a interpolação de atributo se comporta como quando o modo de rasterização conservador está desabilitado. No entanto, o comportamento do valor de profundidade é o mesmo, independentemente do modo de rasterização conservador, ou seja, primitivos que se enquadram fora do intervalo de profundidade ainda devem receber o valor do limite mais próximo do intervalo de profundidade do visor. O comportamento de interpolação de atributo dentro do intervalo de 0 <= z <= w deve permanecer inalterado.

### <a name="clip-distance-interaction"></a>Interação de distância do clipe

A distância do clipe é válida quando o modo de rasterização conservador está habilitado e se comporta para um pixel com rasterização conservadora como faz quando a rasterização conservadora não está habilitada com todos os exemplos cobertos.

Observe que a rasterização conservadora pode causar extrapolação da coordenada de vértice W, o que pode causar W <= 0. Isso pode fazer com que as implementações de distância de clipe por pixel operem em uma distância de clipe que tenha sido uma perspectiva dividida por um valor W inválido. As implementações de distância do clipe devem se proteger contra invocação de rasterização para pixels em que a coordenada de vértice W <= 0 (por exemplo, devido à extrapolação quando estiver no modo de rasterização conservador).

### <a name="target-independent-rasterization-interaction"></a>Interação de rasterização independente de destino

O modo de rasterização conservador é compatível com a TIR (rasterização independente de destino). Regras e restrições do TIR se aplicam, comportando um pixel conservadormente rasterizado como se todas as amostras forem cobertas.

### <a name="ia-primitive-topology-interaction"></a>Interação da topologia primitiva de IA

A rasterização conservadora não está definida para primitivos de linha ou de ponto. Portanto, as topologias primitivas que especificam pontos ou linhas produzem um comportamento indefinido se forem alimentadas para a unidade rasterizadora quando a rasterização conservadora estiver habilitada.

A validação da camada de depuração verifica se os aplicativos não usam essas topologias primitivas.

### <a name="query-interaction"></a>Interação de consulta

Para um pixel rasterizado conservadormente, as consultas se comportam como fazem quando a rasterização conservadora não é habilitada quando todas as amostras são cobertas. Por exemplo, para um pixel rasterizado conservadormente, o \_ \_ tipo de consulta D3D12 \_ oclusão e D3D12 \_ tipo de consulta as \_ \_ \_ Estatísticas de pipeline (de [**D3D12 \_ \_ tipo de consulta**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)) devem se comportar como seriam quando a rasterização conservadora não está habilitada quando todas as amostras são cobertas.

As invocações do sombreador de pixel devem ser incrementadas para cada pixel com rasterização conservadora no modo de rasterização conservador.

### <a name="cull-state-interaction"></a>Seleção de interação de estado

Todos os Estados de seleção são válidos no modo de rasterização conservadora e seguem as mesmas regras que quando a rasterização conservadora não está habilitada.

Ao comparar a rasterização conservadora entre as resoluções para si mesma ou sem a rasterização conservadora habilitada, há a possibilidade de que alguns primitivos tenham uma certa incompatibilidade (ou seja, um voltado para frente, o outro front voltado). Os aplicativos podem evitar essa incerteza usando \_ \_ o modo \_ de seleção D3D12 nenhum (do [**\_ \_ modo de seleção D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)) e não usando o `IsFrontFace` valor gerado pelo sistema.

### <a name="isfrontface-interaction"></a>Interação IsFrontFace

O `IsFrontFace` valor gerado pelo sistema é válido para ser usado no modo de rasterização conservador e segue o comportamento definido quando a rasterização conservadora não está habilitada.

### <a name="fill-modes-interaction"></a>Interação dos modos de preenchimento

O único [**modo de \_ preenchimento \_ de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) válido para rasterização conservadora é D3D12 \_ preenchimento \_ sólido, qualquer outro modo de preenchimento é um parâmetro inválido para o estado do rasterizador.

Isso ocorre porque a especificação funcional D3D12 especifica que o modo de preenchimento de wireframe deve converter bordas de triângulo em linhas e seguir as regras de rasterização de linha e o comportamento de rasterização de linha conservador não foi definido.

## <a name="implementation-details"></a>Detalhes de implementação

O tipo de rasterização com suporte no Direct3D 12 é às vezes chamado de "rasterização conservadora estimada". Também há o conceito de "rasterização conservadora subestimada", o que significa que apenas os pixels totalmente cobertos por um primitivo renderizado são rasterizados. As informações de rasterização conservadora subestimadas estão disponíveis por meio do sombreador de pixel através do uso de dados de cobertura de entrada e apenas a rasterização conservadora Sobreestimada está disponível como um modo de rasterização.

Se qualquer parte de um primitivo sobrepuser um pixel, esse pixel será considerado coberto e, em seguida, será rasterizado. Quando uma borda ou canto de um primitivo cai ao longo da borda ou do canto de um pixel, o aplicativo da "regra de cima para a esquerda" é específico da implementação. No entanto, para implementações que dão suporte a triângulos de degeneração, um triângulo degenerado ao longo de uma borda ou canto deve abranger pelo menos um pixel.

Implementações de rasterização conservadoras podem variar em hardwares diferentes e produzir falsos positivos, o que significa que eles podem decidir incorretamente que os pixels são cobertos. Isso pode ocorrer devido a detalhes específicos da implementação, como erros primitivos de crescimento ou encaixe inerentes às coordenadas de vértice de ponto fixo usadas na rasterização. O motivo pelo qual falsos positivos (em relação às coordenadas de vértice de ponto fixo) é válido porque alguns falsos positivos são necessários para permitir que uma implementação faça a avaliação de cobertura em vértices de postagem (ou seja, coordenadas de vértice que foram convertidas do ponto flutuante para o ponto fixo 16,8 usado no rasterizador), mas obedeça a cobertura produzida pelas coordenadas originais do vértice do ponto flutuante

Implementações de rasterização conservadoras não produzem falsos negativos em relação às coordenadas de vértice de ponto flutuante para primitivos post-snap não degenerados: se qualquer parte de um primitivo sobrepuser qualquer parte de um pixel, esse pixel será rasterizado.

Triângulos que são degenerados (índices duplicados em um buffer de índice ou colineares em 3D) ou tornam-se degenerados após a conversão de ponto fixo (vértices de colineares no rasterizador), pode ou não ser possível fazer a remoção; Ambos são comportamentos válidos. Os triângulos de degeneração devem ser considerados voltados, portanto, se um comportamento específico for exigido por um aplicativo, ele poderá usar a remoção ou teste de face para frente. Os triângulos de degeneração usam os valores atribuídos ao vértice 0 para todos os valores interpolados.

Há três camadas de suporte a hardware, além da possibilidade de que o hardware não ofereça suporte a esse recurso.

-   A camada 1 impõe uma região máxima de incerteza de 1/2 pixels e não oferece suporte a degerações de pós-snap. Isso é bom para a renderização de ladrilho, um Atlas de textura, geração de mapa claro e mapas de sombra de subpixel.
-   A camada 2 reduz a região de incerteza máxima para 1/256 e exige que as congerações após o encaixe não sejam reescolhedas. Essa camada é útil para a aceleração de algoritmos baseada em CPU (como voxelization).
-   A camada 3 mantém uma região de incerteza máxima de 1/256 e adiciona suporte para cobertura de entrada interna. Cobertura de entrada interna adiciona o novo valor `SV_InnerCoverage` à HLSL (linguagem de sombreamento de alto nível). Este é um inteiro escalar de 32 bits que pode ser especificado na entrada para um sombreador de pixel e representa as informações de rasterização conservadora subestimadas (ou seja, se um pixel é garantido para ser totalmente coberto). Essa camada é útil para a remoção de oclusão.

## <a name="api-summary"></a>Resumo da API

Os seguintes métodos, estruturas, enumerações e classes auxiliares referenciam a rasterização conservadora:

-   [**D3D12 \_ Rerasterizador \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) : estrutura que contém a descrição do rasterizador.
-   [**D3D12 \_ \_ \_ Modo de rasterização conservador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) : valores de enumeração para o modo (ativado ou desativado).
-   [**D3D12 \_ \_Opções de \_ D3D12 \_ de dados de recurso**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : estrutura que mantém a camada de suporte.
-   [**D3D12 \_ \_ \_ Camada de rasterização conservadora**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier) : valores de enumeração para cada camada de suporte pelo hardware.
-   [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : método para acessar os recursos com suporte.
-   [**CD3DX12 \_ Classe do RASTERIZAdor \_ desc**](cd3dx12-rasterizer-desc.md) : Helper para criar descrições do rasterizador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tutoriais de vídeo do DirectX Advanced Learning: rasterização conservadora](https://www.youtube.com/watch?v=zL0oSY_YmDY)
</dt> <dt>

[Modos de exibição ordenados do rasterizador](rasterizer-order-views.md)
</dt> <dt>

[Renderização](rendering.md)
</dt> </dl>

 

 




