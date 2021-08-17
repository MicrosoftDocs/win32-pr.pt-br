---
title: Método asrasterizador ID3DX11EffectVariable (D3dx11effect. h)
description: Obter uma variável de rasterizador.
ms.assetid: 6a55d067-f527-4a1b-a4d4-a6d1719aebe7
keywords:
- Método asrasterizador Direct3D 11
- Método asrasterizador Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método asrasterizador
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRasterizer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfaf83debc6c7e73a89f78b0c8c3899cce2fb83fb6a5884fa5a5ed9ed5b35912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858096"
---
# <a name="id3dx11effectvariableasrasterizer-method"></a>Método ID3DX11EffectVariable:: asrasterizador

Obter uma variável de rasterizador.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectRasterizerVariable* AsRasterizer();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***

Um ponteiro para uma variável rasterizadora. Consulte [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md).

## <a name="remarks"></a>Comentários

O asrasterizador retorna uma versão da variável de efeito que foi especializada em uma variável rasterizadora. De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados rasterizadores.

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

 

 





