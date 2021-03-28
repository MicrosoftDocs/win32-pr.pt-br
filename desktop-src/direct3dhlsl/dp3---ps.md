---
title: DP3-PS
description: Computa o produto de três componentes do ponto dos registros de origem. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968364"
---
# <a name="dp3---ps"></a>DP3-PS

Computa o produto de três componentes do ponto dos registros de origem.

## <a name="syntax"></a>Syntax



| DP3 DST, src0, src1 |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

O trecho de código a seguir mostra as operações executadas:


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



Essa instrução é executada no pipeline de vetor, sempre gravando nos canais de cor. Para a versão 1 \_ 4, essa instrução ainda usa o pipeline de vetor, mas pode gravar em qualquer canal.

Uma instrução com uma máscara de gravação de registro de destino. RGB (. xyz) pode ser emitida em conjunto com DP3, conforme mostrado abaixo.


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



A instrução DP3 pode ser modificada usando o modificador de argumento de entrada de [dimensionamento assinado do registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) aplicado aos seus argumentos de entrada se eles ainda não estiverem expandidos para o intervalo dinâmico assinado. Para um sombreador de iluminação, o modificador de instrução saturação ( \_ SAT) é geralmente usado para fixe os valores negativos para preto, conforme mostrado no exemplo a seguir.


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




