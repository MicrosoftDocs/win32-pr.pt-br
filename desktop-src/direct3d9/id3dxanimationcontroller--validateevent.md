---
description: Verifica se um alça de evento especificado é válido e se o evento de animação ainda não foi concluído.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: Método ID3DXAnimationController::ValidateEvent (D3dx9anim.h)
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
ms.openlocfilehash: 24c5195d38aeaebefd1713df31f23b6b2ec7b2324a31381027f3442b541678c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094173"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a>Método ID3DXAnimationController::ValidateEvent

Verifica se um alça de evento especificado é válido e se o evento de animação ainda não foi concluído.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hEvent* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Alça de evento para um evento de animação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retornará S \_ OK se o handle de evento for válido e o evento ainda não tiver sido concluído.

Retorna E \_ FAIL se o alça de evento for inválido e/ou se o evento tiver sido concluído.

## <a name="remarks"></a>Comentários

O método indicará que um handle de evento é válido mesmo se o evento estiver em execução, mas ainda não tiver sido concluído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




