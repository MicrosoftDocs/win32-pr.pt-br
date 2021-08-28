---
description: 'Saiba mais sobre: função JetBackup'
title: Função JetBackup
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e17ee5029da8ac71b5421e44a3647494e676ba71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982989"
---
# <a name="jetbackup-function"></a>Função JetBackup


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetbackup-function"></a>Função JetBackup

A função **JetBackup** cria um backup do banco de dados enquanto o banco de dados está online. essa função é usada principalmente para compatibilidade com versões anteriores com Windows 2000 e mecanismos de banco de dados anterior, em que apenas uma instância de um banco de dados é permitida. Nesse caso, a instância ativa é a instância que é submetida a backup.

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parâmetros

*szBackupPath*

O diretório em que o backup está armazenado. Se o caminho de backup for nulo, a função truncará os logs, se possível.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Cria um backup completo do banco de dados. Isso permite a preservação de um backup existente no mesmo diretório se o novo backup falhar.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Cria um backup incremental em oposição a um backup completo. Isso significa que somente os arquivos de log desde o último backup completo ou incremental serão submetidos a backup.</p> | 



*pfnStatus*

Aponta para a função de retorno de chamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , que fornece informações de notificação sobre o progresso da operação de backup.

### <a name="return-value"></a>Valor Retornado

A função retorna um dos [JET_ERR](./jet-err.md) códigos de erro. Veja a seguir as mais comumente retornadas. (para obter uma lista completa de erros para essa API, consulte [códigos de erro do mecanismo de Armazenamento extensível](./extensible-storage-engine-error-codes.md).)


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Um backup já está em andamento para a mesma instância. Não são permitidos vários backups ao mesmo tempo.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>A instância ainda não está pronta para backup durante a inicialização.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong> esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errInvalidBackup</p> | <p>Um backup incremental não será permitido se o log circular estiver ativado.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>As opções especificadas são inválidas.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro inválido foi passado para a API.</p> | 
| <p>JET_errInvalidPath</p> | <p>O caminho de destino não existe.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>A instância está sendo executada sem registro em log. Nenhum backup é permitido.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>Erro de verificação de checksum em um arquivo de log.</p> | 
| <p>JET_errLogWriteFail</p> | <p>O log da instância é temporário ou permanentemente desabilitado devido a um erro inesperado.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errReadVerifyFailure</p> | <p>Ocorreu um erro de verificação de checksum em uma página de banco de dados.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong> esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 



Se a função for realizada com sucesso, todos os arquivos necessários para uma restauração até o momento do backup estarão contidos no diretório de backup. Se esse for um backup completo, os arquivos serão os arquivos de banco de dados e os arquivos de log necessários para colocar o banco de dados em um estado consistente. Se esse for um backup incremental, somente os arquivos de log serão adicionados aos diretórios, mas os arquivos já existentes (bancos de dados e arquivos de log), juntamente com os novos arquivos de log, poderão ser restaurados para colocar o banco de dados novamente no estado em que ele estava no momento em que o backup começou.

Como um efeito colateral do backup, os arquivos de log que não são mais necessários serão truncados.

Ao mesmo tempo, os cabeçalhos de banco de dados serão atualizados com as informações quando o último backup tiver ocorrido.

Se a função falhar, não haverá nenhum arquivo no destino do diretório de backup, portanto, nenhuma restauração será possível. Ao mesmo tempo, os arquivos de log atuais não serão truncados.

#### <a name="remarks"></a>Comentários

As diferentes etapas do backup terão entradas de log de eventos geradas, incluindo os nomes de arquivo, o truncamento de log e o resultado final do backup.

Os backups incrementais são possíveis somente após a tomada de um backup completo. Além disso, os backups incrementais só serão possíveis se o log circular estiver desativado. É recomendável que o diretório de backup não contenha nenhum arquivo que não seja o usado no backup ou adicionado por um backup bem-sucedido anterior.

O diretório de backup deve existir, a menos que o parâmetro *JET_paramCreatePathIfNotExist* esteja definido para a instância. Para obter informações, consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md).

o backup fará uma verificação de checksum em todas as páginas de banco de dados usadas e a partir do Windows Server 2003, nos arquivos de log também. Isso dá a oportunidade de estimar a integridade do banco de dados, mesmo para páginas que não são lidas durante operações normais. Se algum dano for encontrado, o backup falhará.

Durante o backup, o arquivo de log atual será concluído e um novo log será gerado. Dessa forma, todos os arquivos de log necessários podem ser copiados, porque o log atual não estará mais em uso.

É altamente recomendável que o backup não seja usado para nenhuma finalidade diferente do backup e da restauração no nível do mecanismo. Isso minimizará a possibilidade de obter erros durante as operações de backup e restauração.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetBackupW</strong> (Unicode) e <strong>JetBackupA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
