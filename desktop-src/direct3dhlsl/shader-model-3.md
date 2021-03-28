---
title: Modelo de sombreador 3 (referência de HLSL)
description: Os sombreadores de vértices e sombreadores de pixel são simplificados consideravelmente das versões anteriores do sombreador.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3517266ace77b9235604770d9b42d10cd80e2d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366197"
---
# <a name="shader-model-3-hlsl-reference"></a>Modelo de sombreador 3 (referência de HLSL)

Os sombreadores de vértices e sombreadores de pixel são simplificados consideravelmente das versões anteriores do sombreador. Se você estiver implementando sombreadores em hardware, não poderá usar \_ o vs 3 \_ 0 ou o PS \_ 3 \_ 0 com outras versões de sombreador e não poderá usar um tipo de sombreador com o pipeline de função fixo. Essas alterações possibilitam simplificar os drivers e o tempo de execução. A única exceção é que somente os \_ sombreadores vs 3 0 de software \_ podem ser usados com qualquer versão de sombreador de pixel. Além disso, se você estiver usando um sombreador do vs \_ 3 0 somente de software \_ com uma versão de sombreador de pixel anterior, o sombreador de vértice só poderá usar semânticas de saída compatíveis com códigos FVF (formato de vértice flexível).

A semântica usada em saídas de sombreador de vértice deve ser usada em entradas de sombreador de pixel. A semântica é usada para mapear as saídas do sombreador de vértice para as entradas do sombreador de pixel, semelhante à forma como a declaração de vértice é mapeada para os registros de entrada do sombreador de vértice e para os modelos de sombreador anteriores. Consulte corresponder a semântica em sombreadores vs 3,0 e PS 3,0.

Os Estados de renderização do modo de encapsulamento adicionais foram adicionados para cobrir a possibilidade de coordenadas de textura adicionais neste novo esquema. Os atributos com D3DDECLUSAGE \_ TEXCOORD e o índice de uso de 0 a 15 são interpolados no modo Wrap quando o [**\_ \* encapsulamento D3DRS**](/windows/desktop/direct3d9/d3drenderstatetype) correspondente é definido.

