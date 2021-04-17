---
description: 'Um aplicativo implementa essa interface para lidar com retornos de chamada em conjuntos de animação gerados por chamadas para ID3DXAnimationController:: AdvanceTime.'
ms.assetid: 5a24ac96-2e68-49c0-acf6-8715d87b202d
title: Interface ID3DXAnimationCallbackHandler (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb3b58c58c6a0bd71924fb207170a177797b9f84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763271"
---
# <a name="id3dxanimationcallbackhandler-interface"></a>Interface ID3DXAnimationCallbackHandler

Um aplicativo implementa essa interface para lidar com retornos de chamada em conjuntos de animação gerados por chamadas para [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="members"></a>Membros

A interface **ID3DXAnimationCallbackHandler** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationCallbackHandler** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXAnimationCallbackHandler** tem esses métodos.



| Método                                                                  | Descrição                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HandleCallback**](id3dxanimationcallbackhandler--handlecallback.md) | O aplicativo implementa esse método. Esse método é chamado quando ocorre um retorno de chamada para uma animação definida em uma das faixas durante uma chamada para [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).<br/> |



 

## <a name="remarks"></a>Comentários

O tipo LPD3DXANIMATIONCALLBACKHANDLER é definido como um ponteiro para essa interface.


```
typedef interface ID3DXAnimationCallbackHandler ID3DXAnimationCallbackHandler;
typedef interface ID3DXAnimationCallbackHandler *LPD3DXANIMATIONCALLBACKHANDLER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
