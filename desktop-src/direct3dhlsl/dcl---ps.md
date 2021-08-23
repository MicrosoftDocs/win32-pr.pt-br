---
title: DCL-(SM2, SM3-PS ASM)
description: Declare um registro de entrada de sombreador de pixel.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dab377a36cb1323daf450b9566e419b60edc1fb80dde54591a932b2e0f28223a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793462"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>DCL-(SM2, SM3-PS ASM)

Declare um registro de entrada de sombreador de pixel.

## <a name="syntax"></a>Syntax

\[ \_ máscara de \] dest PP \[ . Mask\]



 

Em que:

-   \[\_PP \] é precisão parcial opcional. Consulte [precisão parcial](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).
-   dest é um registro de destino. Ele deve ser um [registro de cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn) ou um [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN).
-   \[. Mask \] é uma máscara de gravação opcional que controla quais componentes do registro de destino podem ser gravados. Consulte [máscara de gravação do registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DCL                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Todas as instruções de DCL devem aparecer antes da primeira instrução executável.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




