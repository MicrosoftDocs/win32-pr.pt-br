---
title: Método ID3DX11Effect GetVariableBySemantic (D3dx11effect. h)
description: Obter uma variável por semântica.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- Método GetVariableBySemantic Direct3D 11
- Método GetVariableBySemantic Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetVariableBySemantic
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173132"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a>Método ID3DX11Effect:: GetVariableBySemantic

Obter uma variável por semântica.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Semântico* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

O nome semântico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Um ponteiro para a variável de efeito indicada pela semântica. Consulte [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Comentários

Cada variável de efeito pode ter uma semântica anexada, que é uma cadeia de caracteres de metadados definida pelo usuário. Algumas [semânticas de valor do sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) são palavras reservadas que disparam a funcionalidade interna por estágios de pipeline.

O método retornará um ponteiro para uma [**interface variável de efeito**](id3dx11effectvariable.md) se uma variável não for encontrada; Você pode chamar [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) para verificar se a semântica existe ou não.

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

