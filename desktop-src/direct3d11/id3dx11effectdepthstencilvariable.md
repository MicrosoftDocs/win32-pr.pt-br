---
title: Interface ID3DX11EffectDepthStencilVariable (D3dx11effect.h)
description: Uma interface de variável de estêncil de profundidade acessa o estado de estêncil de profundidade.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- ID3DX11EffectDepthStencilVariable interface Direct3D 11
- ID3DX11EffectDepthStencilVariable interface Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d743bfebfa9722261d220800a633bdc8b268a520b883c9fea11f9f7948f7bca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989766"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a>Interface ID3DX11EffectDepthStencilVariable

Uma interface de variável de estêncil de profundidade acessa o estado de estêncil de profundidade.

## <a name="members"></a>Membros

A interface **ID3DX11EffectDepthStencilVariable** herda de [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectDepthStencilVariable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectDepthStencilVariable** tem esses métodos.



| Método                                                                                         | Descrição                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | Obter um ponteiro para uma variável que contém o estado de estêncil de profundidade.<br/> |
| [**GetDepthStencilState**](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | Obter um ponteiro para uma interface de estêncil de profundidade.<br/>                    |
| [**SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | Define o estado de estêncil de profundidade.<br/>                                  |
| [**UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | Reverte um estado de estêncil de profundidade definido anteriormente.<br/>                  |



 

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

 

 





