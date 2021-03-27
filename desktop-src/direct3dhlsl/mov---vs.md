---
title: MOV-vs
description: Mover dados de ponto flutuante entre os registros.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638886"
---
# <a name="mov---vs"></a>MOV-vs

Mover dados de ponto flutuante entre os registros.

## <a name="syntax"></a>Syntax



| MOV DST, src |
|--------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| média                    | x    | x    | x    | x     | x    | x     |



 

Pode ser usado para dados de ponto flutuante. Para a versão vs \_ 1 \_ 1, ele também pode ser usado para gravar o registro de endereço. Quando usado para atualizar os registros de endereço, os valores são convertidos do ponto flutuante usando o arredondamento para o mais próximo.

O fragmento de código a seguir mostra as operações executadas.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




