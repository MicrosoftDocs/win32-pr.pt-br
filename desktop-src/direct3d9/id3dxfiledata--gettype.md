---
description: Recupera a ID do modelo neste objeto de dados de arquivo.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'Método ID3DXFileData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e386c27638ced2be41197bf5f0095a481365dd19bc39b69d5d13d1ac8ec8dc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748526"
---
# <a name="id3dxfiledatagettype-method"></a>Método ID3DXFileData:: GetType

Recupera a ID do modelo neste objeto de dados de arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pType* \[ no\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Ponteiro para o GUID que representa o modelo neste objeto de dados de arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




