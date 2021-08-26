---
title: Método AsString ID3DX11EffectVariable (D3dx11effect.h)
description: Obter uma variável de cadeia de caracteres.
ms.assetid: 60f8a730-bf95-4577-9259-7348d479ac3d
keywords:
- Método AsString Direct3D 11
- Método AsString Direct3D 11 , interface ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , método AsString
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c69eecaabec6b7da49f7f36f6c75677fdd20cdb462f26fe5e02650e6746c01f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069606"
---
# <a name="id3dx11effectvariableasstring-method"></a>Método ID3DX11EffectVariable::AsString

Obter uma variável de cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectStringVariable* AsString();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***

Um ponteiro para uma variável de cadeia de caracteres. Consulte [**ID3DX11EffectStringVariable.**](id3dx11effectstringvariable.md)

## <a name="remarks"></a>Comentários

AsString retorna uma versão da variável de efeito que foi especializada em uma variável de cadeia de caracteres. Semelhante a uma cast, essa especialização retornará um objeto inválido se a variável de efeito não contém dados de cadeia de caracteres.

Os aplicativos podem testar a validade do objeto retornado chamando [**IsValid.**](id3dx11effectvariable-isvalid.md)

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





