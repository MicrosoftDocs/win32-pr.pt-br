---
title: Método ID3DX11EffectDepthStencilViewVariable SetDepthStencil (D3dx11effect.h)
description: Definir um recurso de exibição de estêncil de profundidade.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Método SetDepthStencil Direct3D 11
- Método SetDepthStencil Direct3D 11 , interface ID3DX11EffectDepthStencilViewVariable
- ID3DX11EffectDepthStencilViewVariable interface Direct3D 11 , método SetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae1e8b984bb15e083360ef99036549c534d8e047a2375ad0b0a6e5469b9191c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069676"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a>Método ID3DX11EffectDepthStencilViewVariable::SetDepthStencil

Definir um recurso de exibição de estêncil de profundidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Presource* 
</dt> <dd>

Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***

Um ponteiro para uma interface de exibição de estêncil de profundidade. Consulte [**ID3D11DepthStencilView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





