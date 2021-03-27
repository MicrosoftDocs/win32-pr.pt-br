---
title: Método getbool ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Obter uma variável booliana.
ms.assetid: 9d2789af-c59f-4d2d-87c6-9f36286e8a15
keywords:
- Método getbool Direct3D 11
- Método getbool Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, método getbool
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 754dd8856876ca441e83267250dcfad4f4011c69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664096"
---
# <a name="id3dx11effectscalarvariablegetbool-method"></a>Método ID3DX11EffectScalarVariable:: getbool

Obter uma variável booliana.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBool(
   BOOL *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Valores* 
</dt> <dd>

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***

Um ponteiro para a variável.

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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

