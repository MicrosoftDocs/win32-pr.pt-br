---
title: sgn – vs
description: Calcula o sinal da entrada.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1a4994c807ff1df99016aad734edf71e5e1ce6efe59fd53a4fb9bb3ee91a4b25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671676"
---
# <a name="sgn---vs"></a>sgn – vs

Calcula o sinal da entrada.

## <a name="syntax"></a>Syntax



| sgn dst, src0, src1, src2 |
|---------------------------|



 

onde

-   dst é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro temporário que contém resultados intermediários. Após a execução, o conteúdo é indefinido.
-   src2 é um registro temporário que contém resultados intermediários. Após a execução, o conteúdo é indefinido.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Sgn                    |      | x    | x    | x     | x    | x     |



 

Essa instrução funciona conforme mostrado abaixo.


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



src1 e src2 devem ser diferentes [do Registro Temporário.](dx9-graphics-reference-asm-vs-registers-temporary.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




