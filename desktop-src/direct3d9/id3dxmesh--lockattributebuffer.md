---
description: Bloqueia o buffer de malha que contém os dados de atributo de malha e retorna um ponteiro para ele.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'Método ID3DXMesh:: LockAttributeBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760487"
---
# <a name="id3dxmeshlockattributebuffer-method"></a>Método ID3DXMesh:: LockAttributeBuffer

Bloqueia o buffer de malha que contém os dados de atributo de malha e retorna um ponteiro para ele.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de zero ou mais sinalizadores de bloqueio que descrevem o tipo de bloqueio a ser executado. Para esse método, os sinalizadores válidos são:

-   \_Descartar D3DLOCK
-   D3DLOCK \_ nenhuma \_ \_ atualização suja
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ ReadOnly

Para obter uma descrição dos sinalizadores, consulte [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Endereço de um ponteiro para um buffer que contém um DWORD para cada face na malha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Se [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) tiver sido chamado, a malha também terá uma tabela de atributos que pode ser acessada usando o método [**ID3DXBaseMesh:: getattributetable**](id3dxbasemesh--getattributetable.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[**ID3DXBaseMesh:: getattributetable**](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[**ID3DXMesh:: SetAttributeTable**](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
