---
title: Vinculação de Sombreador de Efeito
description: O Direct2D usa uma otimização chamada vinculação de sombreador de efeito que combina vários efeitos que a renderização de gráfico passa em uma única passagem.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6bad2170f2b897a5cf8ac3086a74945efa8bf
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549231"
---
# <a name="effect-shader-linking"></a>Vinculação de Sombreador de Efeito

O Direct2D usa uma otimização chamada vinculação de sombreador de efeito que combina vários efeitos que a renderização de gráfico passa em uma única passagem.

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

O efeito que as otimizações de vinculação do sombreador se baseia na vinculação do sombreador HLSL, um recurso do Direct3D 11,2 que permite que os sombreadores de pixel e vértice sejam gerados em tempo de execução por meio da vinculação de funções de sombreador pré-compilados. As figuras a seguir ilustram o conceito de vinculação de sombreador de efeito em um grafo de efeito. A primeira figura mostra um grafo típico de efeito de Direct2D com quatro transformações de renderização. Sem vinculação de sombreador, cada transformação consome uma passagem de renderização e requer uma superfície intermediária; no total, esse grafo requer 4 passagens e 3 intermediários.

![transformação de grafo sem vinculação de sombreador: 4 passagens e 3 intermediários.](images/shader-transform-graph.png)

A segunda figura mostra o mesmo grafo de efeito em que cada transformação de renderização foi substituída por uma versão de função vinculável. O Direct2D é capaz de vincular todo o grafo e executá-lo em uma passagem sem exigir nenhum intermediário. Isso pode proporcionar uma diminuição significativa no tempo de execução da GPU e na redução do consumo máximo de memória da GPU.

![Grafo de transformação com vinculação de sombreador: 1 passagem, 0 intermediários.](images/shader-linking-graph.png)



 

A vinculação do sombreador de efeito opera em transformaçãos individuais dentro de um efeito; isso significa que até mesmo um grafo com um único efeito poderá se beneficiar da vinculação do sombreador se esse efeito tiver várias transformação válidas.

## <a name="using-effect-shader-linking"></a>Usando a vinculação do sombreador de efeito

Se você estiver criando um aplicativo Direct2D que usa efeitos, não será necessário fazer nada para aproveitar a vinculação do sombreador de efeito. O Direct2D analisa automaticamente o grafo de efeito para determinar a maneira mais ideal de vincular cada transformação.

Os autores de efeito são responsáveis por implementar seu efeito de uma maneira que dá suporte à vinculação do sombreador de efeito; Para obter mais informações, consulte [a seção Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) abaixo. Todos os efeitos integrados são suportados pela vinculação do sombreador.

O Direct2D vincula apenas as transformações de renderização adjacentes em situações em que ela é benéfica. Ele leva em conta vários fatores ao determinar se é necessário vincular duas transformaçãos. Por exemplo, a vinculação do sombreador não será executada se uma das transformaçãos usar sombreadores de vértice ou de computação, pois somente sombreadores de pixel podem ser vinculados. Além disso, se um efeito não tiver sido autor para ser compatível com a vinculação do sombreador, as transformaçãos ao redor não serão vinculadas a ele.

Caso esse risco de vinculação exista, o Direct2D não vincula nenhuma transformação adjacente ao risco, mas ainda tentará vincular o restante do grafo.

