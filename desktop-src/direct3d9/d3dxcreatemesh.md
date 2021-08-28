---
description: Função D3DXCreateMesh – cria um objeto de malha usando um declarator.
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: Função D3DXCreateMesh (D3DX9Mesh.h)
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
ms.openlocfilehash: 8a1e9ed35325390f3315cd269d89284fd3426a9f1cbad4c1c025be06dd33204f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676256"
---
# <a name="d3dxcreatemesh-function"></a>Função D3DXCreateMesh

Cria um objeto de malha usando um declarator.

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

*NumFaces* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de faces para a malha. O intervalo válido para esse número é maior que 0 e um menor que o DWORD máximo (normalmente 65534), porque o último índice é reservado.

</dd> <dt>

*NumVertices* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices para a malha. Esse parâmetro deve ser maior que 0.

</dd> <dt>

*Opções* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH,**](./d3dxmesh.md) especificando opções para a malha.

</dd> <dt>

*pDeclaration* \[ Em\]
</dt> <dd>

Tipo: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matriz de [**elementos D3DVERTEXELEMENT9,**](d3dvertexelement9.md) descrevendo o formato de vértice para a malha retornada. Esse parâmetro deve mapear diretamente para um FVF (formato de vértice flexível).

</dd> <dt>

*pD3DDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) o objeto do dispositivo a ser associado à malha.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXMesh,**](id3dxmesh.md) que representa o objeto de malha criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
