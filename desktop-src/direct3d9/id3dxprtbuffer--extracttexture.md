---
description: Extrai dados de coeficiente de um canal de cores do buffer para um intervalo especificado de coeficientes e adiciona os dados a um objeto IDirect3DTexture9.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: Método ID3DXPRTBuffer::ExtractTexture (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6f91186a15aa166928103073fdaca30d79809ad8c0a522abf3b136cb20a1d43a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120620"
---
# <a name="id3dxprtbufferextracttexture-method"></a>Método ID3DXPRTBuffer::ExtractTexture

Extrai dados de coeficiente de um canal de cores do buffer para um intervalo especificado de coeficientes e adiciona os dados a [**um objeto IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Canal* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Canal de cor do buffer do qual extrair dados de textura.

</dd> <dt>

*StartCoefficient* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Valor inicial do coeficiente de buffer do qual extrair dados de textura.

</dd> <dt>

*NumCoefficients* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de escalares, começando em StartCoefficient, do qual extrair dados de textura.

</dd> <dt>

*pTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para um [**objeto de textura IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que armazenará coeficientes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
