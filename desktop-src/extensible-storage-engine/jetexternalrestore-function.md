---
description: 'Saiba mais sobre: função JetExternalRestore'
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
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105786273"
---
# <a name="jetexternalrestore-function"></a>Função JetExternalRestore


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetexternalrestore-function"></a>Função JetExternalRestore

A função **JetExternalRestore** restaura um backup externo que foi feito com as APIs de backup externo e especifica um intervalo de números de arquivos de log a serem reproduzidos durante o processo de restauração. Isso é conhecido como recuperação complexa, que é semelhante a, mas diferente da recuperação simples, conforme executado pela função [JetInit](./jetinit-function.md) .

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

O caminho para o arquivo de ponto de verificação a ser usado durante a recuperação se *szTargetInstanceCheckpointPath* não for especificado ou se já tiver uma instância ativa ou em execução.

*szLogPath*

O caminho ou diretório para os logs da fase final (desfazer) de recuperação e, possivelmente, para os logs de roll-forward. Esse caminho pode ser o mesmo que o *szBackupLogPath*.

*rgrstmap*

Esta é uma matriz de estruturas de [JET_RSTMAP](./jet-rstmap-structure.md) . Este é um mapa de caminhos de banco de dados novos e antigos ou nomes de File. Isso é usado porque os bancos de dados podem precisar ser recuperados para um local diferente do local do qual foram feitos backup. No caso em que vários bancos de dados são anexados a um único conjunto de registros, o mapa de restauração pode especificar um subconjunto de bancos de dados a serem restaurados.

*crstfilemap*

O número de entradas no parâmetro de matriz *rgrstmap* .

*szBackupLogPath*

O caminho para o diretório em que os arquivos de log são restaurados. Esses são os logs que foram lidos durante a sequência de backup externo. Esse caminho pode ser o mesmo que o szLogPath.

*genLow*

O número de arquivo de log mais baixo a ser reproduzido de *szBackupLogPath*. A fidelidade total de um longo não assinado deve ser preservada, mas nas versões atuais do mecanismo esse número é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF. Isso pode ser alterado em versões futuras.

*genHigh*

O número do arquivo de log mais alto a ser reproduzido de *szBackupLogPath*. A fidelidade total de um longo não assinado deve ser preservada, mas nas versões atuais do mecanismo esse número é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF. Isso pode ser alterado em versões futuras.

*PFN*

O retorno de chamada de status para relatar o progresso da recuperação.

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
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <strong>JetExternalRestore</strong>, e assim por diante, quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> não forem especificados ou não forem ambos não especificados. Ou seja, eles devem corresponder e ser especificados ou ambos não especificados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Isso indica que o banco de dados foi corrompido ou um arquivo não reconhecido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>A operação falhou porque não pôde abrir o arquivo solicitado porque ele não foi encontrado no caminho especificado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>A operação falhou porque o caminho especificado não foi encontrado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Esse erro será retornado se o arquivo de banco de dados especificado durante a restauração não for um banco de dados cujo backup foi feito com backup externo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Esse erro será retornado se um dos arquivos de log no <em>szBackupLogPath</em>tiver uma geração de log abaixo especificada pelo <em>genLow</em> ou <em>pLogInfo. ulGenLow</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Esse erro será retornado se um dos arquivos de log no <em>szBackupLogPath</em>tiver uma geração de log acima especificada em <em>genHigh</em> ou <em>pLogInfo. ulGenHigh</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>O <em>szTargetInstanceLogPath</em> especificado não pertence a uma instância inicializada. Esse erro só será retornado no Windows XP e posterior.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>O mecanismo de banco de dados não pode executar restauração externa ou recuperação de hardware no modo de instância única. Esse erro só será retornado no Windows XP e posterior.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, todos os bancos de dados do *rgrstmap* são completamente recuperados e em um estado limpo ou consistente. Neste ponto, o banco de dados pode ser remontado em uma instância existente.

Em caso de falha, o mecanismo não pôde recuperar o banco de dados. O banco de dados está em um estado inválido e, para tentar a recuperação complexa, todo o banco de dados deve ser restaurado novamente. Normalmente, a origem de tal situação é a corrupção de disco ou log, ou alguma outra forma de gerenciamento de ingestão de log ou um conjunto de logs não contínuo.

#### <a name="remarks"></a>Comentários

Para entender como funciona uma recuperação "rígida", você deve entender que há três fases de recuperação, e a segunda fase pode ter duas partes. Na fase I, os logs são necessários para colocar um banco de dados de backup em consistência (ou um conjunto inicial de logs incrementais pode ser usado). Na fase II, todos os logs de roll-forward adicionais disponíveis são consumidos para tornar o banco de dados consistente. Também há uma repetição dos logs adicionais de roll-forward. A fase III é a fase desfazer da recuperação.

Fase I: a reprodução do conjunto de logs que devem ser restaurados para que o banco de dados seja trazido para um estado consistente (ou um conjunto inicial de arquivos de log) seja executado. Basicamente, essa é a repetição do conjunto de arquivos de log que não são opcionais para os bancos de dados que estão sendo restaurados. Se houver logs ausentes desse intervalo de logs, a restauração falhará. Esses logs devem ser colocados no diretório especificado no parâmetro *szBackupLogPath* .

Fase II: opcionalmente, pode haver alguns conjuntos de arquivos de log que são arquivos de log de roll-forward que vêm de backups incrementais ou diferenciais e dos arquivos de log de uma instância ativa. No caso de arquivos de log de backups incrementais ou diferenciais, os arquivos de log podem ser colocados nos diretórios especificados nos parâmetros *szBackupLogPath* ou *szTargetInstanceLogPath* , sendo que o primeiro é o diretório recomendado. Os logs usados para a fase de roll-forward (fase II) devem vir da mesma série de logs reproduzidos durante a fase I e devem ter um incremento contínuo de números de log sem intervalos da fase I logs. Para reproduzir um banco de dados para ser totalmente atualizado com os arquivos de log que estão sendo usados atualmente por uma instância ativa, os parâmetros *szTargetInstanceLogPath* e *szTargetInstanceCheckpointPath* devem ser especificados. Isso pode ser feito mesmo enquanto outros bancos de dados são anexados a esse conjunto de logs.

Fase III: na fase final de recuperação, todas as transações não confirmadas são revertidas, o que requer a geração de novos arquivos de log e a atualização do arquivo de ponto de verificação. Às vezes, essa fase é chamada de "desfazer". O caminho do arquivo de ponto de verificação a ser usado durante essa fase é o caminho análogo ao local do log da fase III, ou seja, se *szLogPath* for usado para a fase III, *szCheckpointFilePath* será usado se *szTargetInstanceLogPath* for usado para a fase III de recuperação *szTargetInstanceCheckpointPath* será usado.

Para entender como os caminhos funcionam, use este gráfico de fluxo:

![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
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
<td><p>Implementado como <strong>JetExternalRestoreW</strong> (Unicode) e <strong>JetExternalRestoreA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetInit](./jetinit-function.md)
