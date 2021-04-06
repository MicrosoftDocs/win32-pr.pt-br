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
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646893"
---
# <a name="jetupdate2-function"></a>Função JetUpdate2


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetupdate2-function"></a>Função JetUpdate2

A função **JetUpdate2** executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente. Essa função contém uma lista de opções de *grbit* que podem ser definidas durante a execução de uma atualização. A exclusão de uma linha de tabela é executada chamando [JetDelete](./jetdelete-function.md).

**Windows server 2003: o JetUpdate2** é introduzido no windows Server 2003.

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
<td><p>JET_bitUpdateCheckESE97Compatibility</p></td>
<td><p>Esse sinalizador faz com que a atualização retorne um erro se a atualização não fosse possível na versão 2000 do Windows do ESE, que impõe um número menor máximo de instâncias de coluna com vários valores em cada registro do que as versões posteriores do ESE. Isso é importante apenas para aplicativos que desejam replicar dados entre aplicativos hospedados no Windows 2000 e aplicativos hospedados no Windows Server 2003 ou versões posteriores do ESE. Não deve ser necessário para a maioria dos aplicativos.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>O buffer fornecido para o indicador de registro não é suficientemente grande o suficiente para armazenar o indicador de registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>A operação de atualização requer o crescimento do arquivo de banco de dados ou a alocação do arquivo de log, mas a unidade de disco em que reside o arquivo de banco de dados ou a série de logs está cheia. Como alternativa, o arquivo de banco de dados está em um volume formatado em FAT32 e o arquivo de banco de dados já está 4GBytes, o limite por arquivo para FAT32.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>O parâmetro <em>Prep</em> fornecido na função <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> não é um sinalizador válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate</p></td>
<td><p>Uma chave de índice para este registro é uma duplicata de outra chave de índice para outro registro que já está na tabela e o índice não permite duplicatas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated</p></td>
<td><p>O registro inserido ou atualizado tem um ou mais índices para os quais a chave gerada teria excedido o tamanho máximo permitido. Como resultado, a operação falhou ao impedir o truncamento de chave.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation</p></td>
<td><p>O registro inserido ou atualizado tem uma coluna de vários valores indexada com dois ou mais valores que são idênticos no tamanho de chave de comprimento máximo definido para o índice. Como resultado, o registro tem duas entradas idênticas no índice que são inválidas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Uma ou mais colunas no registro a serem inseridas ou no estado atualizado de um registro que está sendo substituído são <strong>nulas</strong> , o que viola a restrição definida para essas colunas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed</p></td>
<td><p>Um ou mais índices estão definidos para não permitir uma chave <strong>nula</strong> e o estado inserido ou atualizado de um registro que está sendo substituído viola essa restrição definida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordPrimaryChanged</p></td>
<td><p>Uma operação de substituição de registro atualizou a chave primária. As atualizações nas colunas de chave primária devem ser feitas por meio da exclusão do registro existente e da inserção de um novo registro com os dados desejados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> foi chamado com JET_prepCancel, mas o cursor não estava no estado preparado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflict</p></td>
<td><p>Uma operação de substituição de registro para a qual um bloqueio de gravação ainda não foi alocado pode encontrar um conflito de gravação no momento da atualização.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, a operação abrir atualização no cursor é concluída. Se uma coluna de incremento automático for definida para a tabela, esse valor será definido para registros inseridos. Se uma coluna de versão for definida para a tabela, seu valor será inicializado para registros recentemente inseridos ou incrementado cada vez que um registro for substituído. Todos os índices, incluindo índices clusterizados e não clusterizados, são atualizados.

Em caso de falha, nenhuma alteração de qualquer tipo é feita no banco de dados. Antes de INSERT e before, as funções REPLACE de retorno de chamada podem ter sido chamadas, mas após INSERT e After Replace não serão chamadas, já que o último não pode fazer com que uma atualização falhe. O buffer de cópia do cursor é deixado em seu estado preparado, para que a oportunidade exista para corrigir incrementalmente os problemas que causaram erros e repita a operação de atualização.

#### <a name="remarks"></a>Comentários

As limitações de tamanho de registro são impostas por [JetSetColumn](./jetsetcolumn-function.md)e não em geral por [JetUpdate](./jetupdate-function.md). A única exceção é quando o sinalizador de compatibilidade JET_bitUpdateCheckESE97Compatibility está sendo usado. Nesse caso, o registro inteiro é verificado, pois uma operação [JetSetColumn](./jetsetcolumn-function.md) individual que excedeu o limite pode ser compensada por uma chamada subsequente para [JetSetColumn](./jetsetcolumn-function.md).

Consulte a seção comentários em [JetUpdate](./jetupdate-function.md) para obter mais informações.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
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
</tbody>
</table>


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
