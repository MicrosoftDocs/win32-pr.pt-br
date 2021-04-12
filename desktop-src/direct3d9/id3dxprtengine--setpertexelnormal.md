---
description: Define um vetor normal para cada Texel em um objeto de textura. Esse método é usado para armazenar vetores normais de vértice de uma malha (ou um vértice interpolado Normals se a transferência de radiante (PRT) baseada em pixels estiver sendo computada).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'Método ID3DXPRTEngine:: SetPerTexelNormal (D3DX9Mesh. h)'
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
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370973"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a>Método ID3DXPRTEngine:: SetPerTexelNormal

Define um vetor normal para cada Texel em um objeto de textura. Esse método é usado para armazenar vetores normais de vértice de uma malha (ou um vértice interpolado Normals se a transferência de radiante (PRT) baseada em pixels estiver sendo computada).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNormalTexture* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para um objeto de textura [**IDirect3DTexture9**](/windows/desktop/api) que serve como um mapa normal de espaço de objeto no qual armazenar vetores normais. A textura deve ter as mesmas dimensões que [**ID3DXPRTBuffer**](id3dxprtbuffer.md) e deve ser capaz de armazenar formatos de textura assinados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
