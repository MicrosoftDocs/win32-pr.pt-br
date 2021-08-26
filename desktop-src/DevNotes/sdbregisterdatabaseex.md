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
ms.openlocfilehash: 512e180549c246a5504bc14675d61082c68904aa767d98deca5111d9a275dc60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984096"
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

## <a name="return-value"></a>Valor retornado

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="remarks"></a>Comentários

Um banco de dados deve ser registrado antes que você possa usar outras funções SDB.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




