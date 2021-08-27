---
description: 'Saiba mais sobre: função JetUpdate'
title: Função JetUpdate
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b66c80f506942e2815c8b8795c32250c827527b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982339"
---
# <a name="jetupdate-function"></a>Função JetUpdate


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetupdate-function"></a>Função JetUpdate

A função **JetUpdate** executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente. A exclusão de uma linha de tabela é executada chamando [JetDelete](./jetdelete-function.md).

**JetUpdate** é a etapa final na execução de uma inserção ou atualização. A atualização é iniciada chamando [JetPrepareUpdate](./jetprepareupdate-function.md) e, em seguida, chamando [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) uma ou mais vezes para definir o estado do registro. Por fim, **JetUpdate** é chamado para concluir a operação de atualização. Os índices são atualizados somente por **JetUpdate** ou [JetUpdate2](./jetupdate2-function.md), e não durante [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md).

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pvBookmark*

Ponteiro para um indicador retornado para uma linha inserida.

*cbBookmark*

Tamanho do buffer apontado por *pvBookmark*.

*pcbActual*

O tamanho retornado do indicador para a linha inserida retornada em *pvBookmark*.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>O buffer fornecido para o indicador de registro não é suficientemente grande o suficiente para armazenar o indicador de registro.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>O mesmo que JET_errNullInvalid.</p> | 
| <p>JET_errDiskFull</p> | <p>A operação de atualização requer o crescimento do arquivo de banco de dados ou a alocação do arquivo de log, mas a unidade de disco em que reside o arquivo de banco de dados ou a série de logs está cheia. Como alternativa, o arquivo de banco de dados está em um volume formatado em FAT32 e o arquivo de banco de dados já está 4GBytes, o limite por arquivo para FAT32.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>O parâmetro <em>Prep</em> fornecido na função <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> não é um sinalizador válido.</p> | 
| <p>JET_errKeyDuplicate</p> | <p>Uma chave de índice para este registro é uma duplicata de outra chave de índice para outro registro que já está na tabela e o índice não permite duplicatas.</p> | 
| <p>JET_errKeyTruncated</p> | <p>O registro inserido ou atualizado tem um ou mais índices para os quais a chave gerada teria excedido o tamanho máximo permitido. Como resultado, a operação falhou ao impedir o truncamento de chave.</p> | 
| <p>JET_errMultiValuedIndexViolation</p> | <p>O registro inserido ou atualizado tem uma coluna de vários valores indexada com dois ou mais valores que são idênticos no tamanho de chave de comprimento máximo definido para o índice. Como resultado, o registro tem duas entradas idênticas no índice que são inválidas.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errNullInvalid</p> | <p>Uma ou mais colunas no registro a serem inseridas ou no estado atualizado de um registro que está sendo substituído são <strong>nulas</strong> , o que viola a restrição definida para essas colunas.</p> | 
| <p>JET_errNullKeyDisallowed</p> | <p>Um ou mais índices estão definidos para não permitir uma chave <strong>nula</strong> e o estado inserido ou atualizado de um registro que está sendo substituído viola essa restrição definida.</p> | 
| <p>JET_errRecordPrimaryChanged</p> | <p>Uma operação de substituição de registro atualizou a chave primária. As atualizações nas colunas de chave primária devem ser feitas por meio da exclusão do registro existente e da inserção de um novo registro com os dados desejados.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 
| <p>JET_errTransReadOnly</p> | <p>É ilegal tentar uma atualização quando dentro do escopo de uma transação somente leitura. Uma transação somente leitura é uma transação que foi iniciada usando uma chamada para <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> com JET_bitTransactionReadOnly.</p><p><strong>Windows XP:</strong>  esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> foi chamado com JET_prepCancel, mas o cursor não estava no estado preparado.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>A operação falhou porque não há memória suficiente para reter informações transacionais sobre a atualização.</p> | 
| <p>JET_errWriteConflict</p> | <p>Outra sessão bloqueou anteriormente o registro para atualização. A atualização tentada por esta sessão falhará.</p> | 



Em caso de sucesso, a operação abrir atualização no cursor é concluída. Se uma coluna de incremento automático for definida para a tabela, esse valor será definido para registros inseridos. Se uma coluna de versão for definida para a tabela, seu valor será inicializado para registros recentemente inseridos ou incrementado cada vez que um registro for substituído. Todos os índices, incluindo índices clusterizados e não clusterizados, são atualizados.

Em caso de falha, nenhuma alteração de qualquer tipo é feita no banco de dados. Antes de INSERT e before, as funções REPLACE de retorno de chamada podem ter sido chamadas, mas após INSERT e After Replace não serão chamadas, já que o último não pode fazer com que uma atualização falhe. O buffer de cópia do cursor é deixado em seu estado preparado, para que a oportunidade exista para corrigir incrementalmente os problemas que causaram erros e repita a operação de atualização.

#### <a name="remarks"></a>Comentários

As funções de retorno de chamada podem ser registradas para serem chamadas antes ou depois da inserção, e antes ou após a atualização.

As limitações de tamanho de registro são impostas por [JetSetColumn](./jetsetcolumn-function.md)e não em geral por **JetUpdate**.

É importante entender o impacto da execução de um grande número de operações de atualização dentro de uma única transação. Cada atualização do banco de dados deve ser controlada pelo mecanismo de banco de dados no repositório de versão. O repositório de versão mantém um registro ao vivo de todas as diferentes versões de cada registro ou entrada de índice no banco de dados que pode ser visto por todas as transações ativas. Essas versões são usadas para dar suporte ao controle de simultaneidade de várias versões em uso pelo mecanismo de banco de dados para dar suporte a transações usando o isolamento de instantâneo. Depois que o mecanismo de banco de dados tiver esgotado os recursos usados para armazenar essas versões, ele não poderá mais aceitar outras alterações até que algumas transações tenham sido concluídas para permitir que esses recursos sejam recuperados. Quando o mecanismo estiver nesse estado, todas as atualizações falharão com JET_errVersionStoreOutOfMemory. Os recursos disponíveis para o mecanismo de banco de dados para armazenar essas versões podem ser controlados usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com [JET_paramMaxVerPages](./resource-parameters.md) e [JET_paramGlobalMinVerPages](./resource-parameters.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDelete](./jetdelete-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
