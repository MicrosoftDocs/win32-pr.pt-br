---
description: Remove todos os eventos de uma faixa de animação especificada.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: 'Método ID3DXAnimationController:: UnkeyAllTrackEvents (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 196f1041d725f8aed39e54626e00b849f2be09587d5ccd40fbc3d8a091fc1b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791106"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a>Método ID3DXAnimationController:: UnkeyAllTrackEvents

Remove todos os eventos de uma faixa de animação especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador do controle no qual todos os eventos devem ser removidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método impede a execução de todos os eventos agendados anteriormente na faixa e descarta todos os dados associados a esses eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
