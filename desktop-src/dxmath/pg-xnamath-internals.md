---
description: Este tópico descreve o design interno da biblioteca DirectXMath.
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: Elementos internos da biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7c1843a83a81e7acac241c66dd18ff26217569
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827230"
---
# <a name="library-internals"></a>Elementos internos da biblioteca

Este tópico descreve o design interno da biblioteca DirectXMath.

-   [Convenções de chamada](#calling-conventions)
-   [Equivalência do tipo de biblioteca de gráficos](#graphics-library-type-equivalence)
-   [Constantes globais na biblioteca DirectXMath](#global-constants-in-the-directxmath-library)
-   [Windows SSE versus SSE2](#windows-sse-versus-sse2)
-   [Variantes de rotina](#routine-variants)
-   [Inconsistências de plataforma](#platform-inconsistencies)
-   [Extensões específicas da plataforma](#platform-specific-extensions)
-   [Tópicos relacionados](#related-topics)

## <a name="calling-conventions"></a>Convenções de chamada

Para aprimorar a portabilidade e otimizar o layout dos dados, você precisa usar as convenções de chamada apropriadas para cada plataforma com suporte da biblioteca DirectXMath. Especificamente, quando você passa objetos [**XMVECTOR**](xmvector-data-type.md) como parâmetros, que são definidos como alinhados em um limite de 16 bytes, há diferentes conjuntos de requisitos de chamada, dependendo da plataforma de destino:

**Para o Windows de 32 bits**

Para o Windows de 32 bits, há duas convenções de chamada disponíveis para a passagem eficiente de valores de [ \_ \_ m128](/cpp/cpp/m128) (que implementa [**XMVECTOR**](xmvector-data-type.md) nessa plataforma). O padrão é [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall), que pode passar os três primeiros valores [ \_ \_ m128](/cpp/cpp/m128) (instâncias **XMVECTOR** ) como argumentos para uma função em um registro *SSE/SSE2* . [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall) passa os argumentos restantes por meio da pilha.

Os compiladores Microsoft Visual Studio mais recentes dão suporte a uma nova Convenção de chamada, \_ \_ vectorcall, que pode passar até seis valores de [ \_ \_ m128](/cpp/cpp/m128) (instâncias [**XMVECTOR**](xmvector-data-type.md) ) como argumentos para uma função em um registro *SSE/SSE2* . Ele também pode passar agregações de vetores heterogêneos (também conhecidos como [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) por meio de registros *SSE/SSE2* se houver espaço suficiente.

**Para edições de 64 bits do Windows**

Para o Windows de 64 bits, há duas convenções de chamada disponíveis para a passagem eficiente de valores [ \_ \_ m128](/cpp/cpp/m128) . O padrão é [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall), que passa todos os valores de [ \_ \_ m128](/cpp/cpp/m128) na pilha.

Os compiladores do Visual Studio mais recentes dão suporte à \_ \_ Convenção de chamada vectorcall, que pode passar até seis valores [ \_ \_ m128](/cpp/cpp/m128) (instâncias [**XMVECTOR**](xmvector-data-type.md) ) como argumentos para uma função em um registro *SSE/SSE2* . Ele também pode passar agregações de vetores heterogêneos (também conhecidos como [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) por meio de registros *SSE/SSE2* se houver espaço suficiente.

**Para Windows no ARM**

O Windows no ARM & ARM64 dá suporte à passagem dos quatro primeiros \_ \_ valores de n128 (instâncias [**XMVECTOR**](xmvector-data-type.md) ) no registro.

**Solução DirectXMath**

Os aliases **FXMVECTOR**, **GXMVECTOR**, **HXMVECTOR** e **CXMVECTOR** dão suporte a essas convenções:

-   Use o alias **FXMVECTOR** para passar para as três primeiras instâncias de [**XMVECTOR**](xmvector-data-type.md) usadas como argumentos para uma função.
-   Use o alias **GXMVECTOR** para passar a 4ª instância de um [**XMVECTOR**](xmvector-data-type.md) usado como um argumento para uma função.
-   Use o alias **HXMVECTOR** para passar as quinta e 6º instâncias de um [**XMVECTOR**](xmvector-data-type.md) usado como um argumento para uma função. Para obter informações sobre considerações adicionais, consulte a \_ \_ documentação do vectorcall.
-   Use o alias **CXMVECTOR** para passar quaisquer instâncias adicionais de [**XMVECTOR**](xmvector-data-type.md) usadas como argumentos.

> [!Note]  
> Para parâmetros de saída, sempre use XMVECTOR \* ou XMVECTOR& e ignore-os com relação às regras anteriores para parâmetros de entrada.

 

Devido a limitações com o \_ \_ vectorcall, recomendamos que você não use **GXMVECTOR** ou **HXMVECTOR** para construtores do C++. Basta usar **FXMVECTOR** para os três primeiros valores de [**XMVECTOR**](xmvector-data-type.md) e, em seguida, usar **CXMVECTOR** para o restante.

Os aliases **FXMMATRIX** e **CXMMATRIX** ajudam o suporte a aproveitar o argumento HVA passando com \_ \_ vectorcall.

-   Use o alias **FXMMATRIX** para passar o primeiro [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) como um argumento para a função. Isso pressupõe que você não tem mais de dois argumentos **FXMVECTOR** ou mais de dois argumentos float, Double ou **FXMVECTOR** para o ' right ' da matriz. Para obter informações sobre considerações adicionais, consulte a \_ \_ documentação do vectorcall.
-   Caso contrário, use o alias **CXMMATRIX** .

Devido a limitações com o \_ \_ vectorcall, recomendamos que você nunca use **FXMMATRIX** para construtores do C++. Basta usar **CXMMATRIX**.

Além dos aliases de tipo, você também deve usar a \_ anotação XM CALLCONV para certificar-se de que a função usa a Convenção de chamada apropriada ( \_ \_ fastcall versus \_ \_ vectorcall) com base em seu compilador e arquitetura. Devido a limitações com o \_ \_ vectorcall, recomendamos que você não use o XM \_ CALLCONV para construtores do C++.

Veja a seguir as declarações de exemplo que ilustram esta Convenção:


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



Para dar suporte a essas convenções de chamada, esses aliases de tipo são definidos da seguinte maneira (os parâmetros devem ser passados pelo valor para que o compilador os considere para a passagem no registro):

**Para aplicativos do Windows de 32 bits**

Quando você usa o \_ \_ fastcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Quando você usa o \_ \_ vectorcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Para aplicativos Windows nativos de 64 bits**

Quando você usa o \_ \_ fastcall:


```C++
typedef const XMVECTOR& FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Quando você usa o \_ \_ vectorcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Windows no ARM**


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> Embora todas as funções sejam declaradas embutidas e, em muitos casos, o compilador não precisará usar convenções de chamada para essas funções, há casos em que o compilador pode decidir que é mais eficiente não embutir a função e, nesses casos, queremos a melhor convenção de chamada possível para cada plataforma.

 

## <a name="graphics-library-type-equivalence"></a>Equivalência do tipo de biblioteca de gráficos

Para dar suporte ao uso da biblioteca DirectXMath, muitos tipos e estruturas de biblioteca DirectXMath são equivalentes às implementações do Windows dos tipos **D3DDECLTYPE** e **D3DFORMAT** , bem como aos tipos de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) .

| DirectXMath                      | D3DDECLTYPE                                                                           | D3DFORMAT                                                     | \_formato dxgi                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | \_Formato dxgi \_ R8G8 \_ Santo                                                                                                                                                                                |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | D3DDECLTYPE \_ BYTE4 (somente Xbox)                                                        | D3DFMT \_ x8x8x8x8                                              | \_Formato dxgi \_ x8x8x8x8 \_ Santo                                                                                                                                                                            |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | D3DFMT \_ V8U8                                                  | \_Formato dxgi \_ R8G8 \_ SNORM                                                                                                                                                                               |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | D3DDECLTYPE \_ BYTE4N (somente Xbox)                                                       | D3DFMT \_ x8x8x8x8                                              | \_Formato dxgi \_ x8x8x8x8 \_ SNORM                                                                                                                                                                           |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | D3DDECLTYPE \_ D3DCOLOR                                                                 | D3DFMT \_ A8R8G8B8                                              | \_Formato dxgi \_ B8G8R8A8 \_ UNORM (dxgi 1.1 +)                                                                                                                                                               |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | D3DDECLTYPE \_ DEC4 (somente Xbox)                                                         | D3DDECLTYPE \_ DEC3 (somente Xbox)                                 |                                                                                                                                                                                                         |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | D3DDECLTYPE \_ DEC4N (somente Xbox)                                                        | D3DDECLTYPE \_ DEC3N (somente Xbox)                                |                                                                                                                                                                                                         |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | \_ \_ Float R32G32 de formato dxgi \_                                                                                                                                                                             |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))   | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | \_ \_ Float R32G32 de formato dxgi \_                                                                                                                                                                             |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | \_ \_ Float R32G32B32 de formato dxgi \_                                                                                                                                                                          |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | \_ \_ Float R32G32B32 de formato dxgi \_                                                                                                                                                                          |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | FORMATO DXGI \_ \_ R11G11B10 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | DXGI \_ FORMAT \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                                                       |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                       |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                       |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | D3DDECLTYPE \_ FLOAT16 \_ 2                                                               | D3DFMT \_ G16R16F                                               | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                                                                                                                                                             |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | D3DDECLTYPE \_ FLOAT16 \_ 4                                                               | D3DFMT \_ A16B16G16R16F                                         | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                       |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | DXGI \_ FORMAT \_ R32G32 \_ SINT                                                                                                                                                                              |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | DXGI \_ FORMAT \_ R32G32B32 \_ SINT                                                                                                                                                                           |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | DXGI \_ FORMAT \_ R32G32B32A32 \_ SINT                                                                                                                                                                        |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | D3DDECLTYPE \_ SHORT2                                                                   | D3DFMT \_ V16U16                                                | DXGI \_ FORMAT \_ R16G16 \_ SINT                                                                                                                                                                              |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | D3DDECLTYPE \_ SHORT2N                                                                  | D3DFMT \_ V16U16                                                | FORMATO DXGI \_ \_ R16G16 \_ SNORM                                                                                                                                                                             |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | D3DDECLTYPE \_ SHORT4                                                                   | D3DFMT \_ x16x16x16x16                                          | DXGI \_ FORMAT \_ R16G16B16A16 \_ SINT                                                                                                                                                                        |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | D3DDECLTYPE \_ SHORT4N                                                                  | D3DFMT \_ x16x16x16x16                                          | FORMATO DXGI \_ \_ R16G16B16A16 \_ SNORM                                                                                                                                                                       |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | FORMATO DXGI \_ \_ R8G8 \_ UINT                                                                                                                                                                                |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | D3DFMT \_ A8P8, D3DFMT \_ A8L8                                    | DXGI \_ FORMAT \_ R8G8 \_ UNORM                                                                                                                                                                               |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32 \_ UINT                                                                                                                                                                              |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | DXGI \_ FORMAT \_ R32G32B32 \_ UINT                                                                                                                                                                           |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32B32A32 \_ UINT                                                                                                                                                                        |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | D3DFMT \_ X1R5G5B5, D3DFMT \_ A1R5G5B5                            | FORMATO DXGI \_ \_ B5G5R5A1 \_ UNORM                                                                                                                                                                           |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | D3DFMT \_ R5G6B5                                                | FORMATO DXGI \_ \_ B5G6R5 \_ UNORM                                                                                                                                                                             |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | D3DDECLTYPE \_ UBYTE4                                                                   | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ UINT                                                                                                                                                                            |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | D3DDECLTYPE \_ UBYTE4N                                                                  | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ UNORM<br/> DXGI \_ FORMAT \_ R10G10B10 \_ XR BIAS \_ \_ A2 \_ UNORM (use [**XMLoadUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) e [**XMStoreUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr).)<br/> |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | D3DDECLTYPE \_ UDEC4 (somente Xbox)<br/> D3DDECLTYPE \_ UDEC3 (somente Xbox)<br/>   | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | FORMATO DXGI \_ \_ R10G10B10A2 \_ UINT                                                                                                                                                                         |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | D3DDECLTYPE \_ UDEC4N (somente Xbox)<br/> D3DDECLTYPE \_ UDEC3N (somente Xbox)<br/> | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM                                                                                                                                                                        |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | D3DFMT \_ A4R4G4B4, D3DFMT \_ X4R4G4B4                            | DXGI \_ FORMAT \_ B4G4R4A4 \_ UNORM (DXGI 1.2+)                                                                                                                                                               |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | D3DDECLTYPE \_ USHORT2                                                                  | D3DFMT \_ G16R16                                                | FORMATO DXGI \_ \_ R16G16 \_ UINT                                                                                                                                                                              |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | D3DDECLTYPE \_ USHORT2N                                                                 | D3DFMT \_ G16R16                                                | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                             |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | D3DDECLTYPE \_ USHORT4 (somente Xbox)                                                      | D3DFMT \_ x16x16x16x16                                          | FORMATO DXGI \_ \_ R16G16B16A16 \_ UINT                                                                                                                                                                        |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | D3DDECLTYPE \_ USHORT4N                                                                 | D3DFMT \_ x16x16x16x16                                          | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a>Constantes globais na biblioteca DirectXMath

Para reduzir o tamanho do segmento de dados, a biblioteca DirectXMath usa a macro [XMGLOBALCONST](xmglobalconst.md) para fazer uso de várias constantes internas globais em sua implementação. Por convenção, essas constantes globais internas são prefixadas por **g \_ XM**. Normalmente, eles são um dos seguintes tipos: [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORF32**](xmvectorf32-data-type.md)ou **XMVECTORI32**.

Essas constantes globais internas estão sujeitas a alterações em revisões futuras da biblioteca DirectXMath. Use funções públicas que encapsulam as constantes quando possível, em vez de usar diretamente os valores globais **g \_ XM** . Você também pode declarar suas próprias constantes globais usando [XMGLOBALCONST](xmglobalconst.md).

## <a name="windows-sse-versus-sse2"></a>Windows SSE versus SSE2

O conjunto de instruções SSE fornece suporte apenas para vetores de ponto flutuante de precisão simples. DirectXMath deve fazer uso do conjunto de instruções SSE2 para fornecer suporte a vetor de inteiro. O SSE2 tem suporte de todos os processadores Intel desde a introdução do Pentium 4, todos os processadores AMD K8 e posteriores e todos os processadores compatíveis com x64.

> [!Note]  
> O Windows 8 para x86 ou posterior requer suporte para SSE2. Todas as versões do Windows x64 exigem suporte para SSE2. O Windows no ARM/ARM64 requer \_ Neon ARM.

 

## <a name="routine-variants"></a>Variantes de rotina

Há várias variantes de funções DirectXMath que facilitam o trabalho:

-   Funções de comparação para criar ramificações condicionais complicadas com base em um número menor de operações de comparação de vetores. O nome dessas funções terminam em "R", como XMVector3InBoundsR. As funções retornam um registro de comparação como um valor de retorno UINT ou como um parâmetro de saída UINT. Você pode usar as macros **XMComparision \*** para testar o valor.
-   Funções em lote para executar operações em estilo de lote em matrizes de vetor maiores. O nome dessas funções termina em "Stream", como [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream). As funções operam em uma matriz de entradas e geram uma matriz de saídas. Normalmente, eles usam um stride de entrada e saída.
-   Funções de estimativa que implementam uma estimativa mais rápida em vez de um resultado mais lento e preciso. O nome dessas funções terminam em "est", como [**XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest). A qualidade e o impacto do desempenho do uso de estimativas variam de plataforma para plataforma, mas recomendamos que você use variantes de estimativas para código sensível ao desempenho.

## <a name="platform-inconsistencies"></a>Inconsistências de plataforma

A biblioteca DirectXMath destina-se a uso em aplicativos gráficos sensíveis ao desempenho e jogos. Portanto, a implementação foi projetada para uma velocidade ideal fazendo o processamento normal em todas as plataformas com suporte. Os resultados em condições de limite, especialmente aqueles que geram especialidades de ponto flutuante, provavelmente variam de destino para destino. Esse comportamento também dependerá de outras configurações de tempo de execução, como a palavra de controle x87 para o destino do Windows 32-bit não intrínsecos ou a palavra de controle SSE para o Windows 32 bits e o 64-bit. Além disso, haverá diferenças nas condições de limite entre vários fornecedores de CPU.

Não use DirectXMath em aplicativos científicos ou outros em que a precisão numérica seja fundamental. Além disso, essa limitação é refletida na falta de suporte para cálculos de precisão estendida ou duplo.

> [!Note]  
> Os \_ \_ caminhos de \_ código escalar XM não intrínsecos \_ geralmente são escritos para fins de conformidade, e não para o desempenho. Seus resultados de condição de limite também variam.

 

## <a name="platform-specific-extensions"></a>Extensões específicas da plataforma

A biblioteca DirectXMath destina-se a simplificar a programação C++ SIMD, fornecendo suporte excelente para plataformas x86, x64 e Windows RT usando instruções de intrínsecos com suporte amplo (SSE2 e ARM-NEON).

No entanto, há ocasiões em que as instruções específicas da plataforma podem ser úteis. Devido à maneira como o DirectXMath é implementado, em muitos casos, é trivial usar tipos DirectXMath diretamente em instruções de intrínsecos com suporte do compilador padrão e usar DirectXMath como o caminho de fallback para plataformas que não dão suporte à instrução estendida.

Por exemplo, aqui está um exemplo simplificado de aproveitar a instrução SSE 4,1 dot-Product. Observe que você deve proteger explicitamente o caminho do código para evitar a geração de exceções de instrução inválidas em tempo de execução. Certifique-se de que os caminhos de código façam um trabalho suficientemente significativo para justificar o custo adicional de ramificação, a complexidade da manutenção de vários caminhos de código e assim por diante.


```
#include <Windows.h>
#include <stdio.h>

#include <DirectXMath.h>

#include <intrin.h>
#include <smmintrin.h>

using namespace DirectX;

bool g_bSSE41 = false;

void DetectCPUFeatures()
{
#ifndef _M_ARM
   // See __cpuid documentation on MSDN for more information

   int CPUInfo[4] = {-1};
#if defined(__clang__) || defined(__GNUC__)
   __cpuid(0, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
   __cpuid(CPUInfo, 0);
#endif

   if ( CPUInfo[0] >= 1 )
   {
#if defined(__clang__) || defined(__GNUC__)
        __cpuid(1, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
        __cpuid(CPUInfo, 1);
#endif

       if ( CPUInfo[2] & 0x80000 )
           g_bSSE41 = true;
   }
#endif
}

int main()
{
   if ( !XMVerifyCPUSupport() )
       return -1;

   DetectCPUFeatures();

   ...

   XMVECTORF32 v1 = { 1.f, 2.f, 3.f, 4.f };
   XMVECTORF32 v2 = { 5.f, 6.f, 7.f, 8.f };

   XMVECTOR r2, r3, r4;

   if ( g_bSSE41 )
   {
#ifndef _M_ARM
       r2 = _mm_dp_ps( v1, v2, 0x3f );
       r3 = _mm_dp_ps( v1, v2, 0x7f );
       r4 = _mm_dp_ps( v1, v2, 0xff );
#endif
   }
   else
   {
       r2 = XMVector2Dot( v1, v2 );
       r3 = XMVector3Dot( v1, v2 );
       r4 = XMVector4Dot( v1, v2 );
   }

   ...

   return 0;
}
```



Para obter mais informações sobre extensões específicas da plataforma, consulte:

<dl>

[DirectXMath: SSE, SSE2 e ARM-NEON](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[DirectXMath: SSE3 e SSSE3](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[DirectXMath: SSE 4.1 e SSE 4.2](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[DirectXMath: AVX](https://walbourn.github.io/directxmath-avx/)  
[DirectXMath: F16C e FMA](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[DirectXMath: AVX2](https://walbourn.github.io/directxmath-avx2/)  
[DirectXMath: ARM64](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
