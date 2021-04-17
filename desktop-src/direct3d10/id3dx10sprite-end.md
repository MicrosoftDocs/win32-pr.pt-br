---
description: 'Chame isso após ID3DX10Sprite:: flush. Se \_ o estado de salvamento de Sprite do D3DX10 \_ \_ tiver sido especificado quando ID3DX10Sprite:: BEGIN for chamado, essa API restaurará o estado do dispositivo para como ele estava antes de ID3DX10Sprite:: Begin ser chamado.'
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'Método ID3DX10Sprite:: End (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02d25e41916bd5d7605f3c0e1bc6e7998ea06e86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762164"
---
# <a name="id3dx10spriteend-method"></a>Método ID3DX10Sprite:: End

Chame isso após ID3DX10Sprite:: flush. Se \_ o estado de salvamento de Sprite do D3DX10 \_ \_ tiver sido especificado quando ID3DX10Sprite:: BEGIN for chamado, essa API restaurará o estado do dispositivo para como ele estava antes de ID3DX10Sprite:: Begin ser chamado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




