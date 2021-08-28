---
description: 'Saiba mais sobre: Função JetBackupInstance'
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
ms.openlocfilehash: 0a32b07ddcbe36a2a986a669592d3e047fc74178
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983749"
---
# <a name="jetbackupinstance-function"></a>Função JetBackupInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetbackupinstance-function"></a>Função JetBackupInstance

A **função JetBackupInstance** executa um backup de streaming de uma instância, incluindo todos os bancos de dados anexados, para um diretório. Com vários métodos de backup com suporte pelo mecanismo, essa é a função mais simples e mais encapsulada.

**Windows XP: JetBackupInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

A instância do banco de dados a ser backup.

*szBackupPath*

O diretório em que o backup é armazenado. Se o caminho de backup for NULL para usar, a função truncará os logs, se possível.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Cria um backup completo do banco de dados. Isso permitirá a preservação de um backup existente no mesmo diretório se o novo backup falhar.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Cria um backup incremental em vez de um backup completo. Isso significa que somente os arquivos de log criados desde o último backup completo ou incremental terão o backup feito.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Reservado para uso futuro.</p> | 



*pfnStatus*

Ponteiro para a [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) de retorno de chamada, que fornece informações de notificação sobre o progresso da operação de backup.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Um backup já está em andamento para a mesma instância. Vários backups não são permitidos ao mesmo tempo.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>A instância ainda não está pronta para backup, pois está sendo inicializada.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong> Esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errInvalidBackup</p> | <p>Um backup incremental não será permitido se o log circular estiver em.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>As opções especificadas são inválidas.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro inválido foi passado para a API.</p> | 
| <p>JET_errInvalidPath</p> | <p>O caminho de destino não existe.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>A instância está em execução sem registro em log. Nenhum backup é permitido.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>Houve um erro de verificação de verificação de verificação em um arquivo de log.</p> | 
| <p>JET_errLogWriteFail</p> | <p>O log da instância é temporário ou permanentemente desabilitado devido a um erro inesperado.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errReadVerifyFailure</p> | <p>Ocorreu um erro de verificação de verificação de verificação em uma página de banco de dados.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong> Esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p> | 



Depois que a função retornar êxito, no diretório de backup, todos os arquivos necessários para uma restauração até o momento do backup estarão presentes. Se esse for um backup completo, os arquivos serão os arquivos de banco de dados e os arquivos de log necessários para colocar o banco de dados em um estado consistente. Se esse for um backup incremental, somente os arquivos de log serão adicionados aos diretórios, mas os arquivos já existentes (bancos de dados e arquivos de log) junto com os novos arquivos de log poderão ser restaurados e trazer o banco de dados de volta para o estado no momento do backup.

Como um efeito colateral do backup, os arquivos de log que não são mais necessários serão truncados.

Ao mesmo tempo, os headers de banco de dados serão atualizados com as informações quando o último backup ocorreu.

Em caso de falha, não haverá nenhum arquivo no destino do diretório de backup para que nenhuma restauração seja possível. Ao mesmo tempo, os arquivos de log atuais não serão truncados.

#### <a name="remarks"></a>Comentários

As diferentes etapas do backup terão entradas do Log de Eventos geradas, incluindo os nomes de arquivo, o truncamento de log e o resultado final do backup.

O backup incremental só é possível depois que um backup completo foi feito. Além disso, backups incrementais só serão possíveis se o log circular estiver desligado. É recomendável que o diretório de backup não contenha outros arquivos e, em seguida, aquele envolvido no backup ou adicionado por um backup anterior bem-sucedido.

O diretório de backup deve existir, a menos que o *parâmetro JET_paramCreatePathIfNotExist* esteja definido para a instância. Para obter informações, consulte [Parâmetros do sistema.](./extensible-storage-engine-system-parameters.md)

O backup fará a verificação de verificação em todas as páginas de banco de dados usadas e, a partir do Windows Server 2003, nos arquivos de log também. Isso oferece uma oportunidade de estimar a saúde do banco de dados mesmo para páginas que não são lidas durante operações normais. Se algum desses dados de corrupção for encontrado, o backup falhará.

Durante o backup, o arquivo de log atual será concluído e iniciaremos uma nova geração de log. Isso permitirá copiar os arquivos de log necessários porque o último necessário não estará mais em uso.

É altamente recomendável que o backup não deva ser usado para outros fins além do backup e restaurado no nível do mecanismo. Isso minimizará a alteração da recuperação de erros durante as operações de backup e restauração.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetBackupInstanceW</strong> (Unicode) e <strong>JetBackupInstanceA</strong> (ANSI).</p> | 



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
