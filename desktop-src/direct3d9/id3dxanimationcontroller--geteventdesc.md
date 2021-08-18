---
description: Obtém uma descrição de um evento de animação especificado.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'Método ID3DXAnimationController:: GetEventDesc (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc113788a8eb6b64accfcba8c58dd3a3512e17601ec02ce5dd33349628c69212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987936"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a>Método ID3DXAnimationController:: GetEventDesc

Obtém uma descrição de um evento de animação especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hEvent* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para um evento de animação a ser descrito.

</dd> <dt>

*pDesc* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXEVENT \_ desc**](d3dxevent-desc.md)**

Ponteiro para uma [**estrutura \_ desc de D3DXEVENT**](d3dxevent-desc.md) que contém uma descrição do evento de animação.

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

 

 




