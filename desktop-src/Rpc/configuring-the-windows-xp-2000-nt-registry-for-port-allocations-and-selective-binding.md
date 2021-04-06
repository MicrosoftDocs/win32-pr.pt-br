---
title: Configurando o registro para alocações de porta e Associação seletiva
description: A partir do Windows 2000, um utilitário no Windows Resource Kit chamado Rpccfg.exe deve ser usado para definir associações. Para obter mais informações, consulte o Windows Resource Kit para obter a versão apropriada do sistema operacional.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- Chamada de procedimento remoto RPC, tarefas, configurando o registro para alocações de porta e Associação seletiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef1749fab1beb8e637d208a7d7af64577066fe6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103917755"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a><span data-ttu-id="2b827-105">Configurando o registro para alocações de porta e Associação seletiva</span><span class="sxs-lookup"><span data-stu-id="2b827-105">Configuring the Registry for Port Allocations and Selective Binding</span></span>

<span data-ttu-id="2b827-106">A partir do Windows 2000, um utilitário no Windows Resource Kit chamado Rpccfg.exe deve ser usado para definir associações.</span><span class="sxs-lookup"><span data-stu-id="2b827-106">Starting with Windows 2000, a utility in the Windows Resource Kit called Rpccfg.exe should be used to set bindings.</span></span> <span data-ttu-id="2b827-107">Para obter mais informações, consulte o Windows Resource Kit para obter a versão apropriada do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2b827-107">For more information, consult the Windows Resource Kit for the appropriate operating system version.</span></span>

<span data-ttu-id="2b827-108">Para versões do Windows anteriores ao Windows 2000, as chaves do registro na tabela a seguir especificam os padrões do sistema para a alocação de porta dinâmica e para a associação a NICs em computadores de hospedagem múltipla.</span><span class="sxs-lookup"><span data-stu-id="2b827-108">For versions of windows prior to Windows 2000, the registry keys in the following table specify the system defaults for dynamic port allocation and for binding to NICs on multihomed computers.</span></span> <span data-ttu-id="2b827-109">Você deve primeiro criar essas chaves e, em seguida, especificar as configurações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2b827-109">You must first create these keys and then specify the appropriate settings.</span></span>

<span data-ttu-id="2b827-110">O uso da função [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) afeta essas configurações.</span><span class="sxs-lookup"><span data-stu-id="2b827-110">Using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function affects these settings.</span></span> <span data-ttu-id="2b827-111">Os desenvolvedores devem estar familiarizados com as configurações do registro explicadas nesta seção e a função **RpcServerUseProtseqEx** ao gerenciar as alocações de porta.</span><span class="sxs-lookup"><span data-stu-id="2b827-111">Developers should be familiar with the registry settings explained in this section and the **RpcServerUseProtseqEx** function when managing port allocations.</span></span> <span data-ttu-id="2b827-112">Um exemplo com três aplicativos hipotéticos segue a tabela abaixo e ilustra como essas configurações e a função **RpcServerUseProtseqEx** interoperam.</span><span class="sxs-lookup"><span data-stu-id="2b827-112">An example with three hypothetical applications follows the table below, and illustrates how these settings and the **RpcServerUseProtseqEx** function interoperate.</span></span>

<span data-ttu-id="2b827-113">Se uma chave estiver ausente ou se contiver um valor inválido, a configuração inteira será marcada como inválida e todas as chamadas de **RpcServerUseProtseq \*** sobre o IP [**\_ \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) ou [**ncadg \_ IP \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) falharão.</span><span class="sxs-lookup"><span data-stu-id="2b827-113">If a key is missing or if it contains an invalid value, the entire configuration is marked as invalid, and all **RpcServerUseProtseq\*** calls over [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) or [**ncadg\_ip\_udp**](/windows/desktop/Midl/ncadg-ip-udp) will fail.</span></span>

