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
# <a name="format-of-the-http-server-api-error-logs"></a><span data-ttu-id="9564e-104">Formato dos logs de erro da API do servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="9564e-104">Format of the HTTP Server API Error Logs</span></span>

<span data-ttu-id="9564e-105">Em geral, os arquivos de log de erros da API do servidor HTTP têm o mesmo formato que os logs de erros do W3C, exceto que os arquivos de log de erros da API do servidor HTTP não contêm cabeçalhos de coluna.</span><span class="sxs-lookup"><span data-stu-id="9564e-105">In general, HTTP Server API error log files have the same format as W3C error logs except that HTTP Server API error log files do not contain column headings.</span></span> <span data-ttu-id="9564e-106">Cada linha de um log de erros da API do servidor HTTP registra um erro com campos em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="9564e-106">Each line of an HTTP Server API error log records one error with fields in a specific order.</span></span> <span data-ttu-id="9564e-107">Cada campo é separado do campo anterior por um caractere de espaço único (0x0020).</span><span class="sxs-lookup"><span data-stu-id="9564e-107">Each field is separated from the preceding field by a single space character (0x0020).</span></span> <span data-ttu-id="9564e-108">Dentro de cada campo, caracteres de espaço, tabulações e caracteres de controle não imprimíveis são substituídos por sinais de adição (0x002B).</span><span class="sxs-lookup"><span data-stu-id="9564e-108">Within each field, space characters, tabs, and unprintable control characters are replaced by plus signs (0x002B).</span></span>

