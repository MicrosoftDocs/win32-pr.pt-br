---
title: Getting started (DirectXMath)
description: A Biblioteca DirectXMath implementa uma interface ideal e portátil para operações aritméticas e lineares de álgebra em vetores de ponto flutuante de precisão simples (2D, 3D e 4D) ou matrizes (3×3 e 4×4).
ms.assetid: 9972e382-7a0f-88a7-ad44-18521af3520d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ad7de99a462dc533d8010c45dfadcb1bcfa1b6f33317a941e91c16f30c3d2c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117496"
---
# <a name="getting-started-directxmath"></a>Getting started (DirectXMath)

A Biblioteca DirectXMath implementa uma interface ideal e portátil para operações aritméticas e lineares de álgebra em vetores de ponto flutuante de precisão simples (2D, 3D e 4D) ou matrizes (3×3 e 4×4). A biblioteca tem suporte limitado para operações de vetor inteiro. Essas operações são amplamente usadas na renderização e animação por programas gráficos. Não há suporte para vetores de precisão dupla (incluindo longs, shorts ou bytes) e apenas operações de vetor inteiro limitado.

A biblioteca está disponível em uma variedade de Windows plataformas. Como a biblioteca fornece funcionalidades não disponíveis anteriormente, essa versão é a que se sobressaltou as seguintes bibliotecas:

-   Biblioteca matemática do Xbox fornecida pelo header Xboxmath.h
-   Biblioteca D3DX 9 fornecida pelas DLLs D3DX 9
-   Biblioteca matemática D3DX 10 fornecida por meio das DLLs D3DX 10
-   Biblioteca matemática XNA fornecida pelo header xnamath.h no SDK do DirectX e Xbox 360 XDK

Estas seções descreve as noções básicas de como começar.

