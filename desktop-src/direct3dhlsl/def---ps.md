---
title: def-PS
description: Define constantes de ponto flutuante do sombreador de pixel.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008306"
---
# <a name="def---ps"></a>def-PS

Define constantes de ponto flutuante do sombreador de pixel.

## <a name="syntax"></a>Syntax



| def DST, fVvalue1, fValue2, fValue3, fValue4 |
|----------------------------------------------|



 

Em que:

-   DST é o registro de destino.
-   fValue1 fValue4 são valores de ponto flutuante..

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| def                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Há duas maneiras de definir uma constante de ponto flutuante em um sombreador de pixel.

1.  Use def para definir a constante diretamente dentro de um sombreador.
2.  Use a API para definir uma constante com [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

def define uma constante de sombreador cujo valor é carregado sempre que um sombreador é definido como um dispositivo. Elas são chamadas de constantes imediatas. Constantes imediatas têm precedência sobre constantes definidas pelo método de API.

-   Deve aparecer antes da primeira instrução aritmética ou de endereçamento no sombreador.
-   Podem ser combinados com as instruções [DCL-(SM2, SM3-PS ASM)](dcl---ps.md) (que são o outro tipo de instrução que reside no início de um sombreador).
-   o registro de hora de verão deve ser um [registro constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).
-   A máscara de gravação deve estar cheia (padrão).
-   Se um [registro constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) for definido várias vezes em um sombreador, o último persistirá.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 