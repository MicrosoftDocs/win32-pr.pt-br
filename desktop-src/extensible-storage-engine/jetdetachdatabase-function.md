---
description: 'Saiba mais sobre: Função JetDetachDatabase'
title: Função JetDetachDatabase
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 028e156cffd5eef0d4baa1f043dddf5105fd1023
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985869"
---
# <a name="jetdetachdatabase-function"></a>Função JetDetachDatabase


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdetachdatabase-function"></a>Função JetDetachDatabase

A **função JetDetachDatabase** libera um arquivo de banco de dados anexado anteriormente a uma sessão de banco de dados.

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser desconectado. Se *szFilename for* **NULL ou uma** cadeia de caracteres vazia, todos os bancos de dados anexados *ao sesid* serão desanudos.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupInProgress</p> | <p>O banco de dados está sendo feito backup e não pode ser desvinculado.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>O banco de dados foi aberto pelo <a href="gg269299(v=exchg.10).md">JetOpenDatabase.</a> Os bancos de dados devem ser fechados antes de desconectar.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> ou <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de desconectar um banco de dados em uma transação.</p> | 



#### <a name="remarks"></a>Comentários

Se um banco de dados anexado tiver sido aberto (com [JetAttachDatabase),](./jetattachdatabase-function.md)ele deverá ser fechado com [JetCloseDatabase](./jetclosedatabase-function.md) antes de desconectar.

Windows 2000: os bancos de dados que não foram desacopladas antes de chamar [JetTerm](./jetterm-function.md) serão anexados automaticamente quando [JetInit](./jetinit-function.md) for chamado pela próxima vez.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetDetachDatabaseW</strong> (Unicode) e <strong>JetDetachDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetTerm](./jetterm-function.md)
