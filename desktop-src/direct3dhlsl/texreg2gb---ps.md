---
title: texreg2gb – ps
description: Interpreta os componentes de cor verde e azul do registro de origem como dados de endereço de textura para amostrar a textura no estágio correspondente ao número do registro de destino.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb18a2a79132a08e2659c6df426299ce996beba79566af277500ab9eb0a885f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505744"
---
# <a name="texreg2gb---ps"></a>texreg2gb – ps

Interpreta os componentes de cor verde e azul do registro de origem como dados de endereço de textura para amostrar a textura no estágio correspondente ao número do registro de destino.

## <a name="syntax"></a>Syntax



| texreg2gb dst, src |
|--------------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2gb             |      | x    | x    |      |      |      |       |      |       |



 

Essa instrução é útil para operações de remapeamento de espaço em cores.

Aqui está um exemplo da sequência que a instrução segue.

<dl> tex t(n)  
texreg2gb t(m), t(n) em que m > n  
A primeira instrução carrega a cor da textura (RGBA)  
em registrar tn  
tn de tex  
A segunda instrução remapa a cor  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> usando t(n)<sub>GB</sub> como coordenadas
</dl>

\_bx2 não pode ser usado no registro src para [instruções texreg2ar – ps](texreg2ar---ps.md) ou texreg2gb.

Para essa instrução, o registro de origem deve usar dados não assinados. O uso de dados assinados ou mistos no registro de origem produzirá resultados indefinido. Para obter mais informações, [consulte D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 