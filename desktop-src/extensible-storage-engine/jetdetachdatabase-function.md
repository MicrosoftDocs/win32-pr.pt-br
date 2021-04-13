---
description: 'Saiba mais sobre: função JetDetachDatabase'
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
ms.openlocfilehash: 2e4437955acc0ed5714f7fbfb9f42fd4abafa58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297634"
---
# <a name="jetdetachdatabase-function"></a>Função JetDetachDatabase


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetdetachdatabase-function"></a>Função JetDetachDatabase

A função **JetDetachDatabase** libera um arquivo de banco de dados que foi anexado anteriormente a uma sessão de banco de dados.

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser desanexado. Se *szFilename* for **nulo** ou uma cadeia de caracteres vazia, todos os bancos de dados anexados a *sesid* serão desanexados.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress</p></td>
<td><p>O backup do banco de dados está sendo feito e não pode ser desanexado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>O banco de dados foi aberto pelo <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>. Os bancos de dados devem ser fechados antes da desanexação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> ou <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Foi feita uma tentativa de desanexar um banco de dados enquanto estava em uma transação.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Se um banco de dados anexado foi aberto (com [JetAttachDatabase](./jetattachdatabase-function.md)), ele deve ser fechado com [JetCloseDatabase](./jetclosedatabase-function.md) antes de desanexar.

Somente Windows 2000: os bancos de dados que não foram desanexados antes de chamar [JetTerm](./jetterm-function.md) serão automaticamente reanexados quando [JetInit](./jetinit-function.md) for próximo chamado.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetDetachDatabaseW</strong> (Unicode) e <strong>JetDetachDatabaseA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
