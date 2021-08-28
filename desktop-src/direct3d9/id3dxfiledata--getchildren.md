---
description: Recupera o número de filhos neste objeto de dados de arquivo.
ms.assetid: ebc6905b-a453-4a15-adae-956ce7034084
title: 'Método ID3DXFileData:: GetChildren (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: dca2197a321efea6cf86ee0f38b1778935e5f4cb336b55b5d662e49a4465162a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493836"
---
# <a name="id3dxfiledatagetchildren-method"></a>Método ID3DXFileData:: GetChildren

Recupera o número de filhos neste objeto de dados de arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*puiChildren* \[ no\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***

Endereço de um ponteiro para receber o número de filhos neste objeto de dados de arquivo.

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

 

 
