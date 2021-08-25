---
description: Recupera o tamanho dos dados binários. Preterido.
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: Método IDirectXFileBinary::GetSize (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1af59f6a32d163275df02d1469ba4777bf5c5152535c2df52fcf7d7c40218e2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846936"
---
# <a name="idirectxfilebinarygetsize-method"></a>Método IDirectXFileBinary::GetSize

Recupera o tamanho dos dados binários. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcbSize* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para o tamanho retornado dos dados binários, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
