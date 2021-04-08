---
description: Lê os dados binários. Preterido.
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: 'Método IDirectXFileBinary:: Read (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 60548640fbbb0e67909eab1fed2df24a3465bf95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012144"
---
# <a name="idirectxfilebinaryread-method"></a>Método IDirectXFileBinary:: Read

Lê os dados binários. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pvData* \[ fora\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para o buffer que recebe os dados que foram lidos.

</dd> <dt>

*cbSize* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Tamanho do buffer apontado por pvData, em bytes.

</dd> <dt>

*pcbRead* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Ponteiro para o número de bytes realmente lidos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
