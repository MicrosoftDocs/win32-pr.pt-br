---
description: 'Saiba mais sobre: parâmetros do log de eventos'
title: Parâmetros do log de eventos
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
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
ms.openlocfilehash: 912dc3e1e8588e18ef0d1db8fbf7edccfca7bdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011203"
---
# <a name="event-log-parameters"></a>Parâmetros do log de eventos


_**Aplica-se a:** Windows | Windows Server_

## <a name="event-log-parameters"></a>Parâmetros do log de eventos

Este tópico contém parâmetros que são usados para o log de eventos.

JET_paramEventLogCache  
Esse parâmetro controla o tamanho (em bytes) de um cache de mensagens do EventLog que manterá as mensagens de EventLog emitidas pelo mecanismo de banco de dados enquanto o serviço EventLog é interrompido. Essas mensagens em cache serão liberadas para o log de eventos quando o serviço se tornar operacional. Todas as mensagens que excedem o cache serão descartadas.

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
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramEventLoggingLevel*  
  
Esse parâmetro configura o nível de detalhe das mensagens de log de eventos emitidas para o log de eventos pelo mecanismo de banco de dados. Números mais altos resultarão em mensagens de log de eventos mais detalhadas.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>JET_EventLoggingLevelMax</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>JET_EventLoggingDisable – JET_EventLoggingLevelMax</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramEventSource*  
4  

Esse parâmetro fornece uma cadeia de caracteres específica do aplicativo que será adicionada a qualquer mensagem de log de eventos emitida pelo mecanismo de banco de dados. Isso permite uma fácil correlação de mensagens de log de eventos com o aplicativo de origem. Se uma cadeia de caracteres vazia for especificada (como é o padrão), o nome executável do aplicativo host será usado.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 259 caracteres</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramEventSourceKey*  
49  

Esse parâmetro pode ser usado para controlar qual log de eventos o mecanismo de banco de dados usa para suas mensagens de log de eventos. Por padrão, todas as mensagens de log de eventos vão para o log de eventos do aplicativo. Se o nome da chave do registro para outro log de eventos estiver configurado, as mensagens do log de eventos entrarão em seu lugar.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 a 259 caracteres</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramNoInformationEvent*  
50  

Quando esse parâmetro for true, as mensagens de log de eventos informativas que normalmente seriam geradas pelo mecanismo de banco de dados serão suprimidas.

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
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
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
