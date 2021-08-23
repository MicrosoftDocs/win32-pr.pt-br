---
title: Modelo de sombreador 3 (referência HLSL)
description: Sombreadores de vértice e sombreadores de pixel são simplificados consideravelmente de versões anteriores do sombreador.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 899284777f86c3a1e5d77da9a2f21ed9aa4b5368b540082cc92bd56b7fb780da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788636"
---
# <a name="shader-model-3-hlsl-reference"></a>Modelo de sombreador 3 (referência HLSL)

Sombreadores de vértice e sombreadores de pixel são simplificados consideravelmente de versões anteriores do sombreador. Se você estiver implementando sombreadores em hardware, talvez não use vs \_ 3 0 ou ps 3 0 com outras versões de sombreador e não poderá usar nenhum tipo de sombreador com o pipeline de funções \_ \_ \_ fixas. Essas alterações possibilitam simplificar os drivers e o runtime. A única exceção é que os sombreadores somente de software \_ \_ versus 3 0 podem ser usados com qualquer versão do sombreador de pixel. Além disso, se você estiver usando um sombreador somente de software versus 3 0 com uma versão anterior do sombreador de pixel, o sombreador de vértice só poderá usar a semântica de saída compatível com códigos FVF (formato de vértice \_ \_ flexível).

A semântica usada nas saídas do sombreador de vértice deve ser usada em entradas de sombreador de pixel. A semântica é usada para mapear as saídas do sombreador de vértice para as entradas do sombreador de pixel, semelhante à maneira como a declaração de vértice é mapeada para os registros de entrada do sombreador de vértice e modelos de sombreador anteriores. Consulte Semântica de corresponder em sombreadores vs 3.0 e ps 3.0.

Outros estados de renderização do modo de wrap foram adicionados para cobrir a possibilidade de coordenadas de textura adicionais nesse novo esquema. Atributos com D3DDECLUSAGE TEXCOORD e índice de uso de 0 a 15 são interpolados no modo de wrap quando o \_ [**\_ WRAP \* D3DRS**](/windows/desktop/direct3d9/d3drenderstatetype) correspondente é definido.

