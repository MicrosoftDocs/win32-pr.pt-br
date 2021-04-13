---
description: Cancela o registro do banco de dados especificado, tornando-o não mais disponível.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: Função SdbUnregisterDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456974"
---
# <a name="sdbunregisterdatabase-function"></a>Função SdbUnregisterDatabase

Cancela o registro do banco de dados especificado, tornando-o não mais disponível.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pguidDB* \[ no\]
</dt> <dd>

O GUID do banco de dados. Este parâmetro não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