> [!Note]  
> <span data-ttu-id="2b827-114">As portas alocadas a um processo permanecem alocadas até que o processo seja desativado.</span><span class="sxs-lookup"><span data-stu-id="2b827-114">Ports allocated to a process remain allocated until that process dies.</span></span> <span data-ttu-id="2b827-115">Se todas as portas disponíveis estiverem em uso, a função retornará RPC \_ S para \_ fora \_ dos \_ recursos.</span><span class="sxs-lookup"><span data-stu-id="2b827-115">If all available ports are in use, the function returns RPC\_S\_OUT\_OF\_RESOURCES.</span></span>

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b827-116">Chave de porta</span><span class="sxs-lookup"><span data-stu-id="2b827-116">Port key</span></span></th>
<th><span data-ttu-id="2b827-117">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2b827-117">Data type</span></span></th>
<th><span data-ttu-id="2b827-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b827-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><span data-ttu-id="2b827-119"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="2b827-119"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="2b827-120">Especifica um conjunto de intervalos de portas IP que consistem em todas as portas disponíveis na Internet ou em todas as portas não disponíveis na Internet.</span><span class="sxs-lookup"><span data-stu-id="2b827-120">Specifies a set of IP port ranges consisting of either all the ports available from the Internet or all the ports not available from the Internet.</span></span> <span data-ttu-id="2b827-121">Cada cadeia de caracteres representa uma única porta ou um conjunto inclusivo de portas (por exemplo, 1000-1050, 1984).</span><span class="sxs-lookup"><span data-stu-id="2b827-121">Each string represents a single port or an inclusive set of ports (for example,1000-1050, 1984).</span></span> <span data-ttu-id="2b827-122">Se alguma entrada estiver fora do intervalo de 0 a 65535, ou se qualquer cadeia de caracteres não puder ser interpretada, o tempo de execução de RPC tratará toda a configuração como inválida.</span><span class="sxs-lookup"><span data-stu-id="2b827-122">If any entries are outside the range 0 to 65535, or if any string cannot be interpreted, the RPC run time will treat the entire configuration as invalid.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><span data-ttu-id="2b827-123"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="2b827-123"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="2b827-124">Y ou N (não diferencia maiúsculas de minúsculas).</span><span class="sxs-lookup"><span data-stu-id="2b827-124">Y or N (not case-sensitive).</span></span> <span data-ttu-id="2b827-125">Se Y, as portas listadas na chave portas serão todas as portas disponíveis para a Internet nesse computador.</span><span class="sxs-lookup"><span data-stu-id="2b827-125">If Y, the ports listed in the Ports key are all the Internet-available ports on that computer.</span></span> <span data-ttu-id="2b827-126">Se N, as portas listadas na chave portas serão todas aquelas portas que não estão disponíveis para a Internet.</span><span class="sxs-lookup"><span data-stu-id="2b827-126">If N, the ports listed in the Ports key are all those ports that are not Internet-available.</span></span></td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><span data-ttu-id="2b827-127"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="2b827-127"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="2b827-128">Y ou N (não diferencia maiúsculas de minúsculas).</span><span class="sxs-lookup"><span data-stu-id="2b827-128">Y or N (not case-sensitive).</span></span> <span data-ttu-id="2b827-129">Especifica a política padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="2b827-129">Specifies the system default policy.</span></span> <span data-ttu-id="2b827-130">Se Y, os processos que usam o padrão serão atribuídos às portas do conjunto de portas disponíveis para a Internet, conforme definido acima.</span><span class="sxs-lookup"><span data-stu-id="2b827-130">If Y, the processes using the default will be assigned ports from the set of Internet-available ports, as defined above.</span></span> <span data-ttu-id="2b827-131">Se N, os processos que usam o padrão serão atribuídos às portas do conjunto de portas somente de intranet.</span><span class="sxs-lookup"><span data-stu-id="2b827-131">If N, processes using the default will be assigned ports from the set of intranet-only ports.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><span data-ttu-id="2b827-132"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="2b827-132"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="2b827-133">Lista os nomes de dispositivos de todas as NICs nas quais associar por padrão (por exemplo, \Device\AMDPCN1).</span><span class="sxs-lookup"><span data-stu-id="2b827-133">Lists the device names of all the NICs on which to bind by default (for example, \Device\AMDPCN1).</span></span> <span data-ttu-id="2b827-134">Se a chave não existir, o servidor será associado a todas as NICs.</span><span class="sxs-lookup"><span data-stu-id="2b827-134">If the key does not exist, the server will bind to all NICs.</span></span> <span data-ttu-id="2b827-135">Se a chave existir, o servidor se associará às NICs especificadas na chave, a menos que o campo NICFlags seja definido como RPC_C_BIND_TO_ALL_NICS.</span><span class="sxs-lookup"><span data-stu-id="2b827-135">If the key does exist, the server will bind to the NICs specified in the key, unless the NICFlags field is set to RPC_C_BIND_TO_ALL_NICS.</span></span> <span data-ttu-id="2b827-136">Se a chave tiver um valor nulo ( &quot; &quot; ), a configuração será marcada como inválida e todas as chamadas para <strong>RpcServerUseProtseq \*</strong> sobre <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> ou <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> falharão.</span><span class="sxs-lookup"><span data-stu-id="2b827-136">If the key has a null (&quot;&quot;) value, the configuration will be marked as invalid and all calls to <strong>RpcServerUseProtseq\*</strong> over <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> or <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> will fail.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2b827-137">A tabela a seguir ilustra como três aplicativos de exemplo são afetados pelas configurações definidas na tabela anterior e como as configurações aplicadas usando a função [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) também são afetadas.</span><span class="sxs-lookup"><span data-stu-id="2b827-137">The following table illustrates how three sample applications are affected by the settings defined in the previous table, and how settings applied using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function are also affected.</span></span>

