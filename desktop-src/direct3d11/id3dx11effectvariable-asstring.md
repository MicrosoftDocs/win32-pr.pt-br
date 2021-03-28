---
title: Método AsString ID3DX11EffectVariable (D3dx11effect. h)
description: Obter uma variável de cadeia de caracteres.
ms.assetid: 60f8a730-bf95-4577-9259-7348d479ac3d
keywords:
- Método AsString Direct3D 11
- Método AsString Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método AsString
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
ms.openlocfilehash: 73092dcd27b5651ad6205fa05bcbb13cc1f86116
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298878"
---
# <a name="id3dx11effectvariableasstring-method"></a>Método ID3DX11EffectVariable:: AsString

Obter uma variável de cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectStringVariable* AsString();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***

Um ponteiro para uma variável de cadeia de caracteres. Consulte [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md).

## <a name="remarks"></a>Comentários

AsString retorna uma versão da variável de efeito que foi especializada em uma variável de cadeia de caracteres. De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados de cadeia de caracteres.

Os aplicativos podem testar a validade do objeto retornado chamando [**IsValid**](id3dx11effectvariable-isvalid.md).

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

 

 





