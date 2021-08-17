---
title: Método ID3DX11EffectVariable IsValid (D3dx11effect.h)
description: Compare o tipo de dados com os dados armazenados.
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- Método IsValid Direct3D 11
- Método IsValid Direct3D 11 , interface ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , método IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198fcd1a5dc39823df8c707d97849c5115d818b784dd78b1e960ee2463087ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734055"
---
# <a name="id3dx11effectvariableisvalid-method"></a>Método ID3DX11EffectVariable::IsValid

Compare o tipo de dados com os dados armazenados.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE** se a sintaxe for válida; caso **contrário, FALSE.**

## <a name="remarks"></a>Comentários

Esse método verifica se o tipo de dados corresponde aos dados armazenados após a transmissão de uma interface para outra (usando qualquer um dos métodos As).

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

 

