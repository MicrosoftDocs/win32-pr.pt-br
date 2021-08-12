---
description: Define um vetor normal para cada texel em um objeto de textura. Esse método é usado para armazenar vetores normais de vértice de uma malha (ou normais de vértice interpolados se a PRT (transferência de radiance pré-computada) baseada em pixel estiver sendo computada).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: Método ID3DXPRTEngine::SetPerTexelNormal (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75877e8af86a22f80703742f148d5171e3a99e5c0c580bff588c27deba269b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293370"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a>Método ID3DXPRTEngine::SetPerTexelNormal

Define um vetor normal para cada texel em um objeto de textura. Esse método é usado para armazenar vetores normais de vértice de uma malha (ou normais de vértice interpolados se a PRT (transferência de radiance pré-computada) baseada em pixel estiver sendo computada).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNormalTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para um objeto de textura [**IDirect3DTexture9**](/windows/desktop/api) que serve como um mapa normal de espaço de objeto no qual armazenar vetores normais. A textura deve ter as mesmas dimensões que [**ID3DXPRTBuffer**](id3dxprtbuffer.md) e deve ser capaz de armazenar formatos de textura assinados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
