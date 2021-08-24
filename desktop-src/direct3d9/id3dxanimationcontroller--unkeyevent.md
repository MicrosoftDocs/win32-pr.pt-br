---
description: Remove um evento especificado de uma faixa de animação, impedindo a execução do evento.
ms.assetid: 658ffe91-44ba-4bde-b78c-c545dff27ab1
title: 'Método ID3DXAnimationController:: UnkeyEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2565091213108c6dcc563d23df9cad50faed6b30d46af08cadfacb4fc60d3989
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564146"
---
# <a name="id3dxanimationcontrollerunkeyevent-method"></a>Método ID3DXAnimationController:: UnkeyEvent

Remove um evento especificado de uma faixa de animação, impedindo a execução do evento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnkeyEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hEvent* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para o evento a ser removido da faixa de animação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




