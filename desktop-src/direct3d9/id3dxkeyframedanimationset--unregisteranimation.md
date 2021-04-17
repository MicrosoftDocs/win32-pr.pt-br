---
description: Remova os dados de animação do conjunto de animações.
ms.assetid: 9821d21e-fe8f-4742-b4f3-63b2578d29ec
title: 'Método ID3DXKeyframedAnimationSet:: UnregisterAnimation (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterAnimation
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5ee7718fb73e441daacf9fdaff38499239915e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791091"
---
# <a name="id3dxkeyframedanimationsetunregisteranimation-method"></a>Método ID3DXKeyframedAnimationSet:: UnregisterAnimation

Remova os dados de animação do conjunto de animações.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnregisterAnimation(
  [in] UINT Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ do no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O índice de animação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
