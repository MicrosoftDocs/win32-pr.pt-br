---
title: Interface ID3DX11EffectDepthStencilViewVariable (D3dx11effect. h)
description: Uma interface de profundidade-estêncil-exibição-variável acessa uma exibição de estêncil de profundidade.
ms.assetid: 316bf0cc-a7cd-4a40-932a-d566e3c2001e
keywords:
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51961bd1300157eef4acb4dd15484d5146a166f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173091"
---
# <a name="id3dx11effectdepthstencilviewvariable-interface"></a>Interface ID3DX11EffectDepthStencilViewVariable

Uma interface de profundidade-estêncil-exibição-variável acessa uma exibição de estêncil de profundidade.

## <a name="members"></a>Membros

A interface **ID3DX11EffectDepthStencilViewVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilViewVariable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectDepthStencilViewVariable** tem esses métodos.



| Método                                                                                     | Descrição                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**GetDepthStencil**](id3dx11effectdepthstencilviewvariable-getdepthstencil.md)           | Obtenha um recurso de exibição de estêncil de profundidade.<br/>            |
| [**GetDepthStencilArray**](id3dx11effectdepthstencilviewvariable-getdepthstencilarray.md) | Obtenha uma matriz de recursos de exibição de estêncil de profundidade.<br/> |
| [**SetDepthStencil**](id3dx11effectdepthstencilviewvariable-setdepthstencil.md)           | Defina um recurso de exibição de estêncil de profundidade.<br/>            |
| [**SetDepthStencilArray**](id3dx11effectdepthstencilviewvariable-setdepthstencilarray.md) | Defina uma matriz de recursos de exibição de estêncil de profundidade.<br/> |



 

## <a name="remarks"></a>Comentários

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

 

 





