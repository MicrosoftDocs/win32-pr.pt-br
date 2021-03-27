---
title: Mova-vs
description: Mover dados de um ponto flutuante registrar para o registro de endereço, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967131"
---
# <a name="mova---vs"></a>Mova-vs

Mover dados de um ponto flutuante registrar para o [registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md), a0.

## <a name="syntax"></a>Syntax



| Mova DST, src |
|---------------|



 

onde

-   o DST deve ser o [registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md), a0.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| mova                   |      | x    | x    | x     | x    | x     |



 

Move os dados de ponto flutuante para um registro de número inteiro. Os valores são convertidos do ponto flutuante usando o arredondamento para o mais próximo.

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



Para as versões 2 \_ x e posteriores, o registro de endereço é um vetor de componente. Portanto, qualquer máscara de gravação é permitida.


```
mova a0.xz, r0
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




