---
description: Concatena um grupo de malhas em uma malha comum. Esse método pode, opcionalmente, aplicar uma transformação de matriz para cada malha de entrada e suas coordenadas de textura.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: Função D3DXConcatenateMeshes (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21801c2f4b8ef8dd2a34c9788b402128da4ce4fed33c3c38a08e61c35a847e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857386"
---
# <a name="d3dxconcatenatemeshes-function"></a>Função D3DXConcatenateMeshes

Concatena um grupo de malhas em uma malha comum. Esse método pode, opcionalmente, aplicar uma transformação de matriz para cada malha de entrada e suas coordenadas de textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppMeshes* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Matriz de ponteiros de malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)). O número de elementos na matriz é NumMeshes.

</dd> <dt>

*NumMeshes* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de malhas de entrada a serem concatenadas.

</dd> <dt>

*Opções* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opções de criação de malha; Essa é uma combinação de um ou mais sinalizadores [**D3DXMESH**](./d3dxmesh.md) . As opções de criação de malha são equivalentes ao parâmetro options exigido por [**D3DXCreateMesh**](d3dxcreatemesh.md).

</dd> <dt>

*pGeomXForms* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matriz opcional de transformações de geometria. O número de elementos na matriz é NumMeshes; cada elemento é uma matriz de transformação (consulte [**D3DXMATRIX**](d3dxmatrix.md)). Pode ser **NULL**.

</dd> <dt>

*pTextureXForms* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matriz opcional de transformações de textura. O número de elementos na matriz é NumMeshes; cada elemento é uma matriz de transformação (consulte [**D3DXMATRIX**](d3dxmatrix.md)). Esse parâmetro pode ser **nulo**.

</dd> <dt>

*pDecl* \[ no\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Ponteiro opcional para uma declaração de vértice (consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)). Esse parâmetro pode ser **nulo**.

</dd> <dt>

*pD3DDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para um dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que é usado para criar a nova malha.

</dd> <dt>

*ppMeshOut* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para a malha criada (consulte [**ID3DXMesh**](id3dxmesh.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Se nenhuma [declaração de vértice](vertex-declaration.md) for fornecida como parte do parâmetro de criação de malha de opções, o método irá gerar uma União de todas as declarações de vértice das submalhas, promovendo canais e tipos, se necessário. O método criará uma tabela de atributos de tabelas de atributos das malhas de entrada. Para garantir a criação de uma tabela de atributos, chame [**Optimize**](id3dxmesh--optimize.md) com flags definido como D3DXMESHOPT \_ Compact e D3DXMESHOPT \_ ATTRSORT (consulte [**D3DXMESHOPT**](./d3dxmeshopt.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
