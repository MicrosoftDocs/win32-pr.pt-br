---
description: Esse método permite que o usuário altere a declaração de malha sem alterar o layout de dados do buffer de vértice. A chamada será válida somente se os formatos de declaração antigo e novo tiverem o mesmo tamanho de vértice.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'Método ID3DXBaseMesh:: UpdateSemantics (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012109"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a>Método ID3DXBaseMesh:: UpdateSemantics

Esse método permite que o usuário altere a declaração de malha sem alterar o layout de dados do buffer de vértice. A chamada será válida somente se os formatos de declaração antigo e novo tiverem o mesmo tamanho de vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Declaração* \[ de entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Uma matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que descreve o formato de vértice dos vértices de malha. O limite superior dessa matriz de Declarador é o [**tamanho máximo de \_ \_ DECL \_ FVF**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

[**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) é usado para reformatar e alterar o layout de dados de vértice. Por exemplo, use-o para adicionar espaço para Normals, coordenadas de textura, cores, pesos, etc. que não estavam presentes antes.

**ID3DXBaseMesh:: UpdateSemantics** é um método para atualizar a declaração de vértice com informações semânticas diferentes, sem alterar o layout do buffer de vértice. Por exemplo, use-o para rerotular uma coordenada de textura 3D como uma binormal ou uma tangente, ou vice-versa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
