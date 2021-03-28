---
title: Método ID3DX11Effect GetVariableByIndex (D3dx11effect. h)
description: Obter uma variável por índice.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Método GetVariableByIndex Direct3D 11
- Método GetVariableByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetVariableByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989371"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a>Método ID3DX11Effect:: GetVariableByIndex

Obter uma variável por índice.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Um índice de base zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Comentários

Um efeito pode conter uma ou mais variáveis. Variáveis fora de uma técnica são consideradas globais para todos os efeitos, aquelas localizadas dentro de uma técnica são locais para essa técnica. Você pode acessar qualquer variável de efeito local não estática usando seu nome ou com um índice.

O método retornará um ponteiro para uma [**interface variável de efeito**](id3dx11effectvariable.md) se uma variável não for encontrada; Você pode chamar [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) para verificar se o índice existe ou não.

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

