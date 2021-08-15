---
description: Dimensiona todos os exemplos associados a um determinado submesh. O método é útil para calcular o dispersão de subsuficiência.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: Método ID3DXPRTEngine::ScaleMeshChunk (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a42046678ef0b44f011c8440cd3456dc9ff236ec0f7a280b4650b49aa53c10d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729580"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a>Método ID3DXPRTEngine::ScaleMeshChunk

Dimensiona todos os exemplos associados a um determinado submesh. O método é útil para calcular o dispersão de subsuficiência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uMeshChunk* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Local na malha na qual começar a dimensionar amostras.

</dd> <dt>

*fScale* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor pelo qual multiplicar cada vetor no submesh.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um [**objeto ID3DXPRTBuffer**](id3dxprtbuffer.md) para receber exemplos redimensionados no submesh.

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

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
