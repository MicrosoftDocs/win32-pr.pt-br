---
title: Interface ID3DX11EffectRenderTargetViewVariable (D3dx11effect.h)
description: Uma interface de exibição de destino de renderização acessa um destino de renderização.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- ID3DX11EffectRenderTargetViewVariable interface Direct3D 11
- ID3DX11EffectRenderTargetViewVariable interface Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645f6253de34c3c4d2306a73f827dca59ae0ce7ce97e33df63edb592b3da651a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045834"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a>Interface ID3DX11EffectRenderTargetViewVariable

Uma interface de exibição de destino de renderização acessa um destino de renderização.

## <a name="members"></a>Membros

A interface **ID3DX11EffectRenderTargetViewVariable** herda de [**ID3DX11EffectRasterizerVariable.**](id3dx11effectvariable.md) **ID3DX11EffectRenderTargetViewVariable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectRenderTargetViewVariable** tem esses métodos.



| Método                                                                                     | Descrição                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [**GetRenderTarget**](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | Obter um destino de renderização.<br/>            |
| [**GetRenderTargetArray**](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | Obter uma matriz de destinos de renderização.<br/> |
| [**Setrendertarget**](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | Definir um destino de renderização.<br/>            |
| [**SetRenderTargetArray**](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | Definir uma matriz de destinos de renderização.<br/> |



 

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

[**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11 Interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





