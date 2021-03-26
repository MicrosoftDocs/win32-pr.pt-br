---
title: Método ID3DX11EffectStringVariable GetStringArray (D3dx11effect. h)
description: Obter uma matriz de cadeias de caracteres.
ms.assetid: 2cc45b2f-1851-49d2-8844-3e249c48f327
keywords:
- Método GetStringArray Direct3D 11
- Método GetStringArray Direct3D 11, interface ID3DX11EffectStringVariable
- Interface ID3DX11EffectStringVariable Direct3D 11, método GetStringArray
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetStringArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2050ebd7c9ae3735385a379e6ef7bdff0e1cfd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968561"
---
# <a name="id3dx11effectstringvariablegetstringarray-method"></a>Método ID3DX11EffectStringVariable:: GetStringArray

Obter uma matriz de cadeias de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStringArray(
   LPCSTR *ppStrings,
   UINT   Offset,
   UINT   Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppStrings* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***

Um ponteiro para a primeira cadeia de caracteres na matriz.

</dd> <dt>

*Deslocamento* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O deslocamento (em número de cadeias de caracteres) entre o início da matriz e a primeira cadeia de caracteres a ser obtida.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de cadeias de caracteres na matriz retornada.

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

[ID3DX11EffectStringVariable](id3dx11effectstringvariable.md)
</dt> </dl>

 

