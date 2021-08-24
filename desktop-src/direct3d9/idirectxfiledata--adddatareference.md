---
description: Cria e adiciona um objeto de referência de dados como um objeto filho. Preterido.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: Método IDirectXFileData::AddDataReference (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 4c291e4f5754975f7e564c8c579b3651b29f0e6b684ad474f2f8436875dbf078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747256"
---
# <a name="idirectxfiledataadddatareference-method"></a>Método IDirectXFileData::AddDataReference

Cria e adiciona um objeto de referência de dados como um objeto filho. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szRef* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do objeto de dados referenciado. Esse parâmetro poderá ser **NULL** se pguidRef fornece uma referência ao GUID.

</dd> <dt>

*pguidRef* \[ Em\]
</dt> <dd>

Tipo: **const [**GUID**](guid.md) \***

Ponteiro para o GUID que representa os dados. Esse parâmetro poderá ser **NULL** se szRef fornece uma referência ao nome.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Comentários

Para que esse método seja bem-sucedido, o parâmetro szRef ou pguidRef deve ser não **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 
