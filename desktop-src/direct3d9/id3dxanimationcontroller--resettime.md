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
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664059"
---
# <a name="id3dxanimationcontrollerresettime-method"></a>Método ID3DXAnimationController:: ResetTime

Redefine o tempo de animação global para zero. Todos os eventos pendentes manterão suas agendas originais, mas no novo período de tempo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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

 

 




