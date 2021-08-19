---
title: texreg2ar – ps
description: Interpreta os componentes de cor alfa e vermelho do registro de origem como dados de endereço de textura (u,v) para amostrar a textura no estágio correspondente ao número do registro de destino. O resultado é armazenado no registro de destino.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee9516c43f5e8d774ef496a0e66ae1a8ee839ff3df6f2f5436caaf887f95da54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283997"
---
# <a name="texreg2ar---ps"></a>texreg2ar – ps

Interpreta os componentes de cor alfa e vermelho do registro de origem como dados de endereço de textura (u,v) para amostrar a textura no estágio correspondente ao número do registro de destino. O resultado é armazenado no registro de destino.

## <a name="syntax"></a>Sintaxe



| texreg2ar dst, src |
|--------------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2ar             | x    | x    | x    |      |      |      |       |      |       |



 

Essa instrução é útil para operações de remapeamento de espaço em cores.

Aqui está um exemplo da sequência que a instrução segue:

<dl> tex t(n)  
texreg2ar t(m), t(n) em que m > n  
A primeira instrução carrega a cor da textura (RGBA)  
em registrar tn  
tn de tex  
A segunda instrução remapa a cor  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> usando t(n)<sub>AR</sub> como coordenadas
</dl>

\_bx2 não pode ser usado no registro src para texreg2ar ou [texreg2gb - instruções ps.](texreg2gb---ps.md)

Para essa instrução, o registro de origem deve usar dados não assinados. O uso de dados assinados ou mistos no registro de origem produzirá resultados indefinido. Para obter mais informações, [consulte D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 