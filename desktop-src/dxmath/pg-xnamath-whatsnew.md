---
description: A biblioteca DirectXMath baseia-se na biblioteca matemática do XNA C++ SIMD versão 2. x. Aqui, descrevemos como o DirectXMath difere do XNA Math e como as versões do DirectXMath são diferentes.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: O que há de novo (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813511"
---
# <a name="whats-new-directxmath"></a>O que há de novo (DirectXMath)

A biblioteca DirectXMath é baseada na [biblioteca de matemática do XNA C++ SIMD versão 2, 4](https://walbourn.github.io/). Aqui, descrevemos como o DirectXMath difere do XNA Math e como as versões do DirectXMath são diferentes.

-   [Histórico de rlease](#release-history)
-   [Diferenças de DirectXMath do XNA Math](#directxmath-differences-from-xna-math)
-   [Tópicos relacionados](#related-topics)

## <a name="release-history"></a>Histórico de versões

<table>
 <tr>
  <td>SDK de atualização do Windows 10 pode 2020</td><td>DirectXMath 3,14</td>
 </tr>
 <tr>
  <td>SDK de atualização do Windows 10 de outubro de 2018</td><td>DirectXMath 3,13</td>
 </tr>
 <tr>
  <td>SDK de atualização de abril de 2018 do Windows 10<br />SDK de atualização dos criadores de outono do Windows 10</td><td>DirectXMath 3,11</td>
 </tr>
 <tr>
  <td>SDK de atualização do Windows 10 para criadores</td><td>DirectXMath 3,10</td>
 </tr>
 <tr>
  <td>SDK de aniversário do Windows 10</td><td>DirectXMath 3, 9</td>
 </tr>
 <tr>
  <td>SDK do Windows 10 (novembro de 2015)</td><td>DirectXMath 3, 8</td>
 </tr>
 <tr>
  <td>SDK do Windows para Windows 8.1 (Spring 2015)</td><td>DirectXMath 3, 7</td>
 </tr>
 <tr>
  <td>SDK do Windows para Windows 8.1</td><td>DirectXMath 3, 6</td>
 </tr>
 <tr>
  <td>SDK do Windows para Windows 8</td><td>DirectXMath 3, 3</td>
 </tr>
</table>

Consulte [versões do DirectXMath](https://github.com/Microsoft/DirectXMath/releases) para obter mais informações.

## <a name="directxmath-differences-from-xna-math"></a>Diferenças de DirectXMath do XNA Math

Veja como a biblioteca DirectXMath é basicamente diferente da biblioteca de matemática do XNA:

-   DirectXMath é apenas C++ (namespaces, sobrecargas, novos modelos e assim por diante).
-   Requer suporte à biblioteca padrão do C++ 11 (ou seja, stdint. h e assim por diante).
-   O ARM-NEON intrínseco dá suporte para a plataforma Windows RT.
-   Nova funcionalidade de cor (conversões de espaço de cor, constantes de cor do .NET).
-   Tipos de volume delimitador (uma versão do que estava anteriormente no cabeçalho XNACollision no exemplo de colisão do SDK do DirectX).
-   Nenhuma versão do Xbox 360 está disponível. O XDK do Xbox 360 continua a lançar o XNAMath v2. x; remoção de tipos de dados específicos do Xbox 360 e variantes de função.
-   [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) retrabalhada para uma otimização aprimorada para os intrínsecos SSE e ARM-Neon.
-   O tipo [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) é totalmente opaco. Para acessar elementos individuais do **XMMATRIX**, use outros tipos, como [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do DirectXMath](ovw-xnamath-progguide.md)
</dt> <dt>

[Versões do DirectXMath](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
