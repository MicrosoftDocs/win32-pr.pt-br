---
description: Obtém o tempo de animação global.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'Método ID3DXAnimationController:: getTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771640"
---
# <a name="id3dxanimationcontrollergettime-method"></a>Método ID3DXAnimationController:: getTime

Obtém o tempo de animação global.

## <a name="syntax"></a>Sintaxe


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Retorna o tempo de animação global.

## <a name="remarks"></a>Comentários

As animações são projetadas usando um tempo de animação local e misturadas em tempo global com o [**adiantamento**](id3dxanimationcontroller--advancetime.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
