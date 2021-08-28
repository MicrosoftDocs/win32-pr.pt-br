---
title: MB_GetString função (User.h)
description: Retorna cadeias de caracteres para botões de caixa de mensagem padrão.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- MB_GetString caixa de diálogo da função
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
ms.openlocfilehash: 9bdd984a2f65ab8c2eed8a77fffa56af1d94633c828196428a674c9eee78c3ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985356"
---
# <a name="mb_getstring-function"></a>Função \_ GetString do MB

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

A ID da cadeia de caracteres a ser retornada. Eles são identificados pelos valores de ID de comando da caixa de diálogo listados em winuser.h.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A cadeia de caracteres ou NULL se não for encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>User.h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>User32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>User32.dll</dt> </dl> |



 

 





