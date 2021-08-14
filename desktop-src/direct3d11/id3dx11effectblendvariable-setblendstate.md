---
title: Método SetBlendState ID3DX11EffectBlendVariable (D3dx11effect.h)
description: Define o estado de combinação de um efeito.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- Método SetBlendState Direct3D 11
- Método SetBlendState Direct3D 11 , interface ID3DX11EffectBlendVariable
- ID3DX11EffectBlendVariable interface Direct3D 11 , método SetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a8f945faaf7f07846ea58b91378bbf2e6c06eeb1c3d0d041a6e0a71e2e9ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046494"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a>Método ID3DX11EffectBlendVariable::SetBlendState

Define o estado de combinação de um efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indexar em uma matriz de interfaces blend-state. Se houver apenas uma interface blend-state, use 0.

</dd> <dt>

*pBlendState* 
</dt> <dd>

Tipo: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***

Um ponteiro para uma [**interface ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) que contém o blend-state a ser definido.

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

