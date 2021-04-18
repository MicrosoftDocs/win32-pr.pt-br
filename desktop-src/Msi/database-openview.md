---
description: O método OpenView do objeto Database retorna um objeto View que representa a consulta especificada por uma cadeia de caracteres SQL.
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
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752857"
---
# <a name="databaseopenview-method"></a>Método Database. OpenView

O método **OpenView** do objeto [**Database**](database-object.md) retorna um objeto [**View**](view-object.md) que representa a consulta especificada por uma cadeia de caracteres SQL.

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

Cadeia de caracteres de consulta SQL necessária.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para obter informações sobre a sintaxe SQL implementada no instalador, consulte [sintaxe SQL](sql-syntax.md).

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| parâmetro<br/>  | <dl> <dt>Certview. h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Backup de banco de dados**](database-object.md)
</dt> <dt>

[Sintaxe SQL](sql-syntax.md)
</dt> </dl>

 

 




