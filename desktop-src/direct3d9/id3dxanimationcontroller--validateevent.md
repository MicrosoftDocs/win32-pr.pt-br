---
description: Verifica se um identificador de evento especificado é válido e se o evento de animação ainda não foi concluído.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'Método ID3DXAnimationController:: ValidateEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752755"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a>Método ID3DXAnimationController:: ValidateEvent

Verifica se um identificador de evento especificado é válido e se o evento de animação ainda não foi concluído.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hEvent* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para um evento de animação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retornará S \_ OK se o identificador de evento for válido e o evento ainda não tiver sido concluído.

Retornará E \_ falhará se o manipulador de eventos for inválido e/ou se o evento tiver sido concluído.

## <a name="remarks"></a>Comentários

O método indicará que um identificador de evento é válido mesmo se o evento estiver em execução, mas ainda não tiver sido concluído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




