---
description: Registra o banco de dados especificado.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: Função SdbRegisterDatabaseEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500873"
---
# <a name="sdbregisterdatabaseex-function"></a>Função SdbRegisterDatabaseEx

Registra o banco de dados especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszDatabasePath* \[ no\]
</dt> <dd>

O caminho do banco de dados. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*dwDatabaseType* \[ no\]
</dt> <dd>

O tipo de banco de dados. Consulte [Shim de tipos de banco de dados](shim-database-types.md) para obter uma lista de valores.

</dd> <dt>

*pTimeStamp* \[ em, opcional\]
</dt> <dd>

O carimbo de data/hora do banco de dados. Se esse parâmetro for **NULL**, a hora do sistema será usada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="remarks"></a>Comentários

Um banco de dados deve ser registrado antes que você possa usar outras funções SDB.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




