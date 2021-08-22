---
description: o método OpenView do objeto Database retorna um objeto View que representa a consulta especificada por uma cadeia de caracteres SQL.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Método Database. OpenView (Certview. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ccc37b72dd44064172672d1067dae293da30048853f3ca83f82fb50b0a90cfaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947519"
---
# <a name="databaseopenview-method"></a>Método Database. OpenView

o método **OpenView** do objeto [**Database**](database-object.md) retorna um objeto [**View**](view-object.md) que representa a consulta especificada por uma cadeia de caracteres SQL.

## <a name="syntax"></a>Sintaxe


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sql* 
</dt> <dd>

SQL cadeia de caracteres de consulta necessária.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

para obter informações sobre a sintaxe de SQL implementada no instalador, consulte [SQL sintaxe](sql-syntax.md).

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| Cabeçalho<br/>  | <dl> <dt>Certview. h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Banco de dados**](database-object.md)
</dt> <dt>

[SQL Sintaxe](sql-syntax.md)
</dt> </dl>

 

 




