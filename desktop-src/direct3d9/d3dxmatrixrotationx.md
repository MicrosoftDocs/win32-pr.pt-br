---
description: Função D3DXMatrixRotationX (D3dx9math. h) – compila uma matriz que gira em volta do eixo x.
ms.assetid: 45a2668d-787f-4354-882a-94a72edaa543
title: Função D3DXMatrixRotationX (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 72ef42d63a67cfb4328e0f73897ca6ac3b38e3e4275b9192eddfb14fe8cd2e62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119076"
---
# <a name="d3dxmatrixrotationx-function-d3dx9mathh"></a>Função D3DXMatrixRotationX (D3dx9math. h)

Cria uma matriz que gira em volta do eixo x.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*Ângulo* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Ângulo de rotação em radianos. Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) girado em volta do eixo x.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXMatrixRotationX** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**D3DXMatrixRotationQuaternion**](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationYawPitchRoll**](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
