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
ms.openlocfilehash: 7a288e3e1a625106c72f57125eea8a4219555f86
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988479"
---
# <a name="jetopentable-function"></a>Função JetOpenTable


_**Aplica-se a:** Windows | Windows Servidor_

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


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableDenyRead</p> | <p>A tabela não pode ser aberta para acesso de leitura por outra sessão de banco de dados.</p> | 
| <p>JET_bitTableDenyWrite</p> | <p>A tabela não pode ser aberta para acesso de gravação por outra sessão de banco de dados.</p> | 
| <p>JET_bitTableNoCache</p> | <p>Não armazene em cache as páginas desta tabela.</p> | 
| <p>JET_bitTablePermitDDL</p> | <p>Permite a modificação de DDL em tabelas sinalizadas como FixedDDL. Essa opção deve ser usada com a opção JET_bitTableDenyRead.</p> | 
| <p>JET_bitTablePreread</p> | <p>Fornece uma dica de que a tabela provavelmente não está no cache do buffer e que a leitura prévia pode ser benéfica para o desempenho.</p> | 
| <p>JET_bitTableReadOnly</p> | <p>Solicita acesso somente leitura à tabela.</p> | 
| <p>JET_bitTableSequential</p> | <p>A tabela deve ser probuscada de forma muito agressiva no disco porque o aplicativo irá examiná-lo em sequência.</p> | 
| <p>JET_bitTableUpdatable</p> | <p>Solicita o acesso de gravação à tabela.</p> | 



*ptableid*

Em caso de sucesso, aponta para o identificador da tabela. Em caso de falha, o conteúdo de *pTableID* é indefinido.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p><em>DBID</em> não é um identificador de banco de dados válido.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Uma combinação inadequada de <em>grbit</em> foi passada.</p> | 
| <p>JET_errInvalidName</p> | <p>O nome fornecido em <em>szTableName</em> é inválido.</p><p>Para obter mais informações sobre nomes de tabela válidos, consulte o parâmetro <em>szTableName</em> em <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Foi feita uma tentativa de abrir uma tabela que não existe no banco de dados.</p> | 
| <p>JET_errOutOfCursors</p> | <p>A operação falhou porque o mecanismo não pode alocar os recursos necessários para abrir um novo cursor. Consulte a seção Comentários.</p> | 
| <p>JET_errTableInUse</p> | <p>A tabela está sendo usada por outra operação de banco de dados.</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>Um aviso não fatal que indica que a tabela está sendo usada pelo sistema.</p> | 
| <p>JET_errTableLocked</p> | <p>A tabela está bloqueada por outra operação de banco de dados.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Foi feita uma tentativa de abrir muitas tabelas exclusivas ao mesmo tempo. Consulte a seção Comentários.</p> | 



#### <a name="remarks"></a>Comentários

As tabelas abertas com **JetOpenTable** normalmente devem ser fechadas com [JetCloseTable](./jetclosetable-function.md). A exceção a essa regra ocorre quando **JetOpenTable** é chamado em uma transação e a transação é revertida (com [JetRollback](./jetrollback-function.md)). Ao reverter uma transação, a tabela é fechada automaticamente. Nesse caso, é um erro fechar a tabela com [JetCloseTable](./jetclosetable-function.md).

É legal abrir tabelas do sistema com **JetOpenTable** (por exemplo, MSysObjects, MSysUnicodeFixup). O esquema das tabelas do sistema pode ser alterado, portanto, o acesso a tabelas do sistema não é recomendado. O número de tabelas exclusivas que podem ser abertas simultaneamente é afetado diretamente pelo *JET_paramMaxOpenTables*. Se a tabela estiver aberta no momento, um novo cursor será criado na tabela. Os recursos de cursor são configurados usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com *JET_paramMaxCursors*. Consulte também [JetDupCursor](./jetdupcursor-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetOpenTableW</strong> (Unicode) e <strong>JetOpenTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros de recurso](./resource-parameters.md)
