---
description: Cria uma interface de conjunto de animações com quadros-chave ID3DXCompressedAnimationSet que armazena dados de quadro de chave em um formato compactado.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: Função D3DXCreateCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2acca9d1b697bb9b06b47aa75948ca74ec00cc7ecb919334c01cf874293cb495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299281"
---
# <a name="d3dxcreatecompressedanimationset-function"></a>Função D3DXCreateCompressedAnimationSet

Cria uma interface de conjunto de animações com quadros-chave [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) que armazena dados de quadro de chave em um formato compactado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
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

*pCompressedData* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Ponteiro para o buffer [**ID3DXBuffer**](id3dxbuffer.md) que armazena a animação definida como dados compactados.

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

Tipo: **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***

Endereço de um ponteiro para a interface [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) que armazena dados de quadros de animação de chave definida em um formato compactado.

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

 

 
