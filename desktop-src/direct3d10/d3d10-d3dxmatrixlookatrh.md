---
description: Cria uma matriz de aparência à direita.
ms.assetid: 98c8932f-f179-42ed-a361-a89065b71876
title: Função D3DXMatrixLookAtRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 28c2ad0cc7eb8a3ba98aacadc764bc277a1fdad0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012136"
---
# <a name="d3dxmatrixlookatrh-function-d3dx10mathh"></a>Função D3DXMatrixLookAtRH (D3DX10Math. h)

Cria uma matriz de aparência à direita.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*pEye* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que define o ponto de olho. Esse valor é usado na tradução.

</dd> <dt>

*pAt* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para a estrutura D3DXVECTOR3 que define o destino da aparência da câmera.

</dd> <dt>

*pUp* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para a estrutura D3DXVECTOR3 que define o mundo atual, geralmente \[ 0, 1, 0 \] .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de aparência da mão direita.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixLookAtRH pode ser usada como um parâmetro para outra função.

Essa função usa a fórmula a seguir para calcular a matriz retornada.


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 -xaxis.x           yaxis.x           -zaxis.x          0
 -xaxis.y           yaxis.y           -zaxis.y          0
 -xaxis.z           yaxis.z           -zaxis.z          0
dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
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

 

 
