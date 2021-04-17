---
title: Função MB_GetString (User. h)
description: Retorna cadeias de caracteres para botões de caixa de mensagem padrão.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- Caixas de diálogo MB_GetString função
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813321"
---
# <a name="mb_getstring-function"></a>\_Função GetString de MB

Retorna cadeias de caracteres para botões de caixa de mensagem padrão.

## <a name="syntax"></a>Sintaxe


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wBtn* 
</dt> <dd>

A ID da cadeia de caracteres a ser retornada. Eles são identificados pelos valores de ID de comando da caixa de diálogo listados em winuser. h.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A cadeia de caracteres ou NULL se não for encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>User. h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>User32. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>User32.dll</dt> </dl> |



 

 





