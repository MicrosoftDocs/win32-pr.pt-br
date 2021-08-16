---
title: Método asblend ID3DX11EffectVariable (D3dx11effect. h)
description: Obter uma variável de combinação de efeito.
ms.assetid: e9670d13-e006-408b-9cdf-352bcfa66a52
keywords:
- Método asblend Direct3D 11
- Método asblend Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método asblend
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsBlend
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fd9f6f76c0e3aa46e176b2f35960196fcc73eb021d4e5a250be4a5b245a5ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531598"
---
# <a name="id3dx11effectvariableasblend-method"></a>Método ID3DX11EffectVariable:: asblend

Obter uma variável de combinação de efeito.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectBlendVariable* AsBlend();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)\***

Um ponteiro para uma variável de combinação de efeito. Consulte [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md).

## <a name="remarks"></a>Comentários

O asblend retorna uma versão da variável de efeito que foi especializada em uma variável de combinação de efeito. De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados de mistura de efeito.

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

 

 





