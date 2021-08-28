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
ms.openlocfilehash: a1c127f538ae80e8bec3dc5a34d5924b838b51ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465873"
---
# <a name="event-log-parameters"></a>Parâmetros do log de eventos


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="event-log-parameters"></a>Parâmetros do log de eventos

Este tópico contém parâmetros que são usados para o log de eventos.

JET_paramEventLogCache  
Esse parâmetro controla o tamanho (em bytes) de um cache de mensagens do EventLog que manterá as mensagens de EventLog emitidas pelo mecanismo de banco de dados enquanto o serviço EventLog é interrompido. Essas mensagens em cache serão liberadas para o log de eventos quando o serviço se tornar operacional. Todas as mensagens que excedem o cache serão descartadas.


| | | <p>Valor padrão:</p> | <p>0</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 a 2147483647</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramEventLoggingLevel*  
  
Esse parâmetro configura o nível de detalhe das mensagens de log de eventos emitidas para o log de eventos pelo mecanismo de banco de dados. Números mais altos resultarão em mensagens de log de eventos mais detalhadas.


| | | <p>Valor padrão:</p> | <p>JET_EventLoggingLevelMax</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>JET_EventLoggingDisable – JET_EventLoggingLevelMax</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramEventSource*  
4  

Esse parâmetro fornece uma cadeia de caracteres específica do aplicativo que será adicionada a qualquer mensagem de log de eventos emitida pelo mecanismo de banco de dados. Isso permite uma fácil correlação de mensagens de log de eventos com o aplicativo de origem. Se uma cadeia de caracteres vazia for especificada (como é o padrão), o nome executável do aplicativo host será usado.


| | | <p>Valor padrão:</p> | <p>""</p> | | <p>Tipo:</p> | <p>String</p> | | <p>Intervalo válido:</p> | <p>0 a 259 caracteres</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramEventSourceKey*  
49  

Esse parâmetro pode ser usado para controlar qual log de eventos o mecanismo de banco de dados usa para suas mensagens de log de eventos. Por padrão, todas as mensagens de log de eventos vão para o log de eventos do aplicativo. Se o nome da chave do registro para outro log de eventos estiver configurado, as mensagens do log de eventos entrarão em seu lugar.


| | | <p>Valor padrão:</p> | <p>""</p> | | <p>Tipo:</p> | <p>String</p> | | <p>Intervalo válido:</p> | <p>0 a 259 caracteres</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramNoInformationEvent*  
50  

Quando esse parâmetro for true, as mensagens de log de eventos informativas que normalmente seriam geradas pelo mecanismo de banco de dados serão suprimidas.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
