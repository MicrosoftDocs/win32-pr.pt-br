---
description: Bloquear o buffer de vértice.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'Método ID3DXPatchMesh:: LockVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837955"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a>Método ID3DXPatchMesh:: LockVertexBuffer

Bloquear o buffer de vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executado. Para esse método, os sinalizadores válidos são:

-   \_Descartar D3DLOCK
-   D3DLOCK \_ nenhuma \_ \_ atualização suja
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ ReadOnly
-   D3DLOCK \_ NOoverwrite

Para obter uma descrição dos sinalizadores, consulte [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*Ponteiro void para um buffer de memória que contém os dados de vértice retornados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

O buffer de vértice é geralmente bloqueado, gravado e, em seguida, desbloqueado para leitura.

As malhas de patch usam buffers de índice de 16 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
