---
title: texreg2gb-PS
description: Interpreta os componentes de cor verde e azul do registro de origem como dados de endereço de textura para amostrar a textura no estágio correspondente ao número de registro de destino.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967185"
---
# <a name="texreg2gb---ps"></a>texreg2gb-PS

Interpreta os componentes de cor verde e azul do registro de origem como dados de endereço de textura para amostrar a textura no estágio correspondente ao número de registro de destino.

## <a name="syntax"></a>Syntax



| texreg2gb DST, src |
|--------------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2gb             |      | x    | x    |      |      |      |       |      |       |



 

Essa instrução é útil para operações de remapeamento de espaço de cor.

Veja a seguir um exemplo da seqüência da instrução.

<dl> Tex t (n)  
texreg2gb t (m), t (n) onde m > n  
A primeira instrução carrega a cor de textura (RGBA)  
em registrar TN  
Tex TN  
A segunda instrução remapeia a cor  
t (m)<sub>RGBA</sub> = TextureSample (estágio m)<sub>RGBA</sub> usando t (n)<sub>GB</sub> como coordenadas
</dl>

\_BX2 não pode ser usado no registro src para instruções [texreg2ar-PS](texreg2ar---ps.md) ou texreg2gb.

Para essa instrução, o registro de origem deve usar dados não assinados. O uso de dados assinados ou mistos no registro de origem produzirá resultados indefinidos. Para obter mais informações, consulte [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 