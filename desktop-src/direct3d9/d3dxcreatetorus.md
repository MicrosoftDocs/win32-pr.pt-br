---
description: Usa um sistema de coordenadas à esquerda para criar uma malha que contém um Torus.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: Função D3DXCreateTorus (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1671641a5088535777cb78bf3773f4c1e56e1c3d35e70d345a39df2dad7bd83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526188"
---
# <a name="d3dxcreatetorus-function"></a>Função D3DXCreateTorus

Usa um sistema de coordenadas à esquerda para criar uma malha que contém um Torus.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à malha Torus criada.

</dd> <dt>

*InnerRadius* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Interno-raio do Torus. O valor deve ser maior ou igual a 0,0 f.

</dd> <dt>

*OuterRadius* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Externo-RADIUS do Torus. O valor deve ser maior ou igual a 0,0 f.

</dd> <dt>

*Lados* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de lados em uma seção cruzada. O valor deve ser maior ou igual a 3.

</dd> <dt>

*Anéis* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de anéis que compõem o Torus. O valor deve ser maior ou igual a 3.

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

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

O Torus criado é centralizado na origem e seu eixo é alinhado com o eixo z. O raio interno do Torus é o raio da seção cruzada (o raio secundário) e o raio externo do Torus é o raio do buraco central.

Essa função retorna uma malha que pode ser usada posteriormente para desenhar ou manipular pelo aplicativo.

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

 

 
