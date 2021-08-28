---
description: 'Saiba mais sobre: Função JetExternalRestore'
title: Função JetExternalRestore
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 480a3411152f1388bee0115ecbcffc88f6ded09b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984849"
---
# <a name="jetexternalrestore-function"></a>Função JetExternalRestore


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetexternalrestore-function"></a>Função JetExternalRestore

A **função JetExternalRestore** restaura um backup externo que foi feito com as APIs de backup externas e especifica um intervalo de números de arquivo de log a repetir durante o processo de restauração. Isso é conhecido como recuperação difícil, que é semelhante a , mas diferente da recuperação suave, conforme executado pela [função JetInit.](./jetinit-function.md)

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a>Parâmetros

*szCheckpointFilePath*

O caminho para o arquivo de ponto de verificação a ser usado durante a recuperação se *szTargetInstanceCheckpointPath* não for especificado ou já tiver uma instância ativa ou em execução.

*szLogPath*

O caminho ou diretório dos logs para a fase final (desfazer) da recuperação e, possivelmente, para os logs de roll forward. Esse caminho pode ser o mesmo que *o szBackupLogPath.*

*rgrstmap*

Essa é uma matriz [de](./jet-rstmap-structure.md) JET_RSTMAP estruturas. Este é um mapa de caminhos de banco de dados novos e antigos ou nomes de arquivo. Isso é usado porque os bancos de dados talvez precisem ser recuperados em um local diferente do local em que foram feito o backup. No caso em que vários bancos de dados são anexados a um único conjunto de log, o mapa de restauração pode especificar um subconjunto de bancos de dados a restaurar.

*crstfilemap*

O número de entradas no parâmetro *de matriz rgrstmap.*

*szBackupLogPath*

O caminho para o diretório onde os arquivos de log são restaurados. Esses são os logs que foram lidos durante a sequência de backup externa. Esse caminho pode ser o mesmo que o szLogPath.

*genLow*

O menor número de arquivo de log que deve ser replayado de *szBackupLogPath.* A fidelidade total de um long sem assinatura deve ser preservada, mas nas versões atuais do mecanismo esse número é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF. Isso pode mudar em versões futuras.

*genHigh*

O número de arquivo de log mais alto que deve ser replayado de *szBackupLogPath.* A fidelidade total de um long sem assinatura deve ser preservada, mas nas versões atuais do mecanismo esse número é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF. Isso pode mudar em versões futuras.

*pfn*

O retorno de chamada de status para relatar o progresso da recuperação.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A operação falhou porque não foi possível alocar memória suficiente para a conclusão.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <strong>JetExternalRestore</strong>e assim por diante quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> não são especificados ou não são especificados. Ou seja, eles devem corresponder e ser especificados ou ambos não especificados.</p> | 
| <p>JET_errDatabaseCorrupted</p> | <p>Isso indica que o banco de dados foi corrompido ou um arquivo não reconheceu.</p> | 
| <p>JET_errFileNotFound</p> | <p>A operação falhou porque não foi possível abrir o arquivo solicitado porque ele não pôde ser encontrado no caminho especificado.</p> | 
| <p>JET_errInvalidPath</p> | <p>A operação falhou porque não foi possível encontrar o caminho especificado.</p> | 
| <p>JET_errRestoreOfNonBackupDatabase</p> | <p>Esse erro será retornado se o arquivo de banco de dados especificado durante a restauração não for um banco de dados que foi feito backup com backup externo.</p> | 
| <p>JET_errStartingRestoreLogTooHigh</p> | <p>Esse erro será retornado se um dos arquivos de log no <em>szBackupLogPath</em>tiver uma geração de log abaixo da especificada pelo <em>genLow</em> ou <em>pLogInfo.ulGenLow.</em></p> | 
| <p>JET_errEndingRestoreLogTooLow</p> | <p>Esse erro será retornado se um dos arquivos de log no <em>szBackupLogPath</em>tiver uma geração de log acima da especificada em <em>genHigh</em> ou <em>pLogInfo.ulGenHigh.</em></p> | 
| <p>JET_errBadRestoreTargetInstance</p> | <p>O <em>szTargetInstanceLogPath especificado</em> não pertence a uma instância inicializada. Esse erro só será retornado no Windows XP e posterior.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>O mecanismo de banco de dados não pode executar a restauração externa ou a recuperação em modo de instância única. Esse erro só será retornado no Windows XP e posterior.</p> | 



Em caso de sucesso, todos os bancos de *dados do rgrstmap* são completamente recuperados e em um estado limpo ou consistente. Neste ponto, o banco de dados pode ser remontado a uma instância existente.

Em caso de falha, o mecanismo não pôde recuperar o banco de dados. O banco de dados está em um estado inválido e, para tentar novamente a recuperação, todo o banco de dados deve ser restaurado novamente. Normalmente, a origem dessa situação é a corrupção de disco ou log, ou alguma outra forma de erro de armazenamento de log ou um conjunto de log não contínuo.

#### <a name="remarks"></a>Comentários

Para entender como funciona uma recuperação "difícil", você deve entender que há três fases de recuperação e que a segunda fase pode ter duas partes. Na Fase I, os logs são necessários para manter a consistência de um banco de dados de backup (ou um conjunto inicial de logs incrementais pode ser usado). Na Fase II, todos os logs de roll forward adicionais disponíveis são consumidos para tornar o banco de dados consistente. Também há uma reprodução dos logs de roll forward adicionais. A fase III é a fase desfazer da recuperação.

Fase I: a reprodução do conjunto de logs que deve ser restaurado para que o banco de dados seja levado para um estado consistente (ou um conjunto inicial de arquivos de log) é executada. Basicamente, essa é a reprodução do conjunto de arquivos de log que não são opcionais para os bancos de dados que estão sendo restaurados. Se houver logs ausentes desse intervalo de logs, a restauração falhará. Esses logs devem ser colocados no diretório especificado no *parâmetro szBackupLogPath.*

Fase II: opcionalmente, pode haver alguns conjuntos de arquivos de log que são arquivos de log roll forward que vêm de backups incrementais ou diferenciais e dos arquivos de log de uma instância ativa. No caso de arquivos de log de backups incrementais ou diferenciais, os arquivos de log podem ser colocados nos diretórios especificados nos parâmetros *szBackupLogPath* ou *szTargetInstanceLogPath,* sendo o primeiro o diretório recomendado. Os logs usados para a fase de roll forward (fase II) devem vir da mesma série de logs tocadas durante a Fase I e devem ter incrementado continuamente os números de log sem lacunas dos logs da Fase I. Para reproduzir um banco de dados para estar totalmente atualizado com os arquivos de log que estão sendo usados atualmente por uma instância ativa, os parâmetros *szTargetInstanceLogPath* e *szTargetInstanceCheckpointPath* devem ser especificados. Isso pode ser feito mesmo enquanto outros bancos de dados estão anexados a esse conjunto de log.

Fase III: na fase final da recuperação, todas as transações não comprometidas são recompactadas, o que exige a geração de novos arquivos de log e a atualização do arquivo de ponto de verificação. Às vezes, essa fase é conhecida como "desfazer". O caminho do arquivo de ponto de verificação a ser usado durante essa fase é o caminho análogo ao local de log da fase III, ou seja, se *szLogPath* for usado para a Fase III, *szCheckpointFilePath* será usado, se *szTargetInstanceLogPath* for usado para a fase III da recuperação *szTargetInstanceCheckpointPath* será usado.

Para entender como os caminhos funcionam, use este fluxograma:

![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetExternalRestoreW</strong> (Unicode) e <strong>JetExternalRestoreA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetInit](./jetinit-function.md)
