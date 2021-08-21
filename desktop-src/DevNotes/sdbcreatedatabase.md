---
description: Cria um novo banco de dados shim.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: Função SdbCreateDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6c7ac5d30c9c5a0154d770266410d278c5c3f31a65166515078a5384b1b8b55d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161547"
---
# <a name="sdbcreatedatabase-function"></a>Função SdbCreateDatabase

Cria um novo banco de dados shim.

## <a name="syntax"></a>Sintaxe


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszPath* \[ Em\]
</dt> <dd>

O caminho em que o banco de dados deve ser salvo. Esse parâmetro não pode ser **NULL.**

</dd> <dt>

*eType* \[ Em\]
</dt> <dd>

O tipo de caminho. Consulte [**PATH \_ TYPE**](path-type.md) para ver uma lista de valores.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna um alça para o banco de dados shim ou **NULL** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




