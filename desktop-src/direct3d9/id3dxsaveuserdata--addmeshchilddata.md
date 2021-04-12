---
description: Adicione dados filho à malha.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'Método ID3DXSaveUserData:: AddMeshChildData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8a9d6b69e64e0e1eca5d4350125e0955254b6127
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173173"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a>Método ID3DXSaveUserData:: AddMeshChildData

Adicione dados filho à malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMeshContainer* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***

Ponteiro para um contêiner de malha. Consulte [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

</dd> <dt>

*pXofSave* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Ponteiro para um arquivo. x salvar objeto. Use o ponteiro para chamar [**ID3DXFileSaveObject:: Adddataobject**](id3dxfilesaveobject--adddataobject.md) para adicionar um objeto de dados filho. Não salve os dados com [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pXofMeshData* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Ponteiro para um nó de dados de arquivo. x. Use o ponteiro para chamar [**ID3DXFileSaveData:: Adddataobject**](id3dxfilesavedata--adddataobject.md) para adicionar um objeto de dados filho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK. Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
