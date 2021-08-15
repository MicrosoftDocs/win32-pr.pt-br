---
description: Anima a malha e avança o tempo de animação global em um valor especificado.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: Método ID3DXAnimationController::AdvanceTime (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c11a3b356fb0f09cc3372db3ccebd824b4dc8290ff586eed9de3b9fa2ea13ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987956"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a>Método ID3DXAnimationController::AdvanceTime

Anima a malha e avança o tempo de animação global em um valor especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TimeDelta* \[ Em\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Quantidade, em segundos, pela qual avançar o tempo de animação global. O valor de TimeDelta deve ser não negativo ou zero.

</dd> <dt>

*pCallbackHandler* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**

Ponteiro para uma interface de manipulador de retorno de chamada de animação definida pelo usuário, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
