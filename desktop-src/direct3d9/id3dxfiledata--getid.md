---
description: Recupera o GUID deste objeto de dados de arquivo.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: 'Método ID3DXFileData:: GetId (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1dafb296541b1702e9163dcc6d460cf149b4007
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664038"
---
# <a name="id3dxfiledatagetid-method"></a>Método ID3DXFileData:: GetId

Recupera o GUID deste objeto de dados de arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pid* \[ fora\]
</dt> <dd>

Tipo: **LPGUID**

Ponteiro para um GUID para receber a ID deste objeto de dados de arquivo. Se o objeto de dados do arquivo não tiver nenhuma ID, o valor do parâmetro retornado será GUID \_ NULL.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 




