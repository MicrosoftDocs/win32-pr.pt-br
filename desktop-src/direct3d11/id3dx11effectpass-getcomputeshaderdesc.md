---
title: Método ID3DX11EffectPass GetComputeShaderDesc (D3dx11effect. h)
description: Obtenha uma descrição do sombreador de computação.
ms.assetid: 9c3a702f-2016-4b1a-a832-d1bb968aec2d
keywords:
- Método GetComputeShaderDesc Direct3D 11
- Método GetComputeShaderDesc Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, método GetComputeShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetComputeShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21cc13699553b0da60498209ddffd31a56607809
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930705"
---
# <a name="id3dx11effectpassgetcomputeshaderdesc-method"></a>Método ID3DX11EffectPass:: GetComputeShaderDesc

Obtenha uma descrição do sombreador de computação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetComputeShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)\***

Um ponteiro para uma descrição de sombreador de computação (consulte [**D3DX11 \_ Pass \_ Shader \_ desc**](d3dx11-pass-shader-desc.md)).

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





