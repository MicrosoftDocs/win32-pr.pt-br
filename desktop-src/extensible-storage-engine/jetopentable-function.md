---
description: 'Saiba mais sobre: função JetOpenTable'
title: Função JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646701"
---
# <a name="jetopentable-function"></a>Função JetOpenTable


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetopentable-function"></a>Função JetOpenTable

A função **JetOpenTable** abre um cursor em uma tabela criada anteriormente.

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado.

*DBID*

O identificador de banco de dados a ser usado para localizar a tabela.

*szTableName*

O nome da tabela a ser aberta.

*pvParameters*

Preterido. Defina como **nulo**.

*cbParameters*

Preterido. Defina como 0 (zero).

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitTableDenyRead</p></td>
<td><p>A tabela não pode ser aberta para acesso de leitura por outra sessão de banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableDenyWrite</p></td>
<td><p>A tabela não pode ser aberta para acesso de gravação por outra sessão de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableNoCache</p></td>
<td><p>Não armazene em cache as páginas desta tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTablePermitDDL</p></td>
<td><p>Permite a modificação de DDL em tabelas sinalizadas como FixedDDL. Essa opção deve ser usada com a opção JET_bitTableDenyRead.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTablePreread</p></td>
<td><p>Fornece uma dica de que a tabela provavelmente não está no cache do buffer e que a leitura prévia pode ser benéfica para o desempenho.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableReadOnly</p></td>
<td><p>Solicita acesso somente leitura à tabela.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableSequential</p></td>
<td><p>A tabela deve ser probuscada de forma muito agressiva no disco porque o aplicativo irá examiná-lo em sequência.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableUpdatable</p></td>
<td><p>Solicita o acesso de gravação à tabela.</p></td>
</tr>
</tbody>
</table>


*ptableid*

Em caso de sucesso, aponta para o identificador da tabela. Em caso de falha, o conteúdo de *pTableID* é indefinido.

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
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p><em>DBID</em> não é um identificador de banco de dados válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Uma combinação inadequada de <em>grbit</em> foi passada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>O nome fornecido em <em>szTableName</em> é inválido.</p>
<p>Para obter mais informações sobre nomes de tabela válidos, consulte o parâmetro <em>szTableName</em> em <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Foi feita uma tentativa de abrir uma tabela que não existe no banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para abrir um novo cursor. Consulte a seção Comentários.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableInUse</p></td>
<td><p>A tabela está sendo usada por outra operação de banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>Um aviso não fatal que indica que a tabela está sendo usada pelo sistema.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>A tabela está bloqueada por outra operação de banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Foi feita uma tentativa de abrir muitas tabelas exclusivas ao mesmo tempo. Consulte a seção Comentários.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

As tabelas abertas com **JetOpenTable** normalmente devem ser fechadas com [JetCloseTable](./jetclosetable-function.md). A exceção a essa regra ocorre quando **JetOpenTable** é chamado em uma transação e a transação é revertida (com [JetRollback](./jetrollback-function.md)). Ao reverter uma transação, a tabela é fechada automaticamente. Nesse caso, é um erro fechar a tabela com [JetCloseTable](./jetclosetable-function.md).

É legal abrir tabelas do sistema com **JetOpenTable** (por exemplo, MSysObjects, MSysUnicodeFixup). O esquema das tabelas do sistema pode ser alterado, portanto, o acesso a tabelas do sistema não é recomendado. O número de tabelas exclusivas que podem ser abertas simultaneamente é afetado diretamente pelo *JET_paramMaxOpenTables*. Se a tabela estiver aberta no momento, um novo cursor será criado na tabela. Os recursos de cursor são configurados usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com *JET_paramMaxCursors*. Consulte também [JetDupCursor](./jetdupcursor-function.md).

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
<td><p>Implementado como <strong>JetOpenTableW</strong> (Unicode) e <strong>JetOpenTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros do recurso](./resource-parameters.md)
