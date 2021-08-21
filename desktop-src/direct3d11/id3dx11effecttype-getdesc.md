---
title: Método GetDesc de ID3DX11EffectType (D3dx11effect. h)
description: Obter uma descrição do tipo de efeito.
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc do Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381f885a15dede6a500e82b08a1f24e4f0542ffa46211e5b68ef7f73f40d0f0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460776"
---
# <a name="id3dx11effecttypegetdesc-method"></a>Método ID3DX11EffectType:: GetDesc

Obter uma descrição do tipo de efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **\_ tipo de efeito D3DX11 \_ \_ desc**](d3dx11-effect-type-desc.md)\***

Um ponteiro para uma descrição de tipo de efeito. Consulte [**o \_ tipo de efeito D3DX11 \_ \_ desc**](d3dx11-effect-type-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

A descrição da variável de efeito contém dados sobre o nome, as anotações, a semântica, os sinalizadores e o deslocamento do buffer do tipo de efeito.

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

 





