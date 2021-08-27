---
description: Usa um sistema de coordenadas à esquerda para criar uma malha que contém uma esfera.
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: Função D3DXCreateSphere (D3dx9shape.h)
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
ms.openlocfilehash: 4c1cea000071f0d097f29138b4e5f2db554f2214d8ca6343c16a39740d82c29e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119346"
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

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o dispositivo associado à malha de esfera criada.

</dd> <dt>

*Raio* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Raio da esfera. Esse valor deve ser maior ou igual a 0,0f.

</dd> <dt>

*Fatias* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de fatias sobre o eixo principal.

</dd> <dt>

*Pilhas* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de pilhas ao longo do eixo principal.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para a forma de saída, uma interface [**ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma [**interface ID3DXBuffer.**](id3dxbuffer.md) Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada rosto na malha. **NULL** pode ser especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A esfera criada é centralizada na origem e seu eixo é alinhado com o eixo z.

Essa função cria uma malha com a opção de criação GERENCIADA D3DXMESH e o formato de vértice flexível \_ [ \_ \| D3DFVF XYZ D3DFVF \_ NORMAL](d3dfvf.md) (FVF).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de desenho de forma](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
