---
title: Método ID3DX11EffectRenderTargetViewVariable SetRenderTarget (D3dx11effect. h)
description: Defina um destino de renderização.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- Método SetRenderTarget Direct3D 11
- Método SetRenderTarget Direct3D 11, interface ID3DX11EffectRenderTargetViewVariable
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11, método SetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb53f0dff19fcd8990575dc9b305b0fb2f7e149b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837984"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a>Método ID3DX11EffectRenderTargetViewVariable:: SetRenderTarget

Defina um destino de renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*origem* 
</dt> <dd>

Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***

Um ponteiro para uma interface de exibição de destino de renderização. Consulte [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

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

[ID3DX11EffectRenderTargetViewVariable](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





