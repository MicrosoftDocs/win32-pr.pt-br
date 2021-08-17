---
description: Um retorno de chamada para o usuário registrar um modelo de arquivo. x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'Método ID3DXSaveUserData:: RegisterTemplates (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a41a43f8f319ee09f24c4f62092e4718773dc312cb7886b0fc7c95781e614c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628726"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a>Método ID3DXSaveUserData:: RegisterTemplates

Um retorno de chamada para o usuário registrar um modelo de arquivo. x.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pXFileApi* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXFILE**](id3dxfile.md)**

Use esse ponteiro para registrar modelos de arquivo. x definidos pelo usuário. Consulte [**ID3DXFile**](id3dxfile.md). Não use esse parâmetro para adicionar objetos de dados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK. Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md), pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.

## <a name="remarks"></a>Comentários

**ID3DXSaveUserData:: RegisterTemplates** e [**ID3DXSaveUserData:: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) fornecem um mecanismo para adicionar um modelo a um arquivo. x para salvar dados do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
