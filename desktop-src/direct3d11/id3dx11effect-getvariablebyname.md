---
title: Método ID3DX11Effect GetVariableByName (D3dx11effect. h)
description: Obter uma variável por nome.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Método GetVariableByName Direct3D 11
- Método GetVariableByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetVariableByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989369"
---
# <a name="id3dx11effectgetvariablebyname-method"></a>Método ID3DX11Effect:: GetVariableByName

Obter uma variável por nome.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

O nome da variável.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Retorna uma variável inválida se o nome especificado não puder ser encontrado.

## <a name="remarks"></a>Comentários

Um efeito pode conter uma ou mais variáveis. Variáveis fora de uma técnica são consideradas globais para todos os efeitos, aquelas localizadas dentro de uma técnica são locais para essa técnica. Você pode acessar uma variável de efeito usando seu nome ou com um índice.

O método retorna um ponteiro para uma [**interface de variável de efeito,**](id3dx11effectvariable.md) independentemente de uma variável ser ou não encontrada. [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) deve ser chamado para verificar se o nome existe ou não.

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

 

