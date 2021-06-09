---
description: Este tópico descreve considerações e estratégias de otimização com a Biblioteca DirectXMath.
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: Otimização de código com a Biblioteca DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15369ab36e199eb1a204cc4b761dc637f114f2a1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827250"
---
# <a name="code-optimization-with-the-directxmath-library"></a>Otimização de código com a Biblioteca DirectXMath

Este tópico descreve considerações e estratégias de otimização com a Biblioteca DirectXMath.

-   [Usar acessadores com moderação](#use-accessors-sparingly)
-   [Usar configurações de compilação corretas](#use-correct-compilation-settings)
-   [Usar funções Est quando apropriado](#use-est-functions-when-appropriate)
-   [Usar tipos e operações de dados alinhados](#use-aligned-data-types-and-operations)
-   [Alinhar alocações corretamente](#properly-align-allocations)
-   [Evitar sobrecargas de operador quando possível](#avoid-operator-overloads-when-possible)
-   [Desnormalizado](#denormals)
-   [Aproveitar a dualidade de ponto flutuante inteiro](#take-advantage-of-the-integer-floating-point-duality)
-   [Preferir formulários de modelo](#prefer-template-forms)
-   [Usando DirectXMath com Direct3D](#using-directxmath-with-direct3d)
-   [Tópicos relacionados](#related-topics)

## <a name="use-accessors-sparingly"></a>Usar acessadores com moderação

Operações baseadas em vetor usam os conjuntos de instruções SIMD e usam registros especiais. O acesso a componentes individuais requer a movimentação dos registros SIMD para os escalares e voltar novamente.

Quando possível, é mais eficiente inicializar todos os componentes de um [**XMVECTOR**](xmvector-data-type.md) ao mesmo tempo, em vez de usar uma série de acessadores de vetor individuais.

## <a name="use-correct-compilation-settings"></a>Usar configurações de compilação corretas

Para destinos do Windows x86, habilita /arch:SSE2. Para todos os destinos do Windows, habilita /fp:fast.

Por padrão, a compilação em relação aos destinos da Biblioteca DirectXMath para Janela x86 é feita com \_ xM \_ SSE \_ INTRINSICS \_ definido. Isso significa que todas as funcionalidades do DirectXMath usarão instruções SSE2. No entanto, o mesmo não é verdadeiro para outro código.

O código fora do DirectXMath é tratado usando padrões do compilador. Sem essa opção, o código gerado geralmente pode usar o código x87 menos eficiente.

É altamente recomendável que você sempre use a versão mais recente disponível do compilador.

## <a name="use-est-functions-when-appropriate"></a>Usar funções Est quando apropriado

Muitas funções têm uma função de estimativa equivalente terminando em Est. Essas funções trocam alguma precisão para melhorar o desempenho. As funções Est são apropriadas para cálculos não críticos em que a precisão pode ser saciada para velocidade. A quantidade exata de precisão perdida e aumento de velocidade depende da plataforma.

Por exemplo, a função [**XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) pode ser usada no lugar da função [**XMVector3AngleBetweenNormals.**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals)

## <a name="use-aligned-data-types-and-operations"></a>Usar tipos e operações de dados alinhados

Os conjuntos de instruções SIMD em versões do Windows que suportam SSE2 normalmente têm versões alinhadas e não qualificadas de operações de memória. O uso das operações alinhadas é mais rápido e deve ser preferencial sempre que possível.

A Biblioteca DirectXMath fornece funcionalidades alinhadas e não alinhadas de acesso por meio de tipos de vetores variantes, estrutura e funções. Essas variantes são indicadas por um "A" no final do nome.

Por exemplo, há uma estrutura [**XMFLOAT4X4 não**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) qualificada e uma estrutura [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) alinhada, que são usadas pelas funções [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) e [**XMStoreFloat4A,**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) respectivamente.

## <a name="properly-align-allocations"></a>Alinhar alocações corretamente

As versões alinhadas dos intrínsecos [da SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) subjacentes à Biblioteca DirectXMath são mais rápidas do que as não qualificadas.

Por esse motivo, as operações do DirectXMath usando [**objetos XMVECTOR**](xmvector-data-type.md) e [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) pressupõe que esses objetos estejam alinhados a 16 byte. Isso é automático para alocações baseadas em pilha, se o código for compilado em relação à Biblioteca DirectXMath usando as configurações de compilador [recomendadas](#use-correct-compilation-settings)do Windows (consulte Usar configurações de compilação corretas). No entanto, é importante garantir que a alocação de heap que contém objetos **XMVECTOR** e **XMMATRIX,** ou que as trocas para esses tipos, atendem a esses requisitos de alinhamento.

Embora as alocações de memória do Windows de 64 bits sejam alinhadas com 16 byte, por padrão, as versões de 32 bits da memória do Windows alocadas são alinhadas apenas com 8 byte. Para obter informações sobre como controlar o alinhamento de memória, consulte [ \_ \_ malloc alinhado.](https://docs.microsoft.com/cpp/c-runtime-library/reference/aligned-malloc)

Ao usar tipos DirectXMath alinhados com a STL (Biblioteca de Modelos Padrão), você precisará fornecer um alocador personalizado que garanta o alinhamento de 16 byte. Consulte o [blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) Visual C++ Team para ver um exemplo de como escrever um alocador personalizado (em vez de malloc/gratuito, você deseja usar o malloc alinhado e alinhado livre em sua \_ \_ \_ \_ implementação).

> [!Note]  
> Alguns modelos STL modificam o alinhamento do tipo fornecido. Por exemplo, [tornar \_ compartilhado<>](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) adiciona algumas informações de acompanhamento internas que podem ou não respeitar o alinhamento do tipo de usuário fornecido, resultando em membros de dados não não associados. Nesse caso, você precisa usar tipos não alinhados em vez de tipos alinhados. Se você derivar de classes existentes, incluindo muitos Windows Runtime, também poderá modificar o alinhamento de uma classe ou estrutura.

 

## <a name="avoid-operator-overloads-when-possible"></a>Evitar sobrecargas de operador quando possível

Como um recurso de conveniência, vários tipos, como [**XMVECTOR**](xmvector-data-type.md) e [**XMMATRIX,**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) têm sobrecargas de operador para operações aritméticas comuns. Essas sobrecargas de operador tendem a criar vários objetos temporários. É recomendável evitar essas sobrecargas de operador no código sensível ao desempenho.

## <a name="denormals"></a>Desnormalizado

Para dar suporte a cálculos próximos de 0, o padrão de ponto flutuante IEEE 754 inclui suporte para subfluxo gradual. O subfluxo gradual é implementado por meio do uso de valores desnormalizados e muitas implementações de hardware são lentas ao lidar com desnormais. Uma otimização a ser considerada é desabilitar a manipulação de desnormals para as operações de vetor usadas pelo DirectXMath.

A alteração da manipulação de desnormals é feita usando a rotina [ \_ controlfp \_ em](/cpp/c-runtime-library/reference/controlfp-s) uma base de pré-thread e pode resultar em melhorias de desempenho. Use este código para alterar a manipulação de desnormais:


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> Em versões de 64 bits do Windows, as [instruções de SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) são usadas para todos os cálculos, não apenas para as operações de vetor. Alterar o tratamento desnormal afeta todos os cálculos de ponto flutuante em seu programa, não apenas as operações de vetor usadas pelo DirectXMath.

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a>Aproveitar a dualidade de ponto flutuante inteiro

O DirectXMath dá suporte a vetores de 4 valores de ponto flutuante de precisão simples ou quatro de 32 bits (assinados ou não assinados).

Como os conjuntos de instruções usados para implementar a Biblioteca DirectXMath têm a capacidade de tratar os mesmos dados que vários tipos diferentes, por exemplo, tratar o mesmo vetor como ponto flutuante e otimizações de dados inteiros podem ser obtidos. Você pode obter essas otimizações usando as rotinas de inicialização de vetor inteiro e operadores bit a bit para manipular valores de ponto flutuante.

O formato binário de números de ponto flutuante de precisão simples usado pela Biblioteca DirectXMath está completamente em conformidade com o padrão IEEE 764:

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

Ao trabalhar com o número de ponto flutuante de precisão simples do IEEE 764, é importante ter em mente que algumas representações têm significado especial (ou seja, não estão em conformidade com a descrição anterior). Os exemplos incluem:

-   Zero positivo é 0
-   Zero negativo é 0x80000000
-   Q \_ NAN é 07FC0000
-   +INF é 0x7F800000
-   -INF é 0xFF800000

## <a name="prefer-template-forms"></a>Preferir formulários de modelo

O formulário de modelo existe para [**XMVectorSwizzle,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) [**XMVectorPermute,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) [**XMVectorInsert,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) [**XMVectorShiftLeft,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)e [**XMVectorRotateRight.**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) Usá-los em vez do formulário de função geral permite que o compilador crie implementações muito mais eficientes. Para [a SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)), isso geralmente se resvalha para um ou dois \_ mm valores \_ ps de embaralhamento. \_ Para ARM-NEON, o modelo **XMVectorSwizzle** pode utilizar vários casos especiais em vez do swizzle/permute mais geral do VTBL.

## <a name="using-directxmath-with-direct3d"></a>Usando DirectXMath com Direct3D

Um uso comum para DirectXMath é executar cálculos gráficos para uso com o Direct3D. Com o Direct3D 10.x e o Direct3D 11.x, você pode usar a biblioteca DirectXMath destas maneiras diretas:

-   Use as [constantes](ovw-xnamath-reference-constants.md) de namespace Colors diretamente no parâmetro *ColorRGBA* em uma chamada para o [**método ID3D11DeviceContext::ClearRenderTargetView**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview) ou [**ID3D10Device::ClearRenderTargetView.**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview) Para o Direct3D 9, você deve converter para o tipo [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) para usá-lo como o parâmetro *Color* em uma chamada para o [**método IDirect3DDevice9::Clear.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
-   Use os tipos [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [**XMVECTOR**](xmvector-data-type.md) e [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)XMMATRIX para configurar estruturas de buffer constante para referência por / [](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) tipos HLSL [**float4**](../direct3dhlsl/dx-graphics-hlsl-scalar.md) ou [**matriz**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)/float4x4.
    > [!Note]  
    > [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**Os tipos XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) estão no formato de linha principal. Portanto, se você usar a opção do compilador /Zpr (o sinalizador de compilação [**D3DCOMPILE \_ PACK MATRIX COLUMN \_ \_ \_ MAJOR)**](../direct3dhlsl/d3dcompile-constants.md) ou omitir a palavra-chave principal da linha ao declarar o tipo de matriz \_ em HLSL, você deverá transpor a matriz ao defini-la no buffer constante. [](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md)

     

-   Com o Direct3D 10.x e o Direct3D 11.x, você pode supor que o ponteiro retornado pelo método Map (por exemplo, [**ID3D11DeviceContext::Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) no membro **pData** ([**D3D10 \_ MAPPED \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d).**pData**, [**D3D10 \_ MAPPED \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d).**pData** ou [**D3D11 \_ \_ MAPPED SUBRESOURCE**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource).**pData**) será alinhado com 16 byte se você usar o nível [de](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) recurso 10 0 ou superior ou sempre que usar recursos de PREPARAÇÃO DE USO \_ [**D3D11. \_ \_**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de Programação do DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
