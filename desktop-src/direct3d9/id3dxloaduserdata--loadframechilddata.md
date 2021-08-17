---
description: Carregar dados filho de quadro de um arquivo .x.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: Método ID3DXLoadUserData::LoadFrameChildData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3dcb9fa8218804b0d6fdb5532dd54bc2b2b4a3921ea4462692a36e671efb404d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802176"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a>Método ID3DXLoadUserData::LoadFrameChildData

Carregar dados filho de quadro de um arquivo .x.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFrame* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Ponteiro para um contêiner de malha. Consulte [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pXofChildData* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Ponteiro para uma estrutura de dados de arquivo .x. Isso é definido em Dxfile.h.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, programe o método para retornar D3D \_ OK. Caso contrário, programe o método para retornar uma mensagem de erro apropriada de D3DERR ou D3DXERR, pois isso fará com que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




