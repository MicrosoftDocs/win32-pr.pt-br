---
description: Define operações de buffer de estêncil.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: Enumeração D3DSTENCILOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105759164"
---
# <a name="d3dstencilop-enumeration"></a>Enumeração D3DSTENCILOP

Define operações de buffer de estêncil.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ manter**
</dt> <dd>

Não atualize a entrada no buffer do estêncil. Esse é o valor padrão.

</dd> <dt>

<span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ zero**
</dt> <dd>

Defina a entrada de buffer de estêncil como 0.

</dd> <dt>

<span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ substituir**
</dt> <dd>

Substitua a entrada de buffer de estêncil por um valor de referência.

</dd> <dt>

<span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ INCRSAT**
</dt> <dd>

Aumente a entrada do buffer de estêncil, fixação MSS para o valor máximo.

</dd> <dt>

<span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ DECRSAT**
</dt> <dd>

Decrementar a entrada de buffer de estêncil, fixação MSS para zero.

</dd> <dt>

<span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**\_Inverter D3DSTENCILOP**
</dt> <dd>

Inverta os bits na entrada do buffer de estêncil.

</dd> <dt>

<span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP \_ incr**
</dt> <dd>

Aumente a entrada do buffer de estêncil, encapsulando para zero se o novo valor exceder o valor máximo.

</dd> <dt>

<span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP \_ DECR**
</dt> <dd>

Decrementar a entrada de buffer de estêncil, encapsulando o valor máximo se o novo valor for menor que zero.

</dd> <dt>

<span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Entradas de buffer de estêncil são valores inteiros variando de 0 a 2 ⁿ-1, em que n é a profundidade de bits do buffer de estêncil.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