-   [Recursos do Modelo 3 do Sombreador de Vértice](#vertex-shader-model-3-features)
-   [Recursos do Modelo 3 do Sombreador de Pixel](#pixel-shader-model-3-features)
-   [Corresponder semântica em \_ \_ versus 3 0 e ps \_ 3 \_ 0 Sombreadores](/windows)
-   [Alterações no modo de sombra, profundidade e sombreamento](#fog-depth-and-shading-mode-changes)
-   [Conversões de ponto flutuante e inteiro](#floating-point-and-integer-conversions)
-   [Especificando precisão total ou parcial](#specifying-full-or-partial-precision)
-   [Sombreadores de vértice e pixel de software](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a>Recursos do Modelo 3 do Sombreador de Vértice

Os tipos de registro de saída do sombreador de vértice foram recolhidos em doze registros (consulte [Registros de Saída](dx9-graphics-reference-asm-vs-registers-output.md)). Cada registro usado precisa ser declarado usando a instrução [dcl](dcl-usage---ps.md) e uma semântica (por exemplo, dcl \_ color0 o0.xyzw).

O modelo de sombreador de vértice \_ 3 0 (versus 3 0) expande os recursos do vs 2 0 com indexação de registro mais eficiente, um conjunto de registros de saída simplificados, a capacidade de amostra de uma textura em um sombreador de vértice e a capacidade de controlar a taxa na qual as entradas do sombreador são \_ \_ \_ \_ inicializadas.

### <a name="index-any-register"></a>Indexar qualquer registro

Todos os registros( [Registro de](dx9-graphics-reference-asm-vs-registers-input.md) Entrada e Registros de Saída [)](dx9-graphics-reference-asm-vs-registers-output.md)podem ser indexados usando o Registro de Contador de [Loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (somente registros constantes podem ser indexados em versões anteriores.)

Você deve declarar registros de entrada e saída antes de indexá-los. No entanto, você não pode indexar nenhum registro de saída que tenha sido declarado com uma semântica de tamanho de posição ou ponto. Na verdade, se a indexação for usada, a posição e a semântica de psize deverão ser declaradas nos registros o0 e o1, respectivamente.

Você só tem permissão para indexar um intervalo contínuo de registros; ou seja, você não pode indexar entre registros que não foram declarados. Embora essa restrição possa ser inconveniente, ela permite que a otimização de hardware seja realizada. A tentativa de indexar entre registros não contíguos produzirá resultados indefinido. A validação do sombreador não impõe essa restrição.

### <a name="simplify-output-registers"></a>Simplificar registros de saída

Todos os vários tipos de registros de saída foram recolhidos em doze registros de saída: 1 para a posição, 2 para cor, 8 para textura e 1 para tamanho de ponto ou cinza. Esses registros interpolarão todos os dados que eles contêm para o sombreador de pixel. As declarações de registro de saída são necessárias e a semântica é atribuída a cada registro.

Os registros podem ser divididos da seguinte forma:

-   Pelo menos um registro deve ser declarado como um registro de posição de quatro componentes. Esse é o único registro de sombreador de vértice necessário.
-   Os dez primeiros registros consumidos por um sombreador podem usar até quatro componentes (xyzw) máximo.
-   O último (ou décimo segundo) registro pode conter apenas um escalar (como tamanho de ponto).

Para ver uma listagem dos registros, consulte [Registros – \_ versus 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).

### <a name="texture-sample-in-a-vertex-shader"></a>Amostra de textura em um sombreador de vértice

O sombreador de vértice 3 0 dá suporte à lookup de textura no sombreador de \_ vértice usando [o texldl – vs](texldl---vs.md).

## <a name="pixel-shader-model-3-features"></a>Recursos do Modelo 3 do Sombreador de Pixel

Os registros de cor e textura do sombreador de pixel foram recolhidos em dez registros de entrada (consulte [Tipos de registro de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)). O Registro Facial é um registro escalar de ponto flutuante. Somente o sinal desse registro é válido. Se o sinal for negativo, o primitivo será uma face traseira. Isso pode ser usado dentro de um sombreador de pixel para obter iluminação de dois lados, por exemplo. O Registro de Posição faz referência aos pixels atuais (x,y).

Os registros constantes do sombreador podem ser definidos usando:

-   [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a>Corresponder semântica em \_ \_ versus 3 0 e ps \_ 3 \_ 0 Sombreadores

Há algumas restrições de uso semântico com vs \_ 3 \_ 0 e ps \_ 3 \_ 0. Em geral, você precisa ter cuidado ao usar uma semântica para uma entrada de sombreador que corresponde a uma semântica usada em uma saída do sombreador.

Por exemplo, esse sombreador de pixel empacota vários nomes em um registro:


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



Cada registro tem uma semântica diferente. Observe que você também pode nomear v0.x e v0.yz com semântica diferente (várias) devido ao uso da máscara de gravação.

Considerando o sombreador de pixel, o seguinte sombreador \_ \_ versus 3 0 não pode ser emparelhado com ele:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



Esses dois sombreadores estão em conflito com o uso da semântica [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) e **D3DDECLUSAGE \_ TEXCOORD1.**

Reescreva o sombreador de vértice como este para evitar a colisão semântica:


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



Da mesma forma, um nome semântico declarado em diferentes registros de entrada no sombreador de pixel (v0 e v1 no sombreador de pixel) não pode ser usado em um único registro de saída nesse sombreador de vértice. Por exemplo, esse sombreador de vértice não pode ser emparelhado com o sombreador de pixel porque D3DDECLUSAGE TEXCOORD1 é usado para registros de entrada do sombreador de pixel (v0, v1) e o registro de saída do sombreador de \_ vértice o3.


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



Por outro lado, esse sombreador de vértice não pode ser emparelhado com o sombreador de pixel porque a máscara de saída para um parâmetro com uma determinada semântica não fornece os dados solicitados pelo sombreador de pixel:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



Esse sombreador de vértice não fornece uma saída com um dos nomes semânticos solicitados pelo sombreador de pixel, portanto, o emparelhamento do sombreador é inválido:


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



## <a name="fog-depth-and-shading-mode-changes"></a>Alterações no modo de sombra, profundidade e sombreamento

Quando D3DRS SHADEMODE é definido para sombreamento simples durante a rasterização de recorte e triângulo, os atributos com \_ D3DDECLUSAGE COLOR são interpolados como \_ sombreados simples. Se qualquer componente de um registro for declarado com uma semântica de cor, mas outros componentes do mesmo registro receberem semântica diferente, a interpolação de sombreamento simples (linear versus simples) será indefinida nos componentes que se registram sem uma semântica de cores.

Se a renderização de replicação for desejada, os sombreadores vs \_ 3 0 e \_ ps \_ 3 \_ 0 deverão implementar o torção. Nenhum cálculo de lodo é feito fora dos sombreadores. Não há nenhum registro de cinza em versus 3 0, e a semântica adicional D3DDECLUSAGE CHAP (para fator de combinação de blend computada por \_ \_ \_ vértice) e D3DDECLUSAGE DEPTH (para passar um valor de profundidade para o sombreador de pixel para calcular o fator de mesclagem de \_ mesclagem) foram adicionadas.

O estado do estágio de textura D3DTSS \_ TEXCOORDINDEX é ignorado ao usar o sombreador de pixel 3.0.

Os seguintes valores foram adicionados para acomodar essas alterações:


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

A matemática de ponto flutuante ocorre em diferentes precisões e intervalos (16 bits, 24 bits e 32 bits) em diferentes partes do pipeline. Um valor maior que o intervalo dinâmico do pipeline que entra nesse pipeline (por exemplo, um mapa de textura float de 32 bits é amostrado em um pipeline float de 24 bits em ps 2 0) cria um resultado \_ \_ indefinido. Para um comportamento previsível, você deve fixar esse valor no intervalo dinâmico máximo.

A conversão de um valor de ponto flutuante em um inteiro ocorre em vários locais, como:

-   Ao encontrar um [mova - vs instrução.](mova---vs.md)
-   Durante o endereçamento de textura.
-   Ao escrever em um destino de renderização de ponto não flutuante.

## <a name="specifying-full-or-partial-precision"></a>Especificando precisão total ou parcial

Ps \_ 3 \_ 0 e ps 2 x dão \_ suporte a dois níveis de \_ precisão:



| ps \_ 3 \_ 0 | ps \_ 2 \_ 0 | Precisão         | Valor                |
|----------|----------|-------------------|----------------------|
| x        |          | Completo              | fp32 ou superior       |
| x        |          | Precisão parcial | fp16=s10e5           |
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



| Modelo de sombreador                                           |  Recurso                                    |  Limite                                                                                                                                  |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
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

 

 
