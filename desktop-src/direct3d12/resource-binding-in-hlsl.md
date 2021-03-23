---
title: Associação de recursos em HLSL
description: Este tópico descreve alguns recursos específicos do usando o modelo de sombreador HLSL (sombreamento de alto nível) 5,1 com o Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 01039550f07de57fb7b2f1e815bced02e549c741
ms.sourcegitcommit: 60120d10c957815d79af566c72e5f4bcfaca4025
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/23/2021
ms.locfileid: "104837484"
---
# <a name="resource-binding-in-hlsl"></a>Associação de recursos em HLSL

Este tópico descreve alguns recursos específicos do usando o [modelo de sombreador](/windows/desktop/direct3dhlsl/shader-model-5-1) HLSL (sombreamento de alto nível) 5,1 com o Direct3D 12. Todo o hardware do Direct3D 12 dá suporte ao modelo de sombreador 5,1, portanto, o suporte para esse modelo não depende do nível de recurso de hardware.

## <a name="resource-types-and-arrays"></a>Tipos de recursos e matrizes

A sintaxe de recurso do Shader Model 5 (SM 5.0) usa a `register` palavra-chave para retransmitir informações importantes sobre o recurso para o compilador HLSL. Por exemplo, a instrução a seguir declara uma matriz de quatro texturas associadas a Slots T3, T4, T5 e T6. T3 é o único slot de registro que aparece na instrução, simplesmente sendo o primeiro na matriz de quatro.

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

A sintaxe de recurso do Shader Model 5,1 (SM 5.1) no HLSL é baseada na sintaxe de recurso de registro existente, para permitir portabilidade mais fácil. Os recursos do Direct3D 12 no HLSL estão associados a registros virtuais em espaços de registro lógico:

-   t – para exibições de recurso do sombreador (SRV)
-   s – para exemplos
-   u – para exibições de acesso não ordenado (UAV)
-   b – para exibições de buffer de constantes (CBV)

A assinatura raiz que faz referência ao sombreador deve ser compatível com os slots de registro declarados. Por exemplo, a seguinte parte de uma assinatura raiz seria compatível com o uso de Slots de textura T3 por meio de T6, pois descreve uma tabela de descritores com slots T0 a T98.

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

Uma declaração de recurso pode ser escalar, uma matriz 1D ou uma matriz multidimensional:

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

O SM 5.1 usa os mesmos tipos de recursos e tipos de elementos que o SM 5.0 faz. Os limites de declaração SM 5.1 são mais flexíveis e restritos apenas pelos limites de tempo de execução/hardware. A `space` palavra-chave especifica a qual espaço de registro lógico a variável declarada está associada. Se a `space` palavra-chave for omitida, o índice de espaço padrão 0 será atribuído implicitamente ao intervalo (de modo que o `tex2` intervalo acima resida `space0` ). `register(t3,  space0)` Nunca entrará em conflito com `register(t3,  space1)` , nem com nenhuma matriz em outro espaço que possa incluir T3.

Um recurso de matriz pode ter um tamanho não associado, que é declarado especificando a primeira dimensão como vazia ou 0:

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

A tabela de descritores de correspondência pode ser:

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

Uma matriz não associada em HLSL corresponde a um número fixo definido com `numDescriptors` na tabela de descritores e um tamanho fixo em HLSL corresponde a uma declaração não associada na tabela de descritores.

Matrizes multidimensionais são permitidas, incluindo um tamanho não associado. Essas matrizes multidimensionais são achatadas no espaço de registro.

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

Não é permitido alias de intervalos de recursos. Em outras palavras, para cada tipo de recurso (t, s, u, b), os intervalos de registro declarados não deve se sobrepõem. Isso também inclui intervalos não associados. Intervalos declarados em espaços de registro diferentes nunca se sobrepõem. Observe que o não associado `tex2` (acima) reside no `space0` , embora `tex3` não esteja associado `space1` , de modo que eles não se sobreponham.

O acesso a recursos que foram declarados como matrizes é tão simples quanto indexá-los.

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

Há uma restrição padrão importante no uso dos índices ( `myMaterialID` e `samplerID` no código acima), pois eles não têm permissão para variar em uma [onda](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology). Mesmo alterando o índice com base em contagens de instâncias como variáveis.

Se a variação do índice for necessária, especifique o `NonUniformResourceIndex` qualificador no índice, por exemplo:

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

Em alguns hardwares, o uso desse qualificador gera código adicional para impor a exatidão (incluindo entre threads), mas com um custo de desempenho secundário. Se um índice for alterado sem esse qualificador e dentro de um empate/expedição, os resultados serão indefinidos.

## <a name="descriptor-arrays-and-texture-arrays"></a>Matrizes de descritores e matrizes de textura

