---
description: 'Saiba mais sobre: Parâmetros do log de eventos'
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
ms.openlocfilehash: 6fdf19d493e60cf229178872f7e33710210cfbec
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985329"
---
# <a name="event-log-parameters"></a>Parâmetros do log de eventos


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="event-log-parameters"></a>Parâmetros do log de eventos

Este tópico contém parâmetros que são usados para o log de eventos.

JET_paramEventLogCache  
Esse parâmetro controla o tamanho (em bytes) de um cache de mensagens do eventlog que conterá mensagens eventlog emitidas pelo mecanismo de banco de dados enquanto o serviço eventlog é interrompido. Essas mensagens armazenadas em cache serão liberados para o eventlog quando o serviço se tornar operacional. Todas as mensagens que estouram o cache serão descartados.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>0</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramEventLoggingLevel*  
  
Esse parâmetro configura o nível de detalhes das mensagens eventlog emitidas para o eventlog pelo mecanismo de banco de dados. Números mais altos resultarão em mensagens de eventlog mais detalhadas.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>JET_EventLoggingLevelMax</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>JET_EventLoggingDisable – JET_EventLoggingLevelMax</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramEventSource*  
4  

Esse parâmetro fornece uma cadeia de caracteres específica do aplicativo que será adicionada a todas as mensagens de log de eventos emitidas pelo mecanismo de banco de dados. Isso permite uma correlação fácil de mensagens de log de eventos com o aplicativo de origem. Se uma cadeia de caracteres vazia for especificada (como é o padrão), o nome executável do aplicativo host será usado.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>""</p> | 
| <p>Tipo:</p> | <p>Cadeia de caracteres</p> | 
| <p>Intervalo válido:</p> | <p>0 – 259 caracteres</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramEventSourceKey*  
49  

Esse parâmetro pode ser usado para controlar qual log de eventos o mecanismo de banco de dados usa para suas mensagens de log de eventos. Por padrão, todas as mensagens do log de eventos serão enviadas para o log de eventos do aplicativo. Se o nome da chave do Registro para outro log de eventos estiver configurado, as mensagens do log de eventos serão enviadas para lá.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>""</p> | 
| <p>Tipo:</p> | <p>Cadeia de caracteres</p> | 
| <p>Intervalo válido:</p> | <p>0 a 259 caracteres</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta os recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramNoInformationEvent*  
50  

Quando esse parâmetro for true, as mensagens de log de eventos informativas que normalmente seriam geradas pelo mecanismo de banco de dados serão suprimidas.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>Falso</p> | 
| <p>Tipo:</p> | <p>Booliano</p> | 
| <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | 
| <p>Escopo:</p> | <p>Instância</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta os recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
