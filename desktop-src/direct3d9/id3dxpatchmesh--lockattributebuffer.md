---
description: Bloqueia o buffer de atributo.
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: 'Método ID3DXPatchMesh:: LockAttributeBuffer (D3DX9Mesh. h)'
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
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105754088"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a>Método ID3DXPatchMesh:: LockAttributeBuffer

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

*sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executado. Para esse método, os sinalizadores válidos são:

-   \_Descartar D3DLOCK
-   D3DLOCK \_ nenhuma \_ \_ atualização suja
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ ReadOnly

Para obter uma descrição dos sinalizadores, consulte [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Endereço de um ponteiro para um buffer que contém um DWORD para cada face na malha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

O buffer de atributo é geralmente bloqueado, gravado e, em seguida, desbloqueado para leitura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
