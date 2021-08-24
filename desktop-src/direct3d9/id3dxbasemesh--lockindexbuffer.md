---
description: Bloqueia um buffer de índice e obtém um ponteiro para a memória do buffer de índice.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: Método ID3DXBaseMesh::LockIndexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2eab2806775572cb4e4c4a50899d48263c6ddf0d55138c37bcaff8367225c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118816"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a>Método ID3DXBaseMesh::LockIndexBuffer

Bloqueia um buffer de índice e obtém um ponteiro para a memória do buffer de índice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LockIndexBuffer(
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

Para ver uma descrição dos sinalizadores, [consulte D3DLOCK.](d3dlock.md)

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

PONTEIRO \* VOID para um buffer que contém os dados de índice. A contagem de índices nesse buffer será igual a [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Ao trabalhar com buffers de índice, você tem permissão para fazer várias chamadas de bloqueio. No entanto, você deve garantir que o número de chamadas de bloqueio corresponder ao número de chamadas de desbloqueio. As chamadas DrawPrimitive não terão êxito com nenhuma contagem de bloqueio pendente em nenhum buffer de índice definido no momento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
