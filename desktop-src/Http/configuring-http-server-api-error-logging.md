---
title: Configurando log de erros da API do servidor HTTP
description: O log de erros da API do servidor HTTP é controlado por três valores de registro em uma \\ chave de parâmetros http.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API do servidor HTTP, configurando logs de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f6b5ae81b1933ea745789e0fae33dfc7ebce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363974"
---
# <a name="configuring-http-server-api-error-logging"></a>Configurando log de erros da API do servidor HTTP

O log de erros da API do servidor http é controlado por três valores de registro em uma chave de \\ **parâmetros** http localizada em:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> O local e a forma dos valores de configuração podem ser alterados em versões futuras do sistema operacional Windows.

 

Um usuário deve ter privilégios de administrador/sistema local para modificar os valores do registro e exibir ou modificar os arquivos de log e a pasta que os contém.

As informações de configuração nos valores do registro são lidas quando o driver da API do servidor HTTP é iniciado. Como resultado, se as configurações forem alteradas, o driver deverá ser interrompido e reiniciado para ler os novos valores. Isso pode ser feito usando os seguintes comandos de console:

**net stop http**

**net start http**

Os arquivos de log são nomeados usando a seguinte convenção:

**Httperr +** *SequenceNumber* **+. log**

Por exemplo: "httperr4. log".

Os arquivos de log são alternados quando atingem o tamanho máximo especificado pelo valor do registro **ErrorLogFileTruncateSize** e o valor não pode ser inferior a um megabyte (MB).

Se a configuração do log de erros for inválida ou algum tipo de falha ocorrer durante a gravação nos arquivos de log, a API do servidor HTTP usará o log de eventos para notificar os administradores de que o log de erros não ocorreu.

Os valores de configuração do registro são descritos na tabela a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor do registro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging<br/></td>
<td>Um <strong>DWORD</strong> que pode ser definido como <strong>true</strong> para habilitar o log de erros ou <strong>false</strong> para desabilitá-lo. O valor padrão é <strong>true</strong>.<br/></td>
</tr>
<tr class="even">
<td><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize<br/></td>
<td>Um <strong>DWORD</strong> que especifica o tamanho máximo de um arquivo de log de erros, em bytes. O valor padrão é 1 MB (0x100000).<br/>
<blockquote>
[!Note]<br />
O valor especificado não pode ser menor que o valor padrão.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir<br/></td>
<td>Uma <strong>cadeia de caracteres</strong> que especifica a pasta sob a qual a API do servidor http coloca seus arquivos de log. <br/> A API do servidor HTTP cria uma subpasta chamada &quot; Httperr &quot; na pasta especificada na qual os arquivos de log são colocados. Essa subpasta e os arquivos de log recebem as mesmas configurações de permissão, o que significa que as contas de administrador e sistema local têm acesso completo, enquanto outros usuários não têm acesso.<br/> Se uma pasta não for especificada no registro, a pasta padrão será a seguinte:<br/> &quot;%SystemRoot%\System32\LogFiles&quot;<br/>
<blockquote>
[!Note]<br />
O valor da cadeia de caracteres ErrorLoggingDir deve ser um caminho totalmente qualificado, mas pode conter &quot; % systemroot% &quot; .
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





