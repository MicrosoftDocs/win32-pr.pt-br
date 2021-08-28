---
description: Desmonte um efeito.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: Função D3DXDisassembleEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e4fa48418513cd9f4f70bc8356965a45499d1c6d822eaa1c1952d25ebe4b1ac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119216"
---
# <a name="d3dxdisassembleeffect-function"></a>Função D3DXDisassembleEffect

Desmonte um efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pEffect* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)**

Ponteiro para uma interface [**ID3DXEffect**](id3dxeffect.md) que contém o efeito.

</dd> <dt>

*EnableColorCode* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Habilite a codificação de cores para facilitar a leitura da desmontagem.

</dd> <dt>

*ppDisassembly* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém o sombreador desmontado. Consulte [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de efeito](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
