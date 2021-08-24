---
description: Carregar dados de nível superior de um arquivo. x.
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'Método ID3DXLoadUserData:: LoadTopLevelData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ba0ed668657fb0195da7a54bad14d996c06c8fba8f81306491e7be4ce0d97b01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629486"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a>Método ID3DXLoadUserData:: LoadTopLevelData

Carregar dados de nível superior de um arquivo. x.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pXofChildData* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Ponteiro para uma estrutura de dados de arquivo. x. Isso é definido em Dxfile. h.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK. Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de D3DERR ou D3DXERR, pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




