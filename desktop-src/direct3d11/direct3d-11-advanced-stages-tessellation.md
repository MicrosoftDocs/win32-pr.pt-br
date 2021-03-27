---
title: Estágios de mosaico
description: O tempo de execução do Direct3D 11 dá suporte a três novos estágios que implementam mosaico, que converte as superfícies de subdivisão de detalhe baixo em primitivos de detalhes mais altos na GPU.
ms.assetid: 4ad2fd3e-6e1a-4326-8469-3198acf931dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aacb48ccc2c95ab93ba4f34212e654880d9a369
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2020
ms.locfileid: "104294569"
---
# <a name="tessellation-stages"></a>Estágios de mosaico

O tempo de execução do Direct3D 11 dá suporte a três novos estágios que implementam mosaico, que converte as superfícies de subdivisão de detalhe baixo em primitivos de detalhes mais altos na GPU. O bloco de mosaico organiza (ou decompõe) as superfícies de ordem superior em estruturas adequadas para renderização.

Implementando o mosaico no hardware, um pipeline gráfico pode avaliar modelos com menos detalhes (contagem inferior de polígonos) e renderizar em maiores detalhes. Embora o mosaico de software possa ser feito, o mosaico implementado por hardware pode gerar uma quantidade incrível de detalhes visuais (incluindo suporte para o mapeamento de deslocamento) sem adicionar os detalhes visuais aos tamanhos de modelo e paralisar as taxas de atualização.

