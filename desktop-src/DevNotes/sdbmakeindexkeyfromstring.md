---
description: Cria uma chave a partir de uma cadeia de caracteres.
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
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920100"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>Função SdbMakeIndexKeyFromString

Cria uma chave a partir de uma cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszKey* \[ no\]
</dt> <dd>

A cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retornará a chave ou 0 se houver um erro.

## <a name="remarks"></a>Comentários

A chave de índice padrão são os oito primeiros caracteres da cadeia de caracteres, convertidos em letras maiúsculas e, em seguida, convertidos em um valor de **ULONGLONG** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




