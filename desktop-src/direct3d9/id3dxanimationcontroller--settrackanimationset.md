---
description: Aplica a animação definida à faixa especificada.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'Método ID3DXAnimationController:: SetTrackAnimationSet (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762479"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a>Método ID3DXAnimationController:: SetTrackAnimationSet

Aplica a animação definida à faixa especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador da faixa à qual o conjunto de animações é aplicado.

</dd> <dt>

*pAnimSet* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Ponteiro para o conjunto de animação [**ID3DXAnimationSet**](id3dxanimationset.md) a ser adicionado à faixa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método define a animação definida como a faixa especificada para a combinação. O conjunto de animações para cada faixa é mesclado de acordo com o peso e a velocidade da faixa quando o [**adiantamento**](id3dxanimationcontroller--advancetime.md) é chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
