---
title: Interface ID3DX11EffectBlendVariable (D3dx11effect. h)
description: A interface Blend-Variable acessa o estado de mesclagem.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- Interface ID3DX11EffectBlendVariable Direct3D 11
- Interface ID3DX11EffectBlendVariable Direct3D 11, descrita
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
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930753"
---
# <a name="id3dx11effectblendvariable-interface"></a>Interface ID3DX11EffectBlendVariable

A interface Blend-Variable acessa o estado de mesclagem.

## <a name="members"></a>Membros

A interface **ID3DX11EffectBlendVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectBlendVariable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectBlendVariable** tem esses métodos.



| Método                                                                    | Descrição                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBackingStore**](id3dx11effectblendvariable-getbackingstore.md)     | Obter um ponteiro para uma variável de estado de mistura.<br/>  |
| [**Getblendstate**](id3dx11effectblendvariable-getblendstate.md)         | Obtenha um ponteiro para uma interface de estado de mesclagem.<br/> |
| [**Setblendstate**](id3dx11effectblendvariable-setblendstate.md)         | Define o estado de mesclagem de um efeito.<br/>             |
| [**UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md) | Reverte um estado de mesclagem definido anteriormente.<br/>     |



 

## <a name="remarks"></a>Comentários

Uma interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é criada quando um efeito é lido na memória.

As variáveis de efeito são salvas na memória no repositório de backup; Quando uma técnica é aplicada, os valores no repositório de backup são copiados para o dispositivo. Você pode usar qualquer um desses métodos para retornar o estado.

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efeitos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





