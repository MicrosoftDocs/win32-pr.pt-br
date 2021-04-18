---
description: Retorna um identificador de evento para o evento em execução no momento na faixa de animação especificada.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'Método ID3DXAnimationController:: GetCurrentTrackEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789404"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a>Método ID3DXAnimationController:: GetCurrentTrackEvent

Retorna um identificador de evento para o evento em execução no momento na faixa de animação especificada.

## <a name="syntax"></a>Sintaxe


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de faixa.

</dd> <dt>

*EventType* \[ no\]
</dt> <dd>

Tipo: **[ **\_ tipo de D3DXEVENT**](./d3dxevent-type.md)**

Tipo de evento a ser consultado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para o evento em execução no momento na faixa especificada. **NULL** será retornado se nenhum evento estiver em execução na faixa especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
