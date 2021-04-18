---
description: Obtém um ponteiro para a função de fluxo DWORD.
ms.assetid: a051b51a-185c-4a9e-a8b9-4096615e2634
title: 'Método ID3DXTextureShader:: GetFunction (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetFunction
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80e504e65e4c8437247b2935794025e1b693433a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761541"
---
# <a name="id3dxtextureshadergetfunction-method"></a>Método ID3DXTextureShader:: GetFunction

Obtém um ponteiro para a função de fluxo DWORD.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFunction(
  [in] LPD3DXBUFFER *ppFunction
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppFunction* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Um ponteiro para a função de fluxo DWORD. Consulte [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




