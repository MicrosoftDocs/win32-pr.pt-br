---
description: Cria uma interface de conjunto de animação de chave ID3DXKeyframedAnimationSet com quadros.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: Função D3DXCreateKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f3eb45e999d25c776014c3df5824e0468d03ffd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813567"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a>Função D3DXCreateKeyframedAnimationSet

Cria uma interface de conjunto de animação de chave [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) com quadros.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do conjunto de animações.

</dd> <dt>

*TicksPerSecond* \[ no\]
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Número de tiques de quadro chave decorridos por segundo.

</dd> <dt>

*Reprodução* \[ no\]
</dt> <dd>

Tipo: **[ **\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md)**

Tipo do loop de reprodução do conjunto de animações. Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).

</dd> <dt>

*NumAnimations* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de conjuntos de animação de escala, girar e traduzir (SRT).

</dd> <dt>

*NumCallbackKeys* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de chaves de retorno de chamada.

</dd> <dt>

*pCallKeys* \[ no\]
</dt> <dd>

Tipo: **[**retorno de \_ chamada**](d3dxkey-callback.md) \* const LPD3DXKEY**

Ponteiro para uma estrutura de [**\_ retorno de chamada D3DXKEY**](d3dxkey-callback.md) que armazena dados de retorno de chamada do usuário.

</dd> <dt>

*ppAnimationSet* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***

Endereço de um ponteiro para a interface do conjunto de animações com quadros chave [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de animação](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
