---
description: Função D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h) – compila uma matriz de projeção de perspectiva personalizada e com o lado direito.
ms.assetid: 51509bfc-2f49-4ba7-8918-3c44d857d4b2
title: Função D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 883ddb49684d4e5f5ca7cfb3585a26653a7f0ef4960b59e3c74aafecdd7e2f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498026"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx10mathh"></a>Função D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h)

Cria uma matriz de projeção de perspectiva personalizada para o lado direito.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
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

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*l* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor x mínimo do volume de exibição.

</dd> <dt>

*r* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor x máximo do volume de exibição.

</dd> <dt>

*b* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor y mínimo do volume de exibição.

</dd> <dt>

*t* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor y máximo do volume de exibição.

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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de projeção de perspectiva de mão com o lado direito personalizada.

## <a name="remarks"></a>Comentários

Todos os parâmetros da função D3DXMatrixPerspectiveOffCenterRH são distâncias no espaço da câmera. Os parâmetros descrevem as dimensões do volume de exibição.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixPerspectiveOffCenterRH pode ser usada como um parâmetro para outra função.

Essa função usa a fórmula a seguir para calcular a matriz retornada.


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
