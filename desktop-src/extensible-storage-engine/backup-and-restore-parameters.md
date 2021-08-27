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
ms.openlocfilehash: e57cc3f1078d46436d56a56c48c31a3fac4956c0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481402"
---
# <a name="backup-and-restore-parameters"></a>Parâmetros de backup e restauração


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="backup-and-restore-parameters"></a>Parâmetros de backup e restauração

Este tópico contém parâmetros usados para backup e restauração.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

O caminho completo para cada banco de dados é persistido nos logs de transações em tempo de executar. Normalmente, esses bancos de dados devem permanecer no local original para que a reprodução da transação funcione corretamente. Esse parâmetro pode ser usado para forçar a recuperação de falhas ou uma operação de restauração para procurar os bancos de dados referenciados no log de transações na pasta especificada.


| | | <p>Valor padrão:</p> | <p>""</p> | | <p>Tipo:</p> | <p>Caminho da Pasta (cadeia de caracteres)</p> | | <p>Intervalo válido:</p> | <p>0 – 246 caracteres</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramCleanupMismatchedLogFiles*  
77  

Esse parâmetro controla o resultado do [JetInit](./jetinit-function.md) quando o mecanismo de banco de dados é configurado para começar a usar arquivos de log de transações em disco de um tamanho diferente do que está configurado. Normalmente, [o JetInit](./jetinit-function.md) recuperará com êxito os bancos de dados, mas falhará com JET_errLogFileSizeMismatchDatabasesConsistent para indicar que o tamanho do arquivo de log está configurado incorretamente. No entanto, quando esse parâmetro for definido como true, o mecanismo de banco de dados excluirá silenciosamente todos os arquivos de log antigos, iniciará um novo conjunto de arquivos de log de transações usando o tamanho do arquivo de log configurado e retornará JET_errSuccess.

Esse parâmetro é útil quando o aplicativo deseja alterar de forma transparente o tamanho do arquivo de log de transações, mas ainda funciona de forma transparente em cenários de atualização e restauração.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramDeleteOutOfRangeLogs*  
52  

Quando esse parâmetro for true, todos os arquivos de log de transações encontrados no disco que não fazem parte da sequência atual de arquivos de log serão excluídos pelo [JetInit](./jetinit-function.md). Isso pode ser usado para limpar automaticamente arquivos de log desagravados após uma operação de restauração.

**Windows XP:**  Introduzido no Windows XP.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramOSSnapshotTimeout*  
82  

Esse parâmetro configura a quantidade de tempo permitida entre uma chamada para [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) e [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) antes que ocorra um tempo máximo. Confira [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) e [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para obter mais informações. O tempoout está em milissegundos.


| | | <p>Valor padrão:</p> | <p>20000 (Windows XP e Windows Server 2003);</p><p>70000 (Windows Server 2003 SP1)</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramZeroDatabaseDuringBackup*  
71  

Quando esse parâmetro for true, cada página em um banco de dados que está passando por um backup de streaming será depurada dos dados excluídos. É importante observar que as páginas de banco de dados que estão sendo depuradas estão no disco. O backup do conjunto de dados completo é feito antes do processo de depuração.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
