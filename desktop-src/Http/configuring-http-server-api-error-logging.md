---
title: Configurando o log de erros da API do servidor HTTP
description: O log de erros da API do Servidor HTTP é controlado por três valores do Registro em uma chave \\ parâmetros HTTP.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API do Servidor HTTP, configurando logs de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10479a1b2bd1ebf559213b6cd4b738f6c0b9ea63c142edcce3c10f64f877dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950885"
---
# <a name="configuring-http-server-api-error-logging"></a>Configurando o log de erros da API do servidor HTTP

O log de erros da API do Servidor HTTP é controlado por três valores do Registro em uma **chave** \\ **parâmetros** HTTP localizada em:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> O local e a forma dos valores de configuração podem mudar em versões futuras do Windows operacional.

 

Um usuário deve ter privilégios de Administrador/Sistema Local para modificar os valores do Registro e exibir ou modificar os arquivos de log e a pasta que os contém.

As informações de configuração nos valores do Registro são lidas quando o driver de API do servidor HTTP é iniciado. Como resultado, se as configurações são alteradas, o driver deve ser interrompido e reiniciado para ler os novos valores. Isso pode ser feito usando os seguintes comandos de console:

**net stop http**

**net start http**

Os arquivos de log são nomeados usando a seguinte convenção:

**httperr +** *SequenceNumber* **+ .log**

Por exemplo: "httperr4.log".

Os arquivos de log são ciclodos quando atingem o tamanho máximo especificado pelo valor do Registro **ErrorLogFileTruncateSize** e o valor não pode ser menor que um MB (megabyte).

Se a configuração do log de erros for inválida ou qualquer tipo de falha ocorrer durante a escrita nos arquivos de log, a API do Servidor HTTP usará o log de eventos para notificar os administradores de que o log de erros não ocorreu.

Os valores de configuração do Registro são descritos na tabela a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor do Registro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging<br/></td>
<td>Um <strong>DWORD que</strong> pode ser definido como <strong>TRUE</strong> para habilitar o log de erros ou <strong>FALSE</strong> para desabilitá-lo. O valor padrão é <strong>TRUE.</strong><br/></td>
</tr>
<tr class="even">
<td><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize<br/></td>
<td>Um <strong>DWORD</strong> que especifica o tamanho máximo de um arquivo de log de erros, em bytes. O valor padrão é um MB (0x100000).<br/>
<blockquote>
[!Note]<br />
O valor especificado não pode ser menor que o valor padrão.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir<br/></td>
<td>Uma <strong>Cadeia de</strong> caracteres que especifica a pasta na qual a API do Servidor HTTP coloca seus arquivos de log. <br/> A API do Servidor HTTP cria uma subpasta chamada HTTPERR na pasta especificada na &quot; qual os arquivos de log são &quot; colocados. Essa subpasta e os arquivos de log recebem as mesmas configurações de permissão, o que significa que as Contas de Sistema Local e Administrador têm acesso completo, enquanto outros usuários não têm acesso.<br/> Se uma pasta não for especificada no Registro, a pasta padrão será a seguinte:<br/> &quot;%SystemRoot%\System32\LogFiles&quot;<br/>
<blockquote>
[!Note]<br />
O valor da cadeia de caracteres ErrorLoggingDir deve ser um caminho totalmente qualificado, mas pode conter &quot; %SystemRoot%. &quot;
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





