---
description: Carrega uma malha de capa de um objeto de dados de arquivo .x directX.
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: Função D3DXLoadSkinMeshFromXof (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28805e56e4c7600b37ce68ac586148de59fe668704726ea0a71c4721a2699a09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564686"
---
# <a name="d3dxloadskinmeshfromxof-function"></a>Função D3DXLoadSkinMeshFromXof

Carrega uma malha de capa de um objeto de dados de arquivo .x directX.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pxofMesh* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Ponteiro para uma interface [**ID3DXFileData,**](id3dxfiledata.md) que representa o objeto de dados do arquivo a ser carregado.

</dd> <dt>

*Opções* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores, da enumeração [**D3DXMESH,**](./d3dxmesh.md) especificando opções de criação para a malha.

</dd> <dt>

*pD3DDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) o objeto de dispositivo associado à malha.

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma [**interface ID3DXBuffer.**](id3dxbuffer.md) Quando esse método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada rosto na malha.

</dd> <dt>

*ppMaterials* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma [**interface ID3DXBuffer.**](id3dxbuffer.md) Quando o método retorna, esse parâmetro é preenchido com uma matriz de [**estruturas D3DXMATERIAL.**](d3dxmaterial.md)

</dd> <dt>

*ppEffectInstances* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ponteiro para um buffer que contém uma matriz de instâncias de efeito, uma por grupo de atributos na malha retornada. Uma instância de efeito é uma instância específica de informações de estado usadas para inicializar um efeito. Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pMatOut* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para o número de [**estruturas D3DXMATERIAL**](d3dxmaterial.md) na *matriz ppMaterials,* quando o método retorna.

</dd> <dt>

*ppSkinInfo* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Endereço de um ponteiro para uma interface [**ID3DXSkinInfo,**](id3dxskininfo.md) que representa as informações de replicação.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXMesh,**](id3dxmesh.md) que representa a malha carregada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY

## <a name="remarks"></a>Comentários

Esse método leva um ponteiro para um objeto interno no arquivo .x, permitindo que você carregue a hierarquia de quadros.

Para arquivos de malha que não contêm informações de instância de efeito, as instâncias de efeito padrão serão geradas com as informações de material no arquivo .x. Uma instância de efeito padrão terá valores padrão que correspondem aos membros da [**estrutura D3DMATERIAL9.**](d3dmaterial9.md)

O nome da textura padrão também é preenchido, mas é tratado de maneira diferente. O nome será , que corresponde a uma variável de efeito pelo nome de "Texture0" com uma anotação Texture0@Name chamada "Name". Isso conterá o nome do arquivo de cadeia de caracteres para a textura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
