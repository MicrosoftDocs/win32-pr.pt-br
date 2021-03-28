---
title: Método IsValid ID3DX11EffectVariable (D3dx11effect. h)
description: Compare o tipo de dados com os dados armazenados.
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- Método IsValid Direct3D 11
- Método IsValid Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método IsValid
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
ms.openlocfilehash: b5136005e675a6f5e54cc3863ef2d80ffadfb7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989380"
---
# <a name="id3dx11effectvariableisvalid-method"></a>Método ID3DX11EffectVariable:: IsValid

Compare o tipo de dados com os dados armazenados.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** se a sintaxe for válida; caso contrário, **false**.

## <a name="remarks"></a>Comentários

Esse método verifica se o tipo de dados corresponde aos dados armazenados após a conversão de uma interface para outra (usando qualquer um dos métodos as).

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

 