As matrizes de textura estão disponíveis desde o DirectX 10. As matrizes de textura exigem um descritor, no entanto, todas as fatias de matriz devem compartilhar o mesmo formato, largura, altura e contagem de MIP. Além disso, a matriz deve ocupar um intervalo contíguo no espaço de endereço virtual. O código a seguir mostra um exemplo de como acessar uma matriz de textura de um sombreador.

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

Em uma matriz de textura, o índice pode ser variado livremente, sem a necessidade de qualificadores como `NonUniformResourceIndex` .

A matriz de descritor equivalente seria:

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

Observe que o uso inadequado de um float para o índice de matriz é substituído por `myArrayOfTex2D[2]` . Além disso, as matrizes de descritores oferecem mais flexibilidade com as dimensões. O tipo, `Texture2D` é este exemplo, não pode variar, mas o formato, a largura, a altura e a contagem MIP podem variar com cada descritor.

É legítimo ter uma matriz de descritores de matrizes de textura:

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

Não é legítimo declarar uma matriz de estruturas, cada estrutura contendo descritores, por exemplo, o código a seguir não tem suporte.

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

Isso teria permitido o layout de memória **abcabcabc..**., mas é uma limitação de idioma e não tem suporte. Um método com suporte para fazer isso seria o seguinte, embora o layout de memória nesse caso seja **AAA... bbb... CCC...**

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

Para obter o layout **abcabcabc...** Memory, use uma tabela de descritor sem usar a `myStruct` estrutura.

## <a name="resource-aliasing"></a>Alias de recurso

Os intervalos de recursos especificados nos sombreadores HLSL são intervalos lógicos. Eles são associados a intervalos concretos de heap em tempo de execução por meio do mecanismo de assinatura raiz. Normalmente, um intervalo lógico é mapeado para um intervalo de heap que não se sobrepõe a outros intervalos de heap. No entanto, o mecanismo de assinatura raiz torna possível o alias (sobreposição) de intervalos de heap de tipos compatíveis. Por exemplo, `tex2` e os `tex3` intervalos do exemplo acima podem ser mapeados para o mesmo intervalo de heap (ou sobreposição), que tem o efeito de texturas de alias no programa HLSL. Se tal alias for desejado, o sombreador deverá ser compilado com \_ \_ a opção de alias d3d10 Shader Resources \_ \_ , que é definida usando a opção */res de \_ \_ alias de maio* para a ferramenta de compilador de [efeito](/windows/win32/direct3dtools/fxc) (FXC). A opção faz com que o compilador produza o código correto impedindo determinadas otimizações de carga/armazenamento sob a suposição de que os recursos podem ser alias.

## <a name="divergence-and-derivatives"></a>Divergência e derivações

O SM 5.1 não impõe limitações no índice de recursos; ou seja, ` tex2[idx].Sample(…)` – o índice Idx pode ser uma constante literal, uma constante CBuffer ou um valor interpolado. Embora o modelo de programação ofereça uma grande flexibilidade, há problemas a serem considerados:

-   Se o índice divergir em um quad, as quantidades derivadas e derivados de hardware computadas, como LOD, poderão ser indefinidas. O compilador HLSL também faz o melhor esforço para emitir um aviso nesse caso, mas não impedirá que um sombreador seja compilado. Esse comportamento é semelhante à computação de derivações no fluxo de controle divergente.
-   Se o índice de recursos for divergente, o desempenho será reduzido em comparação com o caso de um índice uniforme, pois o hardware precisa executar operações em vários recursos. Os índices de recursos que podem ser divergentes devem ser marcados com a `NonUniformResourceIndex` função no código HLSL. Caso contrário, os resultados serão indefinidos.

## <a name="uavs-in-pixel-shaders"></a>UAVs em sombreadores de pixel

O SM 5.1 não impõe restrições em intervalos de UAV em sombreadores de pixel como foi o caso do SM 5.0.

## <a name="constant-buffers"></a>Buffers de constantes

A sintaxe de CBuffer (buffers de constantes) do SM 5.1 foi alterada do SM 5.0 para permitir que os desenvolvedores indexem buffers constantes. Para habilitar buffers constantes indexáveis, o SM 5.1 apresenta a `ConstantBuffer` construção "template":

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

O código anterior declara a variável de buffer constante `myCB1` do tipo `Foo` e do tamanho 6, e uma variável de buffer escalar e constante `myCB2` . Uma variável de buffer constante agora pode ser indexada no sombreador como:

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

Os campos ' a ' e ' b ' não se tornam variáveis globais, mas, em vez disso, devem ser tratados como campos. Para compatibilidade com versões anteriores, o SM 5.1 dá suporte ao conceito antigo de CBuffer para cbuffers escalar. A instrução a seguir faz com que ' a ' e ' b ' as variáveis globais somente leitura como no SM 5.0. No entanto, esse CBuffer de estilo antigo não pode ser indexável.

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

Atualmente, o compilador do sombreador dá suporte `ConstantBuffer` apenas ao modelo para estruturas definidas pelo usuário.

