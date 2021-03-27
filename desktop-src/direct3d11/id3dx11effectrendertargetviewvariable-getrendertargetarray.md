---
title: Método ID3DX11EffectRenderTargetViewVariable GetRenderTargetArray (D3dx11effect. h)
description: Obtenha uma matriz de destinos de renderização.
ms.assetid: cc98a3b3-c2a2-48d0-86a8-77b914a199ec
keywords:
- Método GetRenderTargetArray Direct3D 11
- Método GetRenderTargetArray Direct3D 11, interface ID3DX11EffectRenderTargetViewVariable
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11, método GetRenderTargetArray
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3521b05bbc4e603264b993b6fe7b677a5cf46aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989409"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertargetarray-method"></a>Método ID3DX11EffectRenderTargetViewVariable:: GetRenderTargetArray

Obtenha uma matriz de destinos de renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppResources* 
</dt> <dd>

Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***

Um ponteiro para uma matriz de interfaces de exibição de destino de renderização. Consulte [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

</dd> <dt>

*Deslocamento* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O índice de matriz com base em zero para obter a primeira interface.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de elementos na matriz.

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

 

