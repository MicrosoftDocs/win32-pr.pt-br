---
description: 'Saiba mais sobre: Meta Parameters'
title: Metadados de parâmetros
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
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
ms.openlocfilehash: 2f821d3aea8055f6c1344ed9d5107417adbaf604
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985509"
---
# <a name="meta-parameters"></a>Metadados de parâmetros


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="meta-parameters"></a>Metadados de parâmetros

Este tópico contém parâmetros que são usados para controlar outros parâmetros.

JET_paramConfiguration  
129  
Esse parâmetro expõe vários conjuntos de valores padrão para todo o conjunto de parâmetros do sistema. Quando esse parâmetro é definido como uma configuração específica, todos os valores de parâmetro do sistema são redefinidos para seus valores padrão para essa configuração. Se a configuração for definida para uma instância específica, os parâmetros globais do sistema não serão redefinidos para seus valores padrão.

Além disso, o próprio parâmetro pode ter outros efeitos sobre o comportamento do mecanismo de banco de dados.

Neste momento, há duas configurações com suporte:

  - Configuração pequena (0): o mecanismo de banco de dados é otimizado para uso de memória.

  - Configuração herdda (1): o mecanismo de banco de dados tem seus padrões tradicionais.

A Configuração Pequena altera os padrões dos seguintes parâmetros do sistema para os valores especificados:


| <p>Parâmetro do sistema</p> | <p>Novo valor padrão</p> | 
|-------------------------|--------------------------|
| <p>JET_paramMaxSessions</p> | <p>30000</p> | 
| <p>JET_paramMaxOpenTables</p> | <p>2147483647</p> | 
| <p>JET_paramMaxCursors</p> | <p>2147483647</p> | 
| <p>JET_paramMaxVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramMaxTemporaryTables</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileSize</p> | <p>64</p> | 
| <p>JET_paramLogBuffers</p> | <p>1</p> | 
| <p>JET_paramDbExtensionSize</p> | <p>16</p> | 
| <p>JET_paramPageTempDBMin</p> | <p>14</p> | 
| <p>JET_paramCacheSizeMax</p> | <p>16</p> | 
| <p>JET_paramCheckpointDepthMax</p> | <p>65536</p> | 
| <p>JET_paramLRUKHistoryMax</p> | <p>10</p> | 
| <p>JET_paramOutstandingIOMax</p> | <p>16</p> | 
| <p>JET_paramStartFlushThreshold</p> | <p>1</p> | 
| <p>JET_paramStopFlushThreshold</p> | <p>2</p> | 
| <p>JET_paramNoInformationEvent</p> | <p>1</p> | 
| <p>JET_paramCacheSizeMin</p> | <p>16</p> | 
| <p>JET_paramPreferredVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileCreateAsynch</p> | <p>0</p> | 
| <p>JET_paramGlobalMinVerPages</p> | <p>1</p> | 
| <p>JET_paramPageHintCacheSize</p> | <p>32</p> | 
| <p>JET_paramDisablePerfmon</p> | <p>1</p> | 
| <p>JET_paramEnableFileCache</p> | <p>1</p> | 
| <p>JET_paramEnableViewCache</p> | <p>1</p> | 
| <p>JET_paramVerPageSize</p> | <p>1024</p> | 
| <p>JET_paramEnableAdvanced</p> | <p>0</p> | 
| <p>JET_paramCheckpointIOMax</p> | <p>8</p> | 



A Configuração Pequena também tem vários outros efeitos no mecanismo de banco de dados, incluindo:

  - Todos os recursos gerenciados pelos parâmetros do sistema são alocados do heap conforme necessário

  - Outros recursos internos usados pelo mecanismo de banco de dados são reduzidos em tamanho reduzido

  - Várias atividades de manutenção são dimensionados novamente para evitar a atividade de thread em segundo plano


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>1 (Herdou)</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>0 – 1</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>A partir do Windows Server 2008 e Windows Vista</p> | 



JET_paramEnableAdvanced  
130  
Esse parâmetro é usado para controlar quando o mecanismo de banco de dados aceita ou rejeita alterações em um subconjunto dos parâmetros do sistema. Esse parâmetro é usado em conjunto com JET_paramConfiguration para impedir que alguns parâmetros do sistema sejam definidos fora dos padrões da configuração selecionada.

Os seguintes parâmetros do sistema serão protegidos de serem definidos quando esse parâmetro for definido como false:

  - JET_paramMaxSessionsfon

  - JET_paramMaxOpenTables

  - JET_paramPreferredMaxOpenTables

  - JET_paramMaxCursors

  - JET_paramMaxVerPages

  - JET_paramMaxTemporaryTables

  - JET_paramLogBuffers

  - JET_paramWaitLogFlush

  - JET_paramLogCheckpointPeriod

  - JET_paramLogWaitingUserMax

  - JET_paramDbExtensionSize

  - JET_paramPageTempDBMin

  - JET_paramPageFragment

  - JET_paramBatchIOBufferMax

  - JET_paramCacheSizeMax

  - JET_paramLRUKCorrInterval

  - JET_paramLRUKHistoryMax

  - JET_paramLRUKPolicy

  - JET_paramLRUKTimeout

  - JET_paramLRUKTrxCorrInterval

  - JET_paramOutstandingIOMax

  - JET_paramStartFlushThreshold

  - JET_paramStopFlushThreshold

  - JET_paramCacheSize

  - JET_paramCacheSizeMin

  - JET_paramPreferredVerPages

  - JET_paramBackupChunkSize

  - JET_paramBackupOutstandingReads

  - JET_paramLogFileCreateAsynch

  - JET_paramRecordUpgradeDirtyLevel

  - JET_paramGlobalMinVerPages

  - JET_paramPageHintCacheSize

  - JET_paramVersionStoreTaskQueueMax

  - JET_paramDBAPageAvailMin

  - JET_paramMaxRandomIOSize

  - JET_paramCachedClosedTables

  - JET_paramEnableFileCache

  - JET_paramEnableViewCache

  - JET_paramVerPageSize

  - JET_paramCheckpointIOMax


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>True</p> | 
| <p>Tipo:</p> | <p>Booliano</p> | 
| <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta os recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>a partir do Windows Server 2008 e Windows Vista</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows Server 2008.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
