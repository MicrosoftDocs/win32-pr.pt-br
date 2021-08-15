---
title: Método ID3DX11EffectVariable AsUnorderedAccessView (D3dx11effect.h)
description: Obter uma variável unordered-access-view.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- Método AsUnorderedAccessView Direct3D 11
- Método AsUnorderedAccessView Direct3D 11 , interface ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , método AsUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4cf3a1f146af7ca6faf3ff3e704285ac19f01a117809429842b45df9b7dcfd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531204"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a>Método ID3DX11EffectVariable::AsUnorderedAccessView

Obter uma variável unordered-access-view.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***

Um ponteiro para uma variável unordered-access-view. Consulte [**ID3DX11EffectUnorderedAccessViewVariable.**](id3dx11effectunorderedaccessviewvariable.md)

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

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





