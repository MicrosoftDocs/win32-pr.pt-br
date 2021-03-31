---
title: Formato dos logs de erro da API do servidor HTTP
description: Em geral, os arquivos de log de erros da API do servidor HTTP têm o mesmo formato que os logs de erros do W3C, exceto que os arquivos de log de erros da API do servidor HTTP não contêm cabeçalhos de coluna.
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- API do servidor HTTP, formato do log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2eb914251a809178adef28c8a61b1a174c6e86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159510"
---
# <a name="format-of-the-http-server-api-error-logs"></a>Formato dos logs de erro da API do servidor HTTP

Em geral, os arquivos de log de erros da API do servidor HTTP têm o mesmo formato que os logs de erros do W3C, exceto que os arquivos de log de erros da API do servidor HTTP não contêm cabeçalhos de coluna. Cada linha de um log de erros da API do servidor HTTP registra um erro com campos em uma ordem específica. Cada campo é separado do campo anterior por um caractere de espaço único (0x0020). Dentro de cada campo, caracteres de espaço, tabulações e caracteres de controle não imprimíveis são substituídos por sinais de adição (0x002B).

A tabela a seguir identifica os campos e a ordem dos campos em um registro de log de erros.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date<br/></td>
<td>O campo de data segue o formato W3C e é baseado em UTC (tempo Universal Coordenado). O campo de data sempre é 10 caracteres no formato &quot; aaaa-mm-dd &quot; . Por exemplo, 1 de maio de 2003 é expresso como &quot; 2003-05-01 &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="Time"></span><span id="time"></span><span id="TIME"></span>Momento<br/></td>
<td>O campo hora segue o formato W3C e é baseado em UTC. O campo de tempo sempre tem 8 caracteres no formato &quot; mm: hh: SS &quot; . Por exemplo, 5:30 PM (UTC) é expresso como &quot; 17:30:00 &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Endereço IP do cliente<br/></td>
<td>O endereço IP do cliente afetado que pode ser um endereço IPv4 ou um endereço IPv6. Se o endereço IP do cliente for um endereço IPv6, o campo Identificação_do_escopo também será incluído no endereço.<br/></td>
</tr>
<tr class="even">
<td><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Porta do cliente<br/></td>
<td>O número da porta do cliente afetado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Endereço IP do servidor<br/></td>
<td>O endereço IP do servidor afetado que pode ser um endereço IPv4 ou um endereço IPv6. Se o endereço IP do servidor for um endereço IPv6, o campo Identificação_do_escopo também será incluído no endereço.<br/></td>
</tr>
<tr class="even">
<td><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Porta do servidor<br/></td>
<td>O número da porta do servidor afetado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Versão do protocolo<br/></td>
<td>A versão do protocolo que está sendo usado. <br/>
<ul>
<li>Se a conexão não tiver sido analisada o suficiente para determinar a versão do protocolo, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.</li>
<li>Se o número de versão principal ou secundária analisado for maior ou igual a 10, a versão será registrada como &quot; http/?.? &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo<br/></td>
<td>O estado do verbo passado pela última solicitação analisada. Verbos desconhecidos são incluídos, mas qualquer verbo que tenha mais de 255 bytes é truncado para esse comprimento. Se um verbo não estiver disponível, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.<br/></td>
</tr>
<tr class="odd">
<td><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + consulta<br/></td>
<td>A URL e qualquer consulta associada a ela são registradas como um campo, separados por um ponto de interrogação (0x3F). Este campo está truncado em seu limite de comprimento de 4096 bytes.
<ul>
<li>Se essa URL tiver sido analisada ( &quot; cooked &quot; ), ela será registrada com conversão de página de código local e será tratada como um campo Unicode.</li>
<li>Se essa URL não tiver sido analisada ( &quot; cooked &quot; ) no momento do registro em log, ela será exatamente copiada, sem nenhuma conversão Unicode.</li>
<li>Se a API do servidor HTTP não puder analisar essa URL, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Status do protocolo<br/></td>
<td>O status do protocolo não pode exceder 999. <br/>
<ul>
<li>Se o status do protocolo da resposta a uma solicitação estiver disponível, ele será registrado nesse campo.</li>
<li>Se o status do protocolo não estiver disponível, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId<br/></td>
<td>Não é usado nesta versão da API do servidor HTTP. Um hífen de espaço reservado (0x002D) sempre aparece nesse campo.<br/></td>
</tr>
<tr class="even">
<td><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Frase do motivo<br/></td>
<td>Este campo contém uma cadeia de caracteres que identifica o tipo de erro que está sendo registrado. Ele nunca é deixado vazio.<br/></td>
</tr>
</tbody>
</table>



 

As seguintes linhas de exemplo são de um log de erros da API do servidor HTTP:

``` syntax
2002-07-05 18:45:09 172.31.77.6 2094 172.31.77.6 80 
                    HTTP/1.1 GET /qos/1kbfile.txt 503 - ConnLimit
2002-07-05 19:51:59 127.0.0.1 2780 127.0.0.1 80 
                    HTTP/1.1 GET /ThisIsMyUrl.htm 400 - Hostname
2002-07-05 19:53:00 127.0.0.1 2894 127.0.0.1 80 
                    HTTP/2.0 GET / 505 - Version_N/S
2002-07-05 20:06:01 172.31.77.6 64388 127.0.0.1 80 
                    - - - - - Timer_MinBytesPerSecond
```

 

 





