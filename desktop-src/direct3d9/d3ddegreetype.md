---
description: Define o grau das variáveis na equação que descreve uma curva.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: Enumeração D3DDEGREETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 773ef3a8dd8fc5f4657119c2021c5723e54a3bd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785157"
---
# <a name="d3ddegreetype-enumeration"></a>Enumeração D3DDEGREETYPE

Define o grau das variáveis na equação que descreve uma curva.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE \_ linear**
</dt> <dd>

A curva é descrita por variáveis da primeira ordem.

</dd> <dt>

<span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE \_ quadrática**
</dt> <dd>

A curva é descrita por variáveis da segunda ordem.

</dd> <dt>

<span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE \_ cúbico**
</dt> <dd>

A curva é descrita por variáveis da terceira ordem.

</dd> <dt>

<span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ QUINTIC**
</dt> <dd>

A curva é descrita por variáveis da quarta ordem.

</dd> <dt>

<span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores nessa enumeração são usados para descrever as curvas usadas por patches de retângulo e de triângulo. Para obter mais informações, consulte D3DRS de \_ seleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