-   [Download](#download)
-   [Requisitos do sistema em tempo de executar](#run-time-system-requirements)
-   [Visão geral do design](#design-overview)
-   [Convenção de matriz](#matrix-convention)
-   [Uso Básico](#basic-usage)
-   [Diretrizes de uso de tipo](#type-usage-guidelines)
-   [Criando vetores](#creating-vectors)
    -   [VETORES CONSTANTES](#constant-vectors)
    -   [VETORES DE VARIÁVEIS](#vectors-from-variables)
    -   [VETORES DE VETORES](#vectors-from-vectors)
    -   [VETORES DA MEMÓRIA](#vectors-from-memory)
-   [Extraindo componentes de vetores](#extracting-components-from-vectors)
-   [Tópicos relacionados](#related-topics)

## <a name="download"></a>Baixar

A biblioteca DirectXMath está incluída no SDK do Windows. Como alternativa, você pode baixá-lo [GitHub/Microsoft/DirectXMath](https://github.com/Microsoft/DirectXMath). Esse site também contém projetos de exemplo relacionados.

## <a name="run-time-system-requirements"></a>Run-Time do sistema

A Biblioteca DirectXMath usa instruções de processador especializadas para operações de vetor quando elas estão disponíveis. Para evitar que um programa gere falhas de "exceção de instrução desconhecida", verifique o suporte do processador chamando [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) antes de usar a Biblioteca DirectXMath.

Estes são os requisitos básicos de suporte em tempo de run time da Biblioteca DirectXMath:

-   A compilação padrão em uma Windows (x86/x64) requer suporte à instrução SSE/SSE2.
-   A computação padrão em uma plataforma Windows RT requer suporte à instrução ARM-NEON.
-   A compilação [**\_ com XM \_ NO \_ INTRINSICS definido \_**](ovw-xnamath-reference-directives.md) requer suporte apenas à operação de ponto flutuante padrão.

> [!Note]  
> Ao chamar [**XMVerifyCPUSupport,**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport)inclua <windows.h> antes de incluir <DirectXMath.h>. Essa é a única função na biblioteca que requer qualquer conteúdo do <windows.h> para que você não seja necessário incluir um <windows.h> em cada módulo que usa <DirectXMath.h>.

 

## <a name="design-overview"></a>Visão Geral do design

A Biblioteca DirectXMath dá suporte principalmente à linguagem de programação C++. A biblioteca é implementada usando rotinas em linha nos arquivos de header, DirectXMath \* .inl, DirectXPackedVector.inl e DirectXCollision.inl. Essa implementação usa intrínsecos do compilador de alto desempenho.

A Biblioteca DirectXMath fornece:

-   Uma implementação usando intrínsecos SSE/SSE2.
-   Uma implementação sem intrínsecos.
-   Uma implementação que usa intrínsecos ARM-NEON.

Como a biblioteca é entregue usando arquivos de header, use o código-fonte para personalizar e otimizar para seu próprio aplicativo.

## <a name="matrix-convention"></a>Convenção de matriz

O DirectXMath usa matrizes principais de linha, vetores de linha e pré-multiplicação. A entrega é determinada por qual versão de função é usada (RH versus LH), caso contrário, a função funciona com coordenadas de exibição da esquerda ou direita.

Para referência, o Direct3D usou historicamente o sistema de coordenadas esquerdo, matrizes principais de linha, vetores de linha e pré-multiplicação. O Direct3D moderno não tem um requisito forte para coordenadas esquerda versus direita e normalmente sombreadores HLSL assumem o padrão de consumir matrizes de colunas principais. Consulte [Ordenação de matriz HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math) para obter detalhes.

## <a name="basic-usage"></a>Uso básico

Para usar as funções da Biblioteca DirectXMath, inclua os headers DirectXMath.h, DirectXPackedVector.h, DirectXColors.h e/ou DirectXCollision.h. Os headers são encontrados no Windows Software Development Kit para aplicativos Windows Store.

## <a name="type-usage-guidelines"></a>Diretrizes de uso de tipo

Os [**tipos XMVECTOR**](xmvector-data-type.md) [**e XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) são os tipos de trabalho da Biblioteca DirectXMath. Cada operação consome ou produz dados desses tipos. Trabalhar com eles é a chave para usar a biblioteca. No entanto, como o DirectXMath usa os conjuntos de instruções SIMD, esses tipos de dados estão sujeitos a várias restrições. É essencial que você entenda essas restrições se quiser fazer um bom uso das funções DirectXMath.

Você deve pensar em [**XMVECTOR**](xmvector-data-type.md) como um proxy para um registro de hardware SIMD e [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) como um proxy para um grupo lógico de quatro registros de hardware SIMD. Esses tipos são anotados para indicar que exigem alinhamento de 16 byte para funcionar corretamente. O compilador as colocará automaticamente corretamente na pilha quando elas são usadas como uma variável local ou as colocarão no segmento de dados quando elas são usadas como uma variável global. Com convenções adequadas, elas também podem ser passadas com segurança como parâmetros para uma função (consulte [Convenções de](pg-xnamath-internals.md) chamada para obter detalhes).

No entanto, as alocações do heap são mais complicadas. Assim, você precisa ter cuidado sempre que usar [**XMVECTOR**](xmvector-data-type.md) ou [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) como um membro de uma classe ou estrutura a ser alocada do heap. No Windows x64, todas as alocações de heap são alinhadas de 16 byte, mas para Windows x86, elas são alinhadas apenas com 8 byte. Há opções para alocar estruturas do heap com alinhamento de 16 byte (consulte [Alinhar alocações corretamente).](pg-xnamath-optimizing.md) Para programas C++, você pode usar sobrecargas do operador new/delete/new \[ \] /delete (globalmente ou específicas da classe) para impor o alinhamento ideal, se \[ \] desejado.

> [!Note]  
> Como alternativa à imposição do alinhamento em sua classe C++ diretamente sobrecarregando new/delete, você pode usar a [idiom pImpl](https://en.wikipedia.org/wiki/Opaque_pointer). Se você garantir que sua **classe Impl** esteja alinhada por meio de [**\_ \_ malloc**](/cpp/c-runtime-library/reference/aligned-malloc) alinhado internamente, poderá usar livremente os tipos alinhados dentro da implementação interna. Essa é uma boa opção quando a classe 'public' é uma classe ref do runtime do Windows ou destina-se a ser usada com [**std::shared \_ ptr<>**](/cpp/standard-library/shared-ptr-class), o que pode, de outra forma, interromper o alinhamento cuidadoso.

 

No entanto, geralmente é mais fácil e mais compacto evitar o uso de [**XMVECTOR**](xmvector-data-type.md) ou [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) diretamente em uma classe ou estrutura. Em vez disso, use [**XMFLOAT3,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) [**XMFLOAT4,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) [**XMFLOAT4X3,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)e assim por diante, como membros de sua estrutura. Além disso, você pode usar as funções [vector loading](ovw-xnamath-reference-functions-load.md) e [vector Armazenamento](ovw-xnamath-reference-functions-storage.md) para mover os dados com eficiência para variáveis locais **XMVECTOR** ou **XMMATRIX,** executar cálculos e armazenar os resultados. Também há funções de streaming ([**XMVector3TransformStream,**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream) [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)e assim por diante) que operam com eficiência diretamente em matrizes desses tipos de dados.

## <a name="creating-vectors"></a>Criando vetores

### <a name="constant-vectors"></a>VETORES CONSTANTES

Muitas operações exigem o uso de constantes em cálculos vetoriais e há várias maneiras de carregar um [**XMVECTOR**](xmvector-data-type.md) com os valores desejados.

-   Se estiver carregando uma constante escalar em todos os elementos de [**um XMVECTOR,**](xmvector-data-type.md)use [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) [**ou XMVectorReplicateInt.**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint)
    ```
    XMVECTOR vFive = XMVectorReplicate( 5.f );
    ```

    

-   Se estiver usando uma constante de vetor com valores fixos diferentes como [**um XMVECTOR,**](xmvector-data-type.md)use as estruturas [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32,**](xmvectoru32-data-type.md) **XMVECTORI32** ou [**XMVECTORU8.**](xmvectoru8-data-type.md) Eles podem ser referenciados diretamente em qualquer lugar em que você passe um **valor XMVECTOR.**
    ```
    static const XMVECTORF32 vFactors = { 1.0f, 2.0f, 3.0f, 4.0f };
    ```

    

    > [!Note]  
    > Não use listas de inicializadores diretamente com [**XMVECTOR**](xmvector-data-type.md) (ou seja, XMVECTOR v = { 1.0f, 2.0f, 3.0f, 4.0f }). Esse código é ineficiente e não é portátil em todas as plataformas com suporte do DirectXMath.

     

-   O DirectXMath inclui várias constantes globais pré-definidas que você pode usar em seu código (g \_ XMOne, g \_ XMOne3, g \_ XMTwo, g \_ XMOneHalf, g \_ XMHalfPi, g \_ XMPi e assim por diante). Pesquise o header DirectXMath.h para os **valores XMGLOBALCONSTANT.**
-   Há um conjunto de constantes de vetor para cores RGB comuns (Vermelho, Verde, Azul, Amarelo e assim por diante). Para obter mais informações sobre essas constantes de vetor, consulte DirectXColors.h e o namespace DirectX::Colors.

### <a name="vectors-from-variables"></a>VETORES DE VARIÁVEIS

-   Se estiver criando um vetor de uma única variável escalar, consulte [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) e [**XMVectorReplicateInt.**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint)
    ```
    XMVECTOR v = XMVectorReplicate( f  );
    ```

    

-   Se estiver criando um vetor de quatro variáveis escalares, consulte [**XMVectorSet**](/windows/win32/api/directxmath/nf-directxmath-xmvectorset) e [**XMVectorSetInt.**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetint)
    ```
    XMVECTOR v = XMVectorSet( fx, fy, fz, fw );
    ```

    

### <a name="vectors-from-vectors"></a>VETORES DE VETORES

-   Se estiver criando um vetor de outro vetor com um componente específico definido como uma variável, você poderá considerar o uso de [Funções de Acessador de Vetor](ovw-xnamath-reference-functions-accessors.md).
    ```
    XMVECTOR v2 = XMVectorSetW( v1, fw );
    ```

    

-   Se estiver criando um vetor de outro vetor com um único componente replicado, use [**XMVectorSplatX,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx) [**XMVectorSplatY,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty) [**XMVectorSplatZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)e [**XMVectorSplatW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw).
    ```
    XMVECTOR vz = XMVectorSplatZ( v );
    ```

    

-   Se estiver criando um vetor de outro vetor ou par de vetores com componentes reordenados, consulte [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) e [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute).
    ```
    XMVECTOR v2 = XMVectorSwizzle<XM_SWIZZLE_Z, XM_SWIZZLE_Y, XM_SWIZZLE_W, XM_SWIZZLE_X>( v1 );

    XMVECTOR v3 = XMVectorPermute<XM_PERMUTE_0W, XM_PERMUTE_1X, XM_PERMUTE_0X, XM_PERMUTE_1Z>( v1, v2 );
    ```

    

### <a name="vectors-from-memory"></a>VETORES DA MEMÓRIA

-   Para carregar um único valor float da memória, consulte [**XMVectorReplicatePtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateptr), [**XMVectorReplicateIntPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateintptr), [**XMLoadFloat**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat)e [**XMLoadInt**](/windows/win32/api/directxmath/nf-directxmath-xmloadint).
-   Maneiras comuns de carregar matrizes float são: [**XMLoadFloat2**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2), [**XMLoadFloat3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3), [**XMLoadFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4), [**XMLoadFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3), [**XMLoadFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3)e [**XMLoadFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4).
-   O DirectXMath inclui um conjunto avançado de tipos e cargas e armazenamentos relacionados para lidar com várias estruturas de dados e formatos de GPU comuns. Consulte a [carga de vetor](ovw-xnamath-reference-functions-load.md) e o armazenamento de [vetores](ovw-xnamath-reference-functions-storage.md).

## <a name="extracting-components-from-vectors"></a>Extraindo componentes de vetores

O processamento de SIMD é mais eficiente quando os dados são carregados nos registros de SIMD e totalmente processados antes de extrair os resultados. A conversão entre formulários escalares e vetoriais é ineficiente, portanto, recomendamos que você o faça somente quando necessário. Por esse motivo, as funções na biblioteca DirectXMath que produzem um valor escalar são retornadas em um formato de vetor em que o resultado escalar é replicado pelo vetor resultante (ou seja, [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot), [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length)e assim por diante). No entanto, quando você precisa de valores escalares, aqui estão algumas opções sobre como fazê-lo:

-   Se uma única resposta escalar for computada, o uso das [funções de acessador de vetor](ovw-xnamath-reference-functions-accessors.md) será apropriado:
    ```
    float f = XMVectorGetX( v );
    ```

    

-   Se for necessário extrair vários componentes do vetor, considere armazenar o vetor em uma estrutura de memória e lê-lo de volta. Por exemplo:
    ```
    XMFLOAT4A t;
    XMStoreFloat4A( &t, v );
    // t.x, t.y, t.z, and t.w can be individually accessed now
    ```

    

-   A forma mais eficiente de processamento de vetor é usar o streaming de memória para memória em que os dados de entrada são carregados da memória (usando [funções de carga de vetor](ovw-xnamath-reference-functions-load.md)), processados totalmente no formato SIMD e gravados na memória (usando funções de armazenamento de [vetor](ovw-xnamath-reference-functions-storage.md)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 