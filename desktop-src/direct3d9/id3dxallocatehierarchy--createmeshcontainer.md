---
description: Solicita a alocação de um objeto de contêiner de malha.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'Método ID3DXAllocateHierarchy:: CreateMeshContainer (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781238"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a>Método ID3DXAllocateHierarchy:: CreateMeshContainer

Solicita a alocação de um objeto de contêiner de malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ do no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome da malha.

</dd> <dt>

*pMeshData* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMESHDATA**](d3dxmeshdata.md) \***

Ponteiro para a estrutura de dados de malha. Consulte [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

*pMaterials* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***

Matriz de materiais usada na malha.

</dd> <dt>

*pEffectInstances* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Matriz de instâncias de efeito usadas na malha. Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*NumMaterials* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de materiais na matriz de materiais.

</dd> <dt>

*pAdjacency* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Matriz de adjacência para a malha.

</dd> <dt>

*pSkinInfo* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

Ponteiro para o objeto de malha de capa se forem encontrados dados de capa. Consulte [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

*ppNewMeshContainer* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***

Retorna o contêiner de malha criado. Consulte [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK. Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de D3DERR ou D3DXERR, pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
