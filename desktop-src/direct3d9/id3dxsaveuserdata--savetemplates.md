---
description: Um retorno de chamada para o usuário salvar um modelo de arquivo. x.
ms.assetid: c2e29495-5eeb-42b8-826e-1a60c1c6bda2
title: 'Método ID3DXSaveUserData:: SaveTemplates (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.SaveTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00695f11f267c77838bc2d9a3d2932df108c7323f3751b385c009abe2b21f540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293099"
---
# <a name="id3dxsaveuserdatasavetemplates-method"></a>Método ID3DXSaveUserData:: SaveTemplates

Um retorno de chamada para o usuário salvar um modelo de arquivo. x.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SaveTemplates(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pXofSave* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Ponteiro para um arquivo. x salvar objeto. Não use esse parâmetro para adicionar objetos de dados. Consulte [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK. Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.

## <a name="remarks"></a>Comentários

[**ID3DXSaveUserData:: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) e **ID3DXSaveUserData:: SaveTemplates** fornecem um mecanismo para adicionar um modelo a um arquivo. x para salvar dados do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
