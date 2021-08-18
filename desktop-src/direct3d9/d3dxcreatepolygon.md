---
description: Usa um sistema de coordenadas à esquerda para criar uma malha que contém um polígono de n lados.
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: Função D3DXCreatePolygon (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePolygon
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf3694bb247fb95e654452c8db3887fcebc2832ac28ec0b2ac920b28f285e22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045144"
---
# <a name="d3dxcreatepolygon-function"></a>Função D3DXCreatePolygon

Usa um sistema de coordenadas à esquerda para criar uma malha que contém um polígono de n lados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreatePolygon(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Length,
  _In_  UINT              Sides,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa o dispositivo associado à malha de polígono criada.

</dd> <dt>

*Comprimento* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Comprimento de cada lado.

</dd> <dt>

*Lados* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de lados para o polígono. O valor deve ser maior ou igual a 3.

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

O polígono criado é centralizado na origem.

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

 

 
