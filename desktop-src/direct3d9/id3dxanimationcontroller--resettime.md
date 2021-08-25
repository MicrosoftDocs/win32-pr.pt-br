---
description: Redefine o tempo de animação global para zero. Todos os eventos pendentes manterão suas agendas originais, mas no novo período de tempo.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'Método ID3DXAnimationController:: ResetTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3f5f4ba6f10d5119e479a56e9e207e410b2d1e817d6809e7ceac1c98c8d2ee5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893736"
---
# <a name="id3dxanimationcontrollerresettime-method"></a>Método ID3DXAnimationController:: ResetTime

Redefine o tempo de animação global para zero. Todos os eventos pendentes manterão suas agendas originais, mas no novo período de tempo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método geralmente é usado quando o valor de tempo de animação global está se aproximando da precisão máxima do armazenamento duplo, ou 2 ⁶ ⁴-1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




