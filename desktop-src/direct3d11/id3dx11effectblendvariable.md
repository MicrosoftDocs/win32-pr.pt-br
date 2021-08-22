---
title: Interface ID3DX11EffectBlendVariable (D3dx11effect.h)
description: A interface blend-variable acessa o estado blend.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- ID3DX11EffectBlendVariable interface Direct3D 11
- ID3DX11EffectBlendVariable interface Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bd65c15c40c2e7ce44092baebdef66f17f2de8c1052589a984ff15c9f4b77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046454"
---
# <a name="id3dx11effectblendvariable-interface"></a>Interface ID3DX11EffectBlendVariable

A interface blend-variable acessa o estado blend.

## <a name="members"></a>Membros

A interface **ID3DX11EffectBlendVariable** herda de [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectBlendVariable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectBlendVariable** tem esses métodos.



| Método                                                                    | Descrição                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBackingStore**](id3dx11effectblendvariable-getbackingstore.md)     | Obter um ponteiro para uma variável de estado de combinação.<br/>  |
| [**GetBlendState**](id3dx11effectblendvariable-getblendstate.md)         | Obter um ponteiro para uma interface blend-state.<br/> |
| [**SetBlendState**](id3dx11effectblendvariable-setblendstate.md)         | Define o estado de combinação de um efeito.<br/>             |
| [**UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md) | Reverte um estado de combinação definido anteriormente.<br/>     |



 

## <a name="remarks"></a>Comentários

Uma interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é criada quando um efeito é lido na memória.

As variáveis de efeito são salvas na memória no armazenamento de back-back; quando uma técnica é aplicada, os valores no armazenamento de back-back são copiados para o dispositivo. Você pode usar qualquer um desses métodos para retornar o estado.

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11 Interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





