---
description: Esta visão geral descreve as alterações necessárias para migrar o código existente usando a biblioteca matemática XNA para a biblioteca DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migração de código da Biblioteca matemática XNA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc7a48d30711a870c28b677e458a4f72c3b3c40
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549958"
---
# <a name="code-migration-from-the-xna-math-library"></a>Migração de código da Biblioteca matemática XNA

Esta visão geral descreve as alterações necessárias para migrar o código existente usando a biblioteca matemática XNA para a biblioteca DirectXMath.

## <a name="header-changes"></a>Alterações de cabeça

A biblioteca DirectXMath usa um novo conjunto de headers.

Substitua o `xnamath.h` título por e adicione para os tipos `DirectXMath.h` `DirectXPackedVector.h` *empacotados por GPU.*

Os tipos delimitativos do exemplo de Colisão do SDK do DirectX no agora fazem parte `xnacollision.h` da biblioteca DirectXMath no `DirectXCollision.h` . Eles foram modificados para usar classes C++ em vez de uma API no estilo C.

## <a name="constant-changes"></a>Alterações constantes

A VERSÃO XNAMATH \_ (200, 201, 202, 203, 204 e assim por diante) foi substituída pela VERSÃO DIRECXTMATH \_ (300, 301, 302, 303 e assim por diante).

> [!NOTE]  
> DirectXMath 3.00 e 3.02 fornecidos com versões preliminares do SDK do Windows. O DirectXMath 3.03 está na versão final do SDK do Windows 8.

## <a name="namespaces"></a>Namespaces

A biblioteca DirectXMath usa namespaces C++ para organizar os tipos. A Matemática XNA usou apenas o namespace global. Os tipos DirectXMath em comum com a Matemática XNA estão no namespace **DirectX** **ou directX::P ackedVector.**

Em arquivos de origem do C++, uma solução simples é adicionar `using` instruções.

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

Para os headers, não é considerada uma melhor prática adicionar instruções using. Em vez disso, adicione namespaces totalmente qualificados.

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a>Cargas parciais

Para várias funções que carregam menos de 4 elementos de um XMVECTOR, a biblioteca matemática XNA deixou os elementos adicionais indefinido. DirectXMath sempre preencherá esses elementos adicionais com 0.

## <a name="removal-of-xbox-360-specific-types"></a>Remoção de Xbox 360 tipos específicos

Os seguintes tipos, funções e constantes da biblioteca matemática XNA não estão disponíveis no DirectXMath.

-   HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3
-   XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()
-   XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()
-   g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3
-   XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4
-   XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()
-   XMStoreXIcoN4(), XMStoreXIco4(), XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()
-   g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4

\_\_vector4i foi preterido. Em vez disso, use [**XMVECTORI32**](xmvectori32-data-type.md) [**ou XMVECTORU32.**](xmvectoru32-data-type.md)

As seguintes funções e tipos são preterido porque são somente Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4, XMXDEC4.

## <a name="arm-neon-intrinsics"></a>Intrínsecos arm-NEON

Declarar uma constante de vetor com esse código será compilado para Matemática XNA para SSE e NO-INTRINSICS, mas falhará para DirectXMath usando ARM-NEON.

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

Em geral, não recomendamos esse método de inicialização de um [**XMVECTOR.**](xmvector-data-type.md) No entanto, se você quiser uma constante de vetor, a classe [**XMVECTORF32**](xmvectorf32-data-type.md) dá suporte a esse estilo de inicialização e retorna o tipo **XMVECTOR** automaticamente para que você possa usar **XMVECTORF32** na maioria dos mesmos contextos. Todas as operações de gravação em **uma classe XMVECTORF32** exigem referenciar explicitamente o membro **XMVECTOR** .v.

## <a name="permute"></a>Permutar

A biblioteca matemática XNA tinha o seguinte formulário para o permute de vetor geral:

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

Para DirectXMath, **XMVectorPermuteControl** foi eliminado e o XM \_ PERMUTE \_ 0X .. As \_ constantes XM PERMUTE 1Z foram redefinidas para serem índices simples \_ de 0 a 7. Aqui está a nova assinatura para [**XMVectorPermute:**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

Em vez de uma palavra de controle, essa função usa diretamente os quatro índices como parâmetros, o que também a torna análoga à função [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) usando o novo XM \_ SWIZZLE \_ X . Constantes SWIZZLE W XM definidas como índices simples de \_ \_ 0 a 3.

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> Para valores constantes, há uma maneira muito mais eficiente de implementar o permute. Em vez de usar a forma de função [**de XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use o **formulário de** modelo:

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a>Formulários de modelo

Em geral, o uso de um formulário de modelo em uma forma de função das funções a seguir é muito mais eficiente e permite que a biblioteca faça otimizações específicas da plataforma por meio da especialização de modelo.

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateLeft(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateRight(FXMVECTOR V)

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
```

## <a name="eliminated-functions"></a>Funções eliminadas

| Função eliminada        | Substituição                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| XMStoreFloat3x3NC          | [**XMStoreFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| XMStoreFloat4NC            | [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| XMStoreFloat4x3NC          | [**XMStoreFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| XMStoreFloat4x4NC          | [**XMStoreFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| XMStoreInt4NC              | [**XMStoreInt4**](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| XMVector2InBoundsR         | [**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVector2TransformStreamNC | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| XMVector3InBoundsR         | [**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVector3TransformStreamNC | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| XMVector4InBoundsR         | [**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVectorCosHEst            | [**XMVectorCosH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| XMVectorExpEst             | [**XMVectorExp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| XMVectorLogEst             | [**XMVectorLog**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| XMVectorPowEst             | [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| XMVectorSinHEst            | [**XMVectorSinH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| XMVectorTanHEst            | [**XMVectorTanH**](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a>Tópicos relacionados

[Guia de Programação do DirectXMath](ovw-xnamath-progguide.md)
