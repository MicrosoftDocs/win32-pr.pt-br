---
description: Abre o banco de dados shim especificado.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: Função SdbOpenDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: df0081d7373bf67d3df1723be7d5beb272ef7ee4c77c54da8a6985dfe250d7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161189"
---
# <a name="sdbopendatabase-function"></a>Função SdbOpenDatabase

Abre o banco de dados shim especificado.

## <a name="syntax"></a>Sintaxe


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszPath* \[ Em\]
</dt> <dd>

O caminho do banco de dados. Esse parâmetro não pode ser **NULL.**

</dd> <dt>

*eType* \[ Em\]
</dt> <dd>

O tipo de caminho. Consulte [**PATH \_ TYPE**](path-type.md) para ver uma lista de valores.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna um alça para o banco de dados shim.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> </dl>

 

 




