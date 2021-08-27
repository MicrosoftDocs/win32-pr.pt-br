---
description: 'Saiba mais sobre: função JetDelete'
title: Função JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e5d8fe6cfc4e0521866a12383aa34f7858432d3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477602"
---
# <a name="jetdelete-function"></a>Função JetDelete


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdelete-function"></a>Função JetDelete

A função **JetDelete** exclui o registro atual em uma tabela de banco de dados.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão de banco de dados que será usado para a chamada à API.

*TableID*

O cursor em uma tabela de banco de dados. A linha atual será excluída.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errCallbackFailed</p> | <p>A função de retorno de chamada falhou de alguma maneira. Por exemplo, violações de acesso em funções de retorno de chamada são capturadas e convertidas em JET_errCallbackFailed. esse erro só será retornado pelo Windows XP e posterior.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIllegalOperation</p> | <p>O cursor especificado por <em>TableName</em> não oferece suporte à exclusão. Consulte a seção Comentários.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor especificado por <em>TableName</em> não está em um registro.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errPermissionDenied</p> | <p>O mecanismo de banco de dados não tem permissões suficientes para excluir o registro. Isso pode acontecer se o arquivo de banco de dados foi aberto com acesso somente leitura.</p> | 
| <p>JET_errRollbackError</p> | <p>Um buffer de atualização (consulte <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) existe, mas nem todas as alterações feitas em colunas do tipo JET_coltypLongText e/ou colunas do tipo JET_coltypLongBinary podem ser revertidas.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>É ilegal usar a mesma sessão de mais de um thread ao mesmo tempo. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 
| <p>JET_errTransReadOnly</p> | <p>A transação é uma transação somente leitura e não oferece suporte a exclusões.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>A operação falhou porque não há memória suficiente para reter informações transacionais sobre a atualização.</p> | 
| <p>JET_errWriteConflict</p> | <p>Outra sessão bloqueou anteriormente o registro para atualização. A atualização tentada por esta sessão falhará.</p> | 



Em caso de sucesso, a moeda é deixada logo antes do próximo registro. Se o registro excluído foi o último na tabela, a moeda é deixada no final da tabela (ou seja, após o novo último registro). Se o registro excluído for o único registro na tabela, a moeda será definida como o início.

Os índices apropriados são atualizados automaticamente.

Se uma atualização estiver preparada (usando [JetPrepareUpdate](./jetprepareupdate-function.md)), ela será cancelada. O buffer de atualização será redefinido.

Em caso de falha, a moeda permanece inalterada. Se uma atualização estiver preparada (consulte [JetPrepareUpdate](./jetprepareupdate-function.md)), o buffer de atualização poderá ser redefinido.

#### <a name="remarks"></a>Comentários

Nem todas as tabelas dão suporte à exclusão de linhas. Normalmente, uma tabela temporária não dá suporte à exclusão de linhas. A exclusão de registros pode ser habilitada em tabelas temporárias por vários motivos, algumas das quais são:

  - JET_bitTTUpdatable foi especificado durante a criação.

  - Tabelas temporárias grandes podem dar suporte à exclusão se elas foram criadas com JET_bitTTScrollable ou JET_bitTTIndexed. O limite no qual uma tabela temporária se torna "grande" atualmente é de 64 quilobytes, mas pode ser alterado em versões futuras.

Windows XP e posterior. As funções de retorno de chamada podem ser invocadas por **JetDelete**, incluindo JET_cbtypBeforeDelete e JET_cbtypAfterDelete.

É importante entender o impacto da execução de um grande número de operações de atualização dentro de uma única transação. Cada atualização do banco de dados deve ser controlada pelo mecanismo de banco de dados no repositório de versão. O repositório de versão mantém um registro ao vivo de todas as diferentes versões de cada registro ou entrada de índice no banco de dados que pode ser visto por todas as transações ativas. Essas versões são usadas para dar suporte ao controle de simultaneidade de várias versões em uso pelo mecanismo de banco de dados para dar suporte a transações usando o isolamento de instantâneo. Depois que o mecanismo de banco de dados tiver esgotado os recursos usados para armazenar essas versões, ele não poderá mais aceitar outras alterações até que algumas transações tenham sido concluídas para permitir que esses recursos sejam recuperados. Quando o mecanismo estiver nesse estado, todas as atualizações falharão com JET_errVersionStoreOutOfMemory. Os recursos disponíveis para o mecanismo de banco de dados para armazenar essas versões podem ser controlados usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com *JET_paramMaxVerPages* e *JET_paramGlobalMinVerPages*.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