![transformar grafo com um risco de vinculação: 2 passagens, 1 intermediário.](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a>Como autor de um efeito personalizado compatível com vinculação de sombreador

Se você estiver com seu próprio efeito Direct2D personalizado, precisará garantir que suas transformaçãos sejam compatíveis com a vinculação do sombreador de efeito. Isso requer algumas pequenas alterações de como os efeitos personalizados anteriores foram implementados. Se uma transformação dentro de seu efeito personalizado não dá suporte à vinculação de sombreador, o Direct2D não a vincula a nenhuma transformação adjacente a ela no grafo de efeito.

Como autor de efeito personalizado, você deve estar ciente de vários conceitos e requisitos principais:

-   **Nenhuma alteração nas implementações de interface de efeito**

    Você não precisa modificar nenhum código que implemente as várias interfaces de efeito, como [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).

-   **Fornecer uma versão de função completa e de exportação dos sombreadores**

    Você deve fornecer uma versão da função de exportação dos sombreadores do seu efeito que são vinculáveis por Direct2D. Além disso, você também deve continuar a fornecer o sombreador completo original; Isso ocorre porque Direct2D seleciona em tempo de execução a versão correta do sombreador, dependendo se a vinculação do sombreador deve ser aplicada a um link específico no grafo.

    Se uma transformação fornecer apenas o blob de sombreador de pixel completo (via [ID2D1EffectContext:: LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), ela não será vinculada a transformações adjacentes.

- **Funções auxiliares**

    O Direct2D fornece [funções auxiliares de HLSL](hlsl-helpers.md) e macros que irão gerar automaticamente as versões de função completa e de exportação de um sombreador. Esses auxiliares podem ser encontrados em d2d1effecthelpers. hlsli. Além disso, o compilador HLSL (FXC) permite que você insira o sombreador da função de exportação em um campo particular no sombreador completo. Dessa forma, você só precisa criar um sombreador uma vez e passar as duas versões para Direct2D simultaneamente. Ambos os d2d1effecthelpers. hlsli e o compilador FXC são incluídos como parte do SDK do Windows.

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

    O Direct2D não dá suporte à vinculação de sombreadores de computação ou vértice. No entanto, se o efeito usar um vértice e um sombreador de pixel, a saída do sombreador de pixel ainda poderá ser vinculada.

-   **Amostragem simples versus complexa**

    A vinculação de função de sombreador funciona conectando a saída de uma passagem de sombreador de pixel à entrada de uma passagem de sombreador de pixel subsequente. Isso só é possível quando o sombreador de pixel de consumo requer apenas um único valor de entrada para executar seu cálculo; esse valor normalmente seria de amostragem de uma textura de entrada na coordenada de textura emitida pelo sombreador de vértice. Esse sombreador de pixel é dito para executar amostragem simples.

    ![A conversão em escala de cinza é um exemplo de amostragem simples. O valor de um pixel de saída específico depende apenas do valor do pixel de entrada correspondente.](images/simple-sampling.png)

    Alguns sombreadores de pixel, como um desfoque gaussiano, calculam sua saída de vários exemplos de entrada em vez de apenas um único exemplo. Esse sombreador de pixel é dito para executar amostragem complexa.

    

    ![O desfoque gaussiano é um exemplo de amostragem complexa. O valor do pixel de saída central depende de vários pixels de entrada.](images/complex-sampling.png)

    
    Somente funções de sombreador com entradas simples podem ter sua entrada fornecida por outra função de sombreador. As funções de sombreador com entradas complexas devem ser fornecidas com uma textura de entrada para amostra. Isso significa que o Direct2D não vincula um sombreador com entradas complexas ao seu antecessor.

    Ao usar os [auxiliares HLSL do Direct2D,](hlsl-helpers.md)você deve indicar no HLSL se um sombreador usa entradas complexas ou simples.

## <a name="example-linking-compatible-effect-shader"></a>Sombreador de efeito compatível com vinculação de exemplo

Usando os auxiliares D2D, o snippet de código a seguir representa um sombreador de efeito simples compatível com vinculação:

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

Neste breve exemplo, observe que nenhum parâmetro de função é declarado, que o número de entradas e o tipo de cada entrada são declarados antes da função de entrada, a entrada é recuperada chamando [D2DGetInput](d2dgetinput.md)e que as diretivas de pré-processador devem ser definidas antes que o arquivo auxiliar seja incluído.

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

Para ver uma descrição completa e passo a passo do que você precisa fazer para escrever um efeito compatível com a vinculação, consulte o [tutorial de efeitos personalizados](custom-effects.md) e o [exemplo de efeitos de imagem personalizada do Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

## <a name="compiling-a-linking-compatible-shader"></a>Compilando um sombreador compatível com vinculação

Para ser vinculável, o blob do sombreador de pixel passado para D2D deve conter as versões de função completa e de exportação do sombreador. Isso é feito inserindo-se a função de exportação compilada \_ na \_ área de dados particulares do blob do D3D \_ .

Quando os sombreadores são criados com as funções auxiliares D2D, um destino de compilação D2D deve ser definido no momento da compilação. Os tipos de destino de compilação são D2D \_ Full \_ Shader e D2D \_ Function.

A compilação de um sombreador de efeito compatível com vinculação é um processo de duas etapas:

-   [Compilar a função de exportação](#step-1-compile-the-export-function)
-   [Compilar o sombreador completo e inserir a função de exportação](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> Ao compilar um efeito usando o Visual Studio, você deve criar um arquivo em lotes que execute ambos os comandos FXC e executar esse arquivo em lotes como uma etapa de compilação personalizada que é executada antes da etapa de compilação.

 

### <a name="step-1-compile-the-export-function"></a>Etapa 1: compilar a função de exportação

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

Para compilar a versão da função de exportação do sombreador, você deve passar os seguintes sinalizadores para FXC.



|    Sinalizador                            |    Descrição                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /T <ShaderModel>         | Defina <ShaderModel> como o perfil do sombreador de pixel apropriado, conforme definido na [sintaxe FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax). Deve ser um dos perfis listados em "vinculação de sombreador HLSL". |
| <MyShaderFile>.hlsl      | Defina <MyShaderFile> como o nome do arquivo HLSL.                                                                                                                                                                                                    |
| /D D2D \_ FUNCTION               | Essa definição instrui o FXC a compilar a versão da função de exportação do sombreador.                                                                                                                                                                       |
| /D D2D \_ ENTRY=<entry>    | Defina <entry> como o nome do ponto de entrada HLSL que você definiu dentro da macro [ \_ D2D PS \_ ENTRY.](d2d-ps-entry.md)                                                                                                                                    |
| /Fl <MyShaderFile> .fxlib | De <MyShaderfile> acordo com o local em que você deseja armazenar a versão da função de exportação do sombreador. Observe que a extensão .fxlib é apenas para facilitar a identificação.                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a>Etapa 2: Compilar o sombreador completo e inserir a função de exportação

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

Para compilar a versão completa do sombreador com a versão de exportação inserida, você deve passar os sinalizadores a seguir para o FXC.



|    Sinalizador                                    |    Descrição                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /t <ShaderModel>                 | De <ShaderModel> acordo com o perfil de sombreador de pixel apropriado, conforme definido na Sintaxe [FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax). Esse deve ser o perfil de sombreador de pixel correspondente ao perfil de vinculação especificado na Etapa 1. |
| <MyShaderFile>.hlsl              | Defina <MyShaderFile> como o nome do arquivo HLSL.                                                                                                                                                                                                                               |
| /D D2D \_ FULL \_ SHADER                   | Essa definição instrui o FXC a compilar a versão completa do sombreador.                                                                                                                                                                                                             |
| /D D2D \_ ENTRY=<entry>            | Defina <entry> como o nome do ponto de entrada HLSL que você definiu dentro da macro D2D \_ PS \_ ENTRY().                                                                                                                                                                                 |
| /e <entry>                       | Defina <entry> como o nome do ponto de entrada HLSL que você definiu dentro da macro D2D \_ PS \_ ENTRY().                                                                                                                                                                                 |
| /SetPrivate <MyShaderFile> . fxlib | Esse argumento instrui o FXC a inserir o sombreador da função de exportação gerado na etapa 1 \_ na \_ área de dados particulares do blob do D3D \_ .                                                                                                                                                          |
| /Fo <MyShader> . CSO               | Defina <MyShader> como onde você deseja armazenar o sombreador compilado final e combinado.                                                                                                                                                                                                 |
| /FH <MyShader> . h                 | Defina <MyShader> como onde você deseja armazenar o cabeçalho final combinado.                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a>Exportar especificações de função

É possível – embora não seja recomendado – criar um sombreador de efeito compatível sem usar os auxiliares fornecidos pelo D2D. Deve-se ter cuidado para garantir que as assinaturas de entrada do sombreador completo e da função de exportação estejam de acordo com as especificações de D2D.

As especificações para sombreadores completos são as mesmas que as versões anteriores do Windows. Resumidamente, os parâmetros de entrada do sombreador de pixel devem ser a posição da VA \_ , a posição da cena \_ e uma TEXCOORD por entrada de efeito.

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

    Para entradas complexas, o D2D passará apenas por uma coordenada de textura, conforme descrito na documentação do Windows 8.

-   Local de saída

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    Somente uma entrada de posição de cena \_ pode ser definida. Esse parâmetro só deve ser incluído quando necessário, já que apenas uma função por sombreador vinculado pode utilizar esse parâmetro.

A semântica deve ser definida como acima, pois o D2D inspecionará a semântica para decidir como vincular funções juntas. Se qualquer entrada de função não corresponder a um dos tipos acima, a função será rejeitada para vinculação de sombreador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Auxiliares HLSL](hlsl-helpers.md)
</dt> <dt>

[Interface ID3D11Linker](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[Interface ID3D11FunctionLinkingGraph](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 