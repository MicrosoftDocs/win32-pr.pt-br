---
title: Método ID3DX11EffectDepthStencilViewVariable GetDepthStencil (D3dx11effect. h)
description: Obtenha um recurso de exibição de estêncil de profundidade.
ms.assetid: 7d94d98b-7070-41ee-9a9d-fe848f8914f2
keywords:
- Método GetDepthStencil Direct3D 11
- Método GetDepthStencil Direct3D 11, interface ID3DX11EffectDepthStencilViewVariable
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, método GetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d31b5a947afc9a1b92349b20bc5d075599a16d12abae0ac7d375e8bc0a0de89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989736"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencil-method"></a>Método ID3DX11EffectDepthStencilViewVariable:: GetDepthStencil

Obtenha um recurso de exibição de estêncil de profundidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDepthStencil(
   ID3D11DepthStencilView **ppResource
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppResource* 
</dt> <dd>

Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***

O endereço de um ponteiro para uma interface de exibição de estêncil de profundidade. Consulte [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





