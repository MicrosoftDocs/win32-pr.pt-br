---
title: Método ID3DX11EffectVariable GetMemberBySemantic (D3dx11effect. h)
description: Obtenha um membro de estrutura por semântica.
ms.assetid: e4ae1f6a-43d2-45df-9dba-833d4f767818
keywords:
- Método GetMemberBySemantic Direct3D 11
- Método GetMemberBySemantic Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetMemberBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af8b628247dcc89f8df99c6ffebb04d500e76a1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989400"
---
# <a name="id3dx11effectvariablegetmemberbysemantic-method"></a>Método ID3DX11EffectVariable:: GetMemberBySemantic

Obtenha um membro de estrutura por semântica.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectVariable* GetMemberBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Semântico* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

A semântica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Comentários

Se a variável de efeito for uma estrutura, use esse método para pesquisar um membro por semântica anexada.

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

