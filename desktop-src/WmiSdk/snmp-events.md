---
description: O provedor SNMP dá suporte à gravação em arquivos de log e ao depurador.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b133d2fc81c76949439b3e1f26d1fc448f0b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749879"
---
# <a name="snmp-events"></a><span data-ttu-id="0ae47-103">Eventos SNMP</span><span class="sxs-lookup"><span data-stu-id="0ae47-103">SNMP Events</span></span>

<span data-ttu-id="0ae47-104">O provedor SNMP dá suporte à gravação em arquivos de log e ao depurador.</span><span class="sxs-lookup"><span data-stu-id="0ae47-104">The SNMP provider supports writing to log files and to the debugger.</span></span>

> [!Note]  
> <span data-ttu-id="0ae47-105">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="0ae47-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="0ae47-106">Várias chaves e valores do registro definem o nível e o tipo de log que está sendo gerado no momento:</span><span class="sxs-lookup"><span data-stu-id="0ae47-106">A number of registry keys and values define the level and type of logging currently being generated:</span></span>

-   <span data-ttu-id="0ae47-107">Depuração</span><span class="sxs-lookup"><span data-stu-id="0ae47-107">Debugging</span></span>

    <span data-ttu-id="0ae47-108">A chave de registro de **log do hKey \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ Providers \\** contém o valor de log que indica se as informações podem ser gravadas no depurador.</span><span class="sxs-lookup"><span data-stu-id="0ae47-108">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING** registry key contains the logging value that indicates whether information can be written to the debugger.</span></span> <span data-ttu-id="0ae47-109">O valor de log é definido como 0 para desabilitar a saída de depuração ou 1 para habilitá-la.</span><span class="sxs-lookup"><span data-stu-id="0ae47-109">The logging value is set either to 0 to disable debugging output or 1 to enable it.</span></span> <span data-ttu-id="0ae47-110">Logging é um valor de REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="0ae47-110">Logging is a REG\_DWORD value.</span></span>

-   <span data-ttu-id="0ae47-111">Log</span><span class="sxs-lookup"><span data-stu-id="0ae47-111">Logging</span></span>

    <span data-ttu-id="0ae47-112">A chave de registro **HKEY \_ local \_ \\ software \\ Microsoft \\ WBEM \\ Providers \\ Logging \\ WBEMSNMP** mantém todas as informações de log específicas para o provedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="0ae47-112">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING\\WBEMSNMP** registry key holds all of the logging information specific to the SNMP provider.</span></span> <span data-ttu-id="0ae47-113">A tabela a seguir lista os valores associados a essa chave.</span><span class="sxs-lookup"><span data-stu-id="0ae47-113">The following table lists the values associated with this key.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ae47-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0ae47-114">Value</span></span></th>
