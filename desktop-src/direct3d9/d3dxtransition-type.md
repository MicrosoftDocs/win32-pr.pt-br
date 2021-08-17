---
description: Define o estilo de transição entre valores de uma animação de malha.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: D3DXTRANSITION_TYPE enumeração (D3dx9anim.h)
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
ms.openlocfilehash: f451b94fe204a82cd15c65e424cc214025aa670f82af5224897100cbc6f8f6e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730933"
---
# <a name="d3dxtransition_type-enumeration"></a>Enumeração D3DXTRANSITION \_ TYPE

Define o estilo de transição entre valores de uma animação de malha.

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

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ LINEAR**
</dt> <dd>

Transição linear entre valores.

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**
</dt> <dd>

Transição de spline de facilidade e facilidade entre valores.

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O cálculo da rampa de facilidade para facilitar a saída é calculado da seguinte forma:

<dl> Q(t) = 2(x - y)tá + 3(y - x)t Vezes + x  
</dl>

em que a rampa é uma função Q(t) com as seguintes propriedades:

-   Q(t) é um spline cúbica.
-   Q(t) interpola entre x e y conforme t varia de 0 a 1.
-   Q(t) é horizontal quando t = 0 e t = 1.

Matematicamente, isso se traduz em:

<dl> Q(t) = At igual a + Btá + Ct + D (e, portanto, Q'(t) = 3Atá + 2Bt + C)  
2a) Q(0) = x  
2b) Q(1) = y  
3a) Q'(0) = 0  
3b) Q'(1) = 0  
</dl>

Resolvendo para A, B, C, D:

<dl> D = x (de 2a)  
C = 0 (de 3a)  
3A + 2B = 0 (de 3b)  
A + B = y - x (de 2b e D = x)  
</dl>

Portanto:

<dl> A = 2(x - y), B = 3(y - x), C = 0, D = x  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




