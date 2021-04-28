---
description: Função D3DXCreateMesh – cria um objeto de malha usando um Declarador.
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: Função D3DXCreateMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c7e1c0d626c74f5427f91a5b9eb796e3b79d5a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102754"
---
# <a name="d3dxcreatemesh-function"></a>Função D3DXCreateMesh

Cria um objeto de malha usando um Declarador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateMesh(
  _In_        DWORD               NumFaces,
  _In_        DWORD               NumVertices,
  _In_        DWORD               Options,
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _In_        LPDIRECT3DDEVICE9   pD3DDevice,
  _Out_       LPD3DXMESH          *ppMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NumFaces* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de faces para a malha. O intervalo válido para esse número é maior que 0 e um menor que o DWORD (normalmente 65534), pois o último índice é reservado.

</dd> <dt>

*NumVertices* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices para a malha. Esse parâmetro deve ser maior que 0.

</dd> <dt>

*Opções* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) , especificando as opções para a malha.

</dd> <dt>

*pDeclaration* \[ no\]
</dt> <dd>

Tipo: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que descreve o formato de vértice para a malha retornada. Esse parâmetro deve ser mapeado diretamente para um formato de vértice flexível (FVF).

</dd> <dt>

*pD3DDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo a ser associado à malha.

</dd> <dt>

*ppMesh* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa o objeto de malha criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
