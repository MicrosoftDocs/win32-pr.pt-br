---
title: Método ID3DX11EffectShaderVariable GetShaderDesc (D3dx11effect. h)
description: Obter uma descrição do sombreador.
ms.assetid: 7dd667d3-c500-4486-b279-a165befe8733
keywords:
- Método GetShaderDesc Direct3D 11
- Método GetShaderDesc Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, método GetShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f78e3a41fbd7f1063abdbd8c782119f62e141b7fa5a160106cf85be274435fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676846"
---
# <a name="id3dx11effectshadervariablegetshaderdesc-method"></a>Método ID3DX11EffectShaderVariable:: GetShaderDesc

Obter uma descrição do sombreador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetShaderDesc(
   UINT                      ShaderIndex,
   D3DX11_EFFECT_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Um índice de base zero.

</dd> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ de \_ sombreador de efeito \_ desc**](d3dx11-effect-shader-desc.md)\***

Um ponteiro para uma descrição do sombreador (consulte [**D3DX11 \_ Effect \_ Shader \_ desc**](d3dx11-effect-shader-desc.md)).

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

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

