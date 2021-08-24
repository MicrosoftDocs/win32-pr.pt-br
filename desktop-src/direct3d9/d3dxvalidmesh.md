---
description: Valida uma malha.
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: Função D3DXValidMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 299092700b015840376f3e4b297d7825366b6083e1458155f5963e1b5b1f4d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749666"
---
# <a name="d3dxvalidmesh-function"></a>Função D3DXValidMesh

Valida uma malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMeshIn* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma [**interface ID3DXMesh,**](id3dxmesh.md) representando a malha a ser testada.

</dd> <dt>

*pAdjacency* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada rosto na malha a ser testado.

</dd> <dt>

*ppErrorsAndWarnings* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém uma cadeia de caracteres de erros e avisos, que explica os problemas encontrados na malha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DXERR \_ INVALIDMESH, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método valida a malha verificando se há índices inválidos. As informações de erro estão disponíveis na saída do depurador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
