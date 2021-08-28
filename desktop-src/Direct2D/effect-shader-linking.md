---
title: Vinculação de Sombreador de Efeito
description: Direct2D usa uma otimização chamada vinculação de sombreador de efeito que combina vários efeitos que a renderização de gráfico passa para uma única passagem.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22d9ae245b5bbaa0c13dd7d5296dc419f740404
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881824"
---
# <a name="effect-shader-linking"></a>Vinculação de Sombreador de Efeito

Direct2D usa uma otimização chamada vinculação de sombreador de efeito que combina vários efeitos que a renderização de gráfico passa para uma única passagem.

-   [Visão geral da vinculação de sombreador de efeito](#overview-of-effect-shader-linking)
-   [Usando vinculação de sombreador de efeito](#using-effect-shader-linking)
-   [Criando um efeito personalizado compatível com vinculação de sombreador](#authoring-a-shader-linking-compatible-custom-effect)
-   [Sombreador de efeito de exemplo compatível com vinculação](#example-linking-compatible-effect-shader)
-   [Compilando um sombreador compatível com vinculação](#compiling-a-linking-compatible-shader)
    -   [Etapa 1: compilar a função de exportação](#step-1-compile-the-export-function)
    -   [Etapa 2: compilar o sombreador completo e inserir a função de exportação](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [Exportar especificações de função](#export-function-specifications)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-effect-shader-linking"></a>Visão geral da vinculação de sombreador de efeito

O efeito que as otimizações de vinculação do sombreador se baseia na vinculação do sombreador HLSL, um recurso do Direct3D 11,2 que permite que os sombreadores de pixel e vértice sejam gerados em tempo de execução por meio da vinculação de funções de sombreador pré-compilados. As figuras a seguir ilustram o conceito de vinculação de sombreador de efeito em um grafo de efeito. a primeira figura mostra um grafo de efeito de Direct2D típico com quatro transformações de renderização. Sem vinculação de sombreador, cada transformação consome uma passagem de renderização e requer uma superfície intermediária; no total, esse grafo requer 4 passagens e 3 intermediários.

![transformação de grafo sem vinculação de sombreador: 4 passagens e 3 intermediários.](images/shader-transform-graph.png)

A segunda figura mostra o mesmo grafo de efeito em que cada transformação de renderização foi substituída por uma versão de função vinculável. Direct2D é capaz de vincular todo o grafo e executá-lo em uma passagem sem exigir nenhum intermediário. Isso pode proporcionar uma diminuição significativa no tempo de execução da GPU e na redução do consumo máximo de memória da GPU.

![Grafo de transformação com vinculação de sombreador: 1 passagem, 0 intermediários.](images/shader-linking-graph.png)



 

A vinculação do sombreador de efeito opera em transformações individuais dentro de um efeito; Isso significa que até mesmo um grafo com um único efeito pode se beneficiar da vinculação de sombreador se esse efeito tiver várias transformações válidas.

## <a name="using-effect-shader-linking"></a>Usando vinculação de sombreador de efeito

se você estiver criando um aplicativo de Direct2D que usa efeitos, não precisará fazer nada para tirar proveito da vinculação de sombreador de efeito. Direct2D analisa automaticamente o grafo de efeito para determinar a maneira mais adequada de vincular cada transformação.

Os autores de efeito são responsáveis por implementar seu efeito de forma que dê suporte à vinculação de sombreador de efeito; para obter mais informações, consulte a seção [criando um efeito personalizado compatível com vinculação de sombreador](#authoring-a-shader-linking-compatible-custom-effect) abaixo. Todos os efeitos internos dão suporte à vinculação de sombreador.

Direct2D só vinculará as transformações de renderização adjacentes em situações em que é benéfico. Leva em consideração vários fatores ao determinar se deve vincular duas transformações. Por exemplo, a vinculação de sombreador não é executada se uma das transformações usa um vértice ou sombreadores de computação, pois somente os sombreadores de pixel podem ser vinculados. Além disso, se um efeito não foi criado para ser compatível com a vinculação de sombreador, as transformações ao redor não serão vinculadas a ele.

caso esse risco de vinculação exista, Direct2D não vinculará nenhuma transformação adjacente ao risco, mas ainda tentará vincular o restante do grafo.

![transformação de grafo com um risco de vinculação: 2 passagens, 1 intermediário.](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a>Criando um efeito personalizado compatível com vinculação de sombreador

se você estiver criando seu próprio efeito de Direct2D personalizado, precisará garantir que suas transformações dão suporte à vinculação de sombreador de efeito. Isso requer algumas pequenas alterações de como os efeitos personalizados anteriores foram implementados. se uma transformação dentro de seu efeito personalizado não oferecer suporte à vinculação de sombreador, Direct2D não a vinculará a nenhuma transformação adjacente a ela no grafo de efeito.

Como autor de um efeito personalizado, você deve estar ciente de vários conceitos e requisitos principais:

-   **Nenhuma alteração para afetar as implementações de interface**

    Você não precisa modificar nenhum código que implemente as várias interfaces de efeito, como [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).

-   **Fornecer uma versão de função completa e de exportação dos sombreadores**

    Você deve fornecer uma versão da função de exportação dos sombreadores do seu efeito que podem ser vinculados por Direct2D. Além disso, você também deve continuar a fornecer o sombreador completo original; isso ocorre porque Direct2D seleciona em tempo de execução a versão correta do sombreador, dependendo se a vinculação do sombreador deve ser aplicada a um link específico no grafo.

    Se uma transformação fornecer apenas o blob de sombreador de pixel completo (via [ID2D1EffectContext:: LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), ela não será vinculada a transformações adjacentes.

- **Funções auxiliares**

    Direct2D fornece [funções auxiliares HLSL](hlsl-helpers.md) e macros que irão gerar automaticamente as versões de função completa e de exportação de um sombreador. Esses auxiliares podem ser encontrados em d2d1effecthelpers. hlsli. Além disso, o compilador HLSL (FXC) permite que você insira o sombreador da função de exportação em um campo particular no sombreador completo. dessa forma, você só precisa criar um sombreador uma vez e passar as duas versões para Direct2D simultaneamente. ambos os d2d1effecthelpers. hlsli e o compilador FXC são incluídos como parte do SDK do Windows.

    As funções auxiliares:

  - [D2DGetInput](d2dgetinput.md)  
  - [D2DSampleInput](d2dsampleinput.md)  
  - [D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
  - [D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
  - [D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
  - [D2DGetScenePosition](d2dgetsceneposition.md)  
  - [\_Entrada do PS D2D \_](d2d-ps-entry.md)  

  Você também pode criar manualmente duas versões de cada sombreador e compilá-las duas vezes, contanto que as especificações descritas abaixo nas [especificações da função de exportação](#export-function-specifications) sejam atendidas.

-   **Somente sombreadores de pixel**

    Direct2D não dá suporte à vinculação de sombreadores de computação ou de vértice. No entanto, se o efeito usar um vértice e um sombreador de pixel, a saída do sombreador de pixel ainda poderá ser vinculada.

-   **Amostragem simples versus complexa**

    A vinculação da função de sombreador funciona conectando a saída de um sombreador de pixel passado para a entrada de uma passagem de sombreador de pixel subsequente. Isso só é possível quando o sombreador de pixel de consumo requer apenas um único valor de entrada para executar sua computação; Esse valor normalmente seria proveniente da amostragem de uma textura de entrada na coordenada de textura emitida pelo sombreador de vértice. Esse sombreador de pixel é dito para executar uma amostragem simples.

    ![conversão em escala de cinza é um exemplo de amostragem simples. o valor de um pixel de saída específico depende apenas do valor do pixel de entrada correspondente.](images/simple-sampling.png)

    Alguns sombreadores de pixel, como um desfoque gaussiano, computam a saída de vários exemplos de entrada em vez de apenas um único exemplo. Esse sombreador de pixel é dito para executar uma amostragem complexa.

    

    ![Desfoque Gaussiano é um exemplo de amostragem complexa. o valor do pixel de saída do centro depende de vários pixels de entrada.](images/complex-sampling.png)

    
    Somente as funções de sombreador com entradas simples podem ter sua entrada fornecida por outra função de sombreador. As funções de sombreador com entradas complexas devem ser fornecidas com uma textura de entrada para amostra. isso significa que Direct2D não vinculará um sombreador com entradas complexas ao seu antecessor.

    ao usar os [auxiliares do Direct2D HLSL](hlsl-helpers.md), você deve indicar no HLSL se um sombreador usa entradas complexas ou simples.

## <a name="example-linking-compatible-effect-shader"></a>Sombreador de efeito de exemplo compatível com vinculação

Usando os auxiliares do D2D, o seguinte trecho de código representa um sombreador simples de efeito compatível com vinculação:

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

Neste exemplo curto, observe que nenhum parâmetro de função é declarado, que o número de entradas e o tipo de cada entrada é declarado antes da função de entrada, a entrada é recuperada chamando [D2DGetInput](d2dgetinput.md)e as diretivas de pré-processador devem ser definidas antes de o arquivo auxiliar ser incluído.

Um sombreador compatível com vinculação deve fornecer um sombreador de pixel de passagem simples regular e uma função de sombreador de exportação. A macro de [ \_ \_ entrada do PS D2D](d2d-ps-entry.md) permite que cada um deles seja gerado a partir do mesmo código, quando usado em conjunto com o script de compilação do sombreador.

Ao compilar um sombreador completo, as macros são expandidas no código a seguir, que tem uma assinatura de entrada compatível com efeitos de D2D.

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

Ao compilar uma versão de função de exportação do mesmo código, o código a seguir é gerado:

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

Observe que a entrada de textura, normalmente recuperada por amostragem de um Texture2D, foi substituída por uma entrada de função (input0).

para ver uma descrição completa e passo a passo sobre o que você precisa fazer para escrever um efeito compatível com a vinculação, consulte o [tutorial de efeitos personalizados](custom-effects.md) e o [exemplo de efeitos de imagem personalizada Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

## <a name="compiling-a-linking-compatible-shader"></a>Compilando um sombreador compatível com vinculação

Para ser vinculável, o blob do sombreador de pixel passado para D2D deve conter as versões de função completa e de exportação do sombreador. Isso é feito inserindo-se a função de exportação compilada \_ na \_ área de dados particulares do blob do D3D \_ .

Quando os sombreadores são criados com as funções auxiliares D2D, um destino de compilação D2D deve ser definido no momento da compilação. Os tipos de destino de compilação são D2D \_ Full \_ Shader e D2D \_ Function.

A compilação de um sombreador de efeito compatível com vinculação é um processo de duas etapas:

-   [Compilar a função de exportação](#step-1-compile-the-export-function)
-   [Compilar o sombreador completo e inserir a função de exportação](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> ao compilar um efeito usando Visual Studio, você deve criar um arquivo em lotes que execute ambos os comandos FXC e executar esse arquivo em lotes como uma etapa de compilação personalizada que é executada antes da etapa de compilação.

 

### <a name="step-1-compile-the-export-function"></a>Etapa 1: compilar a função de exportação

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

Para compilar a versão da função de exportação do sombreador, você deve passar os seguintes sinalizadores para FXC.



|    Sinalizador                            |    Descrição                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /T &lt; ShaderModel&gt;         | Defina &lt; ShaderModel como &gt; o perfil do sombreador de pixel apropriado, conforme definido na [sintaxe FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax). Deve ser um dos perfis listados em "vinculação de sombreador HLSL". |
| &lt;Myshaderfile &gt; . HLSL      | Defina &lt; Myshaderfile &gt; como o nome do arquivo HLSL.                                                                                                                                                                                                    |
| /D \_ função D2D               | Essa definição instrui o FXC a compilar a versão da função de exportação do sombreador.                                                                                                                                                                       |
| /D \_ entrada D2D = &lt; entrada&gt;    | Defina a &lt; entrada &gt; como o nome do ponto de entrada HLSL que você definiu dentro da macro de [ \_ \_ entrada do D2D PS](d2d-ps-entry.md) .                                                                                                                                    |
| /FL &lt; Myshaderfile &gt; . fxlib | Defina &lt; Myshaderfile &gt; como onde você deseja armazenar a versão da função de exportação do sombreador. Observe que a extensão. fxlib é apenas para facilidade de identificação.                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a>Etapa 2: compilar o sombreador completo e inserir a função de exportação

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

Para compilar a versão completa do sombreador com a versão de exportação inserida, você deve passar os seguintes sinalizadores para FXC.



|    Sinalizador                                    |    Descrição                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /T &lt; ShaderModel&gt;                 | Defina &lt; ShaderModel como &gt; o perfil do sombreador de pixel apropriado, conforme definido na [sintaxe FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax). Este deve ser o perfil do sombreador de pixel correspondente ao perfil de vinculação especificado na etapa 1. |
| &lt;Myshaderfile &gt; . HLSL              | Defina &lt; Myshaderfile &gt; como o nome do arquivo HLSL.                                                                                                                                                                                                                               |
| /D D2D \_ Full \_ Shader                   | Essa definição instrui o FXC a compilar a versão completa do sombreador.                                                                                                                                                                                                             |
| /D \_ entrada D2D = &lt; entrada&gt;            | Defina a &lt; entrada &gt; como o nome do ponto de entrada HLSL que você definiu dentro da \_ macro de \_ entrada () do D2D PS.                                                                                                                                                                                 |
| Entrada de/e &lt;&gt;                       | Defina a &lt; entrada &gt; como o nome do ponto de entrada HLSL que você definiu dentro da \_ macro de \_ entrada () do D2D PS.                                                                                                                                                                                 |
| /SetPrivate &lt; Myshaderfile &gt; . fxlib | Esse argumento instrui o FXC a inserir o sombreador da função de exportação gerado na etapa 1 \_ na \_ área de dados particulares do blob do D3D \_ .                                                                                                                                                          |
| /Fo &lt; Myshadr &gt; . CSO               | Defina &lt; Myshadr &gt; como onde você deseja armazenar o sombreador compilado final e combinado.                                                                                                                                                                                                 |
| /FH &lt; Myshadr &gt; . h                 | Defina &lt; Myshadr &gt; para onde você deseja armazenar o cabeçalho final combinado.                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a>Exportar especificações de função

É possível – embora não seja recomendado – criar um sombreador de efeito compatível sem usar os auxiliares fornecidos pelo D2D. Deve-se ter cuidado para garantir que as assinaturas de entrada do sombreador completo e da função de exportação estejam de acordo com as especificações de D2D.

as especificações para sombreadores completos são as mesmas que as versões anteriores do Windows. Resumidamente, os parâmetros de entrada do sombreador de pixel devem ser a posição da VA \_ , a posição da cena \_ e uma TEXCOORD por entrada de efeito.

Para a função de exportação, a função deve retornar um FLOAT4 e suas entradas devem ser um dos seguintes tipos:

-   Entrada simples

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    Para entradas simples, o D2D inserirá uma função de exemplo entre a textura de entrada e a função de sombreador, ou a entrada será fornecida pela saída de outra função de sombreador.

-   Entrada complexa

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    para entradas complexas, o D2D passará apenas por uma coordenada de textura, conforme descrito na documentação Windows 8.

-   Local de saída

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    Somente uma entrada de posição de cena \_ pode ser definida. Esse parâmetro só deve ser incluído quando necessário, já que apenas uma função por sombreador vinculado pode utilizar esse parâmetro.

A semântica deve ser definida como acima, pois o D2D inspecionará a semântica para decidir como vincular funções juntas. Se qualquer entrada de função não corresponder a um dos tipos acima, a função será rejeitada para vinculação de sombreador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Auxiliares de HLSL](hlsl-helpers.md)
</dt> <dt>

[Interface ID3D11Linker](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[Interface ID3D11FunctionLinkingGraph](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 
