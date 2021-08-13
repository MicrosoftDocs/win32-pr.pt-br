---
title: Interface ID3DX11EffectDepthStencilViewVariable (D3dx11effect.h)
description: Uma interface depth-stencil-view-variable acessa uma exibição de estêncil de profundidade.
ms.assetid: 316bf0cc-a7cd-4a40-932a-d566e3c2001e
keywords:
- ID3DX11EffectDepthStencilViewVariable interface Direct3D 11
- ID3DX11EffectDepthStencilViewVariable interface Direct3D 11 , descrita
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
ms.openlocfilehash: d445f2250ec29dbc4b964fecf538a4272985d2396c3cd0e605ca751aa810b3d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535914"
---
# <a name="id3dx11effectdepthstencilviewvariable-interface"></a>Interface ID3DX11EffectDepthStencilViewVariable

Uma interface depth-stencil-view-variable acessa uma exibição de estêncil de profundidade.

## <a name="members"></a>Membros

A interface **ID3DX11EffectDepthStencilViewVariable** herda de [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectDepthStencilViewVariable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectDepthStencilViewVariable** tem esses métodos.



| Método                                                                                     | Descrição                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**GetDepthStencil**](id3dx11effectdepthstencilviewvariable-getdepthstencil.md)           | Obter um recurso de exibição de estêncil de profundidade.<br/>            |
| [**GetDepthStencilArray**](id3dx11effectdepthstencilviewvariable-getdepthstencilarray.md) | Obter uma matriz de recursos de exibição de estêncil de profundidade.<br/> |
| [**SetDepthStencil**](id3dx11effectdepthstencilviewvariable-setdepthstencil.md)           | Definir um recurso de exibição de estêncil de profundidade.<br/>            |
| [**SetDepthStencilArray**](id3dx11effectdepthstencilviewvariable-setdepthstencilarray.md) | Definir uma matriz de recursos de exibição de estêncil de profundidade.<br/> |



 

## <a name="remarks"></a>Comentários

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

 

 





