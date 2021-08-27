---
title: Formato dos logs de erro da API do servidor HTTP
description: Em geral, os arquivos de log de erros da API do Servidor HTTP têm o mesmo formato que os logs de erro do W3C, exceto que os arquivos de log de erros da API do Servidor HTTP não contêm cabeçalhos de coluna.
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- API do Servidor HTTP, formato de log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e666e29178695482b05cfef6bdd252fb35072b7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477772"
---
# <a name="format-of-the-http-server-api-error-logs"></a>Formato dos logs de erro da API do servidor HTTP

Em geral, os arquivos de log de erros da API do Servidor HTTP têm o mesmo formato que os logs de erro do W3C, exceto que os arquivos de log de erros da API do Servidor HTTP não contêm cabeçalhos de coluna. Cada linha de um log de erros da API do Servidor HTTP registra um erro com campos em uma ordem específica. Cada campo é separado do campo anterior por um único caractere de espaço (0x0020). Em cada campo, caracteres de espaço, guias e caracteres de controle não imprimíveis são substituídos por sinais de a mais (0x002B).

A tabela a seguir identifica os campos e a ordem dos campos em um registro de log de erros.




| Campo | Descrição | 
|-------|-------------|
| <span id="Date"></span><span id="date"></span><span id="DATE"></span>Data<br /> | O campo Data segue o formato W3C e é baseado Tempo Universal Coordenado (UTC). O campo Data sempre tem 10 caracteres na forma de "AAAA-MM-DD". Por exemplo, 1º de maio de 2003 é expresso como "2003-05-01".<br /> | 
| <span id="Time"></span><span id="time"></span><span id="TIME"></span>Tempo<br /> | O campo Hora segue o formato W3C e é baseado em UTC. O campo de hora sempre tem 8 caracteres na forma de "MM:HH:SS". Por exemplo, 17h30 (UTC) é expresso como "17:30:00".<br /> | 
| <span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Endereço IP do cliente<br /> | O endereço IP do cliente afetado que pode ser um endereço IPv4 ou um endereço IPv6. Se o endereço IP do cliente for um endereço IPv6, o campo ScopeId também será incluído no endereço.<br /> | 
| <span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Porta do cliente<br /> | O número da porta para o cliente afetado.<br /> | 
| <span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Endereço IP do servidor<br /> | O endereço IP do servidor afetado que pode ser um endereço IPv4 ou um endereço IPv6. Se o endereço IP do servidor for um endereço IPv6, o campo ScopeId também será incluído no endereço.<br /> | 
| <span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Porta do servidor<br /> | O número da porta do servidor afetado.<br /> | 
| <span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Versão do protocolo<br /> | A versão do protocolo que está sendo usado. <br /><ul><li>Se a conexão não tiver sido analisado o suficiente para determinar a versão do protocolo, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.</li><li>Se o número de versão principal ou secundário analisado for maior ou igual a 10, a versão será registrada como "HTTP/?.?".</li></ul> | 
| <span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo<br /> | O estado do verbo passado pela última solicitação analisado. Verbos desconhecidos são incluídos, mas qualquer verbo com mais de 255 bytes é truncado para esse comprimento. Se um verbo não estiver disponível, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.<br /> | 
| <span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + Consulta<br /> | A URL e qualquer consulta associada a ela são registradas como um campo, separados por um ponto de interrogação (0x3F). Esse campo é truncado em seu limite de comprimento de 4.096 bytes.<ul><li>Se essa URL tiver sido analisado ("cozida"), ela será registrada com a conversão de página de código local e será tratada como um campo Unicode.</li><li>Se essa URL não tiver sido analisado ("cozida") no momento do registro em log, ela será copiada exatamente, sem nenhuma conversão Unicode.</li><li>Se a API do Servidor HTTP não puder analisar essa URL, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.</li></ul><br /> | 
| <span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Status do protocolo<br /> | O status do protocolo não pode exceder 999. <br /><ul><li>Se o status do protocolo da resposta a uma solicitação estiver disponível, ele será registrado neste campo.</li><li>Se o status do protocolo não estiver disponível, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.</li></ul> | 
| <span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>Siteid<br /> | Não usado nesta versão da API do Servidor HTTP. Um hífen de espaço reservado (0x002D) sempre aparece nesse campo.<br /> | 
| <span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Frase de motivo<br /> | Esse campo contém uma cadeia de caracteres que identifica o tipo de erro que está sendo registrado. Ele nunca é deixado vazio.<br /> | 




 

As linhas de exemplo a seguir são de um log de erros da API do Servidor HTTP:

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

 

 





