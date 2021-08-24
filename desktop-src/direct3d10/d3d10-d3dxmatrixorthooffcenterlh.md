---
description: Função D3DXMatrixOrthoOffCenterLH (D3DX10Math.h) – cria uma matriz de projeção ortográfica personalizada e à esquerda.
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: Função D3DXMatrixOrthoOffCenterLH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4396f060d33efef454e87d8594c2b4ca29e46cbcbc08151cacaa76a7a4965735
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852846"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a>Função D3DXMatrixOrthoOffCenterLH (D3DX10Math.h)

Cria uma matriz de projeção ortográfica personalizada e à esquerda.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para o [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)

</dd> <dt>

*l* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor x mínimo do volume de exibição.

</dd> <dt>

*r* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor x máximo do volume de exibição.

</dd> <dt>

*b* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor y mínimo do volume de exibição.

</dd> <dt>

*t* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor y máximo do volume de exibição.

</dd> <dt>

*zn* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor z mínimo do volume de exibição.

</dd> <dt>

*zf* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor z máximo do volume de exibição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para o [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Comentários

O [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) é um caso especial da função D3DXMatrixOrthoOffCenterLH. Para criar a mesma projeção usando D3DXMatrixOrthoOffCenterLH, use os seguintes valores:

l = -w/2,

r = w/2,

b = -h/2 e

t = h/2.

Todos os parâmetros da função D3DXMatrixOrthoOffCenterLH são distâncias no espaço da câmera. Os parâmetros descrevem as dimensões do volume de exibição.

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixOrthoOffCenterLH pode ser usada como um parâmetro para outra função.

Essa função usa a fórmula a seguir para calcular a matriz retornada.


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
