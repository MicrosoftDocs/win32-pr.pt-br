---
description: 'Saiba mais sobre: função JetUpdate2'
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
ms.openlocfilehash: 34cc43aea463c186d68c0fa0cadc447ba2a02acb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983239"
---
# <a name="jetupdate2-function"></a>Função JetUpdate2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetupdate2-function"></a>Função JetUpdate2

A função **JetUpdate2** executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente. Essa função contém uma lista de opções de *grbit* que podem ser definidas durante a execução de uma atualização. A exclusão de uma linha de tabela é executada chamando [JetDelete](./jetdelete-function.md).

**Windows server 2003: JetUpdate2** é introduzido no Windows server 2003.

**JetUpdate2** é a etapa final na execução de uma inserção ou atualização. A atualização é iniciada chamando [JetPrepareUpdate](./jetprepareupdate-function.md) e, em seguida, chamando [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) uma ou mais vezes para definir o estado do registro. Por fim, **JetUpdate2** é chamado para concluir a operação de atualização. Os índices são atualizados somente por [JetUpdate](./jetupdate-function.md) ou **JetUpdate2**, e não durante [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md).

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

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pvBookmark*

Ponteiro para um indicador retornado para uma linha inserida.

*cbBookmark*

Tamanho do buffer apontado por *pvBookmark*.

*pcbActual*

O tamanho retornado do indicador para a linha inserida retornada em *pvBookmark*.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitUpdateCheckESE97Compatibility</p> | <p>esse sinalizador faz com que a atualização retorne um erro se a atualização não fosse possível na versão Windows 2000 do ese, o que impõe um número máximo menor de instâncias de coluna com vários valores em cada registro do que as versões posteriores do ESE. isso é importante apenas para aplicativos que desejam replicar dados entre aplicativos hospedados no Windows 2000 e aplicativos hospedados no Windows Server 2003 ou versões posteriores do ESE. Não deve ser necessário para a maioria dos aplicativos.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>O buffer fornecido para o indicador de registro não é suficientemente grande o suficiente para armazenar o indicador de registro.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
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
| <p>JET_errUpdateNotPrepared</p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> foi chamado com JET_prepCancel, mas o cursor não estava no estado preparado.</p> | 
| <p>JET_errWriteConflict</p> | <p>Uma operação de substituição de registro para a qual um bloqueio de gravação ainda não foi alocado pode encontrar um conflito de gravação no momento da atualização.</p> | 



Em caso de sucesso, a operação abrir atualização no cursor é concluída. Se uma coluna de incremento automático for definida para a tabela, esse valor será definido para registros inseridos. Se uma coluna de versão for definida para a tabela, seu valor será inicializado para registros recentemente inseridos ou incrementado cada vez que um registro for substituído. Todos os índices, incluindo índices clusterizados e não clusterizados, são atualizados.

Em caso de falha, nenhuma alteração de qualquer tipo é feita no banco de dados. Antes de INSERT e before, as funções REPLACE de retorno de chamada podem ter sido chamadas, mas após INSERT e After Replace não serão chamadas, já que o último não pode fazer com que uma atualização falhe. O buffer de cópia do cursor é deixado em seu estado preparado, para que a oportunidade exista para corrigir incrementalmente os problemas que causaram erros e repita a operação de atualização.

#### <a name="remarks"></a>Comentários

As limitações de tamanho de registro são impostas por [JetSetColumn](./jetsetcolumn-function.md)e não em geral por [JetUpdate](./jetupdate-function.md). A única exceção é quando o sinalizador de compatibilidade JET_bitUpdateCheckESE97Compatibility está sendo usado. Nesse caso, o registro inteiro é verificado, pois uma operação [JetSetColumn](./jetsetcolumn-function.md) individual que excedeu o limite pode ser compensada por uma chamada subsequente para [JetSetColumn](./jetsetcolumn-function.md).

Consulte a seção comentários em [JetUpdate](./jetupdate-function.md) para obter mais informações.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | 
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
