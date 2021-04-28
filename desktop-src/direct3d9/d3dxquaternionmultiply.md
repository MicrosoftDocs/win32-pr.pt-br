---
description: Função D3DXQuaternionMultiply (D3dx9math. h) – Multiplica dois quaternions.
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: Função D3DXQuaternionMultiply (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7250484e4943e8b077a63e35951c17a44eaf2de3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118034"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a>Função D3DXQuaternionMultiply (D3dx9math. h)

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

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.

</dd> <dt>

*pQ1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.

</dd> <dt>

*pQ2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o produto de dois quaternions.

## <a name="remarks"></a>Comentários

O resultado representa a rotação Q1 seguida da rotação Q2 (out = T2 \* Q1). Isso é feito para que **D3DXQuaternionMultiply** mantenha a mesma semântica que [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) porque a unidade quaternions pode ser considerada como outra maneira de representar matrizes de rotação.

As transformações são concatenadas na mesma ordem para as funções **D3DXQuaternionMultiply** e [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) . Por exemplo, supondo que mX e mY representem as mesmas rotações que qX e qY, m e q representarão as mesmas rotações.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



A multiplicação de quaternions não é comutada.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXQuaternionMultiply** pode ser usada como um parâmetro para outra função.

Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




