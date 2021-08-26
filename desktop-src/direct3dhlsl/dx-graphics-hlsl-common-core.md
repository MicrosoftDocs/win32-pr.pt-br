---
title: Núcleo de Common-Shader
description: Núcleo de Common-Shader
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c2d1851025cb051a21a997f5e3a4987d3b6309e148248b3ea55c6b9ca6ad31c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950476"
---
# <a name="common-shader-core"></a>Núcleo de Common-Shader

No sombreador modelo 4, todos os estágios de sombreador implementam a mesma funcionalidade base usando um núcleo de sombreador comum. Além disso, cada um dos três estágios do sombreador (Vertex, Geometry e pixel) oferece a funcionalidade exclusiva para cada estágio, como a capacidade de gerar novos primitivos a partir do palco do sombreador de geometry ou para descartar um pixel específico no estágio do sombreador de pixel. O diagrama a seguir mostra como os dados fluem por meio de um estágio do sombreador e a relação entre o núcleo do sombreador comum e os recursos de memória do sombreador.

![diagrama de fluxo de dados em um estágio do sombreador](images/d3d10-shader-unit.png)

-   **Dados de entrada**: um sombreador de vértice recebe suas entradas do estágio de Assembler de entrada; os sombreadores de geometria e pixel recebem suas entradas do estágio do sombreador anterior. Entradas adicionais incluem [semântica de valor do sistema](dx-graphics-hlsl-semantics.md), que são consumíveis pela primeira unidade no pipeline ao qual são aplicáveis.
-   **Dados de saída**: os sombreadores geram resultados de saída a serem passados para o estágio subsequente no pipeline. Para um sombreador de geometria, a quantidade de saída de dados de uma única invocação pode variar. Algumas saídas são interpretadas pelo núcleo do sombreador comum (como a posição do vértice e o índice de destino de renderização), outras foram projetadas para serem interpretadas por um aplicativo.
-   **Código do sombreador**: os sombreadores podem ler da memória, executar o ponto flutuante de vetor e operações aritméticas de inteiros ou operações de controle de fluxo. Não há nenhum limite para o número de instruções que podem ser implementadas em um sombreador.
-   **Amostras**: os exemplos definem como filtrar as texturas de amostra e de filtro. Até 16 amostras podem ser associadas simultaneamente a um sombreador.
-   **Texturas**: as texturas podem ser filtradas usando amostras ou lidas em uma base por Texel diretamente com a função intrínseca de [carregamento](dx-graphics-hlsl-to-load.md) .
-   **Buffers**: os buffers nunca são filtrados, mas podem ser lidos da memória por elemento diretamente com a função intrínseca de [carregamento](dx-graphics-hlsl-to-load.md) . Até 128 recursos de textura e buffer (combinados) podem ser associados simultaneamente a um sombreador.
-   **Buffers de constantes**: os buffers de constantes são otimizados para variáveis de constante de sombreador. Até 16 buffers de constante podem ser associados a um estágio de sombreador simultaneamente. Elas foram projetadas para atualização mais frequente da CPU; Portanto, têm restrições de tamanho, de layout e de acesso adicionais.


Diferenças entre o Direct3D 9 e o Direct3D 10:

- No Direct3D 9, cada unidade do sombreador tinha um único arquivo de registro constante pequeno para armazenar todas as variáveis de sombreador constantes. Acomodar todos os sombreadores com esse espaço de constante limitado exigiu reciclagem frequente de constantes pela CPU.
- No Direct3D 10, as constantes são armazenadas em buffers imutáveis na memória e são gerenciadas como qualquer outro recurso. Não há nenhum limite para o número de buffers constantes que um aplicativo pode criar. Ao organizar constantes em buffers por frequência de atualização e uso, a quantidade de largura de banda necessária para atualizar constantes para acomodar todos os sombreadores pode ser significativamente reduzida.



 

## <a name="integer-and-bitwise-support"></a>Suporte a inteiros e a bits

O Core do sombreador comum fornece um conjunto completo de operações de inteiro e bit-bit de 32 bits em conformidade com IEEE. Essas operações permitem uma nova classe de algoritmos nos exemplos de hardware de gráficos: técnicas de compactação e empacotamento, FFTs e controle de fluxo de programa de bits.

Os tipos de dados **int** e **uint** no Direct3D 10 HLSL são mapeados para inteiros de 32 bits no hardware.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> Nas entradas de fluxo do Direct3D 9 marcadas como número inteiro em HLSL foram interpretadas como ponto flutuante. No Direct3D 10, as entradas de fluxo marcadas como números inteiros são interpretadas como um inteiro de 32 bits.<br/> Além disso, os valores Boolianos agora são todos definidos bits ou todos os bits são desdefinidos. Os dados convertidos em **bool** serão interpretados como true se o valor não for igual a 0,0 f (zero positivo e negativo) puderem ser falsos) e false caso contrário.<br/> |



 

## <a name="bitwise-operators"></a>Operadores bit a bit

O sombreador comum do é compatível com os seguintes operadores bits:



| Operador  | Função          |
|-----------|-------------------|
| ~         | Não lógico       |
| <<  | Deslocamento à esquerda        |
| >>  | Deslocamento à direita       |
| &         | AND lógico       |
| \|        | Ou lógico        |
| ^         | XOR lógico       |
| <<= | Deslocamento à esquerda igual  |
| >>= | Deslocamento à direita igual |
| &=        | E igual a         |
| \|=       | Ou igual a          |
| ^=        | XOR igual         |



 

Os operadores bit a bit são definidos para operar somente em tipos de dados **int** e **uint** . A tentativa de usar operadores de bit que não seja em tipos de dados **float** ou **struct** resultará em um erro. Os operadores de bits a bit seguem a mesma precedência de C com relação a outros operadores.

## <a name="binary-casts"></a>Conversões binárias

A conversão entre um número inteiro e um tipo de ponto flutuante converterá o valor numérico após as regras de truncamento de C. Converter um valor de um **float**, para um **int** e voltar para um **float** é uma conversão com perda dependente da precisão do tipo de dados de destino. Aqui estão algumas das funções de conversão: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**Asent (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).

As conversões binárias também podem ser executadas usando funções intrínsecas HLSL. Isso faz com que o compilador reinterprete a representação de bits de um número para o tipo de dados de destino.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





