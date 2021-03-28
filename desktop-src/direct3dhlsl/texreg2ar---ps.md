---
title: texreg2ar-PS
description: Interpreta os componentes de cor alfa e vermelha do registro de origem como dados de endereço de textura (u, v) para amostrar a textura no estágio correspondente ao número de registro de destino. O resultado é armazenado no registro de destino.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454149"
---
# <a name="texreg2ar---ps"></a>texreg2ar-PS

Interpreta os componentes de cor alfa e vermelha do registro de origem como dados de endereço de textura (u, v) para amostrar a textura no estágio correspondente ao número de registro de destino. O resultado é armazenado no registro de destino.

## <a name="syntax"></a>Syntax



| texreg2ar DST, src |
|--------------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2ar             | x    | x    | x    |      |      |      |       |      |       |



 

Essa instrução é útil para operações de remapeamento de espaço de cor.

Aqui está um exemplo da seqüência da instrução a seguir:

<dl> Tex t (n)  
texreg2ar t (m), t (n) onde m > n  
A primeira instrução carrega a cor de textura (RGBA)  
em registrar TN  
Tex TN  
A segunda instrução remapeia a cor  
t (m)<sub>RGBA</sub> = TextureSample (estágio m)<sub>RGBA</sub> usando t (n)<sub>ar</sub> como coordenadas
</dl>

\_BX2 não pode ser usado no registro src para obter instruções texreg2ar ou [texreg2gb-PS](texreg2gb---ps.md) .

Para essa instrução, o registro de origem deve usar dados não assinados. O uso de dados assinados ou mistos no registro de origem produzirá resultados indefinidos. Para obter mais informações, consulte [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 