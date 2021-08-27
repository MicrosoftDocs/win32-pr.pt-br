---
title: Método ID3DX11EffectBlendVariable UndoSetBlendState (D3dx11effect. h)
description: Reverte um estado de mesclagem definido anteriormente.
ms.assetid: 375c225b-558f-4ad0-81e7-62eff3e28cf1
keywords:
- Método UndoSetBlendState Direct3D 11
- Método UndoSetBlendState Direct3D 11, interface ID3DX11EffectBlendVariable
- Interface ID3DX11EffectBlendVariable Direct3D 11, método UndoSetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.UndoSetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fefb1e59ef3ef30bcd21700a2573830e3178f574fe631ab4c7373b0bddd5fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046474"
---
# <a name="id3dx11effectblendvariableundosetblendstate-method"></a>Método ID3DX11EffectBlendVariable:: UndoSetBlendState

Reverte um estado de mesclagem definido anteriormente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UndoSetBlendState(
   UINT Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indexe em uma matriz de interfaces de estado de mesclagem. Se houver apenas uma interface de estado de mesclagem, use 0.

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

