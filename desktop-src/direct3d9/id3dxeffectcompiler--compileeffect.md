---
description: Compile um efeito.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: 'Método ID3DXEffectCompiler:: CompileEffect (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f3769f3f7433aadc55e766d68ecc152a4e26444cf506344f80e3f11a0bca8fcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951656"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a>Método ID3DXEffectCompiler:: CompileEffect

Compile um efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opções de compilação identificadas por vários sinalizadores. O compilador do Direct3D 10 HLSL agora é o padrão. Consulte [D3DXSHADER flags](d3dxshader-flags.md) para obter detalhes.

</dd> <dt>

*ppEffect* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém o efeito compilado. Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppErrorMsgs* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém pelo menos a primeira mensagem de erro de compilação que ocorreu. Isso inclui efeitos de erros de compilador e erros de compilação de linguagem de alto nível. Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK.

Se os argumentos forem inválidos, o método retornará D3DERR \_ INVALIDCALL.

Se o método falhar, o valor de retorno será E \_ falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> </dl>

 

 
