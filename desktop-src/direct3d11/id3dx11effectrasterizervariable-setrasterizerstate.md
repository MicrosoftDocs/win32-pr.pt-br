---
title: Método ID3DX11EffectRasterizerVariable SetRasterizerState (D3dx11effect. h)
description: Define o estado do rasterizador.
ms.assetid: b2cd93fb-77bb-4a39-b686-7b8f683c9172
keywords:
- Método SetRasterizerState Direct3D 11
- Método SetRasterizerState Direct3D 11, interface ID3DX11EffectRasterizerVariable
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, método SetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.SetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1f44df653339f274207bfa4283fc8470c8844f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173204"
---
# <a name="id3dx11effectrasterizervariablesetrasterizerstate-method"></a>Método ID3DX11EffectRasterizerVariable:: SetRasterizerState

Define o estado do rasterizador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState *pRasterizerState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indexe em uma matriz de interfaces do rasterizador. Se houver apenas uma interface do rasterizador, use 0.

</dd> <dt>

*pRasterizerState* 
</dt> <dd>

Tipo: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***

Ponteiro para uma interface [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) .

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

