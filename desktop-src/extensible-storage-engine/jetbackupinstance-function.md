---
description: 'Saiba mais sobre: função JetBackupInstance'
title: Função JetBackupInstance
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089884"
---
# <a name="jetbackupinstance-function"></a>Função JetBackupInstance


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetbackupinstance-function"></a>Função JetBackupInstance

A função **JetBackupInstance** executa um backup de streaming de uma instância, incluindo todos os bancos de dados anexados, em um diretório. Com vários métodos de backup com suporte no mecanismo, essa é a função mais simples e encapsulada.

**Windows XP: o JetBackupInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância do banco de dados para backup.

*szBackupPath*

O diretório em que o backup está armazenado. Se o caminho de backup for nulo para usar a função, o truncará os logs, se possível.

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
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Cria um backup completo do banco de dados. Isso permite a preservação de um backup existente no mesmo diretório se o novo backup falhar.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Cria um backup incremental em oposição a um backup completo. Isso significa que somente os arquivos de log criados desde o último backup completo ou incremental serão submetidos a backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Reservado para uso futuro.</p></td>
</tr>
</tbody>
</table>


*pfnStatus*

Aponta para a função de retorno de chamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , que fornece informações de notificação sobre o progresso da operação de backup.

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
<td><p>Um backup já está em andamento para a mesma instância. Não são permitidos vários backups ao mesmo tempo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>A instância ainda não está pronta para backup durante a inicialização.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>A operação não pode ser concluída porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>Um backup incremental não será permitido se o log circular estiver ativado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>As opções especificadas são inválidas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um parâmetro inválido foi passado para a API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>O caminho de destino não existe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>A instância está sendo executada sem registro em log. Nenhum backup é permitido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Erro de verificação de checksum em um arquivo de log.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogWriteFail</p></td>
<td><p>O log da instância é temporário ou permanentemente desabilitado devido a um erro inesperado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Ocorreu um erro de verificação de checksum em uma página de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Depois que a função retornar êxito, no diretório de backup, todos os arquivos necessários para uma restauração até o momento do backup estarão presentes. Se esse for um backup completo, os arquivos serão os arquivos de banco de dados e os arquivos de log necessários para colocar o banco de dados em um estado consistente. Se esse for um backup incremental, somente os arquivos de log serão adicionados aos diretórios, mas os arquivos já existentes (bancos de dados e arquivos de log) junto com os novos arquivos de log poderão ser restaurados e trazer o banco de dados de volta para o estado no momento do backup.

Como um efeito colateral do backup, os arquivos de log que não são mais necessários serão truncados.

Ao mesmo tempo, os cabeçalhos de banco de dados serão atualizados com as informações quando o último backup tiver ocorrido.

Em caso de falha, não haverá nenhum arquivo no destino do diretório de backup, portanto, nenhuma restauração será possível. Ao mesmo tempo, os arquivos de log atuais não serão truncados.

#### <a name="remarks"></a>Comentários

As diferentes etapas do backup terão entradas de log de eventos geradas, incluindo os nomes de arquivo, o truncamento de log e o resultado final do backup.

O backup incremental só é possível depois que um backup completo foi feito. Além disso, os backups incrementais só serão possíveis se o log circular estiver desativado. É recomendável que o diretório de backup não contenha outros arquivos, o que está envolvido no backup ou adicionado por um backup bem-sucedido anterior.

O diretório de backup deve existir, a menos que o parâmetro *JET_paramCreatePathIfNotExist* esteja definido para a instância. Para obter informações, consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md).

O backup fará a verificação de checksum em todas as páginas de banco de dados usadas e a partir do Windows Server 2003, nos arquivos de log também. Isso dá a oportunidade de estimar a integridade do banco de dados mesmo para páginas que não são lidas durante operações normais. Se qualquer dano for encontrado, o backup falhará.

Durante o backup, o arquivo de log atual será concluído e começaremos uma nova geração de log. Isso permitirá copiar os arquivos de log necessários porque o último necessário não estará mais em uso.

É altamente recomendável que o backup não seja usado para outros fins, o backup e restaurado no nível do mecanismo. Isso minimizará a alteração da obtenção de erros durante as operações de backup e restauração.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetBackupInstanceW</strong> (Unicode) e <strong>JetBackupInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
