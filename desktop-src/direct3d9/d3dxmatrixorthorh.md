---
description: Função D3DXMatrixOrthoRH (D3dx9math. h) – compila uma matriz de projeção ortográfica de mão direita.
ms.assetid: 6b9b50d5-0307-4fc7-a28d-8f42d2a21bf0
title: Função D3DXMatrixOrthoRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 060a195dfee7457f671177a756e67d1c3953a16aa7d59394f96eb05e43cfc93c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044844"
---
# <a name="d3dxmatrixorthorh-function-d3dx9mathh"></a>Função D3DXMatrixOrthoRH (D3dx9math. h)

Cria uma matriz de projeção ortográfica de mão direita.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.

</dd> <dt>

*w* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Largura do volume de exibição.

</dd> <dt>

*h* \[\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Altura do volume de exibição.

</dd> <dt>

*Zn* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor z mínimo do volume de exibição.

</dd> <dt>

*ZF* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor z máximo do volume de exibição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para o [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md)resultante.

## <a name="remarks"></a>Comentários

Todos os parâmetros da função **D3DXMatrixOrthoRH** são distâncias no espaço da câmera. Os parâmetros descrevem as dimensões do volume de exibição.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXMatrixOrthoRH** pode ser usada como um parâmetro para outra função.

Essa função usa a fórmula a seguir para calcular a matriz retornada.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterRH**](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterLH**](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
