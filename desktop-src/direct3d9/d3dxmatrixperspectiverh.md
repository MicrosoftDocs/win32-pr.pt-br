---
description: Cria uma matriz de projeção de perspectiva à direita.
ms.assetid: dd9b041b-922b-43df-a6e9-46c97204338a
title: Função D3DXMatrixPerspectiveRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcec04202ecb2de15c479ac4ce84d4ee86c99a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172929"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a>Função D3DXMatrixPerspectiveRH (D3dx9math. h)

Cria uma matriz de projeção de perspectiva à direita.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
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

Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*w* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Largura do volume de exibição no plano de exibição próximo.

</dd> <dt>

*h* \[\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Altura do volume de exibição no plano de exibição próximo.

</dd> <dt>

*Zn* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor Z do plano de exibição próximo.

</dd> <dt>

*ZF* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Z-valor do plano de exibição distante.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de projeção de perspectiva à direita.

## <a name="remarks"></a>Comentários

Todos os parâmetros da função **D3DXMatrixPerspectiveRH** são distâncias no espaço da câmera. Os parâmetros descrevem as dimensões do volume de exibição.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXMatrixPerspectiveRH** pode ser usada como um parâmetro para outra função.

Essa função usa a fórmula a seguir para calcular a matriz retornada.


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
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

[**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
