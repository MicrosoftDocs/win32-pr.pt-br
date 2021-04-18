---
description: Este tópico descreve as considerações e as estratégias de otimização com a biblioteca DirectXMath.
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: Otimização de código com a biblioteca DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11b331077e3d6538952a2f7956641b8b3919e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813510"
---
# <a name="code-optimization-with-the-directxmath-library"></a>Otimização de código com a biblioteca DirectXMath

Este tópico descreve as considerações e as estratégias de otimização com a biblioteca DirectXMath.

-   [Usar acessadores com moderação](#use-accessors-sparingly)
-   [Usar as configurações de compilação corretas](#use-correct-compilation-settings)
-   [Use as funções de est quando apropriado](#use-est-functions-when-appropriate)
-   [Usar operações e tipos de dados alinhados](#use-aligned-data-types-and-operations)
-   [Alinhar as alocações corretamente](#properly-align-allocations)
-   [Evite sobrecargas de operador quando possível](#avoid-operator-overloads-when-possible)
-   [Desnormalizado](#denormals)
-   [Aproveite a dupla de ponto flutuante de inteiro](#take-advantage-of-the-integer-floating-point-duality)
-   [Preferir formulários de modelo](#prefer-template-forms)
-   [Usando o DirectXMath com o Direct3D](#using-directxmath-with-direct3d)
-   [Tópicos relacionados](#related-topics)

## <a name="use-accessors-sparingly"></a>Usar acessadores com moderação

As operações baseadas em vetor usam os conjuntos de instruções SIMD e usam registros especiais. O acesso a componentes individuais exige a mudança dos registros de SIMD para os Scalar e vice-versa.

Quando possível, é mais eficiente inicializar todos os componentes de um [**XMVECTOR**](xmvector-data-type.md) ao mesmo tempo, em vez de usar uma série de acessadores de vetores individuais.

## <a name="use-correct-compilation-settings"></a>Usar as configurações de compilação corretas

Para destinos do Windows x86, habilite/Arch: SSE2. Para todos os destinos do Windows, habilite/fp: Fast.

Por padrão, a compilação na biblioteca DirectXMath para destinos do Windows x86 é feita com \_ XM \_ SSE \_ intrínsecos \_ definidos. Isso significa que toda a funcionalidade do DirectXMath fará uso de instruções SSE2. No entanto, o mesmo não é verdadeiro para outro código.

O código fora do DirectXMath é tratado usando padrões do compilador. Sem essa opção, o código gerado geralmente pode usar o código x87 menos eficiente.

É altamente recomendável que você sempre use a versão mais recente disponível do compilador.

## <a name="use-est-functions-when-appropriate"></a>Use as funções de est quando apropriado

Muitas funções têm uma função de estimativa equivalente que termina em est. Essas funções comercializam alguma precisão para melhorar o desempenho. As funções de est são apropriadas para cálculos não críticos, onde a precisão pode ser sacrificada por velocidade. A quantidade exata de precisão e aumento de velocidade perdido são dependentes da plataforma.

Por exemplo, a função [**XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) pode ser usada no lugar da função [**XMVector3AngleBetweenNormals**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals) .

## <a name="use-aligned-data-types-and-operations"></a>Usar operações e tipos de dados alinhados

Os conjuntos de instruções SIMD em versões do Windows com suporte a SSE2 normalmente têm versões alinhadas e desalinhadas das operações de memória. O uso das operações alinhadas é mais rápido e deve ser preferível sempre que possível.

A biblioteca DirectXMath fornece funcionalidade alinhada e não alinhada por meio de tipos de vetor variantes, estrutura e funções. Essas variantes são indicadas por um "A" no final do nome.

Por exemplo, há uma estrutura [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) não alinhada e uma estrutura [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) alinhada, que são usadas pelas funções [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) e [**XMStoreFloat4A**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) , respectivamente.

## <a name="properly-align-allocations"></a>Alinhar as alocações corretamente

As versões alinhadas dos intrínsecores [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) subjacentes à biblioteca DirectXMath são mais rápidas do que as não alinhadas.

Por esse motivo, as operações de DirectXMath usando objetos [**XMVECTOR**](xmvector-data-type.md) e [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) assumem que esses objetos são alinhados em 16 bytes. Isso é automático para alocações baseadas em pilha, se o código for compilado na biblioteca DirectXMath usando as configurações de compilador recomendadas do Windows (consulte [usar configurações de compilação corretas](#use-correct-compilation-settings)). No entanto, é importante garantir que a alocação de heap contendo objetos **XMVECTOR** e **XMMATRIX** , ou conversões para esses tipos, atenda a esses requisitos de alinhamento.

Enquanto as alocações de memória do Windows de 64 bits são alinhadas em 16 bytes, por padrão, em versões de 32 bits da memória do Windows alocada, há apenas 8 bytes alinhados. Para obter informações sobre como controlar o alinhamento de memória, confira [ \_ \_ malloc alinhado](https://msdn.microsoft.com/library/8z34s9c6(VS.80).aspx).

Ao usar tipos DirectXMath alinhados com a STL (Standard Template Library), você precisará fornecer um alocador personalizado que garanta o alinhamento de 16 bytes. Consulte o [blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) da equipe Visual C++ para obter um exemplo de como escrever um alocador personalizado (em vez de malloc/Free, você desejará usar \_ \_ o malloc alinhado e \_ alinhado \_ gratuitamente em sua implementação).

> [!Note]  
> Alguns modelos STL modificam o alinhamento do tipo fornecido. Por exemplo, [Make \_ Shared<>](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) adiciona algumas informações de acompanhamento internas que podem ou não respeitar o alinhamento do tipo de usuário fornecido, resultando em membros de dados não alinhados. Nesse caso, você precisa usar tipos não alinhados em vez de tipos alinhados. Se você derivar de classes existentes, incluindo muitos objetos Windows Runtime, também poderá modificar o alinhamento de uma classe ou estrutura.

 

## <a name="avoid-operator-overloads-when-possible"></a>Evite sobrecargas de operador quando possível

Como um recurso de conveniência, vários tipos, como [**XMVECTOR**](xmvector-data-type.md) e [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) , têm sobrecargas de operador para operações aritméticas comuns. Essas sobrecargas de operador tendem a criar vários objetos temporários. Recomendamos que você evite essas sobrecargas de operador no código sensível ao desempenho.

## <a name="denormals"></a>Desnormalizado

Para dar suporte a cálculos próximos de 0, o padrão de ponto flutuante do IEEE 754 inclui suporte para estouro negativo. O estouro negativo é implementado por meio do uso de valores desnormalizados e muitas implementações de hardware são lentas durante o tratamento de desnormals. Uma otimização a ser considerada é desabilitar a manipulação de desnormalidades para as operações de vetor usadas pelo DirectXMath.

A alteração da manipulação de desnormalidades é feita usando a rotina [ \_ controlfp \_ s](/cpp/c-runtime-library/reference/controlfp-s) em uma base pré-thread e pode resultar em melhorias de desempenho. Use este código para alterar a manipulação de desnormals:


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> Nas versões de 64 bits do Windows, as instruções [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) são usadas para todos os cálculos, não apenas para as operações de vetor. Alterar a manipulação desnormal afeta todos os cálculos de ponto flutuante em seu programa, não apenas as operações de vetor usadas pelo DirectXMath.

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a>Aproveite a dupla de ponto flutuante de inteiro

O DirectXMath dá suporte a vetores de 4 valores de ponto flutuante de precisão simples ou de 4 32 bits (assinados ou não assinados).

Como os conjuntos de instruções usados para implementar a biblioteca DirectXMath têm a capacidade de tratar os mesmos dados de vários tipos diferentes, por exemplo, tratar o mesmo vetor como ponto flutuante e dados inteiros – determinadas otimizações podem ser obtidas. Você pode obter essas otimizações usando as rotinas de inicialização de vetores inteiros e os operadores de bits para manipular valores de ponto flutuante.

O formato binário dos números de ponto flutuante de precisão simples usados pela biblioteca DirectXMath está totalmente em conformidade com o padrão IEEE 764:

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

Ao trabalhar com o número de ponto flutuante de precisão única do IEEE 764, é importante ter em mente que algumas representações têm um significado especial (ou seja, elas não estão em conformidade com a descrição anterior). Os exemplos incluem:

-   Zero positivo é 0
-   Zero negativo é 0x80000000
-   P \_ Nan é 07FC0000
-   + INF é 0x7F800000
-   -INF é 0xFF800000

## <a name="prefer-template-forms"></a>Preferir formulários de modelo

O formulário de modelo existe para [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle), [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert), [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft), [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)e [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright). Usá-los em vez do formulário de função geral permite que o compilador crie implementações muito mais efficents. Para a [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)), isso geralmente se recolhe a um ou dois \_ valores de PS em \_ ordem aleatória de mm \_ . Para o ARM-NEON, o modelo **XMVectorSwizzle** pode utilizar vários casos especiais em vez do VTBL mais geral swizzle/permudo.

## <a name="using-directxmath-with-direct3d"></a>Usando o DirectXMath com o Direct3D

Um uso comum do DirectXMath é executar cálculos de gráficos para uso com o Direct3D. Com o Direct3D 10. x e o Direct3D 11. x, você pode usar a biblioteca DirectXMath dessas maneiras diretas:

-   Use as [constantes](ovw-xnamath-reference-constants.md) de namespace Colors diretamente no parâmetro *ColorRGBA* em uma chamada para o método [**ID3D11DeviceContext:: ClearRenderTargetView**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview) ou [**ID3D10Device:: ClearRenderTargetView**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview) . Para o Direct3D 9, você deve converter para o tipo [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) para usá-lo como o parâmetro de *cor* em uma chamada para o método [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) .
-   Use os tipos [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [**XMVECTOR**](xmvector-data-type.md) e [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) para configurar estruturas de buffer de constantes para referência por HLSL [**FLOAT4**](../direct3dhlsl/dx-graphics-hlsl-scalar.md) ou tipos de [**matriz**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)/float4x4.
    > [!Note]  
    > [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / Os tipos [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) estão no formato de linha-principal. Portanto, se você usar a opção de compilador/ZPR (o sinalizador de compilação [**principal da coluna de matriz do D3DCOMPILE \_ Pack \_ \_ \_**](../direct3dhlsl/d3dcompile-constants.md) ) ou omitir a \_ [palavra-chave](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md) principal de linha ao declarar o tipo de matriz em HLSL, deverá transpor a matriz quando defini-la no buffer de constantes.

     

-   Com o Direct3D 10. x e o Direct3D 11. x, você pode pressupor que o ponteiro retornado pelo método MAP (por exemplo, [**ID3D11DeviceContext:: map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) no membro **pData** ([**d3d10 \_ mapeado \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d).**pData**, [**d3d10 \_ mapeoud \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d).**** Subrecurso pData [**ou \_ D3D11 \_ mapeado**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource).**pData**) será alinhado em 16 bytes se você usar o [nível de recurso](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ 0 ou superior ou sempre que usar os recursos de [**\_ \_ preparo de uso do D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
