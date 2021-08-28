---
description: 'Saiba mais sobre: Parâmetros de backup e restauração'
title: Parâmetros de backup e restauração
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6b82d3ffa1f55d79ac516ede469d422e7aced99
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982959"
---
# <a name="backup-and-restore-parameters"></a>Parâmetros de backup e restauração


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="backup-and-restore-parameters"></a>Parâmetros de backup e restauração

Este tópico contém parâmetros usados para backup e restauração.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

O caminho completo para cada banco de dados é persistido nos logs de transações em tempo de executar. Normalmente, esses bancos de dados devem permanecer no local original para que a reprodução da transação funcione corretamente. Esse parâmetro pode ser usado para forçar a recuperação de falhas ou uma operação de restauração para procurar os bancos de dados referenciados no log de transações na pasta especificada.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>""</p> | 
| <p>Tipo:</p> | <p>Caminho da Pasta (cadeia de caracteres)</p> | 
| <p>Intervalo válido:</p> | <p>0 – 246 caracteres</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramCleanupMismatchedLogFiles*  
77  

Esse parâmetro controla o resultado do [JetInit](./jetinit-function.md) quando o mecanismo de banco de dados é configurado para começar a usar arquivos de log de transações em disco de um tamanho diferente do que está configurado. Normalmente, [o JetInit](./jetinit-function.md) recuperará com êxito os bancos de dados, mas falhará com JET_errLogFileSizeMismatchDatabasesConsistent para indicar que o tamanho do arquivo de log está configurado incorretamente. No entanto, quando esse parâmetro for definido como true, o mecanismo de banco de dados excluirá silenciosamente todos os arquivos de log antigos, iniciará um novo conjunto de arquivos de log de transações usando o tamanho do arquivo de log configurado e retornará JET_errSuccess.

Esse parâmetro é útil quando o aplicativo deseja alterar de forma transparente o tamanho do arquivo de log de transações, mas ainda funciona de forma transparente em cenários de atualização e restauração.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>Falso</p> | 
| <p>Tipo:</p> | <p>Booliano</p> | 
| <p>Intervalo válido:</p> | <p>False, True</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Sim</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramDeleteOutOfRangeLogs*  
52  

Quando esse parâmetro for true, todos os arquivos de log de transações encontrados no disco que não fazem parte da sequência atual de arquivos de log serão excluídos pelo [JetInit](./jetinit-function.md). Isso pode ser usado para limpar automaticamente arquivos de log desagravados após uma operação de restauração.

**Windows XP:**  Introduzido no Windows XP.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>Falso</p> | 
| <p>Tipo:</p> | <p>Booliano</p> | 
| <p>Intervalo válido:</p> | <p>False, True</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Sim</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramOSSnapshotTimeout*  
82  

Esse parâmetro configura a quantidade de tempo permitida entre uma chamada para [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) e [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) antes que ocorra um tempo máximo. Confira [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) e [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para obter mais informações. O tempoout está em milissegundos.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>20000 (Windows XP e Windows Server 2003);</p><p>70000 (Windows Server 2003 SP1)</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sim</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramZeroDatabaseDuringBackup*  
71  

Quando esse parâmetro for true, todas as páginas em um banco de dados que estão passando por um backup de streaming serão depuradas de dados excluídos. É importante observar que as páginas do banco de dados que estão sendo depuradas estão em disco. O conjunto de dados completo é feito backup antes do processo de limpeza.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>Falso</p> | 
| <p>Tipo:</p> | <p>Booliano</p> | 
| <p>Intervalo válido:</p> | <p>False, True</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
