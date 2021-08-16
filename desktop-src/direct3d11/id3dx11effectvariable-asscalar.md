---
title: Método asscaler ID3DX11EffectVariable (D3dx11effect. h)
description: Obter uma variável escalar.
ms.assetid: 5cc02fb3-351a-4309-9145-1ed7d759a650
keywords:
- Método asscaler Direct3D 11
- Método asscaler Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método asscaler
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsScalar
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704002e17d963897111949f559c4798c433c3d939946a735362876fa2e22f7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531407"
---
# <a name="id3dx11effectvariableasscalar-method"></a>Método ID3DX11EffectVariable:: asscaler

Obter uma variável escalar.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectScalarVariable* AsScalar();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)\***

Um ponteiro para uma variável escalar. Consulte [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md).

## <a name="remarks"></a>Comentários

O asscaler retorna uma versão da variável de efeito que foi especializada em uma variável escalar. De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados escalares.

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

 

 





