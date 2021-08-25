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
ms.openlocfilehash: 2ea0cfeedbf74bea02af60b8c01d04b9e0e02f527ba35c0478da801253687b8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815304"
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

## <a name="return-value"></a>Valor retornado

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




