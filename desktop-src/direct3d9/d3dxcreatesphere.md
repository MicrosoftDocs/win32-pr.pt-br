---
description: Usa um sistema de coordenadas à esquerda para criar uma malha que contém uma esfera.
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: Função D3DXCreateSphere (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56ac6b8e8cc2195e2176e505cf430ea33b6b6ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173012"
---
# <a name="d3dxcreatesphere-function"></a>Função D3DXCreateSphere

Usa um sistema de coordenadas à esquerda para criar uma malha que contém uma esfera.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateSphere(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à malha de sphere criada.

</dd> <dt>

*RADIUS* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Raio da esfera. Esse valor deve ser maior ou igual a 0,0 f.

</dd> <dt>

*Fatias* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de fatias sobre o eixo principal.

</dd> <dt>

*Pilhas* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de pilhas ao longo do eixo principal.

</dd> <dt>

*ppMesh* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para a forma de saída, uma interface [**ID3DXMesh**](id3dxmesh.md) .

</dd> <dt>

*ppAdjacency* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) . Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha. **NULL** pode ser especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A esfera criada é centralizada na origem e seu eixo é alinhado com o eixo z.

Essa função cria uma malha com a \_ opção de criação gerenciada D3DXMESH e [D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) formato de vértice flexível normal (FVF).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9shape. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de desenho de forma](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
