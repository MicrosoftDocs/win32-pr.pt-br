---
description: Clones, ou cópias, um controlador de animação.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'Método ID3DXAnimationController:: CloneAnimationController (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298809"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a>Método ID3DXAnimationController:: CloneAnimationController

Clones, ou cópias, um controlador de animação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MaxNumAnimationOutputs* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de saídas de animação às quais o controlador pode dar suporte.

</dd> <dt>

*MaxNumAnimationSets* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de conjuntos de animação aos quais o controlador pode dar suporte.

</dd> <dt>

*MaxNumTracks* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de faixas às quais o controlador pode dar suporte.

</dd> <dt>

*MaxNumEvents* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de eventos aos quais o controlador pode dar suporte.

</dd> <dt>

*ppAnimController* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Endereço de um ponteiro para o controlador de animação [**ID3DXAnimationController**](id3dxanimationcontroller.md) clonado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
