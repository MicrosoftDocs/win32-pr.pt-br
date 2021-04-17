---
description: A \_ classe Win32 ServerFeature representa os recursos instalados em um computador que executa o Windows Server.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Classe Win32_ServerFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: 1be8a2ea1d646e9d882febc7c8eba08b69bb69f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762987"
---
# <a name="win32_serverfeature-class"></a><span data-ttu-id="2a6bf-103">\_Classe Win32 ServerFeature</span><span class="sxs-lookup"><span data-stu-id="2a6bf-103">Win32\_ServerFeature class</span></span>

<span data-ttu-id="2a6bf-104">\[A classe **Win32 \_ ServerFeature** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-104">\[The **Win32\_ServerFeature** class is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2a6bf-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2a6bf-106">Em vez disso, use as [classes de provedor do servidor de implantação do ServerManager](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span><span class="sxs-lookup"><span data-stu-id="2a6bf-106">Instead, use the [ServerManager Deploymentprovider Provider Classes](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span></span>

<span data-ttu-id="2a6bf-107">A classe **Win32 \_ ServerFeature** representa os recursos instalados em um computador que executa o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-107">The **Win32\_ServerFeature** class represents the features installed on a computer running Windows Server.</span></span>

<span data-ttu-id="2a6bf-108">Essa classe pode ser usada por desenvolvedores e administradores que precisam automatizar o processo de determinação dos recursos instalados em um conjunto de computadores de servidor.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-108">This class can be used by developers and administrators who need to automate the process of determining the features installed on a set of server computers.</span></span> <span data-ttu-id="2a6bf-109">As instâncias dessa classe não estão disponíveis em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-109">Instances of this class are not available on client computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a6bf-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a6bf-110">Syntax</span></span>

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="2a6bf-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2a6bf-111">Members</span></span>

<span data-ttu-id="2a6bf-112">A classe **Win32 \_ ServerFeature** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2a6bf-112">The **Win32\_ServerFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="2a6bf-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2a6bf-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a6bf-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2a6bf-114">Properties</span></span>

<span data-ttu-id="2a6bf-115">A classe **Win32 \_ ServerFeature** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-115">The **Win32\_ServerFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a6bf-116">**ID**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-116">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a6bf-117">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a6bf-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a6bf-119">Qualificadores: [**chave**](key-qualifier.md), [**não \_ nulo**](optional-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-119">Qualifiers: [**Key**](key-qualifier.md), [**Not\_Null**](optional-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2a6bf-120">ID do recurso do servidor.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-120">Server feature ID.</span></span> <span data-ttu-id="2a6bf-121">A lista a seguir mostra os possíveis valores da propriedade ID:</span><span class="sxs-lookup"><span data-stu-id="2a6bf-121">The following list shows the possible values of the ID property:</span></span>



<span data-ttu-id="2a6bf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-122">Value</span></span>

<span data-ttu-id="2a6bf-123">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-123">Name</span></span>

<span data-ttu-id="2a6bf-124">1</span><span class="sxs-lookup"><span data-stu-id="2a6bf-124">1</span></span>

[<span data-ttu-id="2a6bf-125">Servidor de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-125">Application Server</span></span>](/windows)

<span data-ttu-id="2a6bf-126">2</span><span class="sxs-lookup"><span data-stu-id="2a6bf-126">2</span></span>

<span data-ttu-id="2a6bf-127">Servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-127">Web Server (IIS)</span></span>

<span data-ttu-id="2a6bf-128">3</span><span class="sxs-lookup"><span data-stu-id="2a6bf-128">3</span></span>

[<span data-ttu-id="2a6bf-129">Serviços de Mídia de Fluxo Contínuo</span><span class="sxs-lookup"><span data-stu-id="2a6bf-129">Streaming Media Services</span></span>](/windows)

<span data-ttu-id="2a6bf-130">5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-130">5</span></span>

<span data-ttu-id="2a6bf-131">Servidor de Fax</span><span class="sxs-lookup"><span data-stu-id="2a6bf-131">Fax Server</span></span>

<span data-ttu-id="2a6bf-132">6</span><span class="sxs-lookup"><span data-stu-id="2a6bf-132">6</span></span>

<span data-ttu-id="2a6bf-133">Serviços de Arquivo e iSCSI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-133">File and iSCSI Services</span></span><br/> [<span data-ttu-id="2a6bf-134">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-134">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-135">7</span><span class="sxs-lookup"><span data-stu-id="2a6bf-135">7</span></span>

<span data-ttu-id="2a6bf-136">Serviços de impressão e documentos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-136">Print and Document Services</span></span><br/> [<span data-ttu-id="2a6bf-137">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-137">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-138">8</span><span class="sxs-lookup"><span data-stu-id="2a6bf-138">8</span></span>

[<span data-ttu-id="2a6bf-139">Serviços de Federação do Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-139">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="2a6bf-140">9</span><span class="sxs-lookup"><span data-stu-id="2a6bf-140">9</span></span>

<span data-ttu-id="2a6bf-141">Active Directory Lightweight Directory Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-141">Active Directory Lightweight Directory Services</span></span>

<span data-ttu-id="2a6bf-142">10</span><span class="sxs-lookup"><span data-stu-id="2a6bf-142">10</span></span>

<span data-ttu-id="2a6bf-143">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-143">Active Directory Domain Services</span></span>

<span data-ttu-id="2a6bf-144">11</span><span class="sxs-lookup"><span data-stu-id="2a6bf-144">11</span></span>

[<span data-ttu-id="2a6bf-145">Serviços UDDI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-145">UDDI Services</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-146">12</span><span class="sxs-lookup"><span data-stu-id="2a6bf-146">12</span></span>

[<span data-ttu-id="2a6bf-147">Servidor DHCP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-147">DHCP Server</span></span>](/windows)

<span data-ttu-id="2a6bf-148">13</span><span class="sxs-lookup"><span data-stu-id="2a6bf-148">13</span></span>

[<span data-ttu-id="2a6bf-149">Servidor DNS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-149">DNS Server</span></span>](/windows)

<span data-ttu-id="2a6bf-150">14</span><span class="sxs-lookup"><span data-stu-id="2a6bf-150">14</span></span>

<span data-ttu-id="2a6bf-151">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-151">Network Policy and Access Services</span></span>

<span data-ttu-id="2a6bf-152">16</span><span class="sxs-lookup"><span data-stu-id="2a6bf-152">16</span></span>

<span data-ttu-id="2a6bf-153">Serviços de Certificados do Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a6bf-153">Active Directory Certificate Services</span></span>

<span data-ttu-id="2a6bf-154">17</span><span class="sxs-lookup"><span data-stu-id="2a6bf-154">17</span></span>

<span data-ttu-id="2a6bf-155">Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-155">Active Directory Rights Management Services</span></span>

<span data-ttu-id="2a6bf-156">18</span><span class="sxs-lookup"><span data-stu-id="2a6bf-156">18</span></span>

[<span data-ttu-id="2a6bf-157">Serviços de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-157">Remote Desktop Services</span></span>](/windows)<br/> [<span data-ttu-id="2a6bf-158">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-158">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-159">19</span><span class="sxs-lookup"><span data-stu-id="2a6bf-159">19</span></span>

<span data-ttu-id="2a6bf-160">Windows Deployment Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-160">Windows Deployment Services</span></span>

<span data-ttu-id="2a6bf-161">20</span><span class="sxs-lookup"><span data-stu-id="2a6bf-161">20</span></span>

<span data-ttu-id="2a6bf-162">Hyper-v</span><span class="sxs-lookup"><span data-stu-id="2a6bf-162">Hyper-V</span></span>

<span data-ttu-id="2a6bf-163">21</span><span class="sxs-lookup"><span data-stu-id="2a6bf-163">21</span></span>

[<span data-ttu-id="2a6bf-164">Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-164">Windows Server Update Services</span></span>](/windows)

<span data-ttu-id="2a6bf-165">33</span><span class="sxs-lookup"><span data-stu-id="2a6bf-165">33</span></span>

[<span data-ttu-id="2a6bf-166">Clustering de failover</span><span class="sxs-lookup"><span data-stu-id="2a6bf-166">Failover Clustering</span></span>](/windows)

<span data-ttu-id="2a6bf-167">34</span><span class="sxs-lookup"><span data-stu-id="2a6bf-167">34</span></span>

[<span data-ttu-id="2a6bf-168">Balanceamento de Carga de Rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-168">Network Load Balancing</span></span>](/windows)

<span data-ttu-id="2a6bf-169">36</span><span class="sxs-lookup"><span data-stu-id="2a6bf-169">36</span></span>

[<span data-ttu-id="2a6bf-170">Recursos do .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="2a6bf-170">.NET Framework 3.5.1 Features</span></span>](/windows)<br/> [<span data-ttu-id="2a6bf-171">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-171">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-172">37</span><span class="sxs-lookup"><span data-stu-id="2a6bf-172">37</span></span>

[<span data-ttu-id="2a6bf-173">Gerenciador de recursos de sistema do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-173">Windows System Resource Manager</span></span>](/windows)

<span data-ttu-id="2a6bf-174">38</span><span class="sxs-lookup"><span data-stu-id="2a6bf-174">38</span></span>

<span data-ttu-id="2a6bf-175">Serviço de LAN sem fio</span><span class="sxs-lookup"><span data-stu-id="2a6bf-175">Wireless LAN Service</span></span>

<span data-ttu-id="2a6bf-176">39</span><span class="sxs-lookup"><span data-stu-id="2a6bf-176">39</span></span>

[<span data-ttu-id="2a6bf-177">Recursos de Backup do Windows Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-177">Windows Server Backup Features</span></span>](/windows)

<span data-ttu-id="2a6bf-178">40</span><span class="sxs-lookup"><span data-stu-id="2a6bf-178">40</span></span>

<span data-ttu-id="2a6bf-179">Servidor WINS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-179">WINS Server</span></span>

<span data-ttu-id="2a6bf-180">41</span><span class="sxs-lookup"><span data-stu-id="2a6bf-180">41</span></span>

<span data-ttu-id="2a6bf-181">Serviço de Ativação de Processos do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-181">Windows Process Activation Service</span></span>

<span data-ttu-id="2a6bf-182">42</span><span class="sxs-lookup"><span data-stu-id="2a6bf-182">42</span></span>

[<span data-ttu-id="2a6bf-183">Assistência Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-183">Remote Assistance</span></span>](/windows)

<span data-ttu-id="2a6bf-184">43</span><span class="sxs-lookup"><span data-stu-id="2a6bf-184">43</span></span>

<span data-ttu-id="2a6bf-185">Serviços TCP/IP Simples</span><span class="sxs-lookup"><span data-stu-id="2a6bf-185">Simple TCP/IP Services</span></span>

<span data-ttu-id="2a6bf-186">44</span><span class="sxs-lookup"><span data-stu-id="2a6bf-186">44</span></span>

[<span data-ttu-id="2a6bf-187">Cliente Telnet</span><span class="sxs-lookup"><span data-stu-id="2a6bf-187">Telnet Client</span></span>](/windows)

<span data-ttu-id="2a6bf-188">45</span><span class="sxs-lookup"><span data-stu-id="2a6bf-188">45</span></span>

[<span data-ttu-id="2a6bf-189">Servidor Telnet</span><span class="sxs-lookup"><span data-stu-id="2a6bf-189">Telnet Server</span></span>](/windows)

<span data-ttu-id="2a6bf-190">46</span><span class="sxs-lookup"><span data-stu-id="2a6bf-190">46</span></span>

[<span data-ttu-id="2a6bf-191">Subsistema para aplicativos baseados em UNIX</span><span class="sxs-lookup"><span data-stu-id="2a6bf-191">Subsystem For Unix-based Applications</span></span>](/windows)

<span data-ttu-id="2a6bf-192">47</span><span class="sxs-lookup"><span data-stu-id="2a6bf-192">47</span></span>

<span data-ttu-id="2a6bf-193">RPC sobre proxy HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-193">RPC Over HTTP Proxy</span></span>

<span data-ttu-id="2a6bf-194">48</span><span class="sxs-lookup"><span data-stu-id="2a6bf-194">48</span></span>

<span data-ttu-id="2a6bf-195">Servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-195">SMTP Server</span></span>

<span data-ttu-id="2a6bf-196">49</span><span class="sxs-lookup"><span data-stu-id="2a6bf-196">49</span></span>

<span data-ttu-id="2a6bf-197">Enfileiramento de Mensagens</span><span class="sxs-lookup"><span data-stu-id="2a6bf-197">Message Queuing</span></span>

<span data-ttu-id="2a6bf-198">51</span><span class="sxs-lookup"><span data-stu-id="2a6bf-198">51</span></span>

[<span data-ttu-id="2a6bf-199">Banco de Dados Interno do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-199">Windows Internal Database</span></span>](/windows)

<span data-ttu-id="2a6bf-200">52</span><span class="sxs-lookup"><span data-stu-id="2a6bf-200">52</span></span>

[<span data-ttu-id="2a6bf-201">Gerenciador de armazenamento para SANs</span><span class="sxs-lookup"><span data-stu-id="2a6bf-201">Storage Manager For SANs</span></span>](/windows)

<span data-ttu-id="2a6bf-202">53</span><span class="sxs-lookup"><span data-stu-id="2a6bf-202">53</span></span>

<span data-ttu-id="2a6bf-203">Monitor de Porta LPR</span><span class="sxs-lookup"><span data-stu-id="2a6bf-203">LPR Port Monitor</span></span>

<span data-ttu-id="2a6bf-204">55</span><span class="sxs-lookup"><span data-stu-id="2a6bf-204">55</span></span>

[<span data-ttu-id="2a6bf-205">Internet Storage Name Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-205">Internet Storage Name Server</span></span>](/windows)

<span data-ttu-id="2a6bf-206">57</span><span class="sxs-lookup"><span data-stu-id="2a6bf-206">57</span></span>

[<span data-ttu-id="2a6bf-207">Multipath I/O</span><span class="sxs-lookup"><span data-stu-id="2a6bf-207">Multipath I/O</span></span>](/windows)

<span data-ttu-id="2a6bf-208">58</span><span class="sxs-lookup"><span data-stu-id="2a6bf-208">58</span></span>

<span data-ttu-id="2a6bf-209">Cliente TFTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-209">TFTP Client</span></span>

<span data-ttu-id="2a6bf-210">59</span><span class="sxs-lookup"><span data-stu-id="2a6bf-210">59</span></span>

[<span data-ttu-id="2a6bf-211">Serviços SNMP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-211">SNMP Services</span></span>](/windows)

<span data-ttu-id="2a6bf-212">60</span><span class="sxs-lookup"><span data-stu-id="2a6bf-212">60</span></span>

[<span data-ttu-id="2a6bf-213">Gerenciador de armazenamento removível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-213">Removable Storage Manager</span></span>](/windows)

<span data-ttu-id="2a6bf-214">61</span><span class="sxs-lookup"><span data-stu-id="2a6bf-214">61</span></span>

<span data-ttu-id="2a6bf-215">Criptografia de Unidade de Disco BitLocker</span><span class="sxs-lookup"><span data-stu-id="2a6bf-215">BitLocker Drive Encryption</span></span>

<span data-ttu-id="2a6bf-216">62</span><span class="sxs-lookup"><span data-stu-id="2a6bf-216">62</span></span>

[<span data-ttu-id="2a6bf-217">Serviços para sistema de arquivos de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-217">Services For Network File System</span></span>](/windows)

<span data-ttu-id="2a6bf-218">63</span><span class="sxs-lookup"><span data-stu-id="2a6bf-218">63</span></span>

<span data-ttu-id="2a6bf-219">Cliente de Impressão via Internet</span><span class="sxs-lookup"><span data-stu-id="2a6bf-219">Internet Printing Client</span></span>

<span data-ttu-id="2a6bf-220">64</span><span class="sxs-lookup"><span data-stu-id="2a6bf-220">64</span></span>

[<span data-ttu-id="2a6bf-221">Protocolo PNRP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-221">Peer Name Resolution Protocol</span></span>](/windows)

<span data-ttu-id="2a6bf-222">65</span><span class="sxs-lookup"><span data-stu-id="2a6bf-222">65</span></span>

<span data-ttu-id="2a6bf-223">Kit de administração do Gerenciador de conexões</span><span class="sxs-lookup"><span data-stu-id="2a6bf-223">Connection Manager Administration Kit</span></span>

<span data-ttu-id="2a6bf-224">66</span><span class="sxs-lookup"><span data-stu-id="2a6bf-224">66</span></span>

[<span data-ttu-id="2a6bf-225">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-225">Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-226">67</span><span class="sxs-lookup"><span data-stu-id="2a6bf-226">67</span></span>

[<span data-ttu-id="2a6bf-227">Ferramentas Administrativas do Servidor Remoto</span><span class="sxs-lookup"><span data-stu-id="2a6bf-227">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-228">68</span><span class="sxs-lookup"><span data-stu-id="2a6bf-228">68</span></span>

[<span data-ttu-id="2a6bf-229">Quality Windows Audio-Video Experience</span><span class="sxs-lookup"><span data-stu-id="2a6bf-229">Quality Windows Audio Video Experience</span></span>](/windows)

<span data-ttu-id="2a6bf-230">69</span><span class="sxs-lookup"><span data-stu-id="2a6bf-230">69</span></span>

[<span data-ttu-id="2a6bf-231">Gerenciamento de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="2a6bf-231">Group Policy Management</span></span>](/windows)

<span data-ttu-id="2a6bf-232">71</span><span class="sxs-lookup"><span data-stu-id="2a6bf-232">71</span></span>

[<span data-ttu-id="2a6bf-233">Indexing Service</span><span class="sxs-lookup"><span data-stu-id="2a6bf-233">Indexing Service</span></span>](/windows)

<span data-ttu-id="2a6bf-234">72</span><span class="sxs-lookup"><span data-stu-id="2a6bf-234">72</span></span>

[<span data-ttu-id="2a6bf-235">Gerenciador de Recursos de Servidor de Arquivos (FSRM)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-235">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="2a6bf-236">73</span><span class="sxs-lookup"><span data-stu-id="2a6bf-236">73</span></span>

<span data-ttu-id="2a6bf-237">Compressão diferencial remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-237">Remote Differential Compression</span></span>

<span data-ttu-id="2a6bf-238">310</span><span class="sxs-lookup"><span data-stu-id="2a6bf-238">310</span></span>

<span data-ttu-id="2a6bf-239">Serviços de tinta e manuscrito</span><span class="sxs-lookup"><span data-stu-id="2a6bf-239">Ink and Handwriting Services</span></span><br/>

<span data-ttu-id="2a6bf-240">320</span><span class="sxs-lookup"><span data-stu-id="2a6bf-240">320</span></span>

[<span data-ttu-id="2a6bf-241">Ferramentas de Migração do Windows Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-241">Windows Server Migration Tools</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-242">321</span><span class="sxs-lookup"><span data-stu-id="2a6bf-242">321</span></span>

[<span data-ttu-id="2a6bf-243">Extensão IIS WinRM</span><span class="sxs-lookup"><span data-stu-id="2a6bf-243">WinRM IIS Extension</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-244">324</span><span class="sxs-lookup"><span data-stu-id="2a6bf-244">324</span></span>

[<span data-ttu-id="2a6bf-245">BranchCache</span><span class="sxs-lookup"><span data-stu-id="2a6bf-245">BranchCache</span></span>](#branchcache)<br/>

<span data-ttu-id="2a6bf-246">334</span><span class="sxs-lookup"><span data-stu-id="2a6bf-246">334</span></span>

[<span data-ttu-id="2a6bf-247">Console de gerenciamento DirectAccess</span><span class="sxs-lookup"><span data-stu-id="2a6bf-247">DirectAccess Management Console</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-248">335</span><span class="sxs-lookup"><span data-stu-id="2a6bf-248">335</span></span>

[<span data-ttu-id="2a6bf-249">BITS (serviço de Transferência Inteligente em Segundo Plano)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-249">Background Intelligent Transfer Service (BITS)</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-250">338</span><span class="sxs-lookup"><span data-stu-id="2a6bf-250">338</span></span>

[<span data-ttu-id="2a6bf-251">Visualizador XPS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-251">XPS Viewer</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-252">339</span><span class="sxs-lookup"><span data-stu-id="2a6bf-252">339</span></span>

[<span data-ttu-id="2a6bf-253">Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="2a6bf-253">Windows Biometric Framework</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-254">340</span><span class="sxs-lookup"><span data-stu-id="2a6bf-254">340</span></span>

<span data-ttu-id="2a6bf-255">Suporte a WoW64</span><span class="sxs-lookup"><span data-stu-id="2a6bf-255">WoW64 Support</span></span><br/>

<span data-ttu-id="2a6bf-256">351</span><span class="sxs-lookup"><span data-stu-id="2a6bf-256">351</span></span>

[<span data-ttu-id="2a6bf-257">Ambiente de Script Integrado do Windows PowerShell (ISE)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-257">Windows PowerShell Integrated Scripting Environment (ISE)</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-258">352</span><span class="sxs-lookup"><span data-stu-id="2a6bf-258">352</span></span>

<span data-ttu-id="2a6bf-259">Windows TIFF IFilter</span><span class="sxs-lookup"><span data-stu-id="2a6bf-259">Windows TIFF IFilter</span></span><br/>

<span data-ttu-id="2a6bf-260">404</span><span class="sxs-lookup"><span data-stu-id="2a6bf-260">404</span></span>

[<span data-ttu-id="2a6bf-261">Serviços de atualização de servidor do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-261">Window Server Update Services</span></span>](/windows)

<span data-ttu-id="2a6bf-262">409</span><span class="sxs-lookup"><span data-stu-id="2a6bf-262">409</span></span>

[<span data-ttu-id="2a6bf-263">Servidor de Gerenciamento de Endereço IP (IPAM)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-263">IP Address Management (IPAM) Server</span></span>](/windows)

<span data-ttu-id="2a6bf-264">417</span><span class="sxs-lookup"><span data-stu-id="2a6bf-264">417</span></span>

[<span data-ttu-id="2a6bf-265">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-265">Windows PowerShell</span></span>](/windows)

<span data-ttu-id="2a6bf-266">418</span><span class="sxs-lookup"><span data-stu-id="2a6bf-266">418</span></span>

[<span data-ttu-id="2a6bf-267">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-267">.NET Framework 4.5</span></span>](/windows)

<span data-ttu-id="2a6bf-268">432</span><span class="sxs-lookup"><span data-stu-id="2a6bf-268">432</span></span>

[<span data-ttu-id="2a6bf-269">Serviço Windows Search</span><span class="sxs-lookup"><span data-stu-id="2a6bf-269">Windows Search Service</span></span>](/windows)

<span data-ttu-id="2a6bf-270">438</span><span class="sxs-lookup"><span data-stu-id="2a6bf-270">438</span></span>

[<span data-ttu-id="2a6bf-271">Cliente NFS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-271">Client for NFS</span></span>](/windows)

<span data-ttu-id="2a6bf-272">441</span><span class="sxs-lookup"><span data-stu-id="2a6bf-272">441</span></span>

[<span data-ttu-id="2a6bf-273">Desbloqueio de Rede do BitLocker</span><span class="sxs-lookup"><span data-stu-id="2a6bf-273">BitLocker Network Unlock</span></span>](/windows)

<span data-ttu-id="2a6bf-274">442</span><span class="sxs-lookup"><span data-stu-id="2a6bf-274">442</span></span>

[<span data-ttu-id="2a6bf-275">Extensão do IIS do Management OData</span><span class="sxs-lookup"><span data-stu-id="2a6bf-275">Management OData IIS Extension</span></span>](/windows)

<span data-ttu-id="2a6bf-276">450</span><span class="sxs-lookup"><span data-stu-id="2a6bf-276">450</span></span>

[<span data-ttu-id="2a6bf-277">Serviços avançados do .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-277">.NET Framework 4.5 Advanced Services</span></span>](/windows)

<span data-ttu-id="2a6bf-278">466</span><span class="sxs-lookup"><span data-stu-id="2a6bf-278">466</span></span>

[<span data-ttu-id="2a6bf-279">Recursos do .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-279">.NET Framework 4.5 Features</span></span>](/windows)

<span data-ttu-id="2a6bf-280">468</span><span class="sxs-lookup"><span data-stu-id="2a6bf-280">468</span></span>

[<span data-ttu-id="2a6bf-281">Acesso remoto</span><span class="sxs-lookup"><span data-stu-id="2a6bf-281">Remote Access</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-282">477</span><span class="sxs-lookup"><span data-stu-id="2a6bf-282">477</span></span>

[<span data-ttu-id="2a6bf-283">Interfaces do usuário e infraestrutura</span><span class="sxs-lookup"><span data-stu-id="2a6bf-283">User Interfaces and Infrastructure</span></span>](/windows)

<span data-ttu-id="2a6bf-284">478</span><span class="sxs-lookup"><span data-stu-id="2a6bf-284">478</span></span>

[<span data-ttu-id="2a6bf-285">Ferramentas e Infraestrutura de Gerenciamento Gráfico</span><span class="sxs-lookup"><span data-stu-id="2a6bf-285">Graphical Management Tools and Infrastructure</span></span>](/windows)

<span data-ttu-id="2a6bf-286">481</span><span class="sxs-lookup"><span data-stu-id="2a6bf-286">481</span></span>

[<span data-ttu-id="2a6bf-287">Serviços de Arquivo e Armazenamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-287">File and Storage Services</span></span>](/windows)

<span data-ttu-id="2a6bf-288">485</span><span class="sxs-lookup"><span data-stu-id="2a6bf-288">485</span></span>

[<span data-ttu-id="2a6bf-289">Experiência do Windows Server Essentials</span><span class="sxs-lookup"><span data-stu-id="2a6bf-289">Windows Server Essentials Experience</span></span>](/windows)

<span data-ttu-id="2a6bf-290">488</span><span class="sxs-lookup"><span data-stu-id="2a6bf-290">488</span></span>

[<span data-ttu-id="2a6bf-291">Direct Play</span><span class="sxs-lookup"><span data-stu-id="2a6bf-291">Direct Play</span></span>](/windows)

<span data-ttu-id="2a6bf-292">Serviços de arquivos – serviços de função (6)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-292">File Services - Role Services (6)</span></span>

<span data-ttu-id="2a6bf-293">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-293">Value</span></span>

<span data-ttu-id="2a6bf-294">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-294">Name</span></span>

<span data-ttu-id="2a6bf-295">100</span><span class="sxs-lookup"><span data-stu-id="2a6bf-295">100</span></span>

[<span data-ttu-id="2a6bf-296">Sistema de Arquivos Distribuído</span><span class="sxs-lookup"><span data-stu-id="2a6bf-296">Distributed File System</span></span>](/windows)

<span data-ttu-id="2a6bf-297">101</span><span class="sxs-lookup"><span data-stu-id="2a6bf-297">101</span></span>

<span data-ttu-id="2a6bf-298">Namespace de DFS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-298">DFS Namespace</span></span>

<span data-ttu-id="2a6bf-299">102</span><span class="sxs-lookup"><span data-stu-id="2a6bf-299">102</span></span>

<span data-ttu-id="2a6bf-300">Replicação do DFS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-300">DFS Replication</span></span>

<span data-ttu-id="2a6bf-301">103</span><span class="sxs-lookup"><span data-stu-id="2a6bf-301">103</span></span>

[<span data-ttu-id="2a6bf-302">Serviço de Replicação de Arquivos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-302">File Replication Service</span></span>](/windows)

<span data-ttu-id="2a6bf-303">104</span><span class="sxs-lookup"><span data-stu-id="2a6bf-303">104</span></span>

[<span data-ttu-id="2a6bf-304">Gerenciador de Recursos de Servidor de Arquivos (FSRM)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-304">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="2a6bf-305">105</span><span class="sxs-lookup"><span data-stu-id="2a6bf-305">105</span></span>

[<span data-ttu-id="2a6bf-306">Serviços para sistema de arquivos de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-306">Services For Network File System</span></span>](/windows)

<span data-ttu-id="2a6bf-307">106</span><span class="sxs-lookup"><span data-stu-id="2a6bf-307">106</span></span>

[<span data-ttu-id="2a6bf-308">Armazenamento de instância única</span><span class="sxs-lookup"><span data-stu-id="2a6bf-308">Single Instance Storage</span></span>](/windows)

<span data-ttu-id="2a6bf-309">107</span><span class="sxs-lookup"><span data-stu-id="2a6bf-309">107</span></span>

[<span data-ttu-id="2a6bf-310">Serviço Windows Search</span><span class="sxs-lookup"><span data-stu-id="2a6bf-310">Windows Search Service</span></span>](/windows)

<span data-ttu-id="2a6bf-311">108</span><span class="sxs-lookup"><span data-stu-id="2a6bf-311">108</span></span>

[<span data-ttu-id="2a6bf-312">Indexing Service</span><span class="sxs-lookup"><span data-stu-id="2a6bf-312">Indexing Service</span></span>](/windows)

<span data-ttu-id="2a6bf-313">255</span><span class="sxs-lookup"><span data-stu-id="2a6bf-313">255</span></span>

<span data-ttu-id="2a6bf-314">Servidor de arquivos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-314">File Server</span></span>

<span data-ttu-id="2a6bf-315">350</span><span class="sxs-lookup"><span data-stu-id="2a6bf-315">350</span></span>

<span data-ttu-id="2a6bf-316">BranchCache para arquivos de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-316">BranchCache for Network Files</span></span>

<span data-ttu-id="2a6bf-317">431</span><span class="sxs-lookup"><span data-stu-id="2a6bf-317">431</span></span>

[<span data-ttu-id="2a6bf-318">Servidor para NFS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-318">Server for NFS</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-319">434</span><span class="sxs-lookup"><span data-stu-id="2a6bf-319">434</span></span>

[<span data-ttu-id="2a6bf-320">Serviço de Agente VSS de Servidor de Arquivos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-320">File Server VSS Agent Service</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-321">435</span><span class="sxs-lookup"><span data-stu-id="2a6bf-321">435</span></span>

[<span data-ttu-id="2a6bf-322">Servidor de destino iSCSI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-322">iSCSI Target Server</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-323">436</span><span class="sxs-lookup"><span data-stu-id="2a6bf-323">436</span></span>

[<span data-ttu-id="2a6bf-324">Eliminação de Duplicação de Dados</span><span class="sxs-lookup"><span data-stu-id="2a6bf-324">Data Deduplication</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-325">437</span><span class="sxs-lookup"><span data-stu-id="2a6bf-325">437</span></span>

[<span data-ttu-id="2a6bf-326">Provedor de armazenamento de destino iSCSI (provedores de hardware VDS e VSS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-326">iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>](/windows)

<span data-ttu-id="2a6bf-327">486</span><span class="sxs-lookup"><span data-stu-id="2a6bf-327">486</span></span>

[<span data-ttu-id="2a6bf-328">Pastas de trabalho</span><span class="sxs-lookup"><span data-stu-id="2a6bf-328">Work Folders</span></span>](/windows)

<span data-ttu-id="2a6bf-329">Serviços de função de AD DS (10)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-329">AD DS - Role Services (10)</span></span>

<span data-ttu-id="2a6bf-330">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-330">Value</span></span>

<span data-ttu-id="2a6bf-331">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-331">Name</span></span>

<span data-ttu-id="2a6bf-332">110</span><span class="sxs-lookup"><span data-stu-id="2a6bf-332">110</span></span>

[<span data-ttu-id="2a6bf-333">Controlador de Domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a6bf-333">Active Directory Domain Controller</span></span>](/windows)

<span data-ttu-id="2a6bf-334">111</span><span class="sxs-lookup"><span data-stu-id="2a6bf-334">111</span></span>

[<span data-ttu-id="2a6bf-335">Gerenciamento de identidade para UNIX</span><span class="sxs-lookup"><span data-stu-id="2a6bf-335">Identity Management For Unix</span></span>](/windows)

<span data-ttu-id="2a6bf-336">112</span><span class="sxs-lookup"><span data-stu-id="2a6bf-336">112</span></span>

[<span data-ttu-id="2a6bf-337">Servidor para serviços de informações de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-337">Server For Network Information Services</span></span>](/windows)

<span data-ttu-id="2a6bf-338">113</span><span class="sxs-lookup"><span data-stu-id="2a6bf-338">113</span></span>

[<span data-ttu-id="2a6bf-339">Sincronização de senha</span><span class="sxs-lookup"><span data-stu-id="2a6bf-339">Password Synchronization</span></span>](/windows)

<span data-ttu-id="2a6bf-340">294</span><span class="sxs-lookup"><span data-stu-id="2a6bf-340">294</span></span>

[<span data-ttu-id="2a6bf-341">Ferramentas Administrativas do Servidor Remoto</span><span class="sxs-lookup"><span data-stu-id="2a6bf-341">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-342">Streaming de mídia – serviços de função (3)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-342">Streaming Media - Role Services (3)</span></span>

<span data-ttu-id="2a6bf-343">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-343">Value</span></span>

<span data-ttu-id="2a6bf-344">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-344">Name</span></span>

<span data-ttu-id="2a6bf-345">120</span><span class="sxs-lookup"><span data-stu-id="2a6bf-345">120</span></span>

[<span data-ttu-id="2a6bf-346">Windows Media Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-346">Windows Media Server</span></span>](/windows)

<span data-ttu-id="2a6bf-347">121</span><span class="sxs-lookup"><span data-stu-id="2a6bf-347">121</span></span>

[<span data-ttu-id="2a6bf-348">Administração baseada na Web</span><span class="sxs-lookup"><span data-stu-id="2a6bf-348">Web-based Administration</span></span>](/windows)

<span data-ttu-id="2a6bf-349">122</span><span class="sxs-lookup"><span data-stu-id="2a6bf-349">122</span></span>

[<span data-ttu-id="2a6bf-350">Agente de log</span><span class="sxs-lookup"><span data-stu-id="2a6bf-350">Logging Agent</span></span>](/windows)

<span data-ttu-id="2a6bf-351">ADFS – serviços de função (8)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-351">ADFS - Role Services (8)</span></span>

<span data-ttu-id="2a6bf-352">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-352">Value</span></span>

<span data-ttu-id="2a6bf-353">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-353">Name</span></span>

<span data-ttu-id="2a6bf-354">125</span><span class="sxs-lookup"><span data-stu-id="2a6bf-354">125</span></span>

[<span data-ttu-id="2a6bf-355">Serviços de Federação do Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-355">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="2a6bf-356">126</span><span class="sxs-lookup"><span data-stu-id="2a6bf-356">126</span></span>

[<span data-ttu-id="2a6bf-357">Política de Serviço de Federação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-357">Federation Service Policy</span></span>](/windows)

<span data-ttu-id="2a6bf-358">127</span><span class="sxs-lookup"><span data-stu-id="2a6bf-358">127</span></span>

[<span data-ttu-id="2a6bf-359">Agentes Web do AD FS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-359">AD FS Web Agents</span></span>](/windows)

<span data-ttu-id="2a6bf-360">128</span><span class="sxs-lookup"><span data-stu-id="2a6bf-360">128</span></span>

[<span data-ttu-id="2a6bf-361">Agente de Reconhecimento de Declaração</span><span class="sxs-lookup"><span data-stu-id="2a6bf-361">Claims-aware Agent</span></span>](/windows)

<span data-ttu-id="2a6bf-362">129</span><span class="sxs-lookup"><span data-stu-id="2a6bf-362">129</span></span>

[<span data-ttu-id="2a6bf-363">Agente baseado no token do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-363">Windows Token-based Agent</span></span>](/windows)

<span data-ttu-id="2a6bf-364">Serviços de função de Serviços de Área de Trabalho Remota (18)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-364">Remote Desktop Services - Role Services (18)</span></span>

<span data-ttu-id="2a6bf-365">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-365">Value</span></span>

<span data-ttu-id="2a6bf-366">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-366">Name</span></span>

<span data-ttu-id="2a6bf-367">130</span><span class="sxs-lookup"><span data-stu-id="2a6bf-367">130</span></span>

<span data-ttu-id="2a6bf-368">Host de Sessão de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-368">Remote Desktop Session Host</span></span><br/> [<span data-ttu-id="2a6bf-369">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-369">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-370">131</span><span class="sxs-lookup"><span data-stu-id="2a6bf-370">131</span></span>

[<span data-ttu-id="2a6bf-371">Licenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-371">Remote Desktop Licensing</span></span>](/windows)<br/> [<span data-ttu-id="2a6bf-372">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-372">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-373">132</span><span class="sxs-lookup"><span data-stu-id="2a6bf-373">132</span></span>

<span data-ttu-id="2a6bf-374">Gateway de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-374">Remote Desktop Gateway</span></span><br/> [<span data-ttu-id="2a6bf-375">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-375">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-376">133</span><span class="sxs-lookup"><span data-stu-id="2a6bf-376">133</span></span>

<span data-ttu-id="2a6bf-377">Agente de Conexão de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-377">Remote Desktop Connection Broker</span></span><br/> [<span data-ttu-id="2a6bf-378">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-378">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-379">134</span><span class="sxs-lookup"><span data-stu-id="2a6bf-379">134</span></span>

<span data-ttu-id="2a6bf-380">Acesso via Web à Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-380">Remote Desktop Web Access</span></span><br/> [<span data-ttu-id="2a6bf-381">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-381">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-382">322</span><span class="sxs-lookup"><span data-stu-id="2a6bf-382">322</span></span>

<span data-ttu-id="2a6bf-383">Host de Virtualização de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-383">Remote Desktop Virtualization Host</span></span><br/>

<span data-ttu-id="2a6bf-384">Serviços de função de Host de Virtualização de Área de Trabalho Remota (322)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-384">Remote Desktop Virtualization Host - Role Services (322)</span></span>

<span data-ttu-id="2a6bf-385">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-385">Value</span></span>

<span data-ttu-id="2a6bf-386">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-386">Name</span></span>

<span data-ttu-id="2a6bf-387">325</span><span class="sxs-lookup"><span data-stu-id="2a6bf-387">325</span></span>

[<span data-ttu-id="2a6bf-388">Serviços principais</span><span class="sxs-lookup"><span data-stu-id="2a6bf-388">Core Services</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-389">327</span><span class="sxs-lookup"><span data-stu-id="2a6bf-389">327</span></span>

[<span data-ttu-id="2a6bf-390">Gráficos virtuais Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-390">Remote Desktop Virtual Graphics</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-391">Serviços de função de Serviços de Impressão e Documentos (7)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-391">Print and Document Services - Role Services (7)</span></span>

<span data-ttu-id="2a6bf-392">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-392">Value</span></span>

<span data-ttu-id="2a6bf-393">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-393">Name</span></span>

<span data-ttu-id="2a6bf-394">135</span><span class="sxs-lookup"><span data-stu-id="2a6bf-394">135</span></span>

<span data-ttu-id="2a6bf-395">Servidor de Impressão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-395">Print Server</span></span>

<span data-ttu-id="2a6bf-396">136</span><span class="sxs-lookup"><span data-stu-id="2a6bf-396">136</span></span>

<span data-ttu-id="2a6bf-397">Impressão via Internet</span><span class="sxs-lookup"><span data-stu-id="2a6bf-397">Internet Printing</span></span>

<span data-ttu-id="2a6bf-398">137</span><span class="sxs-lookup"><span data-stu-id="2a6bf-398">137</span></span>

<span data-ttu-id="2a6bf-399">Serviço de impressão LPD</span><span class="sxs-lookup"><span data-stu-id="2a6bf-399">LPD Print Service</span></span>

<span data-ttu-id="2a6bf-400">328</span><span class="sxs-lookup"><span data-stu-id="2a6bf-400">328</span></span>

[<span data-ttu-id="2a6bf-401">Servidor de Digitalização Distribuída</span><span class="sxs-lookup"><span data-stu-id="2a6bf-401">Distributed Scan Server</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-402">Servidor Web (IIS)-serviços de função (2)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-402">Web Server (IIS) - Role Services (2)</span></span>

<span data-ttu-id="2a6bf-403">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-403">Value</span></span>

<span data-ttu-id="2a6bf-404">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-404">Name</span></span>

<span data-ttu-id="2a6bf-405">140</span><span class="sxs-lookup"><span data-stu-id="2a6bf-405">140</span></span>

<span data-ttu-id="2a6bf-406">Servidor Web</span><span class="sxs-lookup"><span data-stu-id="2a6bf-406">Web Server</span></span>

<span data-ttu-id="2a6bf-407">141</span><span class="sxs-lookup"><span data-stu-id="2a6bf-407">141</span></span>

<span data-ttu-id="2a6bf-408">Recursos comuns de HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-408">Common HTTP Features</span></span>

<span data-ttu-id="2a6bf-409">142</span><span class="sxs-lookup"><span data-stu-id="2a6bf-409">142</span></span>

<span data-ttu-id="2a6bf-410">Conteúdo Estático</span><span class="sxs-lookup"><span data-stu-id="2a6bf-410">Static Content</span></span>

<span data-ttu-id="2a6bf-411">143</span><span class="sxs-lookup"><span data-stu-id="2a6bf-411">143</span></span>

<span data-ttu-id="2a6bf-412">Documento padrão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-412">Default Document</span></span>

<span data-ttu-id="2a6bf-413">144</span><span class="sxs-lookup"><span data-stu-id="2a6bf-413">144</span></span>

<span data-ttu-id="2a6bf-414">Pesquisa no diretório</span><span class="sxs-lookup"><span data-stu-id="2a6bf-414">Directory Browse</span></span>

<span data-ttu-id="2a6bf-415">145</span><span class="sxs-lookup"><span data-stu-id="2a6bf-415">145</span></span>

<span data-ttu-id="2a6bf-416">Erros HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-416">HTTP Errors</span></span>

<span data-ttu-id="2a6bf-417">146</span><span class="sxs-lookup"><span data-stu-id="2a6bf-417">146</span></span>

<span data-ttu-id="2a6bf-418">Redirecionamento de HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-418">HTTP Redirection</span></span>

<span data-ttu-id="2a6bf-419">147</span><span class="sxs-lookup"><span data-stu-id="2a6bf-419">147</span></span>

<span data-ttu-id="2a6bf-420">Desenvolvimento de aplicativo</span><span class="sxs-lookup"><span data-stu-id="2a6bf-420">Application Development</span></span>

<span data-ttu-id="2a6bf-421">148</span><span class="sxs-lookup"><span data-stu-id="2a6bf-421">148</span></span>

<span data-ttu-id="2a6bf-422">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="2a6bf-422">ASP.NET</span></span>

<span data-ttu-id="2a6bf-423">149</span><span class="sxs-lookup"><span data-stu-id="2a6bf-423">149</span></span>

<span data-ttu-id="2a6bf-424">Extensibilidade .NET</span><span class="sxs-lookup"><span data-stu-id="2a6bf-424">.NET Extensibility</span></span>

<span data-ttu-id="2a6bf-425">150</span><span class="sxs-lookup"><span data-stu-id="2a6bf-425">150</span></span>

<span data-ttu-id="2a6bf-426">ASP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-426">ASP</span></span>

<span data-ttu-id="2a6bf-427">151</span><span class="sxs-lookup"><span data-stu-id="2a6bf-427">151</span></span>

<span data-ttu-id="2a6bf-428">CGI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-428">CGI</span></span>

<span data-ttu-id="2a6bf-429">152</span><span class="sxs-lookup"><span data-stu-id="2a6bf-429">152</span></span>

<span data-ttu-id="2a6bf-430">Extensões ISAPI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-430">ISAPI Extensions</span></span>

<span data-ttu-id="2a6bf-431">153</span><span class="sxs-lookup"><span data-stu-id="2a6bf-431">153</span></span>

<span data-ttu-id="2a6bf-432">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-432">ISAPI Filters</span></span>

<span data-ttu-id="2a6bf-433">154</span><span class="sxs-lookup"><span data-stu-id="2a6bf-433">154</span></span>

<span data-ttu-id="2a6bf-434">Server Side Includes</span><span class="sxs-lookup"><span data-stu-id="2a6bf-434">Server Side Includes</span></span>

<span data-ttu-id="2a6bf-435">155</span><span class="sxs-lookup"><span data-stu-id="2a6bf-435">155</span></span>

<span data-ttu-id="2a6bf-436">Integridade e diagnóstico</span><span class="sxs-lookup"><span data-stu-id="2a6bf-436">Health And Diagnostics</span></span>

<span data-ttu-id="2a6bf-437">156</span><span class="sxs-lookup"><span data-stu-id="2a6bf-437">156</span></span>

<span data-ttu-id="2a6bf-438">Log HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-438">HTTP Logging</span></span>

<span data-ttu-id="2a6bf-439">157</span><span class="sxs-lookup"><span data-stu-id="2a6bf-439">157</span></span>

<span data-ttu-id="2a6bf-440">Ferramentas de log</span><span class="sxs-lookup"><span data-stu-id="2a6bf-440">Logging Tools</span></span>

<span data-ttu-id="2a6bf-441">158</span><span class="sxs-lookup"><span data-stu-id="2a6bf-441">158</span></span>

<span data-ttu-id="2a6bf-442">Monitor de Solicitações</span><span class="sxs-lookup"><span data-stu-id="2a6bf-442">Request Monitor</span></span>

<span data-ttu-id="2a6bf-443">159</span><span class="sxs-lookup"><span data-stu-id="2a6bf-443">159</span></span>

<span data-ttu-id="2a6bf-444">Rastreamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-444">Tracing</span></span>

<span data-ttu-id="2a6bf-445">160</span><span class="sxs-lookup"><span data-stu-id="2a6bf-445">160</span></span>

<span data-ttu-id="2a6bf-446">Registro em log personalizado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-446">Custom Logging</span></span>

<span data-ttu-id="2a6bf-447">161</span><span class="sxs-lookup"><span data-stu-id="2a6bf-447">161</span></span>

<span data-ttu-id="2a6bf-448">Log de ODBC</span><span class="sxs-lookup"><span data-stu-id="2a6bf-448">ODBC Logging</span></span>

<span data-ttu-id="2a6bf-449">162</span><span class="sxs-lookup"><span data-stu-id="2a6bf-449">162</span></span>

<span data-ttu-id="2a6bf-450">Segurança</span><span class="sxs-lookup"><span data-stu-id="2a6bf-450">Security</span></span>

<span data-ttu-id="2a6bf-451">163</span><span class="sxs-lookup"><span data-stu-id="2a6bf-451">163</span></span>

<span data-ttu-id="2a6bf-452">Autenticação Básica</span><span class="sxs-lookup"><span data-stu-id="2a6bf-452">Basic Authentication</span></span>

<span data-ttu-id="2a6bf-453">164</span><span class="sxs-lookup"><span data-stu-id="2a6bf-453">164</span></span>

<span data-ttu-id="2a6bf-454">Autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-454">Windows Authentication</span></span>

<span data-ttu-id="2a6bf-455">165</span><span class="sxs-lookup"><span data-stu-id="2a6bf-455">165</span></span>

<span data-ttu-id="2a6bf-456">Autenticação Digest</span><span class="sxs-lookup"><span data-stu-id="2a6bf-456">Digest Authentication</span></span>

<span data-ttu-id="2a6bf-457">166</span><span class="sxs-lookup"><span data-stu-id="2a6bf-457">166</span></span>

<span data-ttu-id="2a6bf-458">Autenticação de mapeamento de certificado de cliente</span><span class="sxs-lookup"><span data-stu-id="2a6bf-458">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="2a6bf-459">167</span><span class="sxs-lookup"><span data-stu-id="2a6bf-459">167</span></span>

<span data-ttu-id="2a6bf-460">Autenticação de mapeamento de certificado do cliente IIS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-460">IIS Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="2a6bf-461">168</span><span class="sxs-lookup"><span data-stu-id="2a6bf-461">168</span></span>

<span data-ttu-id="2a6bf-462">Autorização de URL</span><span class="sxs-lookup"><span data-stu-id="2a6bf-462">URL Authorization</span></span>

<span data-ttu-id="2a6bf-463">169</span><span class="sxs-lookup"><span data-stu-id="2a6bf-463">169</span></span>

<span data-ttu-id="2a6bf-464">Filtragem de Solicitações</span><span class="sxs-lookup"><span data-stu-id="2a6bf-464">Request Filtering</span></span>

<span data-ttu-id="2a6bf-465">170</span><span class="sxs-lookup"><span data-stu-id="2a6bf-465">170</span></span>

<span data-ttu-id="2a6bf-466">Restrições de IP e domínio</span><span class="sxs-lookup"><span data-stu-id="2a6bf-466">IP And Domain Restrictions</span></span>

<span data-ttu-id="2a6bf-467">171</span><span class="sxs-lookup"><span data-stu-id="2a6bf-467">171</span></span>

<span data-ttu-id="2a6bf-468">Desempenho</span><span class="sxs-lookup"><span data-stu-id="2a6bf-468">Performance</span></span>

<span data-ttu-id="2a6bf-469">172</span><span class="sxs-lookup"><span data-stu-id="2a6bf-469">172</span></span>

<span data-ttu-id="2a6bf-470">Compactação de Conteúdo Estático</span><span class="sxs-lookup"><span data-stu-id="2a6bf-470">Static Content Compression</span></span>

<span data-ttu-id="2a6bf-471">173</span><span class="sxs-lookup"><span data-stu-id="2a6bf-471">173</span></span>

<span data-ttu-id="2a6bf-472">Compactação de Conteúdo Dinâmico</span><span class="sxs-lookup"><span data-stu-id="2a6bf-472">Dynamic Content Compression</span></span>

<span data-ttu-id="2a6bf-473">174</span><span class="sxs-lookup"><span data-stu-id="2a6bf-473">174</span></span>

<span data-ttu-id="2a6bf-474">Ferramentas de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-474">Management Tools</span></span>

<span data-ttu-id="2a6bf-475">175</span><span class="sxs-lookup"><span data-stu-id="2a6bf-475">175</span></span>

<span data-ttu-id="2a6bf-476">Console de Gerenciamento IIS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-476">IIS Management Console</span></span>

<span data-ttu-id="2a6bf-477">176</span><span class="sxs-lookup"><span data-stu-id="2a6bf-477">176</span></span>

<span data-ttu-id="2a6bf-478">Ferramentas e scripts de gerenciamento do IIS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-478">IIS Management Scripts And Tools</span></span>

<span data-ttu-id="2a6bf-479">177</span><span class="sxs-lookup"><span data-stu-id="2a6bf-479">177</span></span>

<span data-ttu-id="2a6bf-480">Management Service</span><span class="sxs-lookup"><span data-stu-id="2a6bf-480">Management Service</span></span>

<span data-ttu-id="2a6bf-481">178</span><span class="sxs-lookup"><span data-stu-id="2a6bf-481">178</span></span>

<span data-ttu-id="2a6bf-482">Compatibilidade de gerenciamento do IIS 6</span><span class="sxs-lookup"><span data-stu-id="2a6bf-482">IIS 6 Management Compatibility</span></span>

<span data-ttu-id="2a6bf-483">179</span><span class="sxs-lookup"><span data-stu-id="2a6bf-483">179</span></span>

<span data-ttu-id="2a6bf-484">Compatibilidade de Metabase do IIS 6</span><span class="sxs-lookup"><span data-stu-id="2a6bf-484">IIS 6 Metabase Compatibility</span></span>

<span data-ttu-id="2a6bf-485">180</span><span class="sxs-lookup"><span data-stu-id="2a6bf-485">180</span></span>

<span data-ttu-id="2a6bf-486">Compatibilidade de WMI do IIS 6</span><span class="sxs-lookup"><span data-stu-id="2a6bf-486">IIS 6 WMI Compatibility</span></span>

<span data-ttu-id="2a6bf-487">181</span><span class="sxs-lookup"><span data-stu-id="2a6bf-487">181</span></span>

<span data-ttu-id="2a6bf-488">Ferramentas de script do IIS 6</span><span class="sxs-lookup"><span data-stu-id="2a6bf-488">IIS 6 Scripting Tools</span></span>

<span data-ttu-id="2a6bf-489">182</span><span class="sxs-lookup"><span data-stu-id="2a6bf-489">182</span></span>

<span data-ttu-id="2a6bf-490">Console de gerenciamento do IIS 6</span><span class="sxs-lookup"><span data-stu-id="2a6bf-490">IIS 6 Management Console</span></span>

<span data-ttu-id="2a6bf-491">183</span><span class="sxs-lookup"><span data-stu-id="2a6bf-491">183</span></span>

<span data-ttu-id="2a6bf-492">Serviço de Publicação FTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-492">FTP Publishing Service</span></span><br/>

<span data-ttu-id="2a6bf-493">184</span><span class="sxs-lookup"><span data-stu-id="2a6bf-493">184</span></span>

<span data-ttu-id="2a6bf-494">Servidor FTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-494">FTP Server</span></span>

<span data-ttu-id="2a6bf-495">185</span><span class="sxs-lookup"><span data-stu-id="2a6bf-495">185</span></span>

<span data-ttu-id="2a6bf-496">Console de Gerenciamento do FTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-496">FTP Management Console</span></span><br/>

<span data-ttu-id="2a6bf-497">314</span><span class="sxs-lookup"><span data-stu-id="2a6bf-497">314</span></span>

<span data-ttu-id="2a6bf-498">Publicação de WebDAV</span><span class="sxs-lookup"><span data-stu-id="2a6bf-498">WebDAV Publishing</span></span>

<span data-ttu-id="2a6bf-499">316</span><span class="sxs-lookup"><span data-stu-id="2a6bf-499">316</span></span>

<span data-ttu-id="2a6bf-500">Serviço de FTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-500">FTP Service</span></span><br/>

<span data-ttu-id="2a6bf-501">317</span><span class="sxs-lookup"><span data-stu-id="2a6bf-501">317</span></span>

<span data-ttu-id="2a6bf-502">Extensibilidade de FTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-502">FTP Extensibility</span></span><br/>

<span data-ttu-id="2a6bf-503">336</span><span class="sxs-lookup"><span data-stu-id="2a6bf-503">336</span></span>

<span data-ttu-id="2a6bf-504">Núcleo da Web Hospedável do IIS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-504">IIS Hostable Web Core</span></span><br/>

<span data-ttu-id="2a6bf-505">413</span><span class="sxs-lookup"><span data-stu-id="2a6bf-505">413</span></span>

[<span data-ttu-id="2a6bf-506">ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-506">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="2a6bf-507">414</span><span class="sxs-lookup"><span data-stu-id="2a6bf-507">414</span></span>

[<span data-ttu-id="2a6bf-508">Extensibilidade 4.5 do .NET</span><span class="sxs-lookup"><span data-stu-id="2a6bf-508">.NET Extensibility 4.5</span></span>](/windows)

<span data-ttu-id="2a6bf-509">445</span><span class="sxs-lookup"><span data-stu-id="2a6bf-509">445</span></span>

[<span data-ttu-id="2a6bf-510">appialization</span><span class="sxs-lookup"><span data-stu-id="2a6bf-510">appialization</span></span>](/windows)

<span data-ttu-id="2a6bf-511">446</span><span class="sxs-lookup"><span data-stu-id="2a6bf-511">446</span></span>

[<span data-ttu-id="2a6bf-512">Suporte Centralizado a Certificado SSL</span><span class="sxs-lookup"><span data-stu-id="2a6bf-512">Centralized SSL Certificate Support</span></span>](/windows)

<span data-ttu-id="2a6bf-513">447</span><span class="sxs-lookup"><span data-stu-id="2a6bf-513">447</span></span>

[<span data-ttu-id="2a6bf-514">Protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="2a6bf-514">WebSocket Protocol</span></span>](/windows)

<span data-ttu-id="2a6bf-515">Enfileiramento de mensagens-recursos (49)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-515">Message Queuing - Features (49)</span></span>

<span data-ttu-id="2a6bf-516">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-516">Value</span></span>

<span data-ttu-id="2a6bf-517">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-517">Name</span></span>

<span data-ttu-id="2a6bf-518">190</span><span class="sxs-lookup"><span data-stu-id="2a6bf-518">190</span></span>

<span data-ttu-id="2a6bf-519">Serviços de enfileiramento de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a6bf-519">Message Queuing Services</span></span>

<span data-ttu-id="2a6bf-520">191</span><span class="sxs-lookup"><span data-stu-id="2a6bf-520">191</span></span>

<span data-ttu-id="2a6bf-521">Servidor de enfileiramento de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a6bf-521">Message Queuing Server</span></span>

<span data-ttu-id="2a6bf-522">192</span><span class="sxs-lookup"><span data-stu-id="2a6bf-522">192</span></span>

<span data-ttu-id="2a6bf-523">Integração de Serviços de Diretório</span><span class="sxs-lookup"><span data-stu-id="2a6bf-523">Directory Service Integration</span></span>

<span data-ttu-id="2a6bf-524">193</span><span class="sxs-lookup"><span data-stu-id="2a6bf-524">193</span></span>

<span data-ttu-id="2a6bf-525">Gatilhos de enfileiramento de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a6bf-525">Message Queuing Triggers</span></span>

<span data-ttu-id="2a6bf-526">194</span><span class="sxs-lookup"><span data-stu-id="2a6bf-526">194</span></span>

<span data-ttu-id="2a6bf-527">Suporte a HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-527">HTTP Support</span></span>

<span data-ttu-id="2a6bf-528">195</span><span class="sxs-lookup"><span data-stu-id="2a6bf-528">195</span></span>

<span data-ttu-id="2a6bf-529">Serviço de roteamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-529">Routing Service</span></span>

<span data-ttu-id="2a6bf-530">196</span><span class="sxs-lookup"><span data-stu-id="2a6bf-530">196</span></span>

[<span data-ttu-id="2a6bf-531">Suporte ao cliente do Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2a6bf-531">Windows 2000 Client Support</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-532">197</span><span class="sxs-lookup"><span data-stu-id="2a6bf-532">197</span></span>

<span data-ttu-id="2a6bf-533">Proxy DCOM do Serviço de Enfileiramento de Mensagens</span><span class="sxs-lookup"><span data-stu-id="2a6bf-533">Message Queuing DCOM Proxy</span></span>

<span data-ttu-id="2a6bf-534">228</span><span class="sxs-lookup"><span data-stu-id="2a6bf-534">228</span></span>

<span data-ttu-id="2a6bf-535">Suporte a multicast</span><span class="sxs-lookup"><span data-stu-id="2a6bf-535">Multicasting Support</span></span>

<span data-ttu-id="2a6bf-536">Serviços de certificados Active Directory – serviços de função (16)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-536">Active Directory Certificate Services - Role Services (16)</span></span>

<span data-ttu-id="2a6bf-537">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-537">Value</span></span>

<span data-ttu-id="2a6bf-538">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-538">Name</span></span>

<span data-ttu-id="2a6bf-539">200</span><span class="sxs-lookup"><span data-stu-id="2a6bf-539">200</span></span>

<span data-ttu-id="2a6bf-540">Autoridade de certificação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-540">Certification Authority</span></span>

<span data-ttu-id="2a6bf-541">201</span><span class="sxs-lookup"><span data-stu-id="2a6bf-541">201</span></span>

<span data-ttu-id="2a6bf-542">Registro na Web de Autoridade de Certificação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-542">Certification Authority Web Enrollment</span></span>

<span data-ttu-id="2a6bf-543">202</span><span class="sxs-lookup"><span data-stu-id="2a6bf-543">202</span></span>

<span data-ttu-id="2a6bf-544">Respondente Online</span><span class="sxs-lookup"><span data-stu-id="2a6bf-544">Online Responder</span></span>

<span data-ttu-id="2a6bf-545">204</span><span class="sxs-lookup"><span data-stu-id="2a6bf-545">204</span></span>

<span data-ttu-id="2a6bf-546">Serviço de Inscrição do Dispositivo de Rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-546">Network Device Enrollment Service</span></span>

<span data-ttu-id="2a6bf-547">318</span><span class="sxs-lookup"><span data-stu-id="2a6bf-547">318</span></span>

[<span data-ttu-id="2a6bf-548">Serviço Web de Registro de Certificado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-548">Certificate Enrollment Web Service</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-549">319</span><span class="sxs-lookup"><span data-stu-id="2a6bf-549">319</span></span>

[<span data-ttu-id="2a6bf-550">Serviço Web de Política de Registro de Certificado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-550">Certificate Enrollment Policy Web Service</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-551">Serviços de acesso e política de rede – serviços de função (14)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-551">Network Policy and Access Services - Role Services (14)</span></span>

<span data-ttu-id="2a6bf-552">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-552">Value</span></span>

<span data-ttu-id="2a6bf-553">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-553">Name</span></span>

<span data-ttu-id="2a6bf-554">205</span><span class="sxs-lookup"><span data-stu-id="2a6bf-554">205</span></span>

[<span data-ttu-id="2a6bf-555">Servidor de Políticas de Rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-555">Network Policy Server</span></span>](/windows)

<span data-ttu-id="2a6bf-556">206</span><span class="sxs-lookup"><span data-stu-id="2a6bf-556">206</span></span>

[<span data-ttu-id="2a6bf-557">VPN</span><span class="sxs-lookup"><span data-stu-id="2a6bf-557">VPN</span></span>](#vpn)

<span data-ttu-id="2a6bf-558">207</span><span class="sxs-lookup"><span data-stu-id="2a6bf-558">207</span></span>

[<span data-ttu-id="2a6bf-559">Serviços de acesso remoto</span><span class="sxs-lookup"><span data-stu-id="2a6bf-559">Remote Access Services</span></span>](/windows)

<span data-ttu-id="2a6bf-560">208</span><span class="sxs-lookup"><span data-stu-id="2a6bf-560">208</span></span>

[<span data-ttu-id="2a6bf-561">Roteamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-561">Routing</span></span>](#routing)

<span data-ttu-id="2a6bf-562">210</span><span class="sxs-lookup"><span data-stu-id="2a6bf-562">210</span></span>

[<span data-ttu-id="2a6bf-563">Autoridade de Registro de Integridade</span><span class="sxs-lookup"><span data-stu-id="2a6bf-563">Health Registration Authority</span></span>](/windows)

<span data-ttu-id="2a6bf-564">250</span><span class="sxs-lookup"><span data-stu-id="2a6bf-564">250</span></span>

[<span data-ttu-id="2a6bf-565">Protocolo de autorização de credenciais do host</span><span class="sxs-lookup"><span data-stu-id="2a6bf-565">Host Credential Authorization Protocol</span></span>](/windows)

<span data-ttu-id="2a6bf-566">Serviços UDDI – serviços de função (11)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-566">UDDI Services - Role Services (11)</span></span>

<span data-ttu-id="2a6bf-567">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-567">Value</span></span>

<span data-ttu-id="2a6bf-568">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-568">Name</span></span>

<span data-ttu-id="2a6bf-569">215</span><span class="sxs-lookup"><span data-stu-id="2a6bf-569">215</span></span>

[<span data-ttu-id="2a6bf-570">Aplicativo Web dos serviços UDDI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-570">UDDI Services Web Application</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-571">216</span><span class="sxs-lookup"><span data-stu-id="2a6bf-571">216</span></span>

[<span data-ttu-id="2a6bf-572">Banco de dados dos serviços UDDI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-572">UDDI Services Database</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-573">Serviço de ativação de processos do Windows – serviços de função (41)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-573">Windows Process Activation Service - Role Services (41)</span></span>

<span data-ttu-id="2a6bf-574">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-574">Value</span></span>

<span data-ttu-id="2a6bf-575">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-575">Name</span></span>

<span data-ttu-id="2a6bf-576">217</span><span class="sxs-lookup"><span data-stu-id="2a6bf-576">217</span></span>

<span data-ttu-id="2a6bf-577">API de configuração</span><span class="sxs-lookup"><span data-stu-id="2a6bf-577">Configuration API</span></span>

<span data-ttu-id="2a6bf-578">218</span><span class="sxs-lookup"><span data-stu-id="2a6bf-578">218</span></span>

<span data-ttu-id="2a6bf-579">Ambiente .NET</span><span class="sxs-lookup"><span data-stu-id="2a6bf-579">.NET Environment</span></span>

<span data-ttu-id="2a6bf-580">219</span><span class="sxs-lookup"><span data-stu-id="2a6bf-580">219</span></span>

<span data-ttu-id="2a6bf-581">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="2a6bf-581">Process Model</span></span>

<span data-ttu-id="2a6bf-582">.NET Framework 3.5.1-recursos (36)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-582">.NET Framework 3.5.1 - Features (36)</span></span>

<span data-ttu-id="2a6bf-583">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-583">Value</span></span>

<span data-ttu-id="2a6bf-584">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-584">Name</span></span>

<span data-ttu-id="2a6bf-585">220</span><span class="sxs-lookup"><span data-stu-id="2a6bf-585">220</span></span>

<span data-ttu-id="2a6bf-586">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="2a6bf-586">.NET Framework 3.5.1</span></span><br/> [<span data-ttu-id="2a6bf-587">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-587">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-588">221</span><span class="sxs-lookup"><span data-stu-id="2a6bf-588">221</span></span>

<span data-ttu-id="2a6bf-589">Ativação de WCF</span><span class="sxs-lookup"><span data-stu-id="2a6bf-589">WCF Activation</span></span>

<span data-ttu-id="2a6bf-590">222</span><span class="sxs-lookup"><span data-stu-id="2a6bf-590">222</span></span>

<span data-ttu-id="2a6bf-591">Ativação HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-591">HTTP Activation</span></span>

<span data-ttu-id="2a6bf-592">223</span><span class="sxs-lookup"><span data-stu-id="2a6bf-592">223</span></span>

<span data-ttu-id="2a6bf-593">Ativação não HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-593">Non-HTTP Activation</span></span>

<span data-ttu-id="2a6bf-594">227</span><span class="sxs-lookup"><span data-stu-id="2a6bf-594">227</span></span>

<span data-ttu-id="2a6bf-595">Visualizador XPS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-595">XPS Viewer</span></span><br/>

<span data-ttu-id="2a6bf-596">Serviços SNMP-recursos (59)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-596">SNMP Services - Features (59)</span></span>

<span data-ttu-id="2a6bf-597">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-597">Value</span></span>

<span data-ttu-id="2a6bf-598">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-598">Name</span></span>

<span data-ttu-id="2a6bf-599">224</span><span class="sxs-lookup"><span data-stu-id="2a6bf-599">224</span></span>

[<span data-ttu-id="2a6bf-600">Serviço SNMP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-600">SNMP Service</span></span>](/windows)

<span data-ttu-id="2a6bf-601">225</span><span class="sxs-lookup"><span data-stu-id="2a6bf-601">225</span></span>

[<span data-ttu-id="2a6bf-602">Provedor WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-602">SNMP WMI Provider</span></span>](/windows)

<span data-ttu-id="2a6bf-603">Serviços de Serviços de Aplicativos função</span><span class="sxs-lookup"><span data-stu-id="2a6bf-603">Application Services - Role Services</span></span>

<span data-ttu-id="2a6bf-604">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-604">Value</span></span>

<span data-ttu-id="2a6bf-605">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-605">Name</span></span>

<span data-ttu-id="2a6bf-606">230</span><span class="sxs-lookup"><span data-stu-id="2a6bf-606">230</span></span>

[<span data-ttu-id="2a6bf-607">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="2a6bf-607">.NET Framework 3.5.1</span></span>](/windows)<br/> [<span data-ttu-id="2a6bf-608">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-608">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-609">231</span><span class="sxs-lookup"><span data-stu-id="2a6bf-609">231</span></span>

[<span data-ttu-id="2a6bf-610">Suporte do Servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-610">Web Server (IIS) Support</span></span>](/windows)

<span data-ttu-id="2a6bf-611">232</span><span class="sxs-lookup"><span data-stu-id="2a6bf-611">232</span></span>

[<span data-ttu-id="2a6bf-612">Acesso à rede COM+</span><span class="sxs-lookup"><span data-stu-id="2a6bf-612">COM+ Network Access</span></span>](/windows)

<span data-ttu-id="2a6bf-613">233</span><span class="sxs-lookup"><span data-stu-id="2a6bf-613">233</span></span>

[<span data-ttu-id="2a6bf-614">Compartilhamento de porta TCP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-614">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="2a6bf-615">234</span><span class="sxs-lookup"><span data-stu-id="2a6bf-615">234</span></span>

[<span data-ttu-id="2a6bf-616">Suporte ao serviço de ativação de processos do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-616">Windows Process Activation Service Support</span></span>](/windows)

<span data-ttu-id="2a6bf-617">235</span><span class="sxs-lookup"><span data-stu-id="2a6bf-617">235</span></span>

[<span data-ttu-id="2a6bf-618">Ativação HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-618">HTTP Activation</span></span>](/windows)

<span data-ttu-id="2a6bf-619">236</span><span class="sxs-lookup"><span data-stu-id="2a6bf-619">236</span></span>

[<span data-ttu-id="2a6bf-620">Ativação do enfileiramento de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a6bf-620">Message Queuing Activation</span></span>](/windows)

<span data-ttu-id="2a6bf-621">237</span><span class="sxs-lookup"><span data-stu-id="2a6bf-621">237</span></span>

[<span data-ttu-id="2a6bf-622">Ativação TCP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-622">TCP Activation</span></span>](/windows)

<span data-ttu-id="2a6bf-623">238</span><span class="sxs-lookup"><span data-stu-id="2a6bf-623">238</span></span>

[<span data-ttu-id="2a6bf-624">Ativação de pipes nomeados</span><span class="sxs-lookup"><span data-stu-id="2a6bf-624">Named Pipes Activation</span></span>](/windows)

<span data-ttu-id="2a6bf-625">239</span><span class="sxs-lookup"><span data-stu-id="2a6bf-625">239</span></span>

[<span data-ttu-id="2a6bf-626">Transações distribuídas</span><span class="sxs-lookup"><span data-stu-id="2a6bf-626">Distributed Transactions</span></span>](/windows)

<span data-ttu-id="2a6bf-627">240</span><span class="sxs-lookup"><span data-stu-id="2a6bf-627">240</span></span>

[<span data-ttu-id="2a6bf-628">Transações remotas de entrada</span><span class="sxs-lookup"><span data-stu-id="2a6bf-628">Incoming Remote Transactions</span></span>](/windows)

<span data-ttu-id="2a6bf-629">241</span><span class="sxs-lookup"><span data-stu-id="2a6bf-629">241</span></span>

[<span data-ttu-id="2a6bf-630">Transações remotas de saída</span><span class="sxs-lookup"><span data-stu-id="2a6bf-630">Outgoing Remote Transactions</span></span>](/windows)

<span data-ttu-id="2a6bf-631">242</span><span class="sxs-lookup"><span data-stu-id="2a6bf-631">242</span></span>

[<span data-ttu-id="2a6bf-632">WS-transações automáticas</span><span class="sxs-lookup"><span data-stu-id="2a6bf-632">WS-Automatic Transactions</span></span>](/windows)

<span data-ttu-id="2a6bf-633">353</span><span class="sxs-lookup"><span data-stu-id="2a6bf-633">353</span></span>

[<span data-ttu-id="2a6bf-634">Extensões do servidor de aplicativos para .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="2a6bf-634">Application Server Extensions for .NET 4.0</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-635">Serviços de implantação do Windows-função (19)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-635">Windows Deployment Services - Role (19)</span></span>

<span data-ttu-id="2a6bf-636">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-636">Value</span></span>

<span data-ttu-id="2a6bf-637">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-637">Name</span></span>

<span data-ttu-id="2a6bf-638">251</span><span class="sxs-lookup"><span data-stu-id="2a6bf-638">251</span></span>

<span data-ttu-id="2a6bf-639">Servidor de Implantação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-639">Deployment Server</span></span>

<span data-ttu-id="2a6bf-640">252</span><span class="sxs-lookup"><span data-stu-id="2a6bf-640">252</span></span>

<span data-ttu-id="2a6bf-641">Servidor de Transporte</span><span class="sxs-lookup"><span data-stu-id="2a6bf-641">Transport Server</span></span>

<span data-ttu-id="2a6bf-642">Serviços de função de Active Directory Rights Management Services (17)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-642">Active Directory Rights Management Services - Role Services (17)</span></span>

<span data-ttu-id="2a6bf-643">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-643">Value</span></span>

<span data-ttu-id="2a6bf-644">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-644">Name</span></span>

<span data-ttu-id="2a6bf-645">253</span><span class="sxs-lookup"><span data-stu-id="2a6bf-645">253</span></span>

<span data-ttu-id="2a6bf-646">Servidor de Gerenciamento de Direitos do Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a6bf-646">Active Directory Rights Management Server</span></span>

<span data-ttu-id="2a6bf-647">254</span><span class="sxs-lookup"><span data-stu-id="2a6bf-647">254</span></span>

<span data-ttu-id="2a6bf-648">Suporte à Federação de Identidade</span><span class="sxs-lookup"><span data-stu-id="2a6bf-648">Identity Federation Support</span></span>

<span data-ttu-id="2a6bf-649">Ferramentas de Administração de Servidor Remoto (67)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-649">Remote Server Administration Tools (67)</span></span>

<span data-ttu-id="2a6bf-650">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-650">Value</span></span>

<span data-ttu-id="2a6bf-651">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-651">Name</span></span>

<span data-ttu-id="2a6bf-652">256</span><span class="sxs-lookup"><span data-stu-id="2a6bf-652">256</span></span>

[<span data-ttu-id="2a6bf-653">Ferramentas de administração de funções</span><span class="sxs-lookup"><span data-stu-id="2a6bf-653">Role Administration Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-654">257</span><span class="sxs-lookup"><span data-stu-id="2a6bf-654">257</span></span>

[<span data-ttu-id="2a6bf-655">Ferramentas de AD DS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-655">AD DS Tools</span></span>](/windows)<br/> [<span data-ttu-id="2a6bf-656">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-656">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-657">258</span><span class="sxs-lookup"><span data-stu-id="2a6bf-657">258</span></span>

[<span data-ttu-id="2a6bf-658">Ferramentas de Snap-Ins e Command-Line de AD LDS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-658">AD LDS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="2a6bf-659">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-659">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-660">259</span><span class="sxs-lookup"><span data-stu-id="2a6bf-660">259</span></span>

<span data-ttu-id="2a6bf-661">Ferramentas de Serviços de Certificados do Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a6bf-661">Active Directory Certificate Services Tools</span></span>

<span data-ttu-id="2a6bf-662">260</span><span class="sxs-lookup"><span data-stu-id="2a6bf-662">260</span></span>

[<span data-ttu-id="2a6bf-663">Network Policy and Access Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-663">Network Policy and Access Services</span></span>](/windows)

<span data-ttu-id="2a6bf-664">261</span><span class="sxs-lookup"><span data-stu-id="2a6bf-664">261</span></span>

<span data-ttu-id="2a6bf-665">Ferramentas de Serviços de Impressão e Documentos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-665">Print and Document Services Tools</span></span><br/> [<span data-ttu-id="2a6bf-666">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-666">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-667">262</span><span class="sxs-lookup"><span data-stu-id="2a6bf-667">262</span></span>

[<span data-ttu-id="2a6bf-668">Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-668">Active Directory Rights Management Services</span></span>](/windows)

<span data-ttu-id="2a6bf-669">263</span><span class="sxs-lookup"><span data-stu-id="2a6bf-669">263</span></span>

[<span data-ttu-id="2a6bf-670">Ferramentas de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-670">Remote Desktop Services Tools</span></span>](/windows)<br/> [<span data-ttu-id="2a6bf-671">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-671">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-672">264</span><span class="sxs-lookup"><span data-stu-id="2a6bf-672">264</span></span>

<span data-ttu-id="2a6bf-673">Ferramentas de serviços de implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-673">Windows Deployment Services Tools</span></span>

<span data-ttu-id="2a6bf-674">265</span><span class="sxs-lookup"><span data-stu-id="2a6bf-674">265</span></span>

[<span data-ttu-id="2a6bf-675">Ferramentas de administração do recurso</span><span class="sxs-lookup"><span data-stu-id="2a6bf-675">Feature Administration Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-676">266</span><span class="sxs-lookup"><span data-stu-id="2a6bf-676">266</span></span>

<span data-ttu-id="2a6bf-677">BitLocker Drive Encryption Tools</span><span class="sxs-lookup"><span data-stu-id="2a6bf-677">BitLocker Drive Encryption Tools</span></span>

<span data-ttu-id="2a6bf-678">267</span><span class="sxs-lookup"><span data-stu-id="2a6bf-678">267</span></span>

<span data-ttu-id="2a6bf-679">Ferramentas de extensões de servidor BITS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-679">BITS Server Extensions Tools</span></span>

<span data-ttu-id="2a6bf-680">268</span><span class="sxs-lookup"><span data-stu-id="2a6bf-680">268</span></span>

[<span data-ttu-id="2a6bf-681">Ferramentas de cluster de failover</span><span class="sxs-lookup"><span data-stu-id="2a6bf-681">Failover Clustering Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-682">269</span><span class="sxs-lookup"><span data-stu-id="2a6bf-682">269</span></span>

<span data-ttu-id="2a6bf-683">Ferramentas de Balanceamento de Carga de Rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-683">Network Load Balancing Tools</span></span>

<span data-ttu-id="2a6bf-684">270</span><span class="sxs-lookup"><span data-stu-id="2a6bf-684">270</span></span>

<span data-ttu-id="2a6bf-685">Ferramentas de servidor SMTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-685">SMTP Server Tools</span></span>

<span data-ttu-id="2a6bf-686">273</span><span class="sxs-lookup"><span data-stu-id="2a6bf-686">273</span></span>

[<span data-ttu-id="2a6bf-687">Ferramentas de servidor DNS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-687">DNS Server Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-688">277</span><span class="sxs-lookup"><span data-stu-id="2a6bf-688">277</span></span>

<span data-ttu-id="2a6bf-689">Ferramentas de serviços de arquivo</span><span class="sxs-lookup"><span data-stu-id="2a6bf-689">File Services Tools</span></span>

<span data-ttu-id="2a6bf-690">278</span><span class="sxs-lookup"><span data-stu-id="2a6bf-690">278</span></span>

<span data-ttu-id="2a6bf-691">Ferramentas de Sistema de Arquivos Distribuído</span><span class="sxs-lookup"><span data-stu-id="2a6bf-691">Distributed File System Tools</span></span>

<span data-ttu-id="2a6bf-692">279</span><span class="sxs-lookup"><span data-stu-id="2a6bf-692">279</span></span>

<span data-ttu-id="2a6bf-693">Ferramentas do Gerenciador de Recursos de Servidor de Arquivos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-693">File Server Resource Manager Tools</span></span>

<span data-ttu-id="2a6bf-694">280</span><span class="sxs-lookup"><span data-stu-id="2a6bf-694">280</span></span>

[<span data-ttu-id="2a6bf-695">Serviços para ferramentas do sistema de arquivos de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-695">Services For Network File System Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-696">281</span><span class="sxs-lookup"><span data-stu-id="2a6bf-696">281</span></span>

<span data-ttu-id="2a6bf-697">Ferramentas do servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-697">Web Server (IIS) Tools</span></span>

<span data-ttu-id="2a6bf-698">284</span><span class="sxs-lookup"><span data-stu-id="2a6bf-698">284</span></span>

[<span data-ttu-id="2a6bf-699">Ferramentas de Host da Sessão da Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-699">Remote Desktop Session Host Tools</span></span>](/windows)<br/> [<span data-ttu-id="2a6bf-700">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-700">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-701">285</span><span class="sxs-lookup"><span data-stu-id="2a6bf-701">285</span></span>

<span data-ttu-id="2a6bf-702">Ferramentas de gateway Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-702">Remote Desktop Gateway Tools</span></span><br/> [<span data-ttu-id="2a6bf-703">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-703">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-704">286</span><span class="sxs-lookup"><span data-stu-id="2a6bf-704">286</span></span>

<span data-ttu-id="2a6bf-705">Ferramentas de licenciamento Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-705">Remote Desktop Licensing Tools</span></span><br/> [<span data-ttu-id="2a6bf-706">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-706">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-707">288</span><span class="sxs-lookup"><span data-stu-id="2a6bf-707">288</span></span>

<span data-ttu-id="2a6bf-708">Ferramentas de servidor de fax</span><span class="sxs-lookup"><span data-stu-id="2a6bf-708">Fax Server Tools</span></span>

<span data-ttu-id="2a6bf-709">290</span><span class="sxs-lookup"><span data-stu-id="2a6bf-709">290</span></span>

<span data-ttu-id="2a6bf-710">Ferramentas de servidor WINS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-710">WINS Server Tools</span></span>

<span data-ttu-id="2a6bf-711">291</span><span class="sxs-lookup"><span data-stu-id="2a6bf-711">291</span></span>

[<span data-ttu-id="2a6bf-712">Ferramentas dos serviços UDDI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-712">UDDI Services Tools</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-713">292</span><span class="sxs-lookup"><span data-stu-id="2a6bf-713">292</span></span>

<span data-ttu-id="2a6bf-714">Ferramentas de autoridade de certificação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-714">Certification Authority Tools</span></span>

<span data-ttu-id="2a6bf-715">293</span><span class="sxs-lookup"><span data-stu-id="2a6bf-715">293</span></span>

<span data-ttu-id="2a6bf-716">Ferramentas de Respondente Online</span><span class="sxs-lookup"><span data-stu-id="2a6bf-716">Online Responder Tools</span></span>

<span data-ttu-id="2a6bf-717">297</span><span class="sxs-lookup"><span data-stu-id="2a6bf-717">297</span></span>

[<span data-ttu-id="2a6bf-718">Ferramentas de Servidor para NIS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-718">Server for NIS Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-719">299</span><span class="sxs-lookup"><span data-stu-id="2a6bf-719">299</span></span>

[<span data-ttu-id="2a6bf-720">Snap-ins AD DS e Ferrramentas de linha de comando</span><span class="sxs-lookup"><span data-stu-id="2a6bf-720">AD DS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="2a6bf-721">alteração de nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-721">name change</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-722">300</span><span class="sxs-lookup"><span data-stu-id="2a6bf-722">300</span></span>

[<span data-ttu-id="2a6bf-723">Centro Administrativo do Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a6bf-723">Active Directory Administrative Center</span></span>](/windows)

<span data-ttu-id="2a6bf-724">301</span><span class="sxs-lookup"><span data-stu-id="2a6bf-724">301</span></span>

<span data-ttu-id="2a6bf-725">Ferramentas do Hyper-V</span><span class="sxs-lookup"><span data-stu-id="2a6bf-725">Hyper-V Tools</span></span>

<span data-ttu-id="2a6bf-726">323</span><span class="sxs-lookup"><span data-stu-id="2a6bf-726">323</span></span>

[<span data-ttu-id="2a6bf-727">Visualizador de senha de recuperação do BitLocker</span><span class="sxs-lookup"><span data-stu-id="2a6bf-727">BitLocker Recovery Password Viewer</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-728">326</span><span class="sxs-lookup"><span data-stu-id="2a6bf-728">326</span></span>

[<span data-ttu-id="2a6bf-729">BitLocker Drive Encryption Administration Utilities</span><span class="sxs-lookup"><span data-stu-id="2a6bf-729">BitLocker Drive Encryption Administration Utilities</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-730">329</span><span class="sxs-lookup"><span data-stu-id="2a6bf-730">329</span></span>

[<span data-ttu-id="2a6bf-731">Ferramentas AD DS e AD LDS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-731">AD DS and AD LDS Tools</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-732">330</span><span class="sxs-lookup"><span data-stu-id="2a6bf-732">330</span></span>

<span data-ttu-id="2a6bf-733">Centro Administrativo do Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a6bf-733">Active Directory Administrative Center</span></span><br/>

<span data-ttu-id="2a6bf-734">331</span><span class="sxs-lookup"><span data-stu-id="2a6bf-734">331</span></span>

[<span data-ttu-id="2a6bf-735">Módulo do Active Directory para o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-735">Active Directory module for Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-736">337</span><span class="sxs-lookup"><span data-stu-id="2a6bf-736">337</span></span>

[<span data-ttu-id="2a6bf-737">Ferramentas do agente de Conexão de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-737">Remote Desktop Connection Broker Tools</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-738">410</span><span class="sxs-lookup"><span data-stu-id="2a6bf-738">410</span></span>

[<span data-ttu-id="2a6bf-739">Cliente IPAM (gerenciamento de endereços IP)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-739">IP Address Management (IPAM) Client</span></span>](/windows)

<span data-ttu-id="2a6bf-740">450</span><span class="sxs-lookup"><span data-stu-id="2a6bf-740">450</span></span>

[<span data-ttu-id="2a6bf-741">Módulo Hyper-V para o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-741">Hyper-V Module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="2a6bf-742">462</span><span class="sxs-lookup"><span data-stu-id="2a6bf-742">462</span></span>

[<span data-ttu-id="2a6bf-743">Ferramentas de Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-743">Active Directory Rights Management Services Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-744">465</span><span class="sxs-lookup"><span data-stu-id="2a6bf-744">465</span></span>

[<span data-ttu-id="2a6bf-745">Ferramenta de gerenciamento de compartilhamento e armazenamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-745">Share and Storage Management Tool</span></span>](/windows)

<span data-ttu-id="2a6bf-746">471</span><span class="sxs-lookup"><span data-stu-id="2a6bf-746">471</span></span>

[<span data-ttu-id="2a6bf-747">Ferramentas de Gerenciamento de Acesso Remoto</span><span class="sxs-lookup"><span data-stu-id="2a6bf-747">Remote Access Management Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-748">472</span><span class="sxs-lookup"><span data-stu-id="2a6bf-748">472</span></span>

[<span data-ttu-id="2a6bf-749">Módulo de Acesso Remoto para o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-749">Remote Access module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="2a6bf-750">473</span><span class="sxs-lookup"><span data-stu-id="2a6bf-750">473</span></span>

[<span data-ttu-id="2a6bf-751">GUI de acesso remoto e ferramentas de Command-Line</span><span class="sxs-lookup"><span data-stu-id="2a6bf-751">Remote Access GUI and Command-Line Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-752">474</span><span class="sxs-lookup"><span data-stu-id="2a6bf-752">474</span></span>

[<span data-ttu-id="2a6bf-753">Ferramentas do Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-753">Windows Server Update Services Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-754">476</span><span class="sxs-lookup"><span data-stu-id="2a6bf-754">476</span></span>

[<span data-ttu-id="2a6bf-755">Ferramentas do diagnosticador de licenciamento Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-755">Remote Desktop Licensing Diagnoser Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-756">479</span><span class="sxs-lookup"><span data-stu-id="2a6bf-756">479</span></span>

[<span data-ttu-id="2a6bf-757">Ferramentas SNMP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-757">SNMP Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-758">480</span><span class="sxs-lookup"><span data-stu-id="2a6bf-758">480</span></span>

[<span data-ttu-id="2a6bf-759">Ferramentas de ativação de volume</span><span class="sxs-lookup"><span data-stu-id="2a6bf-759">Volume Activation Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-760">Backup do Windows Server-recursos (39)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-760">Windows Server Backup - Features (39)</span></span>

<span data-ttu-id="2a6bf-761">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-761">Value</span></span>

<span data-ttu-id="2a6bf-762">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-762">Name</span></span>

<span data-ttu-id="2a6bf-763">296</span><span class="sxs-lookup"><span data-stu-id="2a6bf-763">296</span></span>

[<span data-ttu-id="2a6bf-764">Backup do Windows Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-764">Windows Server Backup</span></span>](/windows)

<span data-ttu-id="2a6bf-765">297</span><span class="sxs-lookup"><span data-stu-id="2a6bf-765">297</span></span>

[<span data-ttu-id="2a6bf-766">Ferramentas de linha de comando</span><span class="sxs-lookup"><span data-stu-id="2a6bf-766">Command Line Tools</span></span>](/windows)

<span data-ttu-id="2a6bf-767">Serviços de Reconhecimento de Manuscrito-recursos (310)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-767">Ink and Handwriting Services - Features (310)</span></span>

<span data-ttu-id="2a6bf-768">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-768">Value</span></span>

<span data-ttu-id="2a6bf-769">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-769">Name</span></span>

<span data-ttu-id="2a6bf-770">311</span><span class="sxs-lookup"><span data-stu-id="2a6bf-770">311</span></span>

[<span data-ttu-id="2a6bf-771">Suporte à tinta</span><span class="sxs-lookup"><span data-stu-id="2a6bf-771">Ink Support</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-772">312</span><span class="sxs-lookup"><span data-stu-id="2a6bf-772">312</span></span>

[<span data-ttu-id="2a6bf-773">Reconhecimento de manuscrito</span><span class="sxs-lookup"><span data-stu-id="2a6bf-773">Handwriting Recognition</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-774">Serviço de Transferência Inteligente em Segundo Plano (BITS)-recursos (335)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-774">Background Intelligent Transfer Service (BITS) - Features (335)</span></span>

<span data-ttu-id="2a6bf-775">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-775">Value</span></span>

<span data-ttu-id="2a6bf-776">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-776">Name</span></span>

<span data-ttu-id="2a6bf-777">54</span><span class="sxs-lookup"><span data-stu-id="2a6bf-777">54</span></span>

<span data-ttu-id="2a6bf-778">Extensão do Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-778">IIS Server Extension</span></span>

<span data-ttu-id="2a6bf-779">332</span><span class="sxs-lookup"><span data-stu-id="2a6bf-779">332</span></span>

[<span data-ttu-id="2a6bf-780">Compact Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-780">Compact Server</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-781">Suporte WOW64-recursos (340)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-781">Wow64 Support - Features (340)</span></span>

<span data-ttu-id="2a6bf-782">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-782">Value</span></span>

<span data-ttu-id="2a6bf-783">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-783">Name</span></span>

<span data-ttu-id="2a6bf-784">341</span><span class="sxs-lookup"><span data-stu-id="2a6bf-784">341</span></span>

[<span data-ttu-id="2a6bf-785">WoW64</span><span class="sxs-lookup"><span data-stu-id="2a6bf-785">WoW64</span></span>](#wow64)<br/>

<span data-ttu-id="2a6bf-786">342</span><span class="sxs-lookup"><span data-stu-id="2a6bf-786">342</span></span>

[<span data-ttu-id="2a6bf-787">WoW64 para .NET Framework 2,0 e Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-787">WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-788">343</span><span class="sxs-lookup"><span data-stu-id="2a6bf-788">343</span></span>

[<span data-ttu-id="2a6bf-789">WoW64 para .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="2a6bf-789">WoW64 for .NET Framework 2.0</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-790">344</span><span class="sxs-lookup"><span data-stu-id="2a6bf-790">344</span></span>

[<span data-ttu-id="2a6bf-791">WoW64 para PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-791">WoW64 for PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-792">345</span><span class="sxs-lookup"><span data-stu-id="2a6bf-792">345</span></span>

[<span data-ttu-id="2a6bf-793">WoW64 para .NET Framework 3,0 e 3,5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-793">WoW64 for .NET Framework 3.0 and 3.5</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-794">346</span><span class="sxs-lookup"><span data-stu-id="2a6bf-794">346</span></span>

[<span data-ttu-id="2a6bf-795">WoW64 para serviços de impressão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-795">WoW64 for Print Services</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-796">347</span><span class="sxs-lookup"><span data-stu-id="2a6bf-796">347</span></span>

[<span data-ttu-id="2a6bf-797">WoW64 para clustering de failover</span><span class="sxs-lookup"><span data-stu-id="2a6bf-797">WoW64 for Failover Clustering</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-798">348</span><span class="sxs-lookup"><span data-stu-id="2a6bf-798">348</span></span>

[<span data-ttu-id="2a6bf-799">WoW64 para editor de método de entrada</span><span class="sxs-lookup"><span data-stu-id="2a6bf-799">WoW64 for Input Method Editor</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-800">349</span><span class="sxs-lookup"><span data-stu-id="2a6bf-800">349</span></span>

[<span data-ttu-id="2a6bf-801">WoW64 para subsistema para aplicativos baseados em UNIX</span><span class="sxs-lookup"><span data-stu-id="2a6bf-801">WoW64 for Subsystem for UNIX-based Applications</span></span>](/windows)<br/>

<span data-ttu-id="2a6bf-802">Interfaces do usuário e serviços de função de infraestrutura (447)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-802">User Interfaces and Infrastructure - Role Services (447)</span></span>

<span data-ttu-id="2a6bf-803">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-803">Value</span></span>

<span data-ttu-id="2a6bf-804">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-804">Name</span></span>

<span data-ttu-id="2a6bf-805">35</span><span class="sxs-lookup"><span data-stu-id="2a6bf-805">35</span></span>

[<span data-ttu-id="2a6bf-806">Experiência Desktop</span><span class="sxs-lookup"><span data-stu-id="2a6bf-806">Desktop Experience</span></span>](/windows)

<span data-ttu-id="2a6bf-807">99</span><span class="sxs-lookup"><span data-stu-id="2a6bf-807">99</span></span>

[<span data-ttu-id="2a6bf-808">Shell gráfico do servidor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-808">Server Graphical Shell</span></span>](/windows)

<span data-ttu-id="2a6bf-809">Windows Server Update Services-recursos (404)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-809">Window Server Update Services - Features (404)</span></span>

<span data-ttu-id="2a6bf-810">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-810">Value</span></span>

<span data-ttu-id="2a6bf-811">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-811">Name</span></span>

<span data-ttu-id="2a6bf-812">405</span><span class="sxs-lookup"><span data-stu-id="2a6bf-812">405</span></span>

[<span data-ttu-id="2a6bf-813">Cmdlets do PowerShell e API</span><span class="sxs-lookup"><span data-stu-id="2a6bf-813">API and PowerShell cmdlets</span></span>](/windows)

<span data-ttu-id="2a6bf-814">406</span><span class="sxs-lookup"><span data-stu-id="2a6bf-814">406</span></span>

[<span data-ttu-id="2a6bf-815">Conectividade de SQL Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-815">SQL Server Connectivity</span></span>](/windows)

<span data-ttu-id="2a6bf-816">407</span><span class="sxs-lookup"><span data-stu-id="2a6bf-816">407</span></span>

[<span data-ttu-id="2a6bf-817">Serviços do WSUS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-817">WSUS Services</span></span>](/windows)

<span data-ttu-id="2a6bf-818">408</span><span class="sxs-lookup"><span data-stu-id="2a6bf-818">408</span></span>

[<span data-ttu-id="2a6bf-819">Console de gerenciamento de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="2a6bf-819">User Interface Management Console</span></span>](/windows)

<span data-ttu-id="2a6bf-820">449</span><span class="sxs-lookup"><span data-stu-id="2a6bf-820">449</span></span>

[<span data-ttu-id="2a6bf-821">Conectividade de WID</span><span class="sxs-lookup"><span data-stu-id="2a6bf-821">WID Connectivity</span></span>](/windows)

<span data-ttu-id="2a6bf-822">Windows PowerShell-recursos (417)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-822">Windows PowerShell - Features (417)</span></span>

<span data-ttu-id="2a6bf-823">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-823">Value</span></span>

<span data-ttu-id="2a6bf-824">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-824">Name</span></span>

<span data-ttu-id="2a6bf-825">411</span><span class="sxs-lookup"><span data-stu-id="2a6bf-825">411</span></span>

[<span data-ttu-id="2a6bf-826">Mecanismo 2,0 do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-826">Windows PowerShell 2.0 Engine</span></span>](/windows)

<span data-ttu-id="2a6bf-827">412</span><span class="sxs-lookup"><span data-stu-id="2a6bf-827">412</span></span>

[<span data-ttu-id="2a6bf-828">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="2a6bf-828">Windows PowerShell 3.0</span></span>](/windows)

<span data-ttu-id="2a6bf-829">448</span><span class="sxs-lookup"><span data-stu-id="2a6bf-829">448</span></span>

[<span data-ttu-id="2a6bf-830">Windows PowerShell Web Access</span><span class="sxs-lookup"><span data-stu-id="2a6bf-830">Windows PowerShell Web Access</span></span>](/windows)

<span data-ttu-id="2a6bf-831">1000</span><span class="sxs-lookup"><span data-stu-id="2a6bf-831">1000</span></span>

[<span data-ttu-id="2a6bf-832">Serviço de configuração de estado desejado do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-832">Windows PowerShell Desired State Configuration Service</span></span>](/windows)

<span data-ttu-id="2a6bf-833">.NET Framework 4,5-recursos (418)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-833">.NET Framework 4.5 - Features (418)</span></span>

<span data-ttu-id="2a6bf-834">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-834">Value</span></span>

<span data-ttu-id="2a6bf-835">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-835">Name</span></span>

<span data-ttu-id="2a6bf-836">419</span><span class="sxs-lookup"><span data-stu-id="2a6bf-836">419</span></span>

[<span data-ttu-id="2a6bf-837">.NET Framework 4,5 estendido</span><span class="sxs-lookup"><span data-stu-id="2a6bf-837">.NET Framework 4.5 Extended</span></span>](/windows)

<span data-ttu-id="2a6bf-838">420</span><span class="sxs-lookup"><span data-stu-id="2a6bf-838">420</span></span>

[<span data-ttu-id="2a6bf-839">Serviços do WCF</span><span class="sxs-lookup"><span data-stu-id="2a6bf-839">WCF Services</span></span>](/windows)

<span data-ttu-id="2a6bf-840">421</span><span class="sxs-lookup"><span data-stu-id="2a6bf-840">421</span></span>

[<span data-ttu-id="2a6bf-841">Ativação HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-841">HTTP Activation</span></span>](/windows)

<span data-ttu-id="2a6bf-842">422</span><span class="sxs-lookup"><span data-stu-id="2a6bf-842">422</span></span>

[<span data-ttu-id="2a6bf-843">Ativação do MSMQ (enfileiramento de mensagens)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-843">Message Queuing (MSMQ) Activation</span></span>](/windows)

<span data-ttu-id="2a6bf-844">423</span><span class="sxs-lookup"><span data-stu-id="2a6bf-844">423</span></span>

[<span data-ttu-id="2a6bf-845">Ativação de pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-845">Named Pipe Activation</span></span>](/windows)

<span data-ttu-id="2a6bf-846">424</span><span class="sxs-lookup"><span data-stu-id="2a6bf-846">424</span></span>

[<span data-ttu-id="2a6bf-847">Ativação TCP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-847">TCP Activation</span></span>](/windows)

<span data-ttu-id="2a6bf-848">425</span><span class="sxs-lookup"><span data-stu-id="2a6bf-848">425</span></span>

[<span data-ttu-id="2a6bf-849">Compartilhamento de porta TCP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-849">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="2a6bf-850">429</span><span class="sxs-lookup"><span data-stu-id="2a6bf-850">429</span></span>

[<span data-ttu-id="2a6bf-851">ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-851">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="2a6bf-852">Acesso remoto-função (468)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-852">Remote Access - Role (468)</span></span>

<span data-ttu-id="2a6bf-853">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-853">Value</span></span>

<span data-ttu-id="2a6bf-854">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-854">Name</span></span>

<span data-ttu-id="2a6bf-855">469</span><span class="sxs-lookup"><span data-stu-id="2a6bf-855">469</span></span>

[<span data-ttu-id="2a6bf-856">DirectAccess e VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-856">DirectAccess and VPN (RAS)</span></span>](/windows)

<span data-ttu-id="2a6bf-857">470</span><span class="sxs-lookup"><span data-stu-id="2a6bf-857">470</span></span>

[<span data-ttu-id="2a6bf-858">Roteamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-858">Routing</span></span>](#routing)

<span data-ttu-id="2a6bf-859">Serviços de arquivo e armazenamento-função (481)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-859">File and Storage Services - Role (481)</span></span>

<span data-ttu-id="2a6bf-860">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-860">Value</span></span>

<span data-ttu-id="2a6bf-861">Nome</span><span class="sxs-lookup"><span data-stu-id="2a6bf-861">Name</span></span>

<span data-ttu-id="2a6bf-862">482</span><span class="sxs-lookup"><span data-stu-id="2a6bf-862">482</span></span>

[<span data-ttu-id="2a6bf-863">Serviços de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-863">Storage Services</span></span>](/windows)

<span data-ttu-id="2a6bf-864">484</span><span class="sxs-lookup"><span data-stu-id="2a6bf-864">484</span></span>

[<span data-ttu-id="2a6bf-865">Ferramentas de gerenciamento de cluster de failover</span><span class="sxs-lookup"><span data-stu-id="2a6bf-865">Failover Cluster Management Tools</span></span>](/windows)



 

</dd> <dt>

<span data-ttu-id="2a6bf-866">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-866">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a6bf-867">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-867">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a6bf-868">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-868">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2a6bf-869">Nome de exibição do recurso do servidor, como "servidor de arquivos", "Servidor de Impressão" ou "experiência desktop".</span><span class="sxs-lookup"><span data-stu-id="2a6bf-869">Display name of the server feature, such as "File Server", "Print Server", or "Desktop Experience".</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-870">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-870">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a6bf-871">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-871">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a6bf-872">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-872">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2a6bf-873">Número de ID do recurso do servidor pai.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-873">ID number of the parent server feature.</span></span> <span data-ttu-id="2a6bf-874">Essa propriedade será 0 se o recurso representado pela instância atual da classe não tiver um recurso pai.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-874">This property is 0 if the feature represented by the current instance of the class does not have a parent feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a6bf-875">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a6bf-875">Remarks</span></span>

<span data-ttu-id="2a6bf-876">Leia a [visão geral técnica do Windows Server 2008 Gerenciador do servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) para saber mais sobre os recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-876">Read the [Windows Server 2008 Server Manager Technical Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) to learn about server features.</span></span>

<span data-ttu-id="2a6bf-877">As empresas que não usam software de gerenciamento que relata recursos do servidor, como System Center Operations Manager com pacotes de gerenciamento instalados, podem obter essas informações consultando a classe **Win32 \_ ServerFeature** .</span><span class="sxs-lookup"><span data-stu-id="2a6bf-877">Enterprises that do not use management software that reports server features, such as System Center Operations Manager with management packs installed, can get that information by querying the **Win32\_ServerFeature** class.</span></span>

<span data-ttu-id="2a6bf-878">Você pode usar os recursos de comunicação remota do WMI ou do WinRM para obter informações de recursos de servidor de servidores remotos.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-878">You can use the remoting features of WMI or WinRM to get server feature information from remote servers.</span></span> <span data-ttu-id="2a6bf-879">Para obter mais informações sobre conexões DCOM remotas do WMI, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="2a6bf-879">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="2a6bf-880">Para obter mais informações sobre o WinRM, confira Gerenciamento Remoto do Windows.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-880">For more information about WinRM, see Windows Remote Management.</span></span>

<span data-ttu-id="2a6bf-881">Windows Server 2012: o **Win32 \_ ServerFeature** foi preterido.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-881">Windows Server 2012: **Win32\_ServerFeature** has been deprecated.</span></span> <span data-ttu-id="2a6bf-882">Para acessar as informações de recurso do Windows Server programaticamente, você pode usar os [cmdlets Gerenciador do servidor](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="2a6bf-882">To access windows server feature information programmatically, you can use the [Server Manager Cmdlets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span></span>

### <a name="windows-server-2012-r2"></a><span data-ttu-id="2a6bf-883">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2a6bf-883">Windows Server 2012 R2</span></span>

<dl> <dt>

<span data-ttu-id="2a6bf-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Servidor de aplicativos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Application Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-885">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-885">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Serviços de mídia de streaming</span><span class="sxs-lookup"><span data-stu-id="2a6bf-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Streaming Media Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-887">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-887">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Serviços de Federação do Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory Federation Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-889">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-889">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>Servidor DHCP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-891">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-891">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>Servidor DNS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-893">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-893">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Remote Desktop Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-895">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-895">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-897">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-897">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Clustering de failover</span><span class="sxs-lookup"><span data-stu-id="2a6bf-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-899">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-899">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Balanceamento de carga de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network Load Balancing</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-901">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-901">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>Recursos do .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="2a6bf-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1 Features</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-903">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-903">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Gerenciador de recursos de sistema do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-905">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-905">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Recursos de Backup do Windows Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Server Backup Features</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-907">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-907">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Assistência remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Remote Assistance</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-909">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-909">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Cliente Telnet</span><span class="sxs-lookup"><span data-stu-id="2a6bf-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet Client</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-911">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-911">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Servidor Telnet</span><span class="sxs-lookup"><span data-stu-id="2a6bf-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-913">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-913">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsistema para aplicativos baseados em UNIX</span><span class="sxs-lookup"><span data-stu-id="2a6bf-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem For Unix-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-915">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-915">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Banco de dados interno do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows Internal Database</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-917">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-917">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Gerenciador de armazenamento para SANs</span><span class="sxs-lookup"><span data-stu-id="2a6bf-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Storage Manager For SANs</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-919">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-919">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Servidor de nomes de armazenamento da Internet</span><span class="sxs-lookup"><span data-stu-id="2a6bf-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Internet Storage Name Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-921">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-921">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O</span><span class="sxs-lookup"><span data-stu-id="2a6bf-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-923">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-923">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>Serviços SNMP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-925">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-925">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Serviços para sistema de arquivos de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-927">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-927">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Protocolo de resolução de nome de par</span><span class="sxs-lookup"><span data-stu-id="2a6bf-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Peer Name Resolution Protocol</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-929">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-929">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Ferramentas de Administração de Servidor Remoto</span><span class="sxs-lookup"><span data-stu-id="2a6bf-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Remote Server Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-931">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-931">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Experiência de vídeo de áudio do Windows de qualidade</span><span class="sxs-lookup"><span data-stu-id="2a6bf-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Quality Windows Audio Video Experience</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-933">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-933">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Gerenciamento de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="2a6bf-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Group Policy Management</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-935">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-935">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Serviço de indexação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-937">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-937">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>FSRM (Gerenciador de recursos de servidor de arquivos)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>File Server Resource Manager (FSRM)</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-939">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-939">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Ferramentas de Migração do Windows Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Server Migration Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-941">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-941">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span><span class="sxs-lookup"><span data-stu-id="2a6bf-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-943">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-943">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console de gerenciamento do DirectAccess</span><span class="sxs-lookup"><span data-stu-id="2a6bf-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-945">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-945">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Serviço de Transferência Inteligente em Segundo Plano (BITS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-947">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-947">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Suporte a WoW64</span><span class="sxs-lookup"><span data-stu-id="2a6bf-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-949">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-949">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Serviços de atualização de servidor do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Window Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-951">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-951">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>Servidor IPAM (gerenciamento de endereços IP)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP Address Management (IPAM) Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-953">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-953">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-955">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-955">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4.5</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-957">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-957">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Serviço de Pesquisa do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-959">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-959">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Cliente para NFS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client for NFS</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-961">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-961">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>Desbloqueio de rede do BitLocker</span><span class="sxs-lookup"><span data-stu-id="2a6bf-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker Network Unlock</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-963">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-963">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Extensão do IIS do Management OData</span><span class="sxs-lookup"><span data-stu-id="2a6bf-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Management OData IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-965">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-965">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework serviços avançados 4,5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-967">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-967">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>Recursos do .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5 Features</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-969">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-969">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfaces do usuário e infraestrutura</span><span class="sxs-lookup"><span data-stu-id="2a6bf-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-971">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-971">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Ferramentas e infraestrutura de gerenciamento gráfico</span><span class="sxs-lookup"><span data-stu-id="2a6bf-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Graphical Management Tools and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-973">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-973">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>Serviços de arquivo e armazenamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>File and Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-975">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-975">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Experiência do Windows Server Essentials</span><span class="sxs-lookup"><span data-stu-id="2a6bf-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Server Essentials Experience</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-977">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-977">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Play direto</span><span class="sxs-lookup"><span data-stu-id="2a6bf-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Direct Play</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-979">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-979">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Sistema de Arquivos Distribuído</span><span class="sxs-lookup"><span data-stu-id="2a6bf-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Distributed File System</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-981">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-981">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>Gerenciador de recursos do servidor de arquivos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>File Server Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-983">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-983">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Serviços para sistema de arquivos de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-985">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-985">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Armazenamento de instância única</span><span class="sxs-lookup"><span data-stu-id="2a6bf-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Single Instance Storage</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-987">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-987">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Serviço de Pesquisa do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-989">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-989">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Serviço de indexação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-991">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-991">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>Provedor de armazenamento de destino iSCSI (provedores de hardware VDS e VSS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-993">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-993">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Pastas de trabalho</span><span class="sxs-lookup"><span data-stu-id="2a6bf-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-995">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-995">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Controlador de Domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a6bf-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory Domain Controller</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-997">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-997">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Gerenciamento de identidade para UNIX</span><span class="sxs-lookup"><span data-stu-id="2a6bf-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Identity Management For Unix</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-999">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-999">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Servidor para serviços de informações de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server For Network Information Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1001">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1001">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Sincronização de senha</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Password Synchronization</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1003">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1003">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Ferramentas de administração</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1005">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1005">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1007">Não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1007">No longer supported.</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Administração baseada na Web</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Web-based Administration</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1009">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1009">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Agente de log</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Logging Agent</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1011">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1011">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Serviço de Federação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Federation Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1013">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1013">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Política de Serviço de Federação</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Federation Service Policy</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1015">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1015">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS agentes Web</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web Agents</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1017">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1017">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Agente baseado em token do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Token-based Agent</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1019">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1019">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Licenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Remote Desktop Licensing</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1021">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1021">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Servidor de políticas de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Network Policy Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1023">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1023">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1024"><span id="VPN"></span><span id="vpn"></span>VPNS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1024"><span id="VPN"></span><span id="vpn"></span>VPN</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1025">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1025">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Serviços de acesso remoto</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Remote Access Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1027">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1027">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Zona</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1029">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1029">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Autoridade de registro de integridade</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Health Registration Authority</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1031">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1031">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Protocolo de autorização de credenciais do host</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Host Credential Authorization Protocol</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1033">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1033">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1035">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1035">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visualizador XPS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1037">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1037">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>Serviço SNMP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1039">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1039">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>Provedor WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP WMI Provider</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1041">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1041">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1043">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1043">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Suporte do servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Web Server (IIS) Support</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1045">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1045">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Acesso à rede COM+</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1047">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1047">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Compartilhamento de porta TCP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1049">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1049">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Suporte ao serviço de ativação de processos do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Process Activation Service Support</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1051">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1051">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Ativação HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1053">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1053">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Ativação do enfileiramento de mensagens</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Message Queuing Activation</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1055">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1055">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Ativação de TCP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1057">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1057">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Ativação de pipes nomeados</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Named Pipes Activation</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1059">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1059">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Transações distribuídas</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Distributed Transactions</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1061">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1061">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Transações remotas de entrada</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Incoming Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1063">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1063">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Transações remotas de saída</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Outgoing Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1065">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1065">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-transações automáticas</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-Automatic Transactions</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1067">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1067">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensões do servidor de aplicativos para .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1069">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1069">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Ferramentas de administração de função</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Role Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1071">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1071">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>Ferramentas de AD DS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1073">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1073">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Ferramentas de Snap-Ins e Command-Line de AD LDS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1075">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1075">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Serviços de acesso e política de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Network Policy and Access Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1077">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1077">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1079">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1079">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Ferramentas de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Remote Desktop Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1081">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1081">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Ferramentas de administração de recursos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Feature Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1083">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1083">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Ferramentas de clustering de failover</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Failover Clustering Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1085">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1085">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>Ferramentas de servidor DNS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS Server Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1087">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1087">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Serviços para ferramentas do sistema de arquivos de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services For Network File System Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1089">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1089">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Ferramentas do servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Web Server (IIS) Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1091">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1091">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Ferramentas de Servidor para NIS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server for NIS Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1093">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1093">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Ferramentas de Snap-Ins e Command-Line de AD DS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1095">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1095">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Ferramentas de AD DS e AD LDS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1097">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1097">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Ferramentas do agente de Conexão de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1099">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1099">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>Cliente IPAM (gerenciamento de endereços IP)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP Address Management (IPAM) Client</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1101">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1101">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Módulo do Hyper-V para Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Hyper-V Module for Windows PowerShell</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="2a6bf-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Ferramenta de Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Tool</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1104">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1104">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Ferramenta de gerenciamento de compartilhamento e armazenamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Share and Storage Management Tool</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1106">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1106">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Ferramentas de gerenciamento de acesso remoto</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Remote Access Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1108">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1108">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Módulo de acesso remoto para Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Remote Access module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1110">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1110">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>GUI de acesso remoto e ferramentas de Command-Line</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Remote Access GUI and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1112">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1112">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Ferramentas de Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1114">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1114">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Ferramentas do diagnosticador de licenciamento Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Remote Desktop Licensing Diagnoser Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1116">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1116">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>Ferramentas SNMP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1118">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1118">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Ferramentas de ativação de volume</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Volume Activation Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1120">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1120">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Backup do Windows Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server Backup</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1122">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1122">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Ferramentas de linha de comando</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Command Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1124">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1124">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Suporte à tinta</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Ink Support</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1126">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1126">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Reconhecimento de manuscrito</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Handwriting Recognition</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1128">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1128">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Servidor Compact</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1130">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1130">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1132">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1132">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 para .NET Framework 2,0 e PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 for .NET Framework 2.0 and PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1134">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1134">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 para .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1136">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1136">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 para PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1138">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1138">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 para .NET Framework 3,0 e 3,5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1140">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1140">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 para serviços de impressão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1142">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1142">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 para clustering de failover</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1144">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1144">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 para editor de método de entrada</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1146">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1146">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 para subsistema para aplicativos baseados em UNIX</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1148">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1148">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Experiência Desktop</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Desktop Experience</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1150">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1150">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Shell gráfico do servidor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Server Graphical Shell</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1152">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1152">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>Cmdlets do PowerShell e API</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API and PowerShell cmdlets</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1154">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1154">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>Conectividade de SQL Server</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1156">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1156">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>Serviços do WSUS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1158">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1158">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Console de gerenciamento de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>User Interface Management Console</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1160">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1160">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>Conectividade de WID</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1162">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1162">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Mecanismo 2,0 do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0 Engine</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1164">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1164">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3.0</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1166">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1166">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Acesso via Web do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Web Access</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1168">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1168">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Serviço de configuração de estado desejado do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1170">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1170">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4,5 estendido</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 Extended</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1172">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1172">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>Serviços WCF</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1174">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1174">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Ativação HTTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1176">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1176">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Ativação do MSMQ (enfileiramento de mensagens)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Message Queuing (MSMQ) Activation</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="2a6bf-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Ativação de pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Named Pipe Activation</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1179">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1179">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Ativação de TCP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1181">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1181">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Compartilhamento de porta TCP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1183">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1183">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4.5</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1185">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1185">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>Extensibilidade do .NET 4,5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET Extensibility 4.5</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1187">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1187">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess e VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess and VPN (RAS)</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1189">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1189">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Zona</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1191">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1191">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Serviços de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1193">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1193">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Ferramentas de gerenciamento de cluster de failover</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Failover Cluster Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1195">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1195">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Ferramentas de Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1197">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1197">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Inicialização do aplicativo</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Application Initialization</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1199">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1199">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Suporte a certificados SSL centralizados</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Centralized SSL Certificate Support</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1201">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1201">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Agente com reconhecimento de declaração</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Claims-aware Agent</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1203">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1203">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Ferramentas de Host da Sessão da Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Remote Desktop Session Host Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1205">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1205">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>Protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket Protocol</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1207">Não tem mais suporte</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1207">no longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Acesso à rede COM+</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1209">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1209">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Alteração de nome de serviços de arquivo e iSCSI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>File and iSCSI Services name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1211">Alterado para serviços de arquivo</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1211">Changed to File Services</span></span>

</dd> </dl>

### <a name="windows-server-2012"></a><span data-ttu-id="2a6bf-1212">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1212">Windows Server 2012</span></span>

<dl> <dt>

<span data-ttu-id="2a6bf-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfaces do usuário e infraestrutura</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1214">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1214">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Servidor para NFS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server for NFS</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1216">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1216">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Serviço de agente VSS do servidor de arquivos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>File Server VSS Agent Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1218">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1218">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>Servidor de destino iSCSI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI Target Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1220">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1220">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Eliminação de duplicação de dados</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Data Deduplication</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1222">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1222">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Pastas de trabalho</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1224">Removido</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1224">Removed</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Serviços principais</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Core Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1226">Adicionado somente para esta versão.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1226">Added for this version only.</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Gráficos virtuais Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Remote Desktop Virtual Graphics</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1228">Adicionado somente para esta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1228">Added for this version only</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Acesso remoto</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Remote Access</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1230">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1230">Added</span></span>

</dd> </dl>

### <a name="windows-server-2008-r2"></a><span data-ttu-id="2a6bf-1231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1231">Windows Server 2008 R2</span></span>

<dl> <dt>

<span data-ttu-id="2a6bf-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>Serviços UDDI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1233">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1233">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Gerenciador de recursos de sistema do Windows</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1235">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1235">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Gerenciador de armazenamento removível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Removable Storage Manager</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1237">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1237">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1239">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1239">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Serviços de Reconhecimento de Manuscrito</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Ink and Handwriting Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1241">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1241">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>Extensão do IIS do WinRM</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1243">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1243">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console de gerenciamento do DirectAccess</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1245">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1245">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Serviço de Transferência Inteligente em Segundo Plano (BITS)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1247">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1247">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visualizador XPS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1249">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1249">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometric Framework</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1251">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1251">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Suporte a WoW64</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1253">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1253">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Ambiente de Script Integrado do Windows PowerShell (ISE)</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1255">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1255">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Serviço de replicação de arquivo</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>File Replication Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1257">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1257">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache para arquivos de rede</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache for Network Files</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1259">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1259">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Pastas de trabalho</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1261">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1261">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Servidor de Digitalização Distribuída</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Distributed Scan Server</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1263">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1263">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>Serviço de publicação FTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP Publishing Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1265">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1265">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>Console de gerenciamento FTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP Management Console</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1267">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1267">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>Serviço FTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1269">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1269">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>Extensibilidade de FTP</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP Extensibility</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1271">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1271">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Núcleo da Web Hospedável do IIS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>IIS Hostable Web Core</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="2a6bf-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Suporte ao cliente do Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 Client Support</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1274">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1274">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Serviço Web de Registro de Certificado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Certificate Enrollment Web Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1276">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1276">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Serviço Web de Política de Registro de Certificado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Certificate Enrollment Policy Web Service</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1278">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1278">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Aplicativo Web dos serviços UDDI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>UDDI Services Web Application</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1280">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1280">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>Banco de dados dos serviços UDDI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>UDDI Services Database</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1282">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1282">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensões do servidor de aplicativos para .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1284">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1284">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Ferramentas dos serviços UDDI</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>UDDI Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1286">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1286">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>Utilitários de administração de Criptografia de Unidade de Disco BitLocker</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker Drive Encryption Administration Utilities</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1288">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1288">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Ferramentas de AD DS e AD LDS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1290">Não é mais compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1290">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Ferramentas de AD DS e AD LDS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1292">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1292">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Centro Administrativo do Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory Administrative Center</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1294">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1294">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Módulo Active Directory para o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Active Directory module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1296">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1296">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Ferramentas do agente de Conexão de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1298">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1298">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1300">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1300">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 para .NET Framework 2,0 e Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1302">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1302">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 para .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1304">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1304">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 para PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1306">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1306">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 para .NET Framework 3,0 e 3,5</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1308">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1308">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 para serviços de impressão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1310">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1310">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 para clustering de failover</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1312">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1312">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 para editor de método de entrada</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1314">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1314">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 para subsistema para aplicativos baseados em UNIX</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1316">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1316">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>Visualizador de senha de recuperação do BitLocker</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker Recovery Password Viewer</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1318">Adicionado</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1318">Added</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Alteração de nome de Serviços de Impressão e Documentos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Print and Document Services name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1320">Serviços de impressão nomeados para esta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1320">named Print Services for this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Alteração de nome de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Remote Desktop Services name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1322">Serviços de terminal nomeados nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1322">named Terminal Services in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>Alteração de nome de recursos do .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 Features name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1324">Recursos do .NET Framework 3,0 nomeados nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1324">Named .NET Framework 3.0 Features in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Alteração de nome de Host da Sessão da Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Remote Desktop Session Host name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1326">Terminal Server nomeado nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1326">Named Terminal Server in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Alteração do nome de licenciamento Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Remote Desktop Licensing name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1328">Licenciamento de TS nomeado nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1328">Named TS Licensing in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Alteração do nome do gateway Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Remote Desktop Gateway name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1330">TS Gateway nomeado nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1330">Named TS Gateway in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Alteração do nome do agente de Conexão de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Remote Desktop Connection Broker name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1332">Agente de Sessão TS nomeado nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1332">Named TS Session Broker in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Alteração de nome de Acesso via Web à Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Remote Desktop Web Access name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1334">Acesso via Web de TS nomeados nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1334">Named TS Web Access in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>Alteração de nome do .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1 name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1336">(220) denominada recursos do NET FX 3,0 nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1336">(220) Named Net FX 3.0 Features in this release</span></span>

<span data-ttu-id="2a6bf-1337">(230) nome do servidor de aplicativos chamado nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1337">(230) Named Application Server Core in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Alteração de nome de ferramentas de AD DS</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>AD DS Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1339">Ferramentas de Active Directory Domain Services nomeadas nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1339">Named Active Directory Domain Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins e Command-Line alteração de nome de ferramentas</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1341">Ferramentas de serviços AD LDS nomeadas nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1341">Named Active Directory Lightweight Directory Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Alteração de nome de ferramentas de Serviços de Impressão e Documentos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Print and Document Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1343">Ferramentas de serviços de impressão nomeados nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1343">Named Print Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Alteração de nome de ferramentas de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Remote Desktop Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1345">Ferramentas de serviços de terminal nomeados nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1345">Named Terminal Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Alteração de nome de ferramentas de Host da Sessão da Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Remote Desktop Session Host Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1347">Ferramentas de Terminal Server nomeadas nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1347">Named Terminal Server Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Alteração de nome das ferramentas de gateway Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Remote Desktop Gateway Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1349">Ferramentas de gateway de TS nomeadas nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1349">Named TS Gateway Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Alteração do nome das ferramentas de licenciamento Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Remote Desktop Licensing Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1351">Ferramentas de Licenciamento TS nomeadas nesta versão</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1351">Named TS Licensing Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins e Command-Line alteração de nome de ferramentas</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-1353">Ferramentas de controlador de domínio Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1353">Active Directory Domain Controller Tools</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2a6bf-1354">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1354">Examples</span></span>

<span data-ttu-id="2a6bf-1355">O script a seguir exibe os nomes de todos os recursos de servidor no computador chamado "FABRIKAM".</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1355">The following script displays the names of all the server features on the computer named "FABRIKAM".</span></span> <span data-ttu-id="2a6bf-1356">Observe que o computador de destino deve estar executando o Windows Server 2008 ou um sistema operacional de servidor posterior.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1356">Note that the target computer must be running Windows Server 2008 or a later server operating system.</span></span>


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a><span data-ttu-id="2a6bf-1357">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1357">Requirements</span></span>



| <span data-ttu-id="2a6bf-1358">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1358">Requirement</span></span> | <span data-ttu-id="2a6bf-1359">Valor</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a6bf-1360">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1360">Minimum supported client</span></span><br/> | <span data-ttu-id="2a6bf-1361">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1361">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2a6bf-1362">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1362">Minimum supported server</span></span><br/> | <span data-ttu-id="2a6bf-1363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1363">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="2a6bf-1364">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1364">Namespace</span></span><br/>                | <span data-ttu-id="2a6bf-1365">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1365">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="2a6bf-1366">MOF</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a6bf-1367"><dt>ServerCompProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a6bf-1367"><dt>ServerCompProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a6bf-1368">DLL</span><span class="sxs-lookup"><span data-stu-id="2a6bf-1368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a6bf-1369"><dt>ServerCompProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a6bf-1369"><dt>ServerCompProv.dll</dt></span></span> </dl> |



 

