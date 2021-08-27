---
description: 'Saiba mais sobre: Função JetUpdate2'
title: Função JetUpdate2
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f85633a16077c3957bebb1e236f5bbca6180778a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479562"
---
# <a name="jetupdate2-function"></a>Função JetUpdate2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetupdate2-function"></a>Função JetUpdate2

A **função JetUpdate2** executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente. Essa função contém uma lista de *opções de grbit* que podem ser definidas durante a execução de uma atualização. A exclusão de uma linha de tabela é executada chamando [JetDelete](./jetdelete-function.md).

**Windows Server 2003: JetUpdate2** é introduzido no Windows Server 2003.

**JetUpdate2** é a etapa final na execução de uma inserção ou atualização. A atualização é iniciada chamando [JetPrepareUpdate](./jetprepareupdate-function.md) e, em seguida, chamando [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) uma ou mais vezes para definir o estado do registro. Por fim, **JetUpdate2** é chamado para concluir a operação de atualização. Os índices são atualizados apenas por [JetUpdate](./jetupdate-function.md) ou **JetUpdate2** e não durante [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns.](./jetsetcolumns-function.md)

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*pvBookmark*

Ponteiro para um indicador retornado para uma linha inserida.

*cbBookmark*

Tamanho do buffer apontado por *pvBookmark.*

*pcbActual*

O tamanho retornado do indicador para a linha inserida retornada em *pvBookmark*.

*grbit*

Um grupo de bits que contém as opções a serem usadas para essa chamada, que incluem zero ou mais dos seguintes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitUpdateCheckESE97Compatibility</p> | <p>Esse sinalizador faz com que a atualização retorne um erro se a atualização não tivesse sido possível na versão do Windows 2000 do ESE, o que impou um número máximo menor de instâncias de colunas com valores múltiplos em cada registro do que as versões posteriores do ESE. Isso é importante apenas para aplicativos que desejam replicar dados entre aplicativos hospedados no Windows 2000 e aplicativos hospedados no Windows Server 2003 ou versões posteriores do ESE. Não deve ser necessário para a maioria dos aplicativos.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>O buffer determinado para o indicador de registro não é suficientemente grande o suficiente para armazenar o indicador de registro.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errDiskFull</p> | <p>A operação de atualização requer o crescimento do arquivo de banco de dados ou a alocação de arquivo de log, mas a unidade de disco em que reside o arquivo de banco de dados ou a série de log está cheia. Como alternativa, o arquivo de banco de dados está em um volume formatado fat32 e o arquivo de banco de dados já é 4GBytes, o limite por arquivo para FAT32.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>O parâmetro <em>de preparação</em> determinado na <a href="gg269339(v=exchg.10).md">função JetPrepareUpdate</a> não é um sinalizador válido.</p> | 
| <p>JET_errKeyDuplicate</p> | <p>Uma chave de índice para esse registro é uma duplicata de outra chave de índice para outro registro já na tabela e o índice não permite duplicatas.</p> | 
| <p>JET_errKeyTruncated</p> | <p>O registro inserido ou atualizado tem um ou mais índices para os quais a chave gerada excederia o tamanho máximo permitida. Como resultado, a operação falhou ao impedir o truncamento de chaves.</p> | 
| <p>JET_errMultiValuedIndexViolation</p> | <p>O registro inserido ou atualizado tem uma coluna de vários valores indexada com dois ou mais valores idênticos dentro do tamanho máximo de chave definido para o índice. Como resultado, o registro tem duas entradas idênticas no índice, o que é inválido.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errNullInvalid</p> | <p>Uma ou mais colunas no registro a ser inserido ou no estado atualizado de um registro que está sendo substituído é <strong>NULL,</strong> o que viola a restrição definida para essas colunas.</p> | 
| <p>JET_errNullKeyDisallowed</p> | <p>Um ou mais índices são definidos para não permitir uma chave <strong>NULL</strong> e o estado inserido ou atualizado de um registro que está sendo substituído viola essa restrição definida.</p> | 
| <p>JET_errRecordPrimaryChanged</p> | <p>Uma operação de substituição de registro atualizou a chave primária. As atualizações nas colunas de chave primária devem ser feitas por meio da exclusão do registro existente e da inserção de um novo registro com os dados desejados.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> foi chamado com JET_prepCancel mas o cursor não estava no estado preparado.</p> | 
| <p>JET_errWriteConflict</p> | <p>Uma operação de substituição de registro para a qual um bloqueio de gravação ainda não foi alocado pode encontrar um conflito de gravação no momento da atualização.</p> | 



Em caso de êxito, a operação de atualização aberta no cursor é concluída. Se uma coluna de incremento automático for definida para a tabela, esse valor será definido para registros inseridos. Se uma coluna de versão for definida para a tabela, seu valor será inicializado para registros recém-inseridos ou incrementado sempre que um registro for substituído. Todos os índices, incluindo índices clusterados e não clusterados, são atualizados.

Em caso de falha, nenhuma alteração de qualquer tipo é feita no banco de dados. Antes de inserir e antes de substituir, as funções de retorno de chamada podem ter sido chamadas, mas depois de inserir e depois de substituir os retornos de chamada não terão sido chamados, pois o último não pode causar falha em uma atualização. O buffer de cópia do cursor é deixado em seu estado preparado, para que exista a oportunidade de corrigir incrementalmente os problemas que causaram erros e repetir a operação de atualização.

#### <a name="remarks"></a>Comentários

As limitações de tamanho do registro são impostas por [JetSetColumn](./jetsetcolumn-function.md)e não em geral por [JetUpdate.](./jetupdate-function.md) A única exceção é quando o JET_bitUpdateCheckESE97Compatibility de compatibilidade está sendo usado. Nesse caso, todo o registro é verificado, pois uma operação [JetSetColumn](./jetsetcolumn-function.md) individual que excedeu o limite pode ser compensada por uma chamada subsequente para [JetSetColumn](./jetsetcolumn-function.md).

Consulte a seção Comentários em [JetUpdate para](./jetupdate-function.md) obter mais informações.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



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
