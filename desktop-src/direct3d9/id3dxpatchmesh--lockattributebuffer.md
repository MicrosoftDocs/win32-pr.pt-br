---
description: Bloqueia o buffer de atributo.
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: Método ID3DXPatchMesh::LockAttributeBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b3c550037e156ea5584b65af6d6adb1cb666614de257c590a8d4944283ebdfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120760"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a>Método ID3DXPatchMesh::LockAttributeBuffer

Bloqueia o buffer de atributo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
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

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Endereço de um ponteiro para um buffer que contém um DWORD para cada rosto na malha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

O buffer de atributo geralmente é bloqueado, gravado e desbloqueado para leitura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
