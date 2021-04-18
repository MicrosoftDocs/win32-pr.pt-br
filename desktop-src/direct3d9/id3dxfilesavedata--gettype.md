---
description: Recupera a ID do modelo deste nó de dados do arquivo.
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: 'Método ID3DXFileSaveData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b774f71b4be111efcdbdaf8bc41b40d4b0efaa95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781197"
---
# <a name="id3dxfilesavedatagettype-method"></a>Método ID3DXFileSaveData:: GetType

Recupera a ID do modelo deste nó de dados do arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* \[ de no\]
</dt> <dd>

Tipo: **[ **GUID**](guid.md)\***

Ponteiro para o GUID que representa o modelo neste nó de dados de arquivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




