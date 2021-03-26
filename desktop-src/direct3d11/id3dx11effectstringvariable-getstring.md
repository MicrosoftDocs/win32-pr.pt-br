---
title: Método GetString ID3DX11EffectStringVariable (D3dx11effect. h)
description: Obter a cadeia de caracteres.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- Método GetString Direct3D 11
- Método GetString Direct3D 11, interface ID3DX11EffectStringVariable
- Interface ID3DX11EffectStringVariable Direct3D 11, método GetString
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d15666bd70bf00395b7052b7820981dd8d0dcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968562"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a>Método ID3DX11EffectStringVariable:: GetString

Obter a cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppString* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***

Um ponteiro para a cadeia de caracteres.

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

 

