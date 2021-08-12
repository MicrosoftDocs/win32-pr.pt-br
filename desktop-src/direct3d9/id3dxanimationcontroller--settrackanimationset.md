---
description: Aplica o conjunto de animação à faixa especificada.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: Método ID3DXAnimationController::SetTrackAnimationSet (D3dx9 multimídia.h)
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
ms.openlocfilehash: a94fee2a0bd80f391b514895aa5b5348cbef6d8a53e31200b49a403a6712e2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296879"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a>Método ID3DXAnimationController::SetTrackAnimationSet

Aplica o conjunto de animação à faixa especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador da faixa à qual o conjunto de animação é aplicado.

</dd> <dt>

*pAnimSet* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Ponteiro para o [**conjunto de animação ID3DXAnimationSet**](id3dxanimationset.md) a ser adicionado à faixa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método define o conjunto de animação para a faixa especificada para combinação. O conjunto de animação para cada faixa é mesclado de acordo com o peso e a velocidade da faixa quando [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) é chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
