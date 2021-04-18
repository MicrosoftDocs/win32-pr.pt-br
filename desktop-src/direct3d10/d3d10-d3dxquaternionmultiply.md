---
description: Multiplica dois quaternions.
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: Função D3DXQuaternionMultiply (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 74e10117bf27d922480418e5aa0b8ea60a13528c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105778460"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a>Função D3DXQuaternionMultiply (D3DX10Math. h)

Multiplica dois quaternions.

## <a name="syntax"></a>Sintaxe


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***

Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.

</dd> <dt>

*pQ1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) de origem.

</dd> <dt>

*pQ2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para uma estrutura [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o produto de dois quaternions.

## <a name="remarks"></a>Comentários

O resultado representa a rotação Q1 seguida da rotação Q2 (out = T2 \* Q1). Isso é feito para que **D3DXQuaternionMultiply** mantenha a mesma semântica que [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) porque a unidade quaternions pode ser considerada como outra maneira de representar matrizes de rotação.

As transformações são concatenadas na mesma ordem para as funções **D3DXQuaternionMultiply** e [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) . Por exemplo, supondo que mX e mY representem as mesmas rotações que qX e qY, m e q representarão as mesmas rotações.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



A multiplicação de quaternions não é comutada.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função **D3DXQuaternionMultiply** pode ser usada como um parâmetro para outra função.

Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
