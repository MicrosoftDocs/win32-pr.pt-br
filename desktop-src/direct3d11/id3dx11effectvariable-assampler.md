---
title: Método ID3DX11EffectVariable de multiamostrar (D3dx11effect. h)
description: Obter uma variável de amostra.
ms.assetid: dff699f7-758a-442b-93eb-23a09468251f
keywords:
- Método asamostrador Direct3D 11
- Método asamostrador Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método asamostrador
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1213320950377f6981348a158c3d8c8ef4d4fd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989425"
---
# <a name="id3dx11effectvariableassampler-method"></a>Método ID3DX11EffectVariable:: asamostrador

Obter uma variável de amostra.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectSamplerVariable* AsSampler();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)\***

Um ponteiro para uma variável de amostra. Consulte [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md).

## <a name="remarks"></a>Comentários

O asamostrador retorna uma versão da variável de efeito que foi especializada em uma variável de amostra. De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados de amostra.

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

 

 





