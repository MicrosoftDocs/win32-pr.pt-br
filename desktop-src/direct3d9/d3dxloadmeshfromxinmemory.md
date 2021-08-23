---
description: Carrega uma malha da memória.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: Função D3DXLoadMeshFromXInMemory (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19427da28b90fe4410a65f0321b5dcd486b4c917d209f1f20762d05899b4eb0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044944"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a>Função D3DXLoadMeshFromXInMemory

Carrega uma malha da memória.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Memória* \[ do no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o buffer de memória que contém os dados de malha.

</dd> <dt>

*SizeOfMemory* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Tamanho do arquivo na memória, em bytes.

</dd> <dt>

*Opções* \[ do fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) , especificando as opções de criação para a malha.

</dd> <dt>

*pD3DDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo associado à malha.

</dd> <dt>

*ppAdjacency* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) . Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.

</dd> <dt>

*ppMaterials* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) . Quando esse método retorna, esse parâmetro é preenchido com uma matriz de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) , contendo informações salvas no arquivo do DirectX.

</dd> <dt>

*ppEffectInstances* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ponteiro para um buffer que contém uma matriz de instâncias de efeito, um por grupo de atributos na malha retornada. Uma instância de efeito é uma instância específica de informações de estado usada para inicializar um efeito. Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pNumMaterials* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Aponta para o número de estruturas [**D3DXMATERIAL**](d3dxmaterial.md) na matriz *ppMaterials* , quando o método retorna.

</dd> <dt>

*ppMesh* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha carregada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Todas as malhas no arquivo serão recolhidas em uma malha de saída. Se o arquivo contiver uma hierarquia de quadros, todas as transformações serão aplicadas à malha.

Para arquivos de malha que não contêm informações de instância de efeito, as instâncias de efeito padrão serão geradas a partir das informações de material no arquivo. x. Uma instância de efeito padrão terá valores padrão que correspondem aos membros da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) .

O nome de textura padrão também é preenchido, mas é tratado de forma diferente. O nome será Texture0@Name , que corresponde a uma variável de efeito pelo nome de "Texture0" com uma anotação chamada "Name". Isso conterá o nome do arquivo de cadeia de caracteres para a textura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
