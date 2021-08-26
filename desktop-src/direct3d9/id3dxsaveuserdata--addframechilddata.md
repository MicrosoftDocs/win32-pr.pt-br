---
description: Adicione dados filho ao quadro.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: Método ID3DXSaveUserData::AddFrameChildData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b0b593010ec9ff8a56833c48b9667dfd0084f99283fc4bf29c9008e9e31ac98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095716"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a>Método ID3DXSaveUserData::AddFrameChildData

Adicione dados filho ao quadro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFrame* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Ponteiro para um contêiner de malha. Consulte [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pXofSave* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Ponteiro para um objeto save de arquivo .x. Use o ponteiro para chamar [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) para adicionar um objeto de dados filho. Não salve os dados com [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pXofFrameData* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Ponteiro para um nó de dados de arquivo .x. Use o ponteiro para chamar [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) para adicionar um objeto de dados filho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, programe o método para retornar D3D \_ OK. Caso contrário, programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR,**](./d3dxerr.md)pois isso fará com que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.

## <a name="remarks"></a>Comentários

[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) e [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) fornecem um mecanismo para adicionar um modelo a um arquivo .x para salvar dados do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
