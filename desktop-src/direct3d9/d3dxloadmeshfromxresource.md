---
description: Carrega uma malha de um recurso.
ms.assetid: 3cf253dc-4f3f-4949-ab24-8225667f95f2
title: Função D3DXLoadMeshFromXResource (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3e1d9d14d86296df48e2d27f77e2f79f3ad73c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663999"
---
# <a name="d3dxloadmeshfromxresource-function"></a>Função D3DXLoadMeshFromXResource

Carrega uma malha de um recurso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXLoadMeshFromXResource(
  _In_  HMODULE           Module,
  _In_  LPCSTR            Name,
  _In_  LPCSTR            Type,
  _In_  DWORD             Options,
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

*Módulo* \[ do no\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Manipule para o módulo em que o recurso está localizado, ou **NULL** para o módulo associado à imagem que o sistema operacional usou para criar o processo atual. Consulte Observações.

</dd> <dt>

*Nome* \[ do no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o recurso do qual criar a malha. Consulte Observações.

</dd> <dt>

*Tipo* \[ de no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o tipo de recurso. Consulte Observações.

</dd> <dt>

*Opções* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) que especificam as opções de criação para a malha.

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

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) para saber mais sobre os parâmetros de módulo, nome e tipo.

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

 

 
