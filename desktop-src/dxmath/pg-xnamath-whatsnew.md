---
description: A biblioteca DirectXMath baseia-se na biblioteca SIMD do XNA Math C++ versão 2.x. Aqui, descrevemos como o DirectXMath difere da Matemática XNA e como as versões do DirectXMath diferem.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novidades (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df1e7f25789ca6f58205ce9f45482e0a49540d1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827622"
---
# <a name="whats-new-directxmath"></a>Novidades (DirectXMath)

A biblioteca DirectXMath baseia-se na biblioteca [SIMD C++ matemática XNA versão 2.04](https://walbourn.github.io/xna-math-version-2-04/). Aqui, descrevemos como o DirectXMath difere da Matemática XNA e como as versões do DirectXMath diferem.

-   [Histórico de lançamento](#release-history)
-   [Diferenças do DirectXMath em relação à matemática XNA](#directxmath-differences-from-xna-math)
-   [Tópicos relacionados](#related-topics)

## <a name="release-history"></a>Histórico de versões

<table>
 <tr>
  <td>Windows 10 SDK (20348), versão 2104</td><td>DirectXMath 3.16</td>
 </td>
 <tr>
  <td>Windows 10 SDK de Atualização de maio de 2020</td><td>DirectXMath 3.14</td>
 </tr>
 <tr>
  <td>Atualização de outubro de 2018 para o Windows 10 SDK</td><td>DirectXMath 3.13</td>
 </tr>
 <tr>
  <td>SDK do Atualização de abril de 2018 para o Windows 10<br />Windows 10 Fall Creators Update SDK</td><td>DirectXMath 3.11</td>
 </tr>
 <tr>
  <td>SDK do Atualização do Windows 10 para Criadores</td><td>DirectXMath 3.10</td>
 </tr>
 <tr>
  <td>SDK Windows 10 Aniversário do Windows 10</td><td>DirectXMath 3.09</td>
 </tr>
 <tr>
  <td>Windows 10 SDK (novembro de 2015)</td><td>DirectXMath 3.08</td>
 </tr>
 <tr>
  <td>SDK do Windows para Windows 8.1 (Spring 2015)</td><td>DirectXMath 3.07</td>
 </tr>
 <tr>
  <td>SDK do Windows para Windows 8.1</td><td>DirectXMath 3.06</td>
 </tr>
 <tr>
  <td>SDK do Windows para Windows 8</td><td>DirectXMath 3.03</td>
 </tr>
</table>

Confira [versões do DirectXMath](https://github.com/Microsoft/DirectXMath/releases) para obter mais informações.

## <a name="directxmath-differences-from-xna-math"></a>Diferenças do DirectXMath em relação à matemática XNA

Veja como a biblioteca DirectXMath difere principalmente da biblioteca matemática XNA:

-   DirectXMath é somente C++ (namespaces, sobrecargas, novos modelos e assim por diante).
-   Requer suporte à biblioteca padrão do C++11 (ou seja, stdint.h e assim por diante).
-   Suporte a intrínsecos arm-NEON para a Windows RT de dados.
-   Nova funcionalidade de cor (conversões de espaço em cores, constantes de cores do .NET).
-   Tipos de volume delimitador (uma versão do que estava anteriormente no header XNACollision no exemplo de Colisão do SDK do DirectX).
-   Nenhuma Xbox 360 está disponível. O Xbox 360 XDK continua a enviar XNAMath v2.x; remoção de Xbox 360 tipos de dados específicos e variantes de função.
-   [**XMVectorPermute retrabalhado para**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) otimização aprimorada para intrínsecos SSE e ARM-NEON.
-   O [**tipo XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) é totalmente opaco. Para acessar elementos individuais **do XMMATRIX,** use outros tipos, como [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de Programação do DirectXMath](ovw-xnamath-progguide.md)
</dt> <dt>

[Versões do DirectXMath](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
