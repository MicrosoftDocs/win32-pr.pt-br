---
title: Método ID3DX11EffectVariable AsRenderTargetView (D3dx11effect. h)
description: Obter uma variável render-Target-View.
ms.assetid: 1eec342e-267a-4eab-886a-a309758065c7
keywords:
- Método AsRenderTargetView Direct3D 11
- Método AsRenderTargetView Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método AsRenderTargetView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRenderTargetView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a8b44b3ed67b6293d4b4add329eef532fdc44cb12cea9e84b1ddf43fb72cc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531417"
---
# <a name="id3dx11effectvariableasrendertargetview-method"></a>Método ID3DX11EffectVariable:: AsRenderTargetView

Obter uma variável render-Target-View.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectRenderTargetViewVariable* AsRenderTargetView();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***

Um ponteiro para uma variável render-Target-View. Consulte [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md).

## <a name="remarks"></a>Comentários

Esse método retorna uma versão da variável de efeito que foi especializada para uma variável render-Target-View. De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados de exibição de destino de renderização.

Os aplicativos podem testar a validade do objeto retornado chamando [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