-   [Recursos do modelo de sombreador de vértice 3](#vertex-shader-model-3-features)
-   [Recursos do Pixel Shader Model 3](#pixel-shader-model-3-features)
-   [Corresponder a semântica em \_ \_ sombreadores vs 3 0 e PS \_ 3 \_ 0](/windows)
-   [Alterações no modo de neblina, profundidade e sombreamento](#fog-depth-and-shading-mode-changes)
-   [Conversões de ponto flutuante e inteiro](#floating-point-and-integer-conversions)
-   [Especificando a precisão total ou parcial](#specifying-full-or-partial-precision)
-   [Vértice de software e sombreadores de pixel](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a>Recursos do modelo de sombreador de vértice 3

Os tipos de registro de saída do sombreador de vértice foram recolhidos em doze registros (consulte [registros de saída](dx9-graphics-reference-asm-vs-registers-output.md)). Cada registrador usado precisa ser declarado usando a instrução [DCL](dcl-usage---ps.md) e uma semântica (por exemplo, DCL \_ color0 o0. xyzw).

O \_ modelo de sombreador do vértice de 3 0 (vs \_ 3 \_ 0) expande os recursos de vs \_ 2 \_ 0 com indexação de registro mais potente, um conjunto de registros de saída simplificados, a capacidade de obter amostras de uma textura em um sombreador de vértice e a capacidade de controlar a taxa na qual as entradas de sombreador são inicializadas.

### <a name="index-any-register"></a>Indexar qualquer registro

Todos os registros (registradores de [entrada](dx9-graphics-reference-asm-vs-registers-input.md) e de [saída](dx9-graphics-reference-asm-vs-registers-output.md)) podem ser indexados usando [o registro de contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (somente registros constantes podem ser indexados em versões anteriores.)

Você deve declarar registros de entrada e de saída antes de indexá-los. No entanto, você não pode indexar nenhum registro de saída declarado com uma semântica de posição ou de tamanho de ponto. Na verdade, se a indexação for usada, a posição e a semântica psize devem ser declaradas nos registros o0 e O1 respectivamente.

Você só tem permissão para indexar um intervalo contínuo de registros; ou seja, você não pode indexar entre registradores que não foram declarados. Embora essa restrição possa ser inconveniente, ela permite que a otimização de hardware ocorra. A tentativa de indexar entre registradores não contíguos produzirá resultados indefinidos. A validação do sombreador não impõe essa restrição.

### <a name="simplify-output-registers"></a>Simplificar registros de saída

Todos os vários tipos de registros de saída foram recolhidos em doze registros de saída: 1 para a posição, 2 para cor, 8 para textura e 1 para tamanho de sombra ou ponto. Esses registros interpolarem todos os dados que eles contêm para o sombreador de pixel. As declarações de registro de saída são necessárias e a semântica é atribuída a cada registro.

Os registros podem ser divididos da seguinte maneira:

-   Pelo menos um registro deve ser declarado como um registro de posição de quatro componentes. Esse é o único registro de sombreador de vértice necessário.
-   Os dez primeiros registros consumidos por um sombreador podem usar até quatro componentes (xyzw) no máximo.
-   O último (ou décimo-segundo) registro pode conter apenas um escalar (como o tamanho do ponto).

Para obter uma lista dos registros, consulte [Registers-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).

### <a name="texture-sample-in-a-vertex-shader"></a>Exemplo de textura em um sombreador de vértice

O sombreador de vértice 3 \_ 0 dá suporte à pesquisa de textura no sombreador de vértice usando [texldl-vs](texldl---vs.md).

## <a name="pixel-shader-model-3-features"></a>Recursos do Pixel Shader Model 3

Os registros de cor e textura do sombreador de pixel foram recolhidos em dez registros de entrada (consulte [tipos de registro de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)). O registro facial é um registro escalar de ponto flutuante. Somente o sinal deste registro é válido. Se o sinal for negativo, o primitivo será um verso. Isso pode ser usado dentro de um sombreador de pixel para atingir a iluminação em dois lados, por exemplo. O registro de posição faz referência aos pixels (x, y) atuais.

Os registros de constante de sombreador podem ser definidos usando:

-   [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a>Corresponder a semântica em \_ \_ sombreadores vs 3 0 e PS \_ 3 \_ 0

Há algumas restrições sobre o uso semântico com vs \_ 3 \_ 0 e PS \_ 3 \_ 0. Em geral, você precisa ter cuidado ao usar uma semântica para uma entrada de sombreador que corresponda a uma semântica usada em uma saída de sombreador.

Por exemplo, esse sombreador de pixel empacota vários nomes em um registro:


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



Cada registrador tem uma semântica diferente. Observe que você também pode nomear V0. x e V0. YZ com uma semântica diferente (várias) devido ao uso da máscara de gravação.

Dado o sombreador de pixel, o \_ seguinte \_ sombreador vs 3 0 não pode ser emparelhado com ele:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



Esses dois sombreadores entram em conflito com o uso da semântica [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) e **D3DDECLUSAGE \_ TEXCOORD1** .

Reescreva o sombreador de vértice como este para evitar a colisão semântica:


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



Da mesma forma, um nome semântico declarado em diferentes registros de entrada no sombreador de pixel (V0 e V1 no sombreador de pixel) não pode ser usado em um único registro de saída neste sombreador de vértice. Por exemplo, este sombreador de vértice não pode ser emparelhado com o sombreador de pixel porque D3DDECLUSAGE \_ TEXCOORD1 é usado para os registros de entrada do sombreador de pixel (V0, v1) e o registro de saída do sombreador de vértice O3.


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



Por outro lado, esse sombreador de vértice não pode ser emparelhado com o sombreador de pixel porque a máscara de saída para um parâmetro com uma semântica específica não fornece os dados solicitados pelo sombreador de pixel:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



Este sombreador de vértice não fornece uma saída com um dos nomes semânticos solicitados pelo sombreador de pixel, portanto, o emparelhamento de sombreador é inválido:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a>Alterações no modo de neblina, profundidade e sombreamento

Quando D3DRS \_ shadmode é definido para sombreamento simples durante a rasterização de recorte e de triângulo, os atributos com a cor de D3DDECLUSAGE \_ são interpolados como sombreados. Se qualquer componente de um registro for declarado com uma semântica de cor, mas outros componentes do mesmo registro receberem semânticas diferentes, a interpolação de sombreamento simples (linear versus plana) será indefinida nos componentes no registro sem uma semântica de cor.

Se a renderização de neblina for desejada, os \_ \_ sombreadores vs 3 0 e PS \_ 3 \_ 0 deverão implementar a neblina. Nenhum cálculo de neblina é feito fora dos sombreadores. Não há nenhum registro de neblina no vs \_ 3 \_ 0, e a D3DDECLUSAGE semântica adicional de \_ neblina (para o fator de mistura de neblina calculado por vértice) e \_ a profundidade de D3DDECLUSAGE (para passar um valor de profundidade para o sombreador de pixel para calcular o fator de fusão de neblina) foram adicionadas.

O estado de estágio de textura D3DTSS \_ TEXCOORDINDEX é ignorado ao usar o sombreador de pixel 3,0.

Os valores a seguir foram adicionados para acomodar essas alterações:


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a>Conversões de ponto flutuante e inteiro

A matemática de ponto flutuante ocorre em diferentes precisão e intervalos (16 bits, 24 bits e 32 bits) em diferentes partes do pipeline. Um valor maior que o intervalo dinâmico do pipeline que entra nesse pipeline (por exemplo, um mapa de textura float de 32 bits é amostrado em um pipeline float de 24 bits no PS \_ 2 \_ 0) cria um resultado indefinido. Para um comportamento previsível, você deve fixe esse valor ao máximo de intervalo dinâmico.

A conversão de um valor de ponto flutuante em um inteiro ocorre em vários locais, como:

-   Ao encontrar uma instrução [mova-vs](mova---vs.md) .
-   Durante o endereçamento de textura.
-   Ao gravar em um destino de renderização de ponto não flutuante.

## <a name="specifying-full-or-partial-precision"></a>Especificando a precisão total ou parcial

O PS \_ 3 \_ 0 e o PS \_ 2 \_ x oferecem suporte para dois níveis de precisão:



|          |          |                   |                      |
|----------|----------|-------------------|----------------------|
| PS \_ 3 \_ 0 | PS \_ 2 \_ 0 | Precisão         | Valor                |
| x        |          | Completo              | FP32 ou superior       |
| x        |          | Precisão parcial | FP16 = s10e5           |
| x        | x        | Completo              | fp24 = s16e7 ou superior |
| x        | x        | Precisão parcial | FP16 = s10e5           |



 

\_o PS 3 \_ 0 dá suporte a mais precisão do que \_ o PS 2 \_ 0. Por padrão, todas as operações ocorrem no nível de precisão total.

A precisão parcial (consulte [modificadores de registro de sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers.md)) é solicitada adicionando o \_ modificador PP ao código do sombreador (desde que a implementação subjacente ofereça suporte a ela). As implementações sempre são gratuitas para ignorar o modificador e executar as operações afetadas com precisão total.

O \_ modificador PP pode ocorrer em dois contextos:

-   Em uma declaração de coordenada de textura para passar coordenadas de textura de precisão parcial para o sombreador de pixel. Isso pode ser usado quando a textura coordena dados de cores de retransmissão para o sombreador de pixel, que pode ser mais rápido com precisão parcial do que com precisão total em algumas implementações.
-   Em qualquer instrução para solicitar o uso de precisão parcial, incluindo instruções de carga de textura. Isso indica que a implementação tem permissão para executar a instrução com precisão parcial e armazenar um resultado de precisão parcial. Na ausência de um modificador explícito, a instrução deve ser executada com precisão total (independentemente da precisão dos operandos de entrada).

Um aplicativo pode deliberadamente optar por compensar a precisão do desempenho. Há vários tipos de dados de entrada de sombreador que são candidatos naturais para processamento de precisão parcial:

-   Os iteradores de cor são bem representados por valores de precisão parcial.
-   Os valores de textura da maioria dos formatos podem ser representados com precisão pelos valores de precisão parcial (os valores amostrados de 32 bits, texturas de formato de ponto flutuante são uma exceção óbvia).
-   As constantes podem ser representadas pela representação de precisão parcial, conforme apropriado para o sombreador.

Em todos esses casos, o desenvolvedor pode optar por especificar a precisão parcial para processar os dados, sabendo que nenhuma precisão de dados de entrada é perdida. Em alguns casos, um sombreador pode exigir que as etapas internas de um cálculo sejam executadas com precisão total mesmo quando os valores de entrada e saída final não tiverem mais do que a precisão parcial.

## <a name="software-vertex-and-pixel-shaders"></a>Vértice de software e sombreadores de pixel

Implementações de software (tempo de execução e referência para sombreadores de vértice e referência para sombreadores de pixel) dos sombreadores da versão 2 \_ 0 e acima têm alguma validação relaxada. Isso é útil para fins de depuração e protótipos. O aplicativo indica ao tempo de execução/Assembler que ele precisa de uma validação relaxada usando o \_ sinalizador SW no assembler (por exemplo, vs \_ 2 \_ SW). Um sombreador de software não funcionará com hardware.

\_o vs 2 \_ SW é um relaxamento até o máximo de Caps de vs \_ 2 \_ x; da mesma forma, \_ o SW de PS 2 \_ é um relaxamento para o máximo de Caps de PS \_ 2 \_ x. Especificamente, as seguintes validações são relaxadas:



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Modelo de Sombreador                               | Recurso                             | Limite                                                                                                                             |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Contagens de instruções                   | Ilimitado                                                                                                                         |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registros de constante float             | 8192                                                                                                                              |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registros de constante de inteiro           | 2.048                                                                                                                              |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registros constantes boolianos           | 2.048                                                                                                                              |
| PS \_ 2 \_ SW                                  | Dependente-ler profundidade                 | Ilimitado                                                                                                                         |
| vs \_ 2 \_ SW                                  | instruções e rótulos de controle de fluxo | Ilimitado                                                                                                                         |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Início/etapa/contagens de loop               | O tamanho da etapa de início e iteração da iteração para instruções de rep e loop são inteiros com sinal de 32 bits. A contagem pode ser até o máximo \_ int/64. |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Limites de porta                          | Os limites de porta para todos os arquivos de registro são relaxados.                                                                                   |
| vs \_ 3 \_ SW                                  | Número de interpoladores              | 16 registros de saída no vs \_ 3 \_ SW.                                                                                                 |
| PS \_ 3 \_ SW                                  | Número de interpoladores              | 14 (16-2) registros de entrada para \_ o \_ software PS 3 SW.                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 