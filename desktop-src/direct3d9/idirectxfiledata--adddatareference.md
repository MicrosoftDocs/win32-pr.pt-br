---
description: Cria e adiciona um objeto de referência de dados como um objeto filho. Preterido.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'Método IDirectXFileData:: AddDataReference (DXFile. h)'
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
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765314"
---
# <a name="idirectxfiledataadddatareference-method"></a>Método IDirectXFileData:: AddDataReference

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

*szRef* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do objeto de dados referenciado. Esse parâmetro poderá ser **nulo** se pguidRef fornecer uma referência para o GUID.

</dd> <dt>

*pguidRef* \[ no\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Ponteiro para o GUID que representa os dados. Esse parâmetro poderá ser **nulo** se szRef fornecer uma referência ao nome.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos valores a seguir. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Comentários

Para que esse método tenha sucesso, o parâmetro szRef ou pguidRef deve ser não **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 
