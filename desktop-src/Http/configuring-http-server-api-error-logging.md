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
# <a name="configuring-http-server-api-error-logging"></a><span data-ttu-id="9a8b9-104">Configurando log de erros da API do servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="9a8b9-104">Configuring HTTP Server API Error Logging</span></span>

<span data-ttu-id="9a8b9-105">O log de erros da API do servidor http é controlado por três valores de registro em uma chave de \\ **parâmetros** http localizada em:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-105">The HTTP Server API error logging is controlled by three registry values under an **HTTP**\\**Parameters** key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> <span data-ttu-id="9a8b9-106">O local e a forma dos valores de configuração podem ser alterados em versões futuras do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-106">The location and form of the configuration values may change in future versions of the Windows operating system.</span></span>

 

<span data-ttu-id="9a8b9-107">Um usuário deve ter privilégios de administrador/sistema local para modificar os valores do registro e exibir ou modificar os arquivos de log e a pasta que os contém.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-107">A user must have Administrator/Local System privileges to modify the registry values, and view or modify the log files and the folder that contains them.</span></span>

<span data-ttu-id="9a8b9-108">As informações de configuração nos valores do registro são lidas quando o driver da API do servidor HTTP é iniciado.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-108">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="9a8b9-109">Como resultado, se as configurações forem alteradas, o driver deverá ser interrompido e reiniciado para ler os novos valores.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-109">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="9a8b9-110">Isso pode ser feito usando os seguintes comandos de console:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-110">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="9a8b9-111">**net stop http**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-111">**net stop http**</span></span>

<span data-ttu-id="9a8b9-112">**net start http**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-112">**net start http**</span></span>

<span data-ttu-id="9a8b9-113">Os arquivos de log são nomeados usando a seguinte convenção:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-113">The log files are named by using the following convention:</span></span>

<span data-ttu-id="9a8b9-114">**Httperr +** *SequenceNumber* **+. log**</span><span class="sxs-lookup"><span data-stu-id="9a8b9-114">**httperr +** *SequenceNumber* **+ .log**</span></span>

<span data-ttu-id="9a8b9-115">Por exemplo: "httperr4. log".</span><span class="sxs-lookup"><span data-stu-id="9a8b9-115">For example: "httperr4.log".</span></span>

<span data-ttu-id="9a8b9-116">Os arquivos de log são alternados quando atingem o tamanho máximo especificado pelo valor do registro **ErrorLogFileTruncateSize** e o valor não pode ser inferior a um megabyte (MB).</span><span class="sxs-lookup"><span data-stu-id="9a8b9-116">Log files are cycled when they reach the maximum size specified by the **ErrorLogFileTruncateSize** registry value, and the value cannot be less than one megabyte (MB).</span></span>

<span data-ttu-id="9a8b9-117">Se a configuração do log de erros for inválida ou algum tipo de falha ocorrer durante a gravação nos arquivos de log, a API do servidor HTTP usará o log de eventos para notificar os administradores de que o log de erros não ocorreu.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-117">If the configuration of error logging is invalid or any kind of failure occurs while writing to the log files, the HTTP Server API uses event logging to notify administrators that error logging did not take place.</span></span>

<span data-ttu-id="9a8b9-118">Os valores de configuração do registro são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-118">Registry configuration values are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a8b9-119">Valor do registro</span><span class="sxs-lookup"><span data-stu-id="9a8b9-119">Registry Value</span></span></th>
<th><span data-ttu-id="9a8b9-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a8b9-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a8b9-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span><span class="sxs-lookup"><span data-stu-id="9a8b9-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span></span><br/></td>
<td><span data-ttu-id="9a8b9-122">Um <strong>DWORD</strong> que pode ser definido como <strong>true</strong> para habilitar o log de erros ou <strong>false</strong> para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-122">A <strong>DWORD</strong> that can be set to <strong>TRUE</strong> to enable error logging, or <strong>FALSE</strong> to disable it.</span></span> <span data-ttu-id="9a8b9-123">O valor padrão é <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-123">The default value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a8b9-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span><span class="sxs-lookup"><span data-stu-id="9a8b9-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span></span><br/></td>
<td><span data-ttu-id="9a8b9-125">Um <strong>DWORD</strong> que especifica o tamanho máximo de um arquivo de log de erros, em bytes.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-125">A <strong>DWORD</strong> that specifies the maximum size of an error log file, in bytes.</span></span> <span data-ttu-id="9a8b9-126">O valor padrão é 1 MB (0x100000).</span><span class="sxs-lookup"><span data-stu-id="9a8b9-126">The default value is one MB (0x100000).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9a8b9-127">O valor especificado não pode ser menor que o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-127">The specified value cannot be smaller than the default value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a8b9-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span><span class="sxs-lookup"><span data-stu-id="9a8b9-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span></span><br/></td>
<td><span data-ttu-id="9a8b9-129">Uma <strong>cadeia de caracteres</strong> que especifica a pasta sob a qual a API do servidor http coloca seus arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-129">A <strong>String</strong> that specifies the folder under which the HTTP Server API places its logging files.</span></span> <br/> <span data-ttu-id="9a8b9-130">A API do servidor HTTP cria uma subpasta chamada &quot; Httperr &quot; na pasta especificada na qual os arquivos de log são colocados.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-130">The HTTP Server API creates a subfolder named &quot;HTTPERR&quot; under the specified folder into which the log files are placed.</span></span> <span data-ttu-id="9a8b9-131">Essa subpasta e os arquivos de log recebem as mesmas configurações de permissão, o que significa que as contas de administrador e sistema local têm acesso completo, enquanto outros usuários não têm acesso.</span><span class="sxs-lookup"><span data-stu-id="9a8b9-131">This subfolder and the log files receive the same permission settings, which means that Administrator and Local System Accounts have full access, while other users do not have access.</span></span><br/> <span data-ttu-id="9a8b9-132">Se uma pasta não for especificada no registro, a pasta padrão será a seguinte:</span><span class="sxs-lookup"><span data-stu-id="9a8b9-132">If a folder is not specified in the registry, the default folder is the following:</span></span><br/> <span data-ttu-id="9a8b9-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span><span class="sxs-lookup"><span data-stu-id="9a8b9-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9a8b9-134">O valor da cadeia de caracteres ErrorLoggingDir deve ser um caminho totalmente qualificado, mas pode conter &quot; % systemroot% &quot; .</span><span class="sxs-lookup"><span data-stu-id="9a8b9-134">The ErrorLoggingDir string value must be a fully qualified path, but it can contain &quot;%SystemRoot%&quot;.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





