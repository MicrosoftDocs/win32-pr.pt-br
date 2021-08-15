---
title: mova - vs
description: Mova dados de um registro de ponto flutuante para o Registro de Endereço, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dec849009ee47b4aaef1bc3766e2b141a8a6ccf5e17b16a370c6ea8284eaf957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986326"
---
# <a name="mova---vs"></a>mova - vs

Mova dados de um registro de ponto flutuante para o [Registro de Endereço](dx9-graphics-reference-asm-vs-registers-address.md), a0.

## <a name="syntax"></a>Syntax



| mova dst, src |
|---------------|



 

onde

-   dst deve ser o [Registro de Endereço](dx9-graphics-reference-asm-vs-registers-address.md), a0.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| mova                   |      | x    | x    | x     | x    | x     |



 

Move dados de ponto flutuante para um registro inteiro. Os valores são convertidos de ponto flutuante usando arredondamento para o mais próximo.

O registro de endereço é o único registro de destino permitido.

O fragmento de código a seguir mostra as operações executadas.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



Para versões 2 \_ x e superiores, o registro de endereço é um vetor de componente. Portanto, qualquer máscara de gravação é permitida.


```
mova a0.xz, r0
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




