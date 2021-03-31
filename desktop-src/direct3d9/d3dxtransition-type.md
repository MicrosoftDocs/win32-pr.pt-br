---
description: Define o estilo de transição entre os valores de uma animação de malha.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: Enumeração de D3DXTRANSITION_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930582"
---
# <a name="d3dxtransition_type-enumeration"></a>\_Enumeração de tipo D3DXTRANSITION

Define o estilo de transição entre os valores de uma animação de malha.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ linear**
</dt> <dd>

Transição linear entre valores.

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**
</dt> <dd>

Uma transição de spline de fácil saída entre valores.

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O cálculo para a rampa da atenuação para facilitar é calculado da seguinte maneira:

<dl> Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x  
</dl>

em que a rampa é uma função Q (t) com as seguintes propriedades:

-   P (t) é uma spline cúbica.
-   P (t) interpola entre x e y como t varia de 0 a 1.
-   Q (t) é horizontal quando t = 0 e t = 1.

Matematicamente, isso se traduz em:

<dl> Q (t) = at ³ + BT ² + CT + D (e, portanto, Q ' (t) = 3At ² + 2Bt + C)  
2a) Q (0) = x  
2B) Q (1) = y  
3a) Q ' (0) = 0  
3B) Q ' (1) = 0  
</dl>

Resolvendo para A, B, C, D:

<dl> D = x (de 2a)  
C = 0 (de 3a)  
3A + 2B = 0 (de 3B)  
A + B = y-x (de 2B e D = x)  
</dl>

Portanto:

<dl> A = 2 (x-y), B = 3 (y-x), C = 0, D = x  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