<th><span data-ttu-id="0ae47-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ae47-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ae47-116">Type</span><span class="sxs-lookup"><span data-stu-id="0ae47-116">Type</span></span></td>
<td><span data-ttu-id="0ae47-117"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="0ae47-117"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="0ae47-118">Usa um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="0ae47-118">Takes one of the following values:</span></span><br/> <span data-ttu-id="0ae47-119">&quot;File &quot; = (padrão) envia a saída de depuração para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0ae47-119">&quot;File&quot; = (Default) Sends debugging output to a file.</span></span><br/> <span data-ttu-id="0ae47-120">&quot;Debugger &quot; = envia a saída de depuração para o depurador.</span><span class="sxs-lookup"><span data-stu-id="0ae47-120">&quot;Debugger&quot; = Sends debugging output to the debugger.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ae47-121">MaxFileSize</span><span class="sxs-lookup"><span data-stu-id="0ae47-121">MaxFileSize</span></span></td>
<td><span data-ttu-id="0ae47-122"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="0ae47-122"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="0ae47-123">Obtém valores inteiros de 1024 a 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="0ae47-123">Takes integer values from 1024 to 2^32-1.</span></span> <span data-ttu-id="0ae47-124">O valor é o tamanho máximo permitido em bytes para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="0ae47-124">The value is the maximum allowed size in bytes for the log file.</span></span> <span data-ttu-id="0ae47-125">Se for menor que 1024, o mecanismo de registro em log usará um valor de 1024.</span><span class="sxs-lookup"><span data-stu-id="0ae47-125">If less than 1024, the logging mechanism uses a value of 1024.</span></span> <span data-ttu-id="0ae47-126">Um tamanho mínimo de 8 KB é recomendado para esse valor.</span><span class="sxs-lookup"><span data-stu-id="0ae47-126">A minimum size of 8 KB is recommended for this value.</span></span> <span data-ttu-id="0ae47-127">Quando o arquivo atinge o tamanho especificado por MaxFileSize, o nome do arquivo é anexado com um caractere ' ~ ' e um novo arquivo é criado.</span><span class="sxs-lookup"><span data-stu-id="0ae47-127">When the file reaches the size specified by MaxFileSize, the file name is prepended with a '~' character and a new file is created.</span></span> <span data-ttu-id="0ae47-128">Portanto, o espaço em disco máximo necessário para o registro em log é o dobro desse valor.</span><span class="sxs-lookup"><span data-stu-id="0ae47-128">Therefore, the maximum disk space required for logging is twice this value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ae47-129">Arquivo</span><span class="sxs-lookup"><span data-stu-id="0ae47-129">File</span></span></td>
<td><span data-ttu-id="0ae47-130"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="0ae47-130"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="0ae47-131">Define o nome do arquivo para o qual a saída de depuração é enviada quando o tipo de log é definido como ' file '.</span><span class="sxs-lookup"><span data-stu-id="0ae47-131">Defines the name of the file to which the debugging output is sent when the logging type is set to 'File'.</span></span> <span data-ttu-id="0ae47-132">O valor padrão é ' <WBEMLOGS> \wbemsnmp.log. '</span><span class="sxs-lookup"><span data-stu-id="0ae47-132">The default value is '<WBEMLOGS>\wbemsnmp.log.'</span></span> <span data-ttu-id="0ae47-133">Se o <WBEMLOGS> diretório não puder ser determinado na seção do registro WMI, o valor padrão será ' c:\wbemsnmp.log '.</span><span class="sxs-lookup"><span data-stu-id="0ae47-133">If the <WBEMLOGS> directory cannot be determined from the WMI registry section, the value defaults to 'c:\wbemsnmp.log'.</span></span> <span data-ttu-id="0ae47-134">Se um compartilhamento for usado, como \\ machine\share\wbemsnmp.log ou M:\wbemsnmp.log, em que M: é \\ machine\share, a conta do sistema local na qual o WMI é executado deve ter direitos de acesso de leitura/gravação para o \\ machine\share.</span><span class="sxs-lookup"><span data-stu-id="0ae47-134">If a share is used, such as \\machine\share\wbemsnmp.log or M:\wbemsnmp.log where M: is \\machine\share, the local SYSTEM account on which WMI runs must have read/write access rights to the \\machine\share.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ae47-135">Nível</span><span class="sxs-lookup"><span data-stu-id="0ae47-135">Level</span></span></td>
<td><span data-ttu-id="0ae47-136"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="0ae47-136"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="0ae47-137">Obtém valores inteiros de 0 a 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="0ae47-137">Takes integer values from 0 through 2^32-1.</span></span> <span data-ttu-id="0ae47-138">O valor é uma máscara lógica que consiste em 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0ae47-138">The value is a logical mask consisting of 32 bits.</span></span> <span data-ttu-id="0ae47-139">As seguintes máscaras de bits são combinadas para definir o tipo de saída de depuração gerada:</span><span class="sxs-lookup"><span data-stu-id="0ae47-139">The following bit masks are combined to define the type of debugging output generated:</span></span><br/>
<ul>
<li><span data-ttu-id="0ae47-140">0: invocações do método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> do provedor de classe SNMP</span><span class="sxs-lookup"><span data-stu-id="0ae47-140">0: SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="0ae47-141">1: implementação do provedor de classe SNMP</span><span class="sxs-lookup"><span data-stu-id="0ae47-141">1: SNMP class provider implementation</span></span></li>
<li><span data-ttu-id="0ae47-142">2: invocações do método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> do provedor de instância SNMP</span><span class="sxs-lookup"><span data-stu-id="0ae47-142">2: SNMP instance provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="0ae47-143">3: implementação do provedor de instância SNMP</span><span class="sxs-lookup"><span data-stu-id="0ae47-143">3: SNMP instance provider implementation</span></span></li>
<li><span data-ttu-id="0ae47-144">4: biblioteca de classes SNMP</span><span class="sxs-lookup"><span data-stu-id="0ae47-144">4: SNMP class library</span></span></li>
<li><span data-ttu-id="0ae47-145">5: SNMP SMIR</span><span class="sxs-lookup"><span data-stu-id="0ae47-145">5: SNMP SMIR</span></span></li>
<li><span data-ttu-id="0ae47-146">6: correlator SNMP</span><span class="sxs-lookup"><span data-stu-id="0ae47-146">6: SNMP correlator</span></span></li>
<li><span data-ttu-id="0ae47-147">7: código de mapeamento de tipo SNMP</span><span class="sxs-lookup"><span data-stu-id="0ae47-147">7: SNMP type mapping code</span></span></li>
<li><span data-ttu-id="0ae47-148">8: código de Threading SNMP</span><span class="sxs-lookup"><span data-stu-id="0ae47-148">8: SNMP threading code</span></span></li>
<li><span data-ttu-id="0ae47-149">9: interfaces e implementação do provedor de eventos SNMP</span><span class="sxs-lookup"><span data-stu-id="0ae47-149">9: SNMP event provider interfaces and implementation</span></span></li>
</ul>
<span data-ttu-id="0ae47-150">Defina nível como (2 ^ 0 + 2 ^ 8 =) 257 para operações envolvendo chamadas para os métodos de <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> do provedor de classe SNMP e operações usando o código de Threading SNMP.</span><span class="sxs-lookup"><span data-stu-id="0ae47-150">Set Level to (2^0 + 2^8=) 257 for operations involving calls to the SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> methods, and operations using SNMP threading code.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




