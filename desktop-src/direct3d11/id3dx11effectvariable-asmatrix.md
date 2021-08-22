---
title: Método AsMatrix ID3DX11EffectVariable (D3dx11effect.h)
description: Obter uma variável de matriz.
ms.assetid: 5d2baf65-ab0d-44df-bc6f-6ffae16cbb01
keywords:
- Método AsMatrix Direct3D 11
- Método AsMatrix Direct3D 11 , interface ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , método AsMatrix
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 294f3f6a01d88f92f606e5120edbfa8d5086f2e0173375fd78f5525c17c4f1f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531497"
---
# <a name="id3dx11effectvariableasmatrix-method"></a>Método ID3DX11EffectVariable::AsMatrix

Obter uma variável de matriz.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectMatrixVariable* AsMatrix();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)\***

Um ponteiro para uma variável de matriz. Consulte [**ID3DX11EffectMatrixVariable.**](id3dx11effectmatrixvariable.md)

## <a name="remarks"></a>Comentários

AsMatrix retorna uma versão da variável de efeito que foi especializada para uma variável de matriz. Semelhante a uma cast, essa especialização retornará um objeto inválido se a variável de efeito não contém dados de matriz.

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

 

 





