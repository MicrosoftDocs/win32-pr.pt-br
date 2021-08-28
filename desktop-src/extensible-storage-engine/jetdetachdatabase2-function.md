---
description: 'Saiba mais sobre: função JetDetachDatabase2'
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
ms.openlocfilehash: 9141646c96d9318667cd11b41aade03363cab230
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474112"
---
# <a name="jetdetachdatabase2-function"></a>Função JetDetachDatabase2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdetachdatabase2-function"></a>Função JetDetachDatabase2

A função **JetDetachDatabase2** libera um arquivo de banco de dados que foi anexado anteriormente a uma sessão de banco de dados.

**Windows xp:** o **JetDetachDatabase2** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser desanexado. Se *szFilename* for **nulo** ou uma cadeia de caracteres vazia, todos os bancos de dados anexados a *sesid* serão desanexados.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitForceCloseAndDetach</p> | <p>Força o banco de dados a ser fechado e desanexado. Se não houver suporte para JET_bitForceCloseAndDetach, JET_errForceDetachNotAllowed será retornado.</p> | 
| <p>JET_bitForceDetach</p> | <p>Força o banco de dados a ser desanexado. Se não houver suporte para JET_bitForceDetach, JET_errForceDetachNotAllowed será retornado.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupInProgress</p> | <p>O backup do banco de dados está sendo feito e não pode ser desanexado.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>O banco de dados foi aberto pelo <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>. Os bancos de dados devem ser fechados antes da desanexação.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> ou <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p> | 
| <p>JET_errForceDetachNotAllowed</p> | <p>Não há suporte para JET_bitForceDetach.</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de desanexar um banco de dados enquanto estava em uma transação.</p> | 



#### <a name="remarks"></a>Comentários

Se um banco de dados anexado foi aberto (com [JetAttachDatabase](./jetattachdatabase-function.md)), ele deve ser fechado com [JetCloseDatabase](./jetclosedatabase-function.md) antes de desanexar.

somente Windows 2000: os bancos de dados que não foram desanexados antes de chamar [JetTerm](./jetterm-function.md) serão automaticamente reanexados quando [JetInit](./jetinit-function.md) for próximo chamado.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetDetachDatabase2W</strong> (Unicode) e <strong>JetDetachDatabase2A</strong> (ANSI).</p> | 



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
