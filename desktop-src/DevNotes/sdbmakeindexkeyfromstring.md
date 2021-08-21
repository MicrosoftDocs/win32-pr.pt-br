---
description: Cria uma chave de uma cadeia de caracteres.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: Função SdbMakeIndexKeyFromString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3298b0e038218aecb9676c596e7dbad09acbbdd4441d0f1cd79c3ec2a0188720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161219"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>Função SdbMakeIndexKeyFromString

Cria uma chave de uma cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszKey* \[ Em\]
</dt> <dd>

A cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retornará a chave ou 0 se houver um erro.

## <a name="remarks"></a>Comentários

A chave de índice padrão é os oito primeiros caracteres da cadeia de caracteres, convertidos em letras maiúsculas e, em seguida, convertidos em **um valor ULONGLONG.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




