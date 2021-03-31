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
ms.openlocfilehash: 13ba0e89602f7e5d4b9df395e89c73c8dc735692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661503"
---
# <a name="io-parameters"></a>Parâmetros de e/s


_**Aplica-se a:** Windows | Windows Server_

## <a name="io-parameters"></a>Parâmetros de e/s

Este tópico contém parâmetros que são usados para entrada e saída (e/s).

*JET_paramAccessDeniedRetryPeriod*  
53  

**Windows XP e posterior:**  Esse parâmetro configura a duração do tempo (em milissegundos) que o mecanismo de banco de dados usará para acessar um arquivo bloqueado antes de falhar com JET_errFileAccessDenied. Esse atraso foi projetado para contornar o software antivírus que pode conter alguns dos arquivos do mecanismo de banco de dados aberto brevemente depois que eles são fechados.

**Observação**  Como resultado da lógica de repetição acima, qualquer tentativa de anexar a um banco de dados ou usar um arquivo de log que já esteja em uso pelo mecanismo de banco de dados resultará em um atraso desse tamanho antes que a chamada à API retorne uma falha (legítima). Esse parâmetro pode ser usado para desativar esse atraso, caso este seja um cenário comum.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>10000</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e posterior</p></td>
</tr>
</tbody>
</table>


*JET_paramCreatePathIfNotExist*  
100  

Quando esse parâmetro for definido como true, qualquer pasta que estiver ausente em um caminho do sistema de arquivos em uso pelo mecanismo de banco de dados será criada silenciosamente. Caso contrário, a operação que usa o caminho do sistema de arquivos ausente irá falhar com JET_errInvalidPath.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Falso, verdadeiro</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableFileCache*  
126  

Quando esse parâmetro for **true**, o mecanismo de banco de dados usará o cache de arquivos do Windows como um cache de leitura para todos os seus vários arquivos. Ele também o usará como um cache de gravação para o banco de dados temporário ou para bancos que estiverem abertos com a recuperação desabilitada. O mecanismo de banco de dados deve desabilitar o cache de gravação para bancos de dados comuns, arquivos de log de transações e arquivos de ponto de verificação para proteger a integridade transacional dos bancos de dados.

É importante observar que o uso do cache de arquivos do Windows adicionará uma segunda camada de armazenamento em cache para arquivos de banco de dados. O cache de banco de dados ainda usará sua própria memória para armazenar em cache os arquivos de banco de dados. A intenção desse modo é permitir que o aplicativo configure o mecanismo de banco de dados com um pequeno cache dedicado e permita que o Windows doar memória sobressalente para melhorar ainda mais o cache dos dados do banco de dado.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Falso, verdadeiro</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows Vista e posterior</p></td>
</tr>
</tbody>
</table>


*JET_paramIOPriority*  
152  

Esse parâmetro controla como o ESE lida com as operações de e/s. Os valores podem ser definidos como 0 (JET_IOPriorityNormal) para operação normal, ou 1 (JET_IOPriorityLow) para operação de baixa prioridade. Quando a prioridade é definida como JET_IOPriorityLow, o ESE usa a nova funcionalidade de prioridade de e/s de thread disponível no Windows Vista para reduzir a prioridade de e/s no thread para que as operações de e/s subsequentes sejam emitidas com a nova prioridade baixa.

**Windows Vista:**  O JET_paramIOPriority é introduzido no Windows Vista.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 - 1</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows Vista</p></td>
</tr>
</tbody>
</table>


*JET_paramOutstandingIOMax*  
30 

Esse parâmetro controla quantas e/SS de arquivo de banco de dados podem ser enfileiradas no sistema operacional do host ao mesmo tempo.

Um valor maior para esse parâmetro pode ajudar significativamente o desempenho de um aplicativo de banco de dados grande.

**Windows XP e Windows Server 2003:**  Esse parâmetro é ignorado no Windows XP e no Windows Server 2003 e não afeta a operação do mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p><strong>Windows 2000: </strong>  64</p>
<p><strong>Windows Vista:</strong>   1024</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000:</strong>  8 a 2147483647</p>
<p><strong>Windows Vista:</strong>  0 a 65536</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCoalesceReadSize*  
164  

Número máximo de bytes que podem ser agrupados para uma operação de leitura agrupada.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>262144</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-1073741824</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCoalesceWriteSize*  
165  

Número máximo de bytes que podem ser agrupados para uma operação de gravação agrupada.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>393216</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-1073741824</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCoalesceReadGapSize*  
166  

Número máximo de bytes que podem ser gappeddos para uma operação de e/s de gravação agrupada.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>262144</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-1073741824</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCoalesceWriteGapSize*  
167  

Número máximo de bytes que podem ser gapped para uma operação de e/s de leitura agrupada.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>393216</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Inteiro</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-1073741824</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

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
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
