---
title: Método ID3DX11EffectShaderVariable GetComputeShader (D3dx11effect. h)
description: Obtenha um sombreador de computação.
ms.assetid: 16a48be1-4e73-4206-837f-615f8d624086
keywords:
- Método GetComputeShader Direct3D 11
- Método GetComputeShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, método GetComputeShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetComputeShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9312a7d603370d53c0721574623733c9e75da8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173208"
---
# <a name="id3dx11effectshadervariablegetcomputeshader-method"></a>Método ID3DX11EffectShaderVariable:: GetComputeShader

Obtenha um sombreador de computação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetComputeShader(
   UINT                ShaderIndex,
   ID3D11ComputeShader **ppPS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice do sombreador de computação.

</dd> <dt>

*ppPS* 
</dt> <dd>

Tipo: **[ **ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***

Ponteiro para um ponteiro [**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) que será definido para o sombreador de computação no retorno.

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

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

