---
description: Função D3DXQuaternionMultiply (D3dx9math.h) – multiplica dois quatternions.
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: Função D3DXQuaternionMultiply (D3dx9math.h)
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
ms.openlocfilehash: e4fe5c7f6d95bef19ce77e7ea7815e6808eae63e7643bbfc40e6b0fa1bb45767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750066"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a>Função D3DXQuaternionMultiply (D3dx9math.h)

Multiplica dois quatternions.

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para a [**estrutura D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.

</dd> <dt>

*pQ1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para uma estrutura [**D3DXQUATERNION de origem.**](d3dxquaternion.md)

</dd> <dt>

*pQ2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para uma estrutura [**D3DXQUATERNION de origem.**](d3dxquaternion.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para uma [**estrutura D3DXQUATERNION**](d3dxquaternion.md) que é o produto de dois quaternões.

## <a name="remarks"></a>Comentários

O resultado representa a rotação Q1 seguida pela rotação Q2 (Out = Q2 \* Q1). Isso é feito para que **D3DXQuaternionMultiply** mantenha a mesma semântica que [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) porque os quaternões de unidade podem ser considerados como outra maneira de representar matrizes de rotação.

As transformações são concatenadas na mesma ordem para as funções **D3DXQuaternionMultiply** e [**D3DXMatrixMultiply.**](d3dxmatrixmultiply.md) Por exemplo, supondo que mX e mY representem as mesmas rotações que qX e qY, m e q representarão as mesmas rotações.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



A multiplicação de quaterões não é comutativa.

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXQuaternionMultiply** pode ser usada como um parâmetro para outra função.

Use [**D3DXQuaternionNormalize para**](d3dxquaternionnormalize.md) qualquer entrada de quatérnion que ainda não tenha sido normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




