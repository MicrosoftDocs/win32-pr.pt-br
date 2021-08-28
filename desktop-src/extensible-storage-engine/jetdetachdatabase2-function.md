---
description: 'Saiba mais sobre: Função JetDetachDatabase2'
title: Função JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4f29253f3b320abb662f7a4334a14c1c49ed546
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984879"
---
# <a name="jetdetachdatabase2-function"></a>Função JetDetachDatabase2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdetachdatabase2-function"></a>Função JetDetachDatabase2

A **função JetDetachDatabase2** libera um arquivo de banco de dados anexado anteriormente a uma sessão de banco de dados.

**Windows XP:****JetDetachDatabase2** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser desconectado. Se *szFilename for* **NULL ou uma** cadeia de caracteres vazia, todos os bancos de dados anexados *ao sesid* serão desanudos.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitForceCloseAndDetach</p> | <p>Força o banco de dados a ser fechado e desvinculado. Se JET_bitForceCloseAndDetach não tiver suporte, JET_errForceDetachNotAllowed será retornado.</p> | 
| <p>JET_bitForceDetach</p> | <p>Força o banco de dados a ser desvinculado. Se JET_bitForceDetach não tiver suporte, JET_errForceDetachNotAllowed será retornado.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupInProgress</p> | <p>O banco de dados está sendo feito backup e não pode ser desvinculado.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>O banco de dados foi aberto pelo <a href="gg269299(v=exchg.10).md">JetOpenDatabase.</a> Os bancos de dados devem ser fechados antes de desconectar.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> ou <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p> | 
| <p>JET_errForceDetachNotAllowed</p> | <p>JET_bitForceDetach não é suportado.</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de desconectar um banco de dados em uma transação.</p> | 



#### <a name="remarks"></a>Comentários

Se um banco de dados anexado tiver sido aberto (com [JetAttachDatabase),](./jetattachdatabase-function.md)ele deverá ser fechado com [JetCloseDatabase](./jetclosedatabase-function.md) antes de desconectar.

Windows 2000: os bancos de dados que não foram desacopladas antes de chamar [JetTerm](./jetterm-function.md) serão anexados automaticamente quando [JetInit](./jetinit-function.md) for chamado pela próxima vez.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetDetachDatabase2W</strong> (Unicode) e <strong>JetDetachDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetInit](./jetinit-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetTerm](./jetterm-function.md)
