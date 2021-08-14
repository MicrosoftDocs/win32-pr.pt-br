---
description: Adicione um objeto de nível superior antes da hierarquia de quadros.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: Método ID3DXSaveUserData::AddTopLevelDataObjectsPre (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52052a24c34c99260a68cd5cdeaa7487e6b71c086ac30922a06de241de8319ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801153"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a>Método ID3DXSaveUserData::AddTopLevelDataObjectsPre

Adicione um objeto de nível superior antes da hierarquia de quadros.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddTopLevelDataObjectsPre(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pXofSave* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Ponteiro para um objeto save de arquivo .x. Use esse ponteiro para chamar [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para criar o objeto de dados a ser salvo. Em [**seguida, chame IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) para salvar os dados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, programe o método para retornar D3D \_ OK. Caso contrário, programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR,**](./d3dxerr.md)pois isso fará com que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
