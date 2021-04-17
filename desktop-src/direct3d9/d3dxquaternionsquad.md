---
description: Interpola entre quaternions, usando interpolação de Quadrangle esférica.
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: Função D3DXQuaternionSquad (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e4fa980d551ac43f66035c1dcaa46d1c1c590a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105759866"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a>Função D3DXQuaternionSquad (D3dx9math. h)

Interpola entre quaternions, usando interpolação de Quadrangle esférica.

## <a name="syntax"></a>Sintaxe


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
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

*PA* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.

</dd> <dt>

*PB* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.

</dd> <dt>

*PC* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.

</dd> <dt>

*t* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Parâmetro que indica a interpolarização entre os quaternions.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da interpolação quadrangle esférica.

## <a name="remarks"></a>Comentários

Essa função usa a seguinte sequência de operações de interpolação linear esférica:


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXQuaternionSquad** pode ser usada como um parâmetro para outra função.

Para obter um exemplo de interpolação entre quaternions, consulte o exemplo SkinnedMesh. Você pode obter esse exemplo e aprender sobre ele no SDK do DirectX. Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionExp**](d3dxquaternionexp.md)
</dt> <dt>

[**D3DXQuaternionLn**](d3dxquaternionln.md)
</dt> <dt>

[**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