Por motivos de compatibilidade, o compilador HLSL pode atribuir automaticamente registros de recursos para intervalos declarados em `space0` . Se ' Space ' for omitido na cláusula Register, o padrão `space0` será usado. O compilador usa a heurística do primeiro perfuração para atribuir os registros. A atribuição pode ser recuperada por meio da API de reflexão, que foi estendida para adicionar o campo *espaço* para espaço, enquanto o campo *BindPoint* indica o limite inferior do intervalo de registro de recursos.

## <a name="bytecode-changes-in-sm51"></a>Alterações de código de bytes no SM 5.1

O SM 5.1 altera como os registros de recursos são declarados e referenciados em instruções. A sintaxe envolve a declaração de uma "variável" de registro, semelhante ao modo como é feito para os registros de memória compartilhada do Grupo:

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

Isso desmontará para:

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

Cada intervalo de recursos do sombreador agora tem uma ID (um nome) que é exclusiva para o código de bytes do sombreador. Por exemplo, a matriz de textura tex1 (T10) se torna 1 "no código de bytes do sombreador. Atribuir IDs exclusivas a cada intervalo de recursos permite duas coisas:

-   Identifique de forma não ambígua qual intervalo de recursos (consulte o \_ recurso DCL \_ Texture2D) está sendo indexado em uma instrução (consulte a instrução de exemplo).
-   Anexando um conjunto de atributos à declaração, por exemplo, tipo de elemento, tamanho de Stride, modo de operação de varredura, etc.

Observe que a ID do intervalo não está relacionada à declaração de limite inferior do HLSL.

A ordem das associações de recursos de reflexão (listagem na parte superior) e as instruções de declaração de sombreador (DCL \_ \* ) são as mesmas para auxiliar na identificação da correspondência entre as variáveis HLSL e as IDs de código de bytes.

Cada instrução de declaração no SM 5.1 usa um operando 3D para definir: ID de intervalo, limites inferiores e superiores. Um token adicional é emitido para especificar o espaço de registro. Outros tokens podem ser emitidos também para transmitir propriedades adicionais do intervalo, por exemplo, CBuffer ou instrução de declaração de buffer estruturado emite o tamanho do CBuffer ou da estrutura. Os detalhes exatos da codificação podem ser encontrados em d3d12TokenizedProgramFormat. h e **D3D10ShaderBinary:: CShaderCodeParser**.

As instruções do SM 5.1 não emitirão informações adicionais do operando de recurso como parte da instrução (como no SM 5.0). Essas informações agora estão nas instruções da declaração. No SM 5.0, as instruções de indexação de recursos exigiam atributos de recurso a serem descritos em tokens de opcode estendidos, já que a indexação ofusca a associação à declaração. No SM 5.1, cada ID (como ' t 1 ') é associada sem ambigüidade a uma única declaração que descreve as informações de recursos necessárias. Portanto, os tokens de opcode estendidos usados em instruções para descrever as informações de recursos não são mais emitidos.

Em instruções de não declaração, um operando de recurso para amostras, SRVs e UAVs é um operando 2D. O primeiro índice é uma constante literal que especifica a ID do intervalo. O segundo índice representa o valor linear do índice. O valor é calculado em relação ao início do espaço de registro correspondente (não relativo ao início do intervalo lógico) para correlacionar melhor com a assinatura raiz e para reduzir a carga do compilador de driver de ajustar o índice.

Um operando de recurso para CBVs é um operando 3D, contendo: ID literal do intervalo, índice do buffer de constantes, offset na instância específica do buffer de constantes.

## <a name="example-hlsl-declarations"></a>Declarações HLSL de exemplo

Os programas HLSL não precisam saber nada sobre assinaturas raiz. Eles podem atribuir associações ao espaço de associação virtual "Register", t \# para SRVs, u \# para UAVs, b \# para CBVs, s \# para amostragens ou dependem do compilador para selecionar atribuições (e consultar os mapeamentos resultantes usando a reflexão do sombreador posteriormente). As tabelas de descritores de mapeamentos de assinatura raiz e as constantes raiz para esse espaço de registro virtual.

Veja a seguir algumas declarações de exemplo que um sombreador HLSL pode ter. Observe que não há referências a assinaturas raiz ou tabelas de descritores.

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a>Tópicos relacionados

* [Indexação dinâmica usando HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
* [Efeito-ferramenta do compilador](/windows/win32/direct3dtools/fxc)
* [Recursos do HLSL Shader Model 5,1 para Direct3D 12](/windows/win32/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
* [Exibições ordenadas do rasterizador](rasterizer-order-views.md)
* [Associação de recursos](resource-binding.md)
* [Assinaturas raiz](root-signatures.md)
* [Modelo do sombreador 5,1](/windows/win32/direct3dhlsl/shader-model-5-1)
* [Valor de referência de estêncil especificado do sombreador](shader-specified-stencil-reference-value.md)
* [Especificando assinaturas raiz em HLSL](specifying-root-signatures-in-hlsl.md)
