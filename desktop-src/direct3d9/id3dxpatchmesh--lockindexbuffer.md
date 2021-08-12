---
description: Bloqueie o buffer de índice.
ms.assetid: b68aff75-9ba6-4088-b35f-f56d700d1aff
title: Método ID3DXPatchMesh::LockIndexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd0e4fc41507e6b01dcbf77ae19a69dbc4b8e3df981f4c3366f441f4e4854aa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294339"
---
# <a name="id3dxpatchmeshlockindexbuffer-method"></a>Método ID3DXPatchMesh::LockIndexBuffer

Bloqueie o buffer de índice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executar. Para esse método, os sinalizadores válidos são:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ SEM \_ ATUALIZAÇÃO \_ SUJA
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ READONLY

Para ver uma descrição dos sinalizadores, [consulte D3DLOCK.](d3dlock.md)

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

Ponteiro VOID \* para um buffer de memória que contém os dados de índice retornados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

O buffer de índice geralmente é bloqueado, gravado e desbloqueado para leitura. Buffers de índice de malha de patch são buffers de 16 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
