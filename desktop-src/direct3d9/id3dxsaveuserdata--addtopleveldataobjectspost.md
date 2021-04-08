---
description: Adicione um objeto de nível superior após a hierarquia de quadros.
ms.assetid: 43b3cdb3-c6f0-4028-bf86-43d643fba73d
title: 'Método ID3DXSaveUserData:: AddTopLevelDataObjectsPost (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPost
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3573bae8cbcb6858b04207f936545b7cf93959c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012170"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspost-method"></a>Método ID3DXSaveUserData:: AddTopLevelDataObjectsPost

Adicione um objeto de nível superior após a hierarquia de quadros.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddTopLevelDataObjectsPost(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pXofSave* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Ponteiro para um arquivo. x salvar objeto. Use este ponteiro para chamar [**IDirectXFileSaveObject:: Createdataobject**](idirectxfilesaveobject--createdataobject.md) para criar o objeto de dados a ser salvo. Em seguida, chame [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md) para salvar os dados.

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

 

 
