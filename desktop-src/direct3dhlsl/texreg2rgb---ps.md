---
title: texreg2rgb – ps
description: Interpreta os componentes de cor vermelho, verde e azul (RGB) do registro de origem como dados de endereço de textura para amostrar a textura no estágio correspondente ao número do registro de destino. O resultado é armazenado no registro de destino.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c32ee8e6b1560bfcebf6a914a45be2c74b19e94568c9d4e9b24084bf56c3f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043044"
---
# <a name="texreg2rgb---ps"></a>texreg2rgb – ps

Interpreta os componentes de cor vermelho, verde e azul (RGB) do registro de origem como dados de endereço de textura para amostrar a textura no estágio correspondente ao número do registro de destino. O resultado é armazenado no registro de destino.

## <a name="syntax"></a>Syntax



| texreg2rgb dst, src |
|---------------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2rgb            |      | x    | x    |      |      |      |       |      |       |



 

Essa instrução é útil para operações de remapeamento de espaço em cores. Ele dá suporte a coordenadas bidimensionais (2D) e tridimensionais (3D). Ele pode ser usado assim como [o texreg2ar - ps](texreg2ar---ps.md) ou [texreg2gb - ps](texreg2gb---ps.md) para remapear dados 2D. No entanto, essa instrução também dá suporte a dados 3D para que possam ser usados com mapas de cubo e texturas de volume 3D.

Aqui está um exemplo da sequência que a instrução segue.


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



Aqui está mais detalhes sobre como o remapeamento é realizado.

<dl> A primeira instrução carrega a cor da textura (RGBA) no registro tn  
tn de tex  
A segunda instrução remapa a cor  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> usando t(n)<sub>RGB</sub> como coordenadas
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




