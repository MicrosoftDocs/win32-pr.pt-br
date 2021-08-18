---
description: Bloqueia um buffer de vértice e obtém um ponteiro para a memória do buffer de vértice.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: Método ID3DXBaseMesh::LockVertexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bb0cd8539a996b66ccf9f413e57ebf1d213fe6372e56b50b35abc5e210595f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987606"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a>Método ID3DXBaseMesh::LockVertexBuffer

Bloqueia um buffer de vértice e obtém um ponteiro para a memória do buffer de vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executar. Para esse método, os sinalizadores válidos são:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ SEM \_ ATUALIZAÇÃO \_ SUJA
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ READONLY
-   D3DLOCK \_ NOOVERWRITE

Para ver uma descrição dos sinalizadores, [consulte D3DLOCK.](d3dlock.md)

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

PONTEIRO \* VOID para um buffer que contém os dados de vértice.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Ao trabalhar com buffers de vértice, você tem permissão para fazer várias chamadas de bloqueio; No entanto, você deve garantir que o número de chamadas de bloqueio corresponder ao número de chamadas de desbloqueio. As chamadas DrawPrimitive não terão êxito com nenhuma contagem de bloqueio pendente em nenhum buffer de vértice definido no momento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