<span data-ttu-id="9564e-109">A tabela a seguir identifica os campos e a ordem dos campos em um registro de log de erros.</span><span class="sxs-lookup"><span data-stu-id="9564e-109">The following table identifies the fields and the order of the fields in an error log record.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9564e-110">Campo</span><span class="sxs-lookup"><span data-stu-id="9564e-110">Field</span></span></th>
<th><span data-ttu-id="9564e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9564e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9564e-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date</span><span class="sxs-lookup"><span data-stu-id="9564e-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date</span></span><br/></td>
<td><span data-ttu-id="9564e-113">O campo de data segue o formato W3C e é baseado em UTC (tempo Universal Coordenado). O campo de data sempre é 10 caracteres no formato &quot; aaaa-mm-dd &quot; .</span><span class="sxs-lookup"><span data-stu-id="9564e-113">The Date field follows the W3C format and is based on Coordinated Universal Time (UTC).The Date field is always 10 characters in the form of &quot;YYYY-MM-DD&quot;.</span></span> <span data-ttu-id="9564e-114">Por exemplo, 1 de maio de 2003 é expresso como &quot; 2003-05-01 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9564e-114">For example, May 1, 2003 is expressed as &quot;2003-05-01&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9564e-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Momento</span><span class="sxs-lookup"><span data-stu-id="9564e-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Time</span></span><br/></td>
<td><span data-ttu-id="9564e-116">O campo hora segue o formato W3C e é baseado em UTC.</span><span class="sxs-lookup"><span data-stu-id="9564e-116">The Time field follows the W3C format and is based on UTC.</span></span> <span data-ttu-id="9564e-117">O campo de tempo sempre tem 8 caracteres no formato &quot; mm: hh: SS &quot; .</span><span class="sxs-lookup"><span data-stu-id="9564e-117">The time field is always 8 characters in the form of &quot;MM:HH:SS&quot;.</span></span> <span data-ttu-id="9564e-118">Por exemplo, 5:30 PM (UTC) é expresso como &quot; 17:30:00 &quot; .</span><span class="sxs-lookup"><span data-stu-id="9564e-118">For example, 5:30 PM (UTC) is expressed as &quot;17:30:00&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9564e-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Endereço IP do cliente</span><span class="sxs-lookup"><span data-stu-id="9564e-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Client IP Address</span></span><br/></td>
<td><span data-ttu-id="9564e-120">O endereço IP do cliente afetado que pode ser um endereço IPv4 ou um endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="9564e-120">The IP address of the affected client that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="9564e-121">Se o endereço IP do cliente for um endereço IPv6, o campo Identificação_do_escopo também será incluído no endereço.</span><span class="sxs-lookup"><span data-stu-id="9564e-121">If the client IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9564e-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Porta do cliente</span><span class="sxs-lookup"><span data-stu-id="9564e-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Client Port</span></span><br/></td>
<td><span data-ttu-id="9564e-123">O número da porta do cliente afetado.</span><span class="sxs-lookup"><span data-stu-id="9564e-123">The port number for the affected client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9564e-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Endereço IP do servidor</span><span class="sxs-lookup"><span data-stu-id="9564e-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Server IP Address</span></span><br/></td>
<td><span data-ttu-id="9564e-125">O endereço IP do servidor afetado que pode ser um endereço IPv4 ou um endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="9564e-125">The IP address of the affected server that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="9564e-126">Se o endereço IP do servidor for um endereço IPv6, o campo Identificação_do_escopo também será incluído no endereço.</span><span class="sxs-lookup"><span data-stu-id="9564e-126">If the server IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9564e-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Porta do servidor</span><span class="sxs-lookup"><span data-stu-id="9564e-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Server Port</span></span><br/></td>
<td><span data-ttu-id="9564e-128">O número da porta do servidor afetado.</span><span class="sxs-lookup"><span data-stu-id="9564e-128">The port number of the affected server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9564e-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Versão do protocolo</span><span class="sxs-lookup"><span data-stu-id="9564e-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Protocol Version</span></span><br/></td>
<td><span data-ttu-id="9564e-130">A versão do protocolo que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="9564e-130">The version of the protocol that is being used.</span></span> <br/>
<ul>
<li><span data-ttu-id="9564e-131">Se a conexão não tiver sido analisada o suficiente para determinar a versão do protocolo, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.</span><span class="sxs-lookup"><span data-stu-id="9564e-131">If the connection has not been parsed enough to determine the protocol version, then a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
<li><span data-ttu-id="9564e-132">Se o número de versão principal ou secundária analisado for maior ou igual a 10, a versão será registrada como &quot; http/?.? &quot; .</span><span class="sxs-lookup"><span data-stu-id="9564e-132">If either the major or minor version number parsed is greater than or equal to 10, the version is logged as &quot;HTTP/?.?&quot;.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9564e-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo</span><span class="sxs-lookup"><span data-stu-id="9564e-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span><br/></td>
<td><span data-ttu-id="9564e-134">O estado do verbo passado pela última solicitação analisada.</span><span class="sxs-lookup"><span data-stu-id="9564e-134">The verb state passed by the last request parsed.</span></span> <span data-ttu-id="9564e-135">Verbos desconhecidos são incluídos, mas qualquer verbo que tenha mais de 255 bytes é truncado para esse comprimento.</span><span class="sxs-lookup"><span data-stu-id="9564e-135">Unknown verbs are included, but any verb that is more than 255 bytes is truncated to this length.</span></span> <span data-ttu-id="9564e-136">Se um verbo não estiver disponível, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.</span><span class="sxs-lookup"><span data-stu-id="9564e-136">If a verb is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9564e-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + consulta</span><span class="sxs-lookup"><span data-stu-id="9564e-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + Query</span></span><br/></td>
<td><span data-ttu-id="9564e-138">A URL e qualquer consulta associada a ela são registradas como um campo, separados por um ponto de interrogação (0x3F).</span><span class="sxs-lookup"><span data-stu-id="9564e-138">The URL and any query associated with it are logged as one field, separated by a question mark (0x3F).</span></span> <span data-ttu-id="9564e-139">Este campo está truncado em seu limite de comprimento de 4096 bytes.</span><span class="sxs-lookup"><span data-stu-id="9564e-139">This field is truncated at its length limit of 4096 bytes.</span></span>
<ul>
<li><span data-ttu-id="9564e-140">Se essa URL tiver sido analisada ( &quot; cooked &quot; ), ela será registrada com conversão de página de código local e será tratada como um campo Unicode.</span><span class="sxs-lookup"><span data-stu-id="9564e-140">If this URL has been parsed (&quot;cooked&quot;), it is logged with local code page conversion, and is treated as a Unicode field.</span></span></li>
<li><span data-ttu-id="9564e-141">Se essa URL não tiver sido analisada ( &quot; cooked &quot; ) no momento do registro em log, ela será exatamente copiada, sem nenhuma conversão Unicode.</span><span class="sxs-lookup"><span data-stu-id="9564e-141">If this URL has not been parsed (&quot;cooked&quot;) at the time of logging, it is copied exactly, without any Unicode conversion.</span></span></li>
<li><span data-ttu-id="9564e-142">Se a API do servidor HTTP não puder analisar essa URL, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.</span><span class="sxs-lookup"><span data-stu-id="9564e-142">If the HTTP Server API cannot parse this URL, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9564e-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Status do protocolo</span><span class="sxs-lookup"><span data-stu-id="9564e-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Protocol Status</span></span><br/></td>
<td><span data-ttu-id="9564e-144">O status do protocolo não pode exceder 999.</span><span class="sxs-lookup"><span data-stu-id="9564e-144">The protocol status cannot exceed 999.</span></span> <br/>
<ul>
<li><span data-ttu-id="9564e-145">Se o status do protocolo da resposta a uma solicitação estiver disponível, ele será registrado nesse campo.</span><span class="sxs-lookup"><span data-stu-id="9564e-145">If the protocol status of the response to a request is available, it is logged in this field.</span></span></li>
<li><span data-ttu-id="9564e-146">Se o status do protocolo não estiver disponível, um hífen (0x002D) será usado como um espaço reservado para o campo vazio.</span><span class="sxs-lookup"><span data-stu-id="9564e-146">If the protocol status is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9564e-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span><span class="sxs-lookup"><span data-stu-id="9564e-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span></span><br/></td>
<td><span data-ttu-id="9564e-148">Não é usado nesta versão da API do servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="9564e-148">Not used in this version of the HTTP Server API.</span></span> <span data-ttu-id="9564e-149">Um hífen de espaço reservado (0x002D) sempre aparece nesse campo.</span><span class="sxs-lookup"><span data-stu-id="9564e-149">A placeholder hyphen (0x002D) always appears in this field.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9564e-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Frase do motivo</span><span class="sxs-lookup"><span data-stu-id="9564e-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Reason Phrase</span></span><br/></td>
<td><span data-ttu-id="9564e-151">Este campo contém uma cadeia de caracteres que identifica o tipo de erro que está sendo registrado.</span><span class="sxs-lookup"><span data-stu-id="9564e-151">This field contains a string that identifies the kind of error that is being logged.</span></span> <span data-ttu-id="9564e-152">Ele nunca é deixado vazio.</span><span class="sxs-lookup"><span data-stu-id="9564e-152">It is never left empty.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9564e-153">As seguintes linhas de exemplo são de um log de erros da API do servidor HTTP:</span><span class="sxs-lookup"><span data-stu-id="9564e-153">The following sample lines are from an HTTP Server API error log:</span></span>

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

 

 