-   [Benefícios do mosaico](#tessellation-benefits)
-   [Novos estágios de pipeline](#new-pipeline-stages)
    -   [Estágio envoltória-Shader](#hull-shader-stage)
    -   [Estágio Tessellator](#tessellator-stage)
    -   [Estágio de sombreador de domínio](#domain-shader-stage)
-   [APIs para inicializar estágios de mosaico](#apis-for-initializing-tessellation-stages)
-   [Como:](#how-tos)
-   [Tópicos relacionados](#related-topics)

## <a name="tessellation-benefits"></a>Benefícios do mosaico

Mosaico

-   Economiza muita memória e largura de banda, o que permite que um aplicativo processe superfícies detalhadas mais altas de modelos de baixa resolução. A técnica de mosaico implementada no pipeline do Direct3D 11 também dá suporte ao mapeamento de deslocamento, que pode produzir quantidades impressionantes de detalhes da superfície.
-   Dá suporte a técnicas de renderização escalonável, como níveis de detalhes contínuos ou de exibição, que podem ser calculados em tempo real.
-   Melhora o desempenho executando computações caras a uma frequência mais baixa (fazendo cálculos em um modelo de detalhes mais baixos). Isso pode incluir a mesclagem de cálculos usando formas de mesclagem ou destinos que mudam de forma para uma animação mais realista ou cálculos de física para a detecção de colisão ou dinâmica de corpo virtual.

O pipeline do Direct3D 11 implementa o mosaico no hardware, que descarrega o trabalho da CPU para a GPU. Isso pode levar a melhorias de desempenho muito grandes se um aplicativo implementar um grande número de destinos que mudam de forma e/ou modelos de aplicação de capas/deformação mais sofisticados. Para acessar os novos recursos de mosaico, você deve aprender sobre alguns estágios de pipeline novos.

## <a name="new-pipeline-stages"></a>Novos estágios de pipeline

O mosaico usa a GPU para calcular uma superfície mais detalhada de uma superfície construída a partir de patches de quadrupleto, patches de triângulo ou isolines. Para aproximar a superfície de ordem superior, cada patch é subdividido em triângulos, pontos ou linhas usando fatores de mosaico. O pipeline do Direct3D 11 implementa o mosaico usando três novos estágios de pipeline:

-   [Envoltória-Shader Stage](#hull-shader-stage) – um estágio programável do sombreador que produz um patch Geometry (e constantes de patch) que correspondem a cada patch de entrada (quad, triângulo ou linha).
-   [Estágio Tessellator](#tessellator-stage) – um estágio de pipeline de função fixa que cria um padrão de amostragem do domínio que representa o patch Geometry e gera um conjunto de objetos menores (triângulos, pontos ou linhas) que conectam esses exemplos.
-   [Estágio de sombreador de domínio](#domain-shader-stage) – um estágio de sombreador programável que calcula a posição do vértice que corresponde a cada exemplo de domínio.

O diagrama a seguir realça os novos estágios do pipeline do Direct3D 11.

![diagrama do pipeline do direct3d 11 que destaca os estágios do sombreador de domínio, sombreadores hull e mosaico](images/d3d11-pipeline-stages-tessellation.png)

O diagrama a seguir mostra o progresso por meio dos estágios de mosaico. A progressão começa com a superfície subdividida em poucos detalhes. A progressão a seguir destaca o patch de entrada com o patch de geometria correspondente, amostras de domínio, e triângulos que conectam essas amostras. Por fim, a progressão destaca os vértices que correspondem a essas amostras.

![diagrama da progressão de mosaico](images/tess-prog.png)

### <a name="hull-shader-stage"></a>Estágio de Hull-Shader

Um sombreador envoltória, que é invocado uma vez por patch, transforma os pontos de controle de entrada que definem uma superfície de ordem inferior em pontos de controle que compõem um patch. Ele também faz alguns cálculos por patch para fornecer dados para o estágio de mosaico e o estágio de domínio. No nível mais simples da caixa preta, o estágio envoltória-Shader seria semelhante ao diagrama a seguir.

![diagrama da fase de sombreadores hull](images/d3d11-hull-shader.png)

Um sombreador envoltória é implementado com uma função HLSL e tem as seguintes propriedades:

-   A entrada do sombreador está entre 1 e 32 pontos de controle.
-   A saída do sombreador é entre 1 e 32 pontos de controle, independentemente do número de fatores de mosaico. Os pontos de controle de saída de um sombreador hull podem ser consumidos pelo estágio do sombreador de domínio. Os dados constantes de patch podem ser consumidos por um sombreador de domínio; fatores de mosaico podem ser consumidos pelo sombreador de domínio e pelo estágio de mosaico.
-   Os fatores de mosaico determinam quanto subdividir cada patch.
-   O sombreador declara o estado exigido pelo estágio Tessellator. Isso inclui informações como o número de pontos de controle, o tipo da face do patch e o tipo de particionamento a ser usado durante a criação do mosaico. Essas informações são exibidas como declarações normalmente na frente do código do sombreador.
-   Se o estágio envoltória-Shader definir qualquer fator de mosaico de borda como = 0 ou NaN, o patch será acrescentado. Como resultado, o estágio de mosaico pode ou não ser executado, o sombreador de domínio não será executado e nenhuma saída visível será produzida para esse patch.

Em um nível mais profundo, um envoltória-Shader realmente opera em duas fases: uma fase de ponto de controle e uma fase de constante de patch, que são executados em paralelo pelo hardware. O compilador HLSL extrai o paralelismo em um sombreador hull e o codifica em código de bytes que orienta o hardware.

-   A fase de ponto de controle opera uma vez para cada ponto de controle, lendo os pontos de controle para um patch e gerando um ponto de controle de saída (identificado por um ControlPointID).
-   A fase de patch constante opera uma vez por patch para gerar fatores de mosaico de borda e outras constantes por patch. Internamente, muitas fases de constante de patch podem ser executadas ao mesmo tempo. A fase de patch constante tem acesso somente leitura a todos os pontos de controle de entrada e saída.

Aqui está um exemplo de um sombreador envoltória:


```
[patchsize(12)]
[patchconstantfunc(MyPatchConstantFunc)]
MyOutPoint main(uint Id : SV_ControlPointID,
     InputPatch<MyInPoint, 12> InPts)
{
     MyOutPoint result;
     
     ...
     
     result = TransformControlPoint( InPts[Id] );

     return result;
}
```



Para obter um exemplo que cria um sombreador envoltória, consulte [como: criar um sombreador envoltória](direct3d-11-advanced-stages-hull-shader-create.md).

### <a name="tessellator-stage"></a>Estágio Tessellator

O Tessellator é um estágio de função fixa inicializado ligando um sombreador envoltória ao pipeline (consulte [como: inicializar o estágio Tessellator](direct3d-11-advanced-stages-tessellator-initialize.md)). O objetivo do estágio de mosaico é subdividir um domínio (quad, tri ou linha) em muitos objetos menores (triângulos, pontos ou linhas). O mosaico organiza um domínio canônico em um sistema de coordenadas normalizado (zero-para-um). Por exemplo, um domínio quadrupleto é transformado em um quadrado de unidade.

O mosaico opera uma vez por patch usando os fatores de mosaico (que especificam o quão delicadamente o domínio será transformado em mosaico) e o tipo de particionamento (que especifica o algoritmo usado para dividir um patch) que são transmitidos do estágio de sombreador hull. O mosaico gera coordenadas uv (e, opcionalmente, w) e a topologia de superfície para o estágio do sombreador de domínio.

Internamente, o Tessellator opera em duas fases:

-   A primeira fase processa os fatores de mosaico, corrigindo problemas de arredondamento, manipulando fatores muito pequenos, reduzindo e combinando fatores, usar aritmética de ponto flutuante de 32 bits.
-   A segunda fase gera listas de pontos ou topologias com base no tipo de particionamento selecionado. Isso é a tarefa principal do estágio de mosaico e usa frações de 16 bits com aritmética de ponto fixo. A aritmética de ponto fixo permite a aceleração de hardware, mantendo a precisão aceitável. Por exemplo, dado um patch com 64 metros de largura, essa precisão pode colocar pontos em uma resolução de 2 mm.



| Tipo de particionamento | Intervalo                       |
|----------------------|-----------------------------|
| ímpar fracionário \_      | \[1... 63\]                  |
| fracionário \_ mesmo     | Intervalo de TessFactor: \[ 2.. 64\] |
| inteiro              | Intervalo de TessFactor: \[ 1.. 64\] |
| pow2                 | Intervalo de TessFactor: \[ 1.. 64\] |



 

### <a name="domain-shader-stage"></a>Estágio de Domain-Shader

Um sombreador de domínio calcula a posição de vértice de um ponto de subdivisão no patch de saída. Um sombreador de domínio é executado uma vez por ponto de saída de estágio Tessellator e tem acesso somente leitura às coordenadas UV de saída de estágio Tessellator, o patch de saída do sombreador envoltória e as constantes de patch de saída do sombreador envoltória, como mostra o diagrama a seguir.

![diagrama do estágio do sombreador de domínio](images/d3d11-domain-shader.png)

As propriedades do sombreador de domínio incluem:

-   Um sombreador de domínio é invocado uma vez por coordenada de saída do estágio Tessellator.
-   Um sombreador de domínio consome pontos de controle de saída do estágio envoltória-Shader.
-   Um sombreador de domínio gera a posição de um vértice.
-   As entradas são as saídas do sombreador envoltória, incluindo pontos de controle, dados constantes de patch e fatores de mosaico. Os fatores de mosaico podem incluir os valores usados pela função fixa Tessellator, bem como os valores brutos (antes de arredondar por mosaico inteiro, por exemplo), que facilita a sobremetamorfoseação, por exemplo.

Depois que o sombreador de domínio for concluído, o mosaico será concluído e os dados do pipeline continuarão no próximo estágio do pipeline (sombreador de geometria, pixel shader, etc.). Um sombreador de geometria que espera primitivos com adjacência (por exemplo, 6 vértices por triângulo) não é válido quando mosaico está ativo (isso resulta em um comportamento indefinido, sobre o qual a camada de depuração emitirá um aviso).

Aqui está um exemplo de um sombreador de domínio:


```
void main( out    MyDSOutput result, 
           float2 myInputUV : SV_DomainPoint, 
           MyDSInput DSInputs,
           OutputPatch<MyOutPoint, 12> ControlPts, 
           MyTessFactors tessFactors)
{
     ...

     result.Position = EvaluateSurfaceUV(ControlPoints, myInputUV);
}
```



## <a name="apis-for-initializing-tessellation-stages"></a>APIs para inicializar estágios de mosaico

O mosaico é implementado com dois novos estágios programáveis de sombreador: um sombreador envoltória e um sombreador de domínio. Esses novos estágios de sombreador são programados com o código HLSL definido no sombreador modelo 5. Os novos destinos do sombreador são: HS \_ 5 \_ 0 e DS \_ 5 \_ 0. Como todos os estágios programáveis do sombreador, o código para o hardware é extraído dos sombreadores compilados passados para o tempo de execução quando os sombreadores são vinculados ao pipeline usando APIs como [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) e [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader). Mas primeiro, o sombreador deve ser criado usando APIs como [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) e [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).

Habilite o mosaico criando um sombreador hull e vinculando-o ao estágio de sombreador hull (isso configura automaticamente o estágio de mosaico). Para gerar as posições de vértice final dos patches de mosaico, você também precisará criar um sombreador domínio e associá-lo ao estágio do sombreador de domínio. Quando o mosaico está habilitado, a entrada de dados para o estágio de entrada-Assembler deve ser dados de patch. Ou seja, a topologia do montador de entrada deve ser uma topologia constante de patch do conjunto de [**\_ \_ topologias primitivos D3D11**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) com [**IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology).

Para desabilitar o mosaico, defina os sombreadores hull e o sombreador de domínio **NULL**. Nem o estágio Geometry-Shader nem o estágio Stream-output podem ler pontos de controle de saída envoltória-Shader ou dados de patch.

-   Novas topologias para o estágio de entrada-Assembler, que são extensões para essa enumeração.

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    A topologia é definida para o estágio de Assembler de entrada usando [ **IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

-   É claro que os novos estágios programáveis do sombreador exigem que outro Estado seja definido, para associar buffers constantes, exemplos e recursos de sombreador aos estágios de pipeline apropriados. Esses novos métodos ID3D11Device são implementados para definir esse estado.
    -   [**DSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetconstantbuffers)
    -   [**DSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetsamplers)
    -   [**DSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshader)
    -   [**DSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshaderresources)
    -   [**DSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetconstantbuffers)
    -   [**DSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetsamplers)
    -   [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader)
    -   [**DSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshaderresources)
    -   [**HSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetconstantbuffers)
    -   [**HSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshaderresources)
    -   [**HSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetsamplers)
    -   [**HSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshader)
    -   [**HSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetconstantbuffers)
    -   [**HSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetsamplers)
    -   [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)
    -   [**HSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshaderresources)

## <a name="how-tos"></a>Como:

A documentação também contém exemplos para inicializar os estágios de mosaico.



| Item                                                                                                                                                                                                                                                                                           | Descrição                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[Como: criar um sombreador envoltória](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                                     | Criar um sombreador envoltória.<br/>              |
| <span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[Como criar um sombreador envoltória](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                                     | Criar um sombreador envoltória.<br/>              |
| <span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[Como inicializar o estágio Tessellator](direct3d-11-advanced-stages-tessellator-initialize.md)<br/> | Inicialize o estágio de mosaico.<br/> |
| <span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[Como: criar um sombreador de domínio](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                                           | Crie um sombreador de domínio.<br/>            |
| <span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[Como criar um sombreador de domínio](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                                           | Crie um sombreador de domínio.<br/>            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 