<span data-ttu-id="2b827-138">Neste exemplo, três aplicativos hipotéticos são considerados:</span><span class="sxs-lookup"><span data-stu-id="2b827-138">In this example, three hypothetical applications are considered:</span></span>

-   <span data-ttu-id="2b827-139">Internetapp: esse aplicativo destina-se à exposição à Internet e especificou que o RPC \_ C \_ usa a porta da \_ Internet \_ no membro **EndpointFlags** da estrutura de [**\_ política RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passada para a função [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="2b827-139">InternetApp: This application is intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTERNET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="2b827-140">LocalApp: este aplicativo não se destina à exposição à Internet e especificou \_ que o RPC C \_ usa a porta de \_ intranet \_ no membro **EndpointFlags** da estrutura de [**\_ política RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passada para a função [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="2b827-140">LocalApp: This application is not intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTRANET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="2b827-141">DefaultApp: esse aplicativo especifica zero no membro **EndpointFlags** da estrutura de [**\_ política RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passada para a função [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="2b827-141">DefaultApp: This application specifies zero in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>

<span data-ttu-id="2b827-142">A tabela a seguir explica o impacto que essas configurações têm com base nos valores especificados nas entradas de registro explicadas na tabela anterior.</span><span class="sxs-lookup"><span data-stu-id="2b827-142">The following table explains the impact these settings have based on values specified in the registry entries explained in the previous table.</span></span> <span data-ttu-id="2b827-143">Para considerações de formatação, os códigos a seguir são atribuídos:</span><span class="sxs-lookup"><span data-stu-id="2b827-143">For formatting considerations, the following codes are assigned:</span></span>

<span data-ttu-id="2b827-144">PIA = valor de chave PortsInternetAvailable</span><span class="sxs-lookup"><span data-stu-id="2b827-144">PIA = PortsInternetAvailable Key value</span></span>

<span data-ttu-id="2b827-145">UIP = valor de chave UseInternetPorts</span><span class="sxs-lookup"><span data-stu-id="2b827-145">UIP = UseInternetPorts Key value</span></span>

<span data-ttu-id="2b827-146">O valor da chave de portas, para fins deste exemplo, é 5000-5100 para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="2b827-146">The value of the Ports key, for sake of this example, is 5000-5100 for each entry.</span></span>



| <span data-ttu-id="2b827-147">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2b827-147">Application</span></span> | <span data-ttu-id="2b827-148">PIA</span><span class="sxs-lookup"><span data-stu-id="2b827-148">PIA</span></span> | <span data-ttu-id="2b827-149">UIP</span><span class="sxs-lookup"><span data-stu-id="2b827-149">UIP</span></span> | <span data-ttu-id="2b827-150">Resultado</span><span class="sxs-lookup"><span data-stu-id="2b827-150">Result</span></span>                                  |
|-------------|-----|-----|-----------------------------------------|
| <span data-ttu-id="2b827-151">Internetapp</span><span class="sxs-lookup"><span data-stu-id="2b827-151">InternetApp</span></span> | <span data-ttu-id="2b827-152">S</span><span class="sxs-lookup"><span data-stu-id="2b827-152">Y</span></span>   | <span data-ttu-id="2b827-153">S</span><span class="sxs-lookup"><span data-stu-id="2b827-153">Y</span></span>   | <span data-ttu-id="2b827-154">Usa portas entre 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="2b827-154">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="2b827-155">LocalApp</span><span class="sxs-lookup"><span data-stu-id="2b827-155">LocalApp</span></span>    | <span data-ttu-id="2b827-156">S</span><span class="sxs-lookup"><span data-stu-id="2b827-156">Y</span></span>   | <span data-ttu-id="2b827-157">S</span><span class="sxs-lookup"><span data-stu-id="2b827-157">Y</span></span>   | <span data-ttu-id="2b827-158">Usa uma porta fora do intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="2b827-158">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="2b827-159">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="2b827-159">DefaultApp</span></span>  | <span data-ttu-id="2b827-160">S</span><span class="sxs-lookup"><span data-stu-id="2b827-160">Y</span></span>   | <span data-ttu-id="2b827-161">S</span><span class="sxs-lookup"><span data-stu-id="2b827-161">Y</span></span>   | <span data-ttu-id="2b827-162">Usa portas entre 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="2b827-162">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="2b827-163">Internetapp</span><span class="sxs-lookup"><span data-stu-id="2b827-163">InternetApp</span></span> | <span data-ttu-id="2b827-164">S</span><span class="sxs-lookup"><span data-stu-id="2b827-164">Y</span></span>   | <span data-ttu-id="2b827-165">N</span><span class="sxs-lookup"><span data-stu-id="2b827-165">N</span></span>   | <span data-ttu-id="2b827-166">Usa portas entre 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="2b827-166">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="2b827-167">LocalApp</span><span class="sxs-lookup"><span data-stu-id="2b827-167">LocalApp</span></span>    | <span data-ttu-id="2b827-168">S</span><span class="sxs-lookup"><span data-stu-id="2b827-168">Y</span></span>   | <span data-ttu-id="2b827-169">N</span><span class="sxs-lookup"><span data-stu-id="2b827-169">N</span></span>   | <span data-ttu-id="2b827-170">Usa uma porta fora do intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="2b827-170">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="2b827-171">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="2b827-171">DefaultApp</span></span>  | <span data-ttu-id="2b827-172">S</span><span class="sxs-lookup"><span data-stu-id="2b827-172">Y</span></span>   | <span data-ttu-id="2b827-173">N</span><span class="sxs-lookup"><span data-stu-id="2b827-173">N</span></span>   | <span data-ttu-id="2b827-174">Usa uma porta fora do intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="2b827-174">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="2b827-175">Internetapp</span><span class="sxs-lookup"><span data-stu-id="2b827-175">InternetApp</span></span> | <span data-ttu-id="2b827-176">N</span><span class="sxs-lookup"><span data-stu-id="2b827-176">N</span></span>   | <span data-ttu-id="2b827-177">S</span><span class="sxs-lookup"><span data-stu-id="2b827-177">Y</span></span>   | <span data-ttu-id="2b827-178">Usa uma porta fora do intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="2b827-178">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="2b827-179">LocalApp</span><span class="sxs-lookup"><span data-stu-id="2b827-179">LocalApp</span></span>    | <span data-ttu-id="2b827-180">N</span><span class="sxs-lookup"><span data-stu-id="2b827-180">N</span></span>   | <span data-ttu-id="2b827-181">S</span><span class="sxs-lookup"><span data-stu-id="2b827-181">Y</span></span>   | <span data-ttu-id="2b827-182">Usa portas entre 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="2b827-182">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="2b827-183">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="2b827-183">DefaultApp</span></span>  | <span data-ttu-id="2b827-184">N</span><span class="sxs-lookup"><span data-stu-id="2b827-184">N</span></span>   | <span data-ttu-id="2b827-185">S</span><span class="sxs-lookup"><span data-stu-id="2b827-185">Y</span></span>   | <span data-ttu-id="2b827-186">Usa uma porta fora do intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="2b827-186">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="2b827-187">Internetapp</span><span class="sxs-lookup"><span data-stu-id="2b827-187">InternetApp</span></span> | <span data-ttu-id="2b827-188">N</span><span class="sxs-lookup"><span data-stu-id="2b827-188">N</span></span>   | <span data-ttu-id="2b827-189">N</span><span class="sxs-lookup"><span data-stu-id="2b827-189">N</span></span>   | <span data-ttu-id="2b827-190">Usa uma porta fora do intervalo de 5000-5100</span><span class="sxs-lookup"><span data-stu-id="2b827-190">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="2b827-191">LocalApp</span><span class="sxs-lookup"><span data-stu-id="2b827-191">LocalApp</span></span>    | <span data-ttu-id="2b827-192">N</span><span class="sxs-lookup"><span data-stu-id="2b827-192">N</span></span>   | <span data-ttu-id="2b827-193">N</span><span class="sxs-lookup"><span data-stu-id="2b827-193">N</span></span>   | <span data-ttu-id="2b827-194">Usa portas entre 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="2b827-194">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="2b827-195">DefaultApp</span><span class="sxs-lookup"><span data-stu-id="2b827-195">DefaultApp</span></span>  | <span data-ttu-id="2b827-196">N</span><span class="sxs-lookup"><span data-stu-id="2b827-196">N</span></span>   | <span data-ttu-id="2b827-197">N</span><span class="sxs-lookup"><span data-stu-id="2b827-197">N</span></span>   | <span data-ttu-id="2b827-198">Usa portas entre 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="2b827-198">Uses ports between 5000 and 5100</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2b827-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b827-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b827-200">**\_política RPC**</span><span class="sxs-lookup"><span data-stu-id="2b827-200">**RPC\_POLICY**</span></span>](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[<span data-ttu-id="2b827-201">**RpcServerUseAllProtseqsEx**</span><span class="sxs-lookup"><span data-stu-id="2b827-201">**RpcServerUseAllProtseqsEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[<span data-ttu-id="2b827-202">**RpcServerUseAllProtseqsIfEx**</span><span class="sxs-lookup"><span data-stu-id="2b827-202">**RpcServerUseAllProtseqsIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[<span data-ttu-id="2b827-203">**RpcServerUseProtseqEx**</span><span class="sxs-lookup"><span data-stu-id="2b827-203">**RpcServerUseProtseqEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[<span data-ttu-id="2b827-204">**RpcServerUseProtseqEpEx**</span><span class="sxs-lookup"><span data-stu-id="2b827-204">**RpcServerUseProtseqEpEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[<span data-ttu-id="2b827-205">**RpcServerUseProtseqIfEx**</span><span class="sxs-lookup"><span data-stu-id="2b827-205">**RpcServerUseProtseqIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[<span data-ttu-id="2b827-206">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="2b827-206">**ncacn\_ip\_tcp**</span></span>](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[<span data-ttu-id="2b827-207">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="2b827-207">**ncadg\_ip\_udp**</span></span>](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 