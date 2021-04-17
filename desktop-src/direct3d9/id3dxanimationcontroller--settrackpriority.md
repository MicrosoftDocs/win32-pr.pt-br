---
description: Define o peso de mesclagem de prioridade para a faixa de animação especificada.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'Método ID3DXAnimationController:: SetTrackPriority (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32f1f8cce4641203782b0a84840d2986780da26a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798016"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a>Método ID3DXAnimationController:: SetTrackPriority

Define o peso de mesclagem de prioridade para a faixa de animação especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de faixa.

</dd> <dt>

*Prioridade* \[ do no\]
</dt> <dd>

Tipo: **[ **\_ tipo de D3DXPRIORITY**](./d3dxpriority-type.md)**

Controlar prioridade. Esse parâmetro deve ser definido como uma das constantes do [**\_ tipo D3DXPRIORITY**](./d3dxpriority-type.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
