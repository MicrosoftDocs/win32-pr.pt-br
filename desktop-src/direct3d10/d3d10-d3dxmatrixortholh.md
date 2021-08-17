---
description: Função D3DXMatrixOrthoLH (D3DX10Math.h) – cria uma matriz de projeção ortográfica à esquerda.
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: Função D3DXMatrixOrthoLH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b8b1b64818f4c0903897dc5b1de83b1aaa963461e909edbbfc9ba8dc4a1f10f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282956"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a>Função D3DXMatrixOrthoLH (D3DX10Math.h)

Cria uma matriz de projeção ortográfica esquerda.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
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

*w* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Largura do volume de exibição.

</dd> <dt>

*h* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Altura do volume de exibição.

</dd> <dt>

*zn* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor z mínimo do volume de exibição, que é conhecido como z-near.

</dd> <dt>

*zf* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor z máximo do volume de exibição, que é conhecido como z-far.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para o [**D3DXMATRIX resultante.**](d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Comentários

Todos os parâmetros da função D3DXMatrixOrthoLH são distâncias no espaço da câmera. Os parâmetros descrevem as dimensões do volume de exibição.

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixOrthoLH pode ser usada como um parâmetro para outra função.

Essa função usa a fórmula a seguir para calcular a matriz retornada.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
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

 

 
