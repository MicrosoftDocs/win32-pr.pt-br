---
title: dp3 – ps
description: Calcula o produto de ponto de três componentes dos registros de origem. | dp3 – ps
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49e957078832f11885ea82baf8438d712394133eb77ad8eeaba705ff0d32a9d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024626"
---
# <a name="dp3---ps"></a>dp3 – ps

Calcula o produto de ponto de três componentes dos registros de origem.

## <a name="syntax"></a>Syntax



| dp3 dst, src0, src1 |
|---------------------|



 

onde

-   dst é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

O snippet de código a seguir mostra as operações executadas:


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



Essa instrução é executado no pipeline de vetor, sempre escrevendo nos canais de cores. Para a versão 1 \_ 4, essa instrução ainda usa o pipeline de vetor, mas pode gravar em qualquer canal.

Uma instrução com uma máscara de gravação .rgb (.xyz) de registro de destino pode ser emitida com dp3, conforme mostrado abaixo.


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



A instrução dp3 pode [](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ser modificada usando o modificador de argumento de entrada de Dimensionamento Assinado do Registro de Origem ( bx2) aplicado a seus argumentos de entrada se eles ainda não estão expandidos para o intervalo dinâmico \_ assinado. Para um sombreador de iluminação, o modificador de instrução saturado ( sáb) geralmente é usado para fixar os valores negativos em preto, conforme \_ mostrado no exemplo a seguir.


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




