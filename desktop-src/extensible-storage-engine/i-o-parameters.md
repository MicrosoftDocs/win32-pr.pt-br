---
description: 'Saiba mais sobre: parâmetros de e/s'
title: Parâmetros de e/s
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 0a980e436dacc020a0606e6a9466492fe687ca0e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473532"
---
# <a name="io-parameters"></a>Parâmetros de e/s


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="io-parameters"></a>Parâmetros de e/s

Este tópico contém parâmetros que são usados para entrada e saída (e/s).

*JET_paramAccessDeniedRetryPeriod*  
53  

**Windows XP e posterior:**  Esse parâmetro configura a duração do tempo (em milissegundos) que o mecanismo de banco de dados usará para acessar um arquivo bloqueado antes de falhar com JET_errFileAccessDenied. Esse atraso foi projetado para contornar o software antivírus que pode conter alguns dos arquivos do mecanismo de banco de dados aberto brevemente depois que eles são fechados.

**Observação**  Como resultado da lógica de repetição acima, qualquer tentativa de anexar a um banco de dados ou usar um arquivo de log que já esteja em uso pelo mecanismo de banco de dados resultará em um atraso desse tamanho antes que a chamada à API retorne uma falha (legítima). Esse parâmetro pode ser usado para desativar esse atraso, caso este seja um cenário comum.


| | | <p>Valor padrão:</p> | <p>10000</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 a 4294967295</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e posterior</p> | 



*JET_paramCreatePathIfNotExist*  
100  

Quando esse parâmetro for definido como true, qualquer pasta que estiver ausente em um caminho do sistema de arquivos em uso pelo mecanismo de banco de dados será criada silenciosamente. Caso contrário, a operação que usa o caminho do sistema de arquivos ausente irá falhar com JET_errInvalidPath.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramEnableFileCache*  
126  

quando esse parâmetro for **True**, o mecanismo de banco de dados usará o cache de arquivos Windows como um cache de leitura para todos os seus vários arquivos. Ele também o usará como um cache de gravação para o banco de dados temporário ou para bancos que estiverem abertos com a recuperação desabilitada. O mecanismo de banco de dados deve desabilitar o cache de gravação para bancos de dados comuns, arquivos de log de transações e arquivos de ponto de verificação para proteger a integridade transacional dos bancos de dados.

é importante observar que o uso do cache de arquivos de Windows adicionará uma segunda camada de armazenamento em cache para arquivos de banco de dados. O cache de banco de dados ainda usará sua própria memória para armazenar em cache os arquivos de banco de dados. a intenção desse modo é permitir que o aplicativo configure o mecanismo de banco de dados com um pequeno cache dedicado e permita que Windows doar memória sobressalente para melhorar ainda mais o cache dos dados do banco de dado.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows Vista e posterior</p> | 



*JET_paramIOPriority*  
152  

Esse parâmetro controla como o ESE lida com as operações de e/s. Os valores podem ser definidos como 0 (JET_IOPriorityNormal) para operação normal, ou 1 (JET_IOPriorityLow) para operação de baixa prioridade. quando a prioridade é definida como JET_IOPriorityLow, o ESE usa a nova funcionalidade de prioridade de e/s de thread disponível no Windows Vista para reduzir a prioridade de e/s no thread para que as operações de e/s subsequentes sejam emitidas com a nova prioridade baixa.

**Windows Vista:**  o JET_paramIOPriority é introduzido no Windows Vista.


| | | <p>Valor padrão:</p> | <p>0</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 - 1</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows Vista</p> | 



*JET_paramOutstandingIOMax*  
30 

Esse parâmetro controla quantas e/SS de arquivo de banco de dados podem ser enfileiradas no sistema operacional do host ao mesmo tempo.

Um valor maior para esse parâmetro pode ajudar significativamente o desempenho de um aplicativo de banco de dados grande.

**Windows XP e Windows Server 2003:**  esse parâmetro é ignorado no Windows XP e no Windows Server 2003 e não afeta a operação do mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p><strong>Windows 2000:</strong> 64</p><p><strong>Windows Vista:</strong> 1024</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 8 – 2147483647</p><p><strong>Windows Vista:</strong> 0 a 65536</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramMaxCoalesceReadSize*  
164  

Número máximo de bytes que podem ser agrupados para uma operação de leitura agrupada.


| | | <p>Valor padrão:</p> | <p>262144</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0-1073741824</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteSize*  
165  

Número máximo de bytes que podem ser agrupados para uma operação de gravação agrupada.


| | | <p>Valor padrão:</p> | <p>393216</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0-1073741824</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceReadGapSize*  
166  

Número máximo de bytes que podem ser gappeddos para uma operação de e/s de gravação agrupada.


| | | <p>Valor padrão:</p> | <p>262144</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0-1073741824</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteGapSize*  
167  

Número máximo de bytes que podem ser mapeados para uma operação de E/S de leitura coalesced.


| | | <p>Valor padrão:</p> | <p>393216</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0-1073741824</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
