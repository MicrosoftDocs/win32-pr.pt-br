---
title: Escrevendo sombreadores HLSL no Direct3D 9
description: Escrevendo sombreadores HLSL no Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 504a1d9ff5a2aa2b37227f0016cdc97d28d967fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007936"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a>Escrevendo sombreadores HLSL no Direct3D 9

-   [Vértice – noções básicas do sombreador](#vertex-shader-basics)
-   [Noções básicas do sombreador de pixel](#pixel-shader-basics)
    -   [Estágio de textura e Estados de amostra](#texture-stage-and-sampler-states)
    -   [Entradas do sombreador de pixel](#pixel-shader-inputs)
    -   [Saídas de sombreador de pixel](#pixel-shader-outputs)
-   [Entradas de sombreador e variáveis de sombreador](#shader-inputs-and-shader-variables)
    -   [Declarando variáveis de sombreador](#declaring-shader-variables)
    -   [Entradas de sombreador uniforme](#uniform-shader-inputs)
    -   [Variantes de entradas e semânticas de sombreador](#varying-shader-inputs-and-semantics)
    -   [Exemplos e objetos de textura](#samplers-and-texture-objects)
-   [Gravando funções](#writing-functions)
-   [Controle de fluxo](#flow-control)
-   [Tópicos relacionados](#related-topics)

## <a name="vertex-shader-basics"></a>Noções básicas do Vertex-Shader

Quando em operação, um sombreador de vértice programável substitui o processamento de vértice realizado pelo pipeline de gráficos do Microsoft Direct3D. Ao usar um sombreador de vértice, as informações de estado sobre as operações de transformação e iluminação são ignoradas pelo pipeline de função fixa. Quando o sombreador de vértice é desabilitado e o processamento de função fixa é retornado, todas as configurações de estado atuais se aplicam.

O mosaico de primitivos de ordem superior deve ser feito antes da execução do sombreador de vértice. As implementações que executam o mosaico de superfície após o processamento do sombreador devem fazer isso de forma que não seja aparente para o código do aplicativo e do sombreador.

Como um mínimo, um sombreador de vértice deve produzir a posição do vértice no espaço de clipe homogêneo. Opcionalmente, o sombreador de vértice pode gerar coordenadas de textura, cor de vértice, iluminação de vértice, fatores de neblina e assim por diante.

## <a name="pixel-shader-basics"></a>Noções básicas do Pixel-Shader

O processamento de pixel é executado por sombreadores de pixel em pixels individuais. Sombreadores de pixel funcionam em conjunto com sombreadores de vértice; a saída de um sombreador de vértice fornece as entradas para um sombreador de pixel. Outras operações de pixel (mesclagem de neblina, operações de estêncil e mesclagem de destino de renderização) ocorrem após a execução do sombreador.

### <a name="texture-stage-and-sampler-states"></a>Estágio de textura e Estados de amostra

Um sombreador de pixel substitui completamente a funcionalidade de mistura de pixels especificada pelo misturador de várias texturas, incluindo operações definidas anteriormente pelos Estados de estágio de textura. As operações de amostragem e filtragem de textura que foram controladas pelos Estados de estágio de textura padrão para minificação, ampliação, filtragem de MIP e os modos de endereçamento de encapsulamento podem ser inicializadas em sombreadores. O aplicativo é livre para alterar esses Estados sem exigir a regeneração do sombreador atualmente ligado. O estado da configuração pode se tornar ainda mais fácil se os sombreadores forem projetados dentro de um efeito.

### <a name="pixel-shader-inputs"></a>Entradas do sombreador de pixel

Para as versões do sombreador de pixel PS \_ 1 \_ 1-PS \_ 2 \_ 0, as cores difusa e especular são saturadas (clamped) no intervalo de 0 a 1 antes de serem usadas pelo sombreador.

A entrada de valores de cor para o sombreador de pixel é considerada uma perspectiva correta, mas isso não é garantido (para todos os hardwares). As cores amostradas das coordenadas de textura são iteradas de maneira correta da perspectiva e são clampeddas para o intervalo de 0 a 1 durante a iteração.

### <a name="pixel-shader-outputs"></a>Saídas de sombreador de pixel

Para as versões do sombreador de pixel PS \_ 1 \_ 1-PS \_ 1 \_ 4, o resultado emitido pelo sombreador de pixel é o conteúdo de Register r0. Tudo o que ele contém quando o sombreador conclui o processamento é enviado ao estágio de neblina e ao Blender de destino de renderização.

Para as versões PS \_ 2 \_ 0 e superior do pixel shader, a cor de saída é emitida de OC0-oC4.

## <a name="shader-inputs-and-shader-variables"></a>Entradas de sombreador e variáveis de sombreador

-   [Declarando variáveis de sombreador](#declaring-shader-variables)
-   [Entradas de sombreador uniforme](#uniform-shader-inputs)
-   [Variantes de entradas e semânticas de sombreador](#varying-shader-inputs-and-semantics)
-   [Exemplos e objetos de textura](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a>Declarando variáveis de sombreador

A declaração de variável mais simples inclui um tipo e um nome de variável, como esta declaração de ponto flutuante:


```
float fVar;
```



Você pode inicializar uma variável na mesma instrução.


```
float fVar = 3.1f;
```



Uma matriz de variáveis pode ser declarada,


```
int iVar[3];
```



ou declarados e inicializados na mesma instrução.


```
int iVar[3] = {1,2,3};
```



Aqui estão algumas declarações que demonstram muitas das características das variáveis de HLSL (linguagem de sombreamento de alto nível):


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



As declarações de dados podem usar qualquer tipo válido, incluindo:

-   [Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
-   [Tipo de vetor (DirectX HLSL)](dx-graphics-hlsl-vector.md)
-   [Tipo de matriz (DirectX HLSL)](dx-graphics-hlsl-matrix.md)
-   [Tipo de sombreador (DirectX HLSL)](dx-graphics-hlsl-shader.md)
-   [Tipo de amostra (DirectX HLSL)](dx-graphics-hlsl-sampler.md)
-   [Tipo definido pelo usuário (DirectX HLSL)](dx-graphics-hlsl-user-defined.md)

Um sombreador pode ter variáveis, argumentos e funções de nível superior.


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



As variáveis de nível superior são declaradas fora de todas as funções. Argumentos de nível superior são parâmetros para uma função de nível superior. Uma função de nível superior é qualquer função chamada pelo aplicativo (em oposição a uma função que é chamada por outra função).

### <a name="uniform-shader-inputs"></a>Entradas de sombreador uniforme

Os sombreadores de vértice e pixel aceitam dois tipos de dados de entrada: variáveis e uniformes. A entrada variável são os dados que são exclusivos para cada execução do sombreador. Para um sombreador de vértice, os dados variados (por exemplo: Position, normal, etc.) são provenientes dos fluxos de vértice. Os dados uniformes (por exemplo: cor do material, transformação mundial, etc.) são constantes para várias execuções de um sombreador. Para aqueles familiarizados com os modelos de sombreador de assembly, os dados uniformes são especificados por registros constantes e dados variados pelos registros v e t.

Os dados uniformes podem ser especificados por dois métodos. O método mais comum é declarar variáveis globais e usá-las em um sombreador. Qualquer uso de variáveis globais dentro de um sombreador resultará na adição dessa variável à lista de variáveis uniformes exigidas por esse sombreador. O segundo método é marcar um parâmetro de entrada da função de sombreador de nível superior como uniforme. Essa marcação Especifica que a variável fornecida deve ser adicionada à lista de variáveis uniformes.

As variáveis uniformes usadas por um sombreador são comunicadas de volta para o aplicativo por meio da tabela constante. A tabela constante é o nome da tabela de símbolos que define como as variáveis uniformes usadas por um sombreador se ajustam aos registros constantes. Os parâmetros de função uniforme aparecem na tabela de constantes precedidas por um cifrão ($), ao contrário das variáveis globais. O sinal de dólar é necessário para evitar colisões de nomes entre entradas uniformes locais e variáveis globais do mesmo nome.

A tabela constante contém os locais de registro constante de todas as variáveis uniformes usadas pelo sombreador. A tabela também inclui as informações de tipo e o valor padrão, se especificado.

### <a name="varying-shader-inputs-and-semantics"></a>Variantes de entradas e semânticas de sombreador

Os parâmetros de entrada variados (de uma função de sombreamento de nível superior) devem ser marcados com uma palavra-chave semântica ou uniforme indicando que o valor é constante para a execução do sombreador. Se uma entrada de sombreador de nível superior não estiver marcada com uma palavra-chave semântica ou uniforme, o sombreador não será compilado.

A semântica de entrada é um nome usado para vincular a entrada fornecida a uma saída da parte anterior do pipeline de gráficos. Por exemplo, a semântica de entrada POSITION0 é usada pelos sombreadores de vértice para especificar onde os dados de posição do buffer de vértice devem ser vinculados.

Os sombreadores de pixel e vértice têm conjuntos diferentes de semântica de entrada devido às diferentes partes do pipeline de gráficos que são alimentadas em cada unidade de sombreador. A semântica de entrada do sombreador de vértice descreve as informações por vértice (por exemplo: posição, normal, coordenadas de textura, cor, tangente, binormal, etc.) a serem carregadas de um buffer de vértice em um formulário que pode ser consumido pelo sombreador de vértice. A semântica de entrada é mapeada diretamente para o uso da declaração de vértice e o índice de uso.

A semântica de entrada do sombreador de pixel descreve as informações fornecidas por pixel pela unidade de rasterização. Os dados são gerados por interpolação entre saídas do sombreador de vértice para cada vértice do primitivo atual. A semântica de entrada do sombreador de pixel básico vincula a cor de saída e as informações de coordenadas de textura a parâmetros de entrada.

A semântica de entrada pode ser atribuída à entrada de sombreador por dois métodos:

-   Acrescentar dois-pontos e o nome semântico à declaração de parâmetro.
-   Definição de uma estrutura de entrada com semântica de entrada atribuída a cada membro da estrutura.

Os sombreadores de vértice e pixel fornecem dados de saída para o estágio de pipeline de gráficos subsequente. A semântica de saída é usada para especificar como os dados gerados pelo sombreador devem ser vinculados às entradas do próximo estágio. Por exemplo, a semântica de saída para um sombreador de vértice é usada para vincular as saídas dos interpoladores no rasterizador para gerar os dados de entrada para o sombreador de pixel. As saídas do sombreador de pixel são os valores fornecidos para a unidade de mesclagem alfa para cada um dos destinos de renderização ou o valor de profundidade gravado no buffer de profundidade.

A semântica de saída do sombreador de vértice é usada para vincular o sombreador ao sombreador de pixel e ao estágio do rasterizador. Um sombreador de vértice que é consumido pelo rasterizador e não exposto ao sombreador de pixel deve gerar dados de posição como um mínimo. Os sombreadores de vértice que geram coordenadas de textura e dados de cor fornecem esses dados para um sombreador de pixel após a conclusão da interpolação.

A semântica de saída do sombreador de pixel associa as cores de saída de um sombreador de pixel com o destino de renderização correto. A cor de saída do sombreador de pixel é vinculada ao estágio Alpha Blend, que determina como os destinos de renderização de destino são modificados. A saída de profundidade do sombreador de pixel pode ser usada para alterar os valores de profundidade de destino no local de varredura atual. A saída de profundidade e vários destinos de renderização só têm suporte com alguns modelos de sombreador.

A sintaxe para a semântica de saída é idêntica à sintaxe para especificar a semântica de entrada. A semântica pode ser especificada diretamente em parâmetros declarados como parâmetros "out" ou atribuídas durante a definição de uma estrutura que é retornada como um parâmetro "out" ou o valor de retorno de uma função.

A semântica identifica de onde vêm os dados. A semântica são identificadores opcionais que identificam entradas e saídas de sombreador. A semântica aparece em um dos três locais:

-   Depois de um membro da estrutura.
-   Depois de um argumento na lista de argumentos de entrada de uma função.
-   Após a lista de argumentos de entrada da função.

Este exemplo usa uma estrutura para fornecer uma ou mais entradas de sombreador de vértice e outra estrutura para fornecer uma ou mais saídas de sombreador de vértice. Cada um dos membros da estrutura usa uma semântica.


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



A estrutura de entrada identifica os dados do buffer de vértice que fornecerá as entradas do sombreador. Esse sombreador mapeia os dados dos elementos position, normal e blendweight do buffer de vértice em registros de sombreador de vértice. O tipo de dados de entrada não precisa corresponder exatamente ao tipo de dados de declaração de vértice. Se não corresponder exatamente, os dados do vértice serão automaticamente convertidos no tipo de dados do HLSL quando forem gravados nos registros do sombreador. Por exemplo, se os dados normais foram definidos para serem do tipo UINT pelo aplicativo, ele seria convertido em um float3 quando lido pelo sombreador.

Se os dados no fluxo de vértice contiverem menos componentes do que o tipo de dados do sombreador correspondente, os componentes ausentes serão inicializados como 0 (exceto para w, que é inicializado como 1).

A semântica de entrada é semelhante aos valores no [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).

A estrutura de saída identifica os parâmetros de saída do sombreador de vértice de posição e cor. Essas saídas serão usadas pelo pipeline para a rasterização de triângulo (no processamento primitivo). A saída marcada como dados de posição denota a posição de um vértice no espaço homogêneo. Como um mínimo, um sombreador de vértice deve gerar dados de posição. A posição do espaço da tela é calculada após a conclusão do sombreador de vértice, dividindo a coordenada (x, y, z) por w. No espaço da tela,-1 e 1 são os valores x e y mínimo e máximo dos limites do visor, enquanto z é usado para teste de buffer z.

A semântica de saída também é semelhante aos valores em [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage). Em geral, uma estrutura de saída para um sombreador de vértice também pode ser usada como a estrutura de entrada para um sombreador de pixel, desde que o sombreador de pixel não leia nenhuma variável marcada com a posição, o tamanho do ponto ou a semântica de neblina. Essas semânticas estão associadas a valores escalares por vértice que não são usados por um sombreador de pixel. Se esses valores forem necessários para o sombreador de pixel, eles poderão ser copiados em outra variável de saída que usa uma semântica de sombreador de pixel.

Variáveis globais são atribuídas a registros automaticamente pelo compilador. As variáveis globais também são chamadas de parâmetros uniformes porque o conteúdo da variável é o mesmo para todos os pixels processados cada vez que o sombreador é chamado. Os registros estão contidos na tabela de constantes, que pode ser lida usando a interface [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) .

A semântica de entrada para sombreadores de pixel mapeia valores em registros de hardware específicos para transporte entre sombreadores de vértice e sombreadores de pixel. Cada tipo de registro tem propriedades específicas. Como atualmente há apenas duas semânticas para coordenadas de cor e textura, é comum que a maioria dos dados seja marcada como uma coordenada de textura mesmo quando não estiver.

Observe que a estrutura de saída do sombreador de vértice usou uma entrada com dados de posição, que não é usada pelo sombreador de pixel. O HLSL permite dados de saída válidos de um sombreador de vértice que não são dados de entrada válidos para um sombreador de pixel, desde que ele não seja referenciado no sombreador de pixel.

Os argumentos de entrada também podem ser matrizes. A semântica é incrementada automaticamente pelo compilador para cada elemento da matriz. Por exemplo, considere a seguinte declaração explícita:


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



A declaração explícita fornecida acima é equivalente à declaração a seguir que terá semânticas incrementadas automaticamente pelo compilador:


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



Assim como a semântica de entrada, a semântica de saída identifica o uso de dados para dados de saída do sombreador de pixel. Muitos sombreadores de pixel gravam em apenas uma cor de saída. Os sombreadores de pixel também podem gravar um valor de profundidade em um ou mais destinos de renderização múltiplos ao mesmo tempo (até quatro). Como os sombreadores de vértice, os sombreadores de pixel usam uma estrutura para retornar mais de uma saída. Esse sombreador grava 0 nos componentes de cor, bem como no componente de profundidade.


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



As cores de saída do sombreador de pixel devem ser do tipo FLOAT4. Ao escrever várias cores, todas as cores de saída devem ser usadas de forma contígua. Em outras palavras, [COLOR1](dx-graphics-hlsl-semantics.md) não pode ser uma saída, a menos que [COLOR0](dx-graphics-hlsl-semantics.md) já tenha sido gravado. A saída de profundidade do sombreador de pixel deve ser do tipo float1.

### <a name="samplers-and-texture-objects"></a>Exemplos e objetos de textura

Um classificador contém o estado de amostra. O estado de amostra especifica a textura a ser amostrada e controla a filtragem feita durante a amostragem. Três coisas são necessárias para fazer amostras de uma textura:

-   Uma textura
-   Uma amostra (com o estado de amostra)
-   Uma instrução de amostragem

Os exemplos podem ser inicializados com texturas e estado de amostra, conforme mostrado aqui:


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



Aqui está um exemplo do código para exemplo de uma textura 2D:


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



A textura é declarada com uma variável de textura tex0.

Neste exemplo, uma variável de amostra chamada s \_ 2D é declarada. O classificador contém o estado de amostra dentro de chaves. Isso inclui a textura que será amostrada e, opcionalmente, o estado do filtro (ou seja, modos de encapsulamento, modos de filtro, etc.). Se o estado de amostra for omitido, um estado de amostra padrão será aplicado especificando a filtragem linear e um modo de encapsulamento para as coordenadas de textura. A função de amostra usa uma coordenada de textura de ponto flutuante de dois componentes e retorna uma cor de dois componentes. Isso é representado com o tipo de retorno float2 e representa dados nos componentes vermelho e verde.

Quatro tipos de amostra são definidos (consulte as [palavras-chave](dx-graphics-hlsl-appendix.md)) e as pesquisas de textura são executadas pelas funções intrínsecas [**: tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**Tex3D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE (s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md). Aqui está um exemplo de amostragem 3D:


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



Esta declaração de amostra usa o estado de amostra padrão para as configurações de filtro e o modo de endereço.

Este é o exemplo de amostragem de cubo correspondente:


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



E, finalmente, aqui está o exemplo de amostragem 1D:


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



Como o tempo de execução não dá suporte a texturas 1D, o compilador usará uma textura 2D com o conhecimento de que a coordenada y não é importante. Como [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) é implementado como uma pesquisa de textura 2D, o compilador é livre para escolher o componente y de maneira eficiente. Em alguns cenários raros, o compilador não pode escolher um componente y eficiente; nesse caso, ele emitirá um aviso.


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



Esse exemplo específico é ineficiente porque o compilador deve mover a coordenada de entrada para outro registro (porque uma pesquisa 1D é implementada como uma pesquisa 2D e a coordenada de textura é declarada como um float1). Se o código for reescrito usando uma entrada float2 em vez de um float1, o compilador poderá usar a coordenada de textura de entrada porque sabe que y foi inicializada para algo.


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



Todas as pesquisas de textura podem ser acrescentadas com "bias" ou "proj" (ou seja, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**TEXCUBEPROJ (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)). Com o sufixo "proj", a coordenada de textura é dividida pelo componente w. Com "tendência", o nível MIP é deslocado pelo componente w-. Assim, todas as pesquisas de textura com um sufixo sempre usam uma entrada FLOAT4. [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) e [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignoram os componentes YZ e z, respectivamente.

Os exemplos também podem ser usados na matriz, embora nenhum back-end atualmente ofereça suporte ao acesso de matriz dinâmica de amostras. Portanto, o seguinte é válido porque pode ser resolvido no momento da compilação:


```
tex2D(s[0],tex)
```



No entanto, este exemplo não é válido.


```
tex2D(s[a],tex)
```



O acesso dinâmico de amostras é útil principalmente para escrever programas com loops literais. O código a seguir ilustra o acesso à matriz de amostras:


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> O uso do Microsoft Direct3D Debug Runtime pode ajudá-lo a detectar incompatibilidades entre o número de componentes em uma textura e uma amostra.

 

## <a name="writing-functions"></a>Gravando funções

As funções dividem tarefas grandes em partes menores. Tarefas pequenas são mais fáceis de depurar e podem ser reutilizadas, uma vez comprovadas. As funções podem ser usadas para ocultar detalhes de outras funções, o que torna um programa composto por funções mais fácil de seguir.

As funções HLSL são semelhantes às funções C de várias maneiras: elas contêm uma definição e um corpo de função e ambas declaram tipos de retorno e listas de argumentos. Como as funções do C, a validação de HLSL faz a verificação de tipo nos argumentos, nos tipos de argumento e no valor de retorno durante a compilação do sombreador.

Ao contrário das funções de C, as funções de ponto de entrada HLSL usam a semântica para associar argumentos de função a entradas e saídas de sombreador (funções HLSL chamadas de semântica de ignorar internamente). Isso facilita a vinculação de dados de buffer a um sombreador e a vinculação de saídas de sombreador a entradas de sombreador.

Uma função contém uma declaração e um corpo, e a declaração deve preceder o corpo.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



A declaração de função inclui tudo na frente das chaves:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Uma declaração de função contém:

-   Um tipo de retorno
-   Um nome de função
-   Uma lista de argumentos (opcional)
-   Uma semântica de saída (opcional)
-   Uma anotação (opcional)

O tipo de retorno pode ser qualquer um dos tipos de dados básicos do HLSL, como um FLOAT4:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



O tipo de retorno pode ser uma estrutura que já foi definida:


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



Se a função não retornar um valor, void poderá ser usado como o tipo de retorno.


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



O tipo de retorno sempre aparece primeiro em uma declaração de função.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Uma lista de argumentos declara os argumentos de entrada para uma função. Ele também pode declarar valores que serão retornados. Alguns argumentos são argumentos de entrada e saída. Aqui está um exemplo de um sombreador que usa quatro argumentos de entrada.


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



Essa função retorna uma cor final, que é uma mistura de um exemplo de textura e a cor clara. A função usa quatro entradas. Duas entradas têm semântica: LightDir tem a semântica [TEXCOORD1](dx-graphics-hlsl-semantics.md) e texcrd tem a semântica [TEXCOORD0](dx-graphics-hlsl-semantics.md) . A semântica significa que os dados dessas variáveis serão provenientes do buffer de vértice. Embora a variável LightDir tenha uma semântica [TEXCOORD1](dx-graphics-hlsl-semantics.md) , o parâmetro provavelmente não é uma coordenada de textura. O tipo semântico de TEXCOORDn geralmente é usado para fornecer uma semântica para um tipo que não é predefinido (não há semântica de entrada de sombreador de vértice para uma direção clara).

As outras duas entradas LightColor e SAMP são rotuladas com a palavra-chave [uniforme](dx-graphics-hlsl-appendix.md) . Essas são constantes uniformes que não serão alteradas entre chamadas de desenho. Os valores para esses parâmetros vêm de variáveis globais do sombreador.

Os argumentos podem ser rotulados como entradas com a palavra-chave in e os argumentos de saída com a palavra-chave out. Os argumentos não podem ser passados por referência; no entanto, um argumento pode ser uma entrada e uma saída se ela for declarada com a palavra-chave InOut. Os argumentos passados para uma função que são marcados com a palavra-chave Inout são considerados cópias do original até que a função seja retornada, e elas são copiadas de volta. Veja um exemplo usando o Inout:


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



Essa função incrementa os valores em A e B e os retorna.

O corpo da função é todo o código após a declaração da função.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



O corpo consiste em instruções que estão entre chaves. O corpo da função implementa toda a funcionalidade usando variáveis, literais, expressões e instruções.

O corpo do sombreador faz duas coisas: ele executa uma multiplicação de matriz e retorna um resultado de FLOAT4. A multiplicação de matriz é realizada com a função [**Mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) , que executa uma multiplicação de matriz 4x4. **Mul (DirectX HLSL)** é chamado de função intrínseca porque já está embutido na biblioteca HLSL de funções. As funções intrínsecas serão abordadas com mais detalhes na próxima seção.

A matriz multiplique combina um PDV de vetor de entrada e uma WorldViewProj de matriz composta. O resultado é a posição dos dados transformados no espaço da tela. Esse é o processamento mínimo de sombreador de vértice que podemos fazer. Se estivesse usando o pipeline de função fixa em vez de um sombreador de vértice, os dados de vértice poderiam ser desenhados depois de fazer essa transformação.

A última instrução em um corpo de função é uma instrução return. Assim como C, essa instrução retorna o controle da função para a instrução que chamou a função.

Os tipos de retorno de função podem ser qualquer um dos tipos de dados simples definidos em HLSL, incluindo bool, Half int, float e Double. Os tipos de retorno podem ser um dos tipos de dados complexos, como vetores e matrizes. Os tipos HLSL que se referem a objetos não podem ser usados como tipos de retorno. Isso inclui PixelShader, vertexshader, Texture e Sample.

Aqui está um exemplo de uma função que usa uma estrutura para um tipo de retorno.


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



O tipo de retorno FLOAT4 foi substituído pela estrutura VS \_ output, que agora contém um único membro FLOAT4.

Uma instrução return sinaliza o final de uma função. Essa é a instrução de retorno mais simples. Ele retorna o controle da função para o programa de chamada. Ele não retorna nenhum valor.


```
void main()
{
    return ;
}
```



Uma instrução return pode retornar um ou mais valores. Este exemplo retorna um valor literal:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



Este exemplo retorna o resultado escalar de uma expressão:


```
return  light.enabled = true ;
```



Este exemplo retorna um FLOAT4 construído a partir de uma variável local e um literal:


```
return  float4(color.rgb, 1) ;
```



Este exemplo retorna um FLOAT4 que é construído a partir do resultado retornado de uma função intrínseca e alguns valores literais:


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



Este exemplo retorna uma estrutura que contém um ou mais membros:


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a>Controle de fluxo

A maioria dos hardwares de vértice e de sombreador de pixel atual foi projetada para executar um sombreador linha por linha, executando cada instrução uma vez. O HLSL dá suporte ao controle de fluxo, que inclui ramificação estática, instruções predicadas, loop estático, ramificação dinâmica e loop dinâmico.

Anteriormente, o uso de uma instrução If resultou em um código de sombreador de linguagem de assembly que implementa tanto o lado If quanto o lado else do fluxo de código. Aqui está um exemplo do código no HLSL que foi compilado para vs \_ 1 \_ 1:


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



E aqui está o código do assembly resultante:


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



Alguns hardwares permitem o loop estático ou dinâmico, mas a maioria exige execução linear. Nos modelos que não dão suporte a looping, todos os loops devem ser não revertidos. Um exemplo é a amostra de exemplo [DepthOfField](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) que usa loops não acumulados até mesmo para os \_ \_ sombreadores PS 1 1.

O HLSL agora inclui suporte para cada um desses tipos de controle de fluxo:

-   ramificação estática
-   instruções predicadas
-   loop estático
-   ramificação dinâmica
-   loop dinâmico

A ramificação estática permite que blocos de código de sombreador sejam ativados ou desativados com base em uma constante de sombreador booliano. Esse é um método conveniente para habilitar ou desabilitar caminhos de código com base no tipo de objeto que está sendo processado no momento. Entre chamadas de desenho, você pode decidir quais recursos deseja dar suporte com o sombreador atual e, em seguida, definir os sinalizadores boolianos necessários para obter esse comportamento. Todas as instruções que são desabilitadas por uma constante booliana são ignoradas durante a execução do sombreador.

O suporte de ramificação mais familiar é a ramificação dinâmica. Com a ramificação dinâmica, a condição de comparação reside em uma variável, o que significa que a comparação é feita para cada vértice ou cada pixel em tempo de execução (ao contrário da comparação que ocorre no momento da compilação ou entre duas chamadas de desenho). O impacto no desempenho é o custo da ramificação mais o custo das instruções no lado da ramificação obtidas. A ramificação dinâmica é implementada no sombreador modelo 3 ou superior. Otimizar os sombreadores que funcionam com esses modelos é semelhante a otimizar o código executado em uma CPU.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 