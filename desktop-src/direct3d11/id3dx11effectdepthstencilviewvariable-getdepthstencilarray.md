---
title: Método ID3DX11EffectDepthStencilViewVariable GetDepthStencilArray (D3dx11effect.h)
description: Obter uma matriz de recursos de exibição de estêncil de profundidade.
ms.assetid: 92b2d9b1-6cf8-4523-88e0-bcd09b95477c
keywords:
- Método GetDepthStencilArray Direct3D 11
- Método GetDepthStencilArray Direct3D 11 , interface ID3DX11EffectDepthStencilViewVariable
- ID3DX11EffectDepthStencilViewVariable interface Direct3D 11 , método GetDepthStencilArray
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2981d3da9bd66066009f2b7e9826514f34681935d0b49fe1b014ea9f847beea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952876"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencilarray-method"></a>Método ID3DX11EffectDepthStencilViewVariable::GetDepthStencilArray

Obter uma matriz de recursos de exibição de estêncil de profundidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppResources* 
</dt> <dd>

Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***

Um ponteiro para uma matriz de interfaces de exibição de estêncil de profundidade. Consulte [**ID3D11DepthStencilView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)

</dd> <dt>

*Deslocamento* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O índice de matriz baseado em zero para obter a primeira interface.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O número de elementos na matriz.

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

 

