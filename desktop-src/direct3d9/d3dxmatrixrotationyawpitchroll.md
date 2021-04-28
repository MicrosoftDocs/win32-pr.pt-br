---
description: Função D3DXMatrixRotationYawPitchRoll (D3dx9math. h) – compila uma matriz com uma guinada, uma densidade e um rolo especificados.
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: Função D3DXMatrixRotationYawPitchRoll (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 789812b6e94efd40ff71209348f0c9727088c253
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118144"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a>Função D3DXMatrixRotationYawPitchRoll (D3dx9math. h)

Cria uma matriz com uma guinada, pitch e roll especificados.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*Guinada* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Desvio em volta do eixo y, em radianos.

</dd> <dt>

*Pitch* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Inclinação em relação ao eixo x, em radianos.

</dd> <dt>

*Rolar* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Sobreponha-se ao eixo z, em radianos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) com a guinada, a densidade e o rolo especificados.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXMatrixRotationYawPitchRoll** pode ser usada como um parâmetro para outra função.

A ordem das transformações é revertida primeiro, depois de pitch e depois da guinada. Em relação ao eixo de coordenadas local do objeto, isso equivale à rotação em volta do eixo z, seguido pela rotação em volta do eixo x, seguido pela rotação em volta do eixo y, conforme mostrado na ilustração a seguir.

![ilustração de roll, pitch e guinada como rotações em volta dos três eixos](images/pitchyawroll.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**D3DXMatrixRotationQuaternion**](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
