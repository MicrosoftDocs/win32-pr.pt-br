---
description: Função D3DXMatrixLookAtRH (D3dx9math. h) – compila uma matriz de aparência à direita.
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: Função D3DXMatrixLookAtRH (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b3a738de31edf373deb65ea9991e1e1502f47c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335600"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a>Função D3DXMatrixLookAtRH (D3dx9math. h)

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

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*pEye* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que define o ponto de olho. Esse valor é usado na tradução.

</dd> <dt>

*pAt* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que define o destino da aparência da câmera.

</dd> <dt>

*pUp* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que define o mundo atual, geralmente \[ 0, 1, 0 \] .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de aparência da mão direita.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a **função D3DXMatrixLookAtRH** pode ser usada como um parâmetro para outra função.

Essa função usa a fórmula a seguir para calcular a matriz retornada.


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x            yaxis.x            zaxis.x           0
 xaxis.y            yaxis.y            zaxis.y           0
 xaxis.z            yaxis.z            zaxis.z           0
 -dot(xaxis, eye)   -dot(yaxis, eye)   -dot(zaxis, eye)  1
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




