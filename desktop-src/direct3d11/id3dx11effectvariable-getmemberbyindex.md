---
title: Método ID3DX11EffectVariable GetMemberByIndex (D3dx11effect. h)
description: Obter um membro de estrutura por índice.
ms.assetid: 256f65aa-5f49-4b83-8dde-ddb6b31c581a
keywords:
- Método GetMemberByIndex Direct3D 11
- Método GetMemberByIndex Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetMemberByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5176eb220dc928a98ec0f579afaeab1c81b1a7ff9ef3555736ed471bf15b9117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124491"
---
# <a name="id3dx11effectvariablegetmemberbyindex-method"></a>Método ID3DX11EffectVariable:: GetMemberByIndex

Obter um membro de estrutura por índice.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectVariable* GetMemberByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Um índice de base zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Comentários

Se a variável de efeito for uma estrutura, use esse método para pesquisar um membro por índice.

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

 

