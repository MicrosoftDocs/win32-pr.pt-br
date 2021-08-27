---
title: Método ID3DX11EffectDepthStencilVariable UndoSetDepthStencilState (D3dx11effect. h)
description: Reverte um estado de estêncil de profundidade definido anteriormente.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- Método UndoSetDepthStencilState Direct3D 11
- Método UndoSetDepthStencilState Direct3D 11, interface ID3DX11EffectDepthStencilVariable
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, método UndoSetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 626c430c268c7c8c63e006bdde9e62a49d139d2212e08d7a3e4cedeea3d31722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989808"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a>Método ID3DX11EffectDepthStencilVariable:: UndoSetDepthStencilState

Reverte um estado de estêncil de profundidade definido anteriormente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indexe em uma matriz de interfaces de estêncil de profundidade. Se houver apenas uma interface de estêncil de profundidade, use 0.

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

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

