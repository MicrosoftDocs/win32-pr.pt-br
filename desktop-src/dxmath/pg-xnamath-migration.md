---
description: Esta visão geral descreve as alterações necessárias para migrar o código existente usando a biblioteca matemática do XNA para a biblioteca DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migração de código da biblioteca de matemática do XNA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c446165d3d0b6b7303424959f96ddf48bc75b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502318"
---
# <a name="code-migration-from-the-xna-math-library"></a>Migração de código da biblioteca de matemática do XNA

Esta visão geral descreve as alterações necessárias para migrar o código existente usando a biblioteca matemática do XNA para a biblioteca DirectXMath.

-   [Alterações de cabeçalho](#header-changes)
-   [Alterações constantes](#constant-changes)
-   [Namespaces](#namespaces)
-   [Cargas parciais](#partial-loads)
-   [Remoção de tipos específicos do Xbox 360](#removal-of-xbox-360-specific-types)
-   [Intrínsecos do ARM-NEON](#arm-neon-intrinsics)
-   [Permudo](#permute)
-   [Formulários de modelo](#template-forms)
-   [Funções eliminadas](#eliminated-functions)
-   [Tópicos relacionados](#related-topics)

## <a name="header-changes"></a>Alterações de cabeçalho

A biblioteca DirectXMath usa um novo conjunto de cabeçalhos.

Substitua o cabeçalho xnamath. h por DirectXMath. h e adicione DirectXPackedVector. h para os tipos "GPU embalado".

Os tipos delimitadores do exemplo de colisão do SDK do DirectX em xnacollision. h agora fazem parte da biblioteca DirectXMath em DirectXCollision. h. Eles foram modificados para usar classes C++ em vez de uma API de estilo C.

## <a name="constant-changes"></a>Alterações constantes

\_A versão XNAMATH (200, 201, 202, 203, 204 e assim por diante) foi substituída pela \_ versão DIRECXTMATH (300, 301, 302, 303 e assim por diante).

> [!Note]  
> DirectXMath 3, 0 e 3, 2 fornecidos com versões preliminares do SDK do Windows. O DirectXMath 3, 3 está na versão final do SDK do Windows 8.

 

## <a name="namespaces"></a>Namespaces

A biblioteca DirectXMath usa namespaces C++ para organizar os tipos. O XNA Math usou apenas o namespace global. Os tipos DirectXMath em comum com o XNA Math estão no namespace "DirectX" ou "DirectX::P ackedVector".

Em arquivos de origem C++, uma solução simples é adicionar instruções ' Using ':


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



Para cabeçalhos, não é considerada "melhor prática" para adicionar usando instruções. Em vez disso, adicione namespaces totalmente qualificados:


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a>Cargas parciais

Para várias funções que carregam menos de 4 elementos de um XMVECTOR, a biblioteca de matemática do XNA deixou os elementos adicionais indefinidos. DirectXMath sempre preencherá esses elementos adicionais com 0.

## <a name="removal-of-xbox-360-specific-types"></a>Remoção de tipos específicos do Xbox 360

Os seguintes tipos de biblioteca matemática do XNA, funções e constantes não estão disponíveis no DirectXMath.

-   HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3
-   XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()
-   XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()
-   g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3
-   XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4
-   XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()
-   XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()
-   g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4

\_\_vector4i foi preterido. Em vez disso, use [**XMVECTORI32**](xmvectori32-data-type.md) ou [**XMVECTORU32**](xmvectoru32-data-type.md) .

As funções e os tipos a seguir são preteridos, pois são apenas o Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.

## <a name="arm-neon-intrinsics"></a>Intrínsecos do ARM-NEON

A declaração de uma constante de vetor com esse código será compilada para o XNA Math para SSE e não INTRÍNSECOs, mas falhará para DirectXMath usando ARM-NEON.


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



Em geral, não recomendamos esse método de inicialização de um [**XMVECTOR**](xmvector-data-type.md). No entanto, se você quiser uma constante de vetor, a classe [**XMVECTORF32**](xmvectorf32-data-type.md) dará suporte a esse estilo de inicialização e retornará o tipo **XMVECTOR** automaticamente para que você possa usar o **XMVECTORF32** na maioria dos mesmos contextos. Qualquer operação de gravação em uma classe **XMVECTORF32** requer a referência explícita ao membro. v **XMVECTOR** .

## <a name="permute"></a>Permudo

A biblioteca de matemática do XNA tinha o seguinte formato para o vetor geral permudo:


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



Para DirectXMath, **XMVectorPermuteControl** foi eliminado e o XM \_ permudo \_ 0x.. As \_ constantes do XM permudo \_ 1Z foram redefinidas para índices simples 0-7. Aqui está a nova assinatura para [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



Em vez de uma palavra de controle, essa função usa diretamente os quatro índices como parâmetros, o que também o torna análogo à função [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) usando o novo XM \_ SWIZZLE \_ X. XM \_ SWIZZLE \_ W as constantes definidas como índices simples 0-3.


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> Para valores constantes, há uma maneira muito mais eficiente de implementar o permudo. Em vez de usar a forma de função de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use o formulário de **modelo** :
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="template-forms"></a>Formulários de modelo
>
> Em geral, o uso de um formulário de modelo sobre uma forma de função das funções a seguir é muito mais eficiente e permite que a biblioteca faça otimizações específicas da plataforma por meio de especialização de modelo.
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
>     XMVECTOR XMVectorSwizzle(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateLeft(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateRight(FXMVECTOR V)
>
> template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
>     XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="eliminated-functions"></a>Funções eliminadas
>
> 
>
> | Função eliminada        | Substituição                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | XMStoreFloat3x3NC          | [**XMStoreFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | XMStoreFloat4NC            | [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | XMStoreFloat4x3NC          | [**XMStoreFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | XMStoreFloat4x4NC          | [**XMStoreFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | XMStoreInt4NC              | [**XMStoreInt4**](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | XMVector2InBoundsR         | [**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
> | XMVector2TransformStreamNC | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | XMVector3InBoundsR         | [**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
> | XMVector3TransformStreamNC | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | XMVector4InBoundsR         | [**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
> | XMVectorCosHEst            | [**XMVectorCosH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | XMVectorExpEst             | [**XMVectorExp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | XMVectorLogEst             | [**XMVectorLog**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | XMVectorPowEst             | [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | XMVectorSinHEst            | [**XMVectorSinH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | XMVectorTanHEst            | [**XMVectorTanH**](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a>Tópicos relacionados
>
> <dl> <dt>

[Guia de programação do DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
