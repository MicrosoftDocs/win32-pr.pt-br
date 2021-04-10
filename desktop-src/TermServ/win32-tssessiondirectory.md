---
title: Classe Win32_TSSessionDirectory
description: Define as definições de configuração do agente de Conexão de Área de Trabalho Remota (agente de conexão RD) para a \_ classe Win32 TSSessionDirectorySetting.
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSSessionDirectory Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSSessionDirectory classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918301"
---
# <a name="win32_tssessiondirectory-class"></a><span data-ttu-id="7f721-105">\_Classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="7f721-105">Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="7f721-106">Define as definições de configuração do agente de Conexão de Área de Trabalho Remota (agente de conexão RD) para a classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="7f721-106">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="7f721-107">No Windows Server 2008 R2, o nome do agente de sessão dos serviços de terminal (agente de Sessão TS) foi alterado para o agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="7f721-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="7f721-108">Essas propriedades se aplicam a todos os sistemas operacionais com suporte, salvo indicação em contrário.</span><span class="sxs-lookup"><span data-stu-id="7f721-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

<span data-ttu-id="7f721-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="7f721-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="7f721-110">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="7f721-110">For reference information about methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f721-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f721-111">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a><span data-ttu-id="7f721-112">Membros</span><span class="sxs-lookup"><span data-stu-id="7f721-112">Members</span></span>

<span data-ttu-id="7f721-113">A classe **Win32 \_ TSSessionDirectory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7f721-113">The **Win32\_TSSessionDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="7f721-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="7f721-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f721-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7f721-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f721-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="7f721-116">Methods</span></span>

<span data-ttu-id="7f721-117">A classe **Win32 \_ TSSessionDirectory** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7f721-117">The **Win32\_TSSessionDirectory** class has these methods.</span></span>



| <span data-ttu-id="7f721-118">Método</span><span class="sxs-lookup"><span data-stu-id="7f721-118">Method</span></span>                                                                                                  | <span data-ttu-id="7f721-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f721-119">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f721-120">**CreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="7f721-120">**CreateUserDiskTemplate**</span></span>](createuserdisktemplate-win32-tssessiondirectory.md)                       | <span data-ttu-id="7f721-121">Cria um modelo de disco de usuário.</span><span class="sxs-lookup"><span data-stu-id="7f721-121">Creates a user disk template.</span></span><br/>                                                                     |
| [<span data-ttu-id="7f721-122">**DisableUserVhd**</span><span class="sxs-lookup"><span data-stu-id="7f721-122">**DisableUserVhd**</span></span>](disableuservhd-win32-tssessiondirectory.md)                                       | <span data-ttu-id="7f721-123">Desabilita um VHD de perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="7f721-123">Disables a user profile VHD.</span></span><br/>                                                                      |
| [<span data-ttu-id="7f721-124">**EnableUserVhd**</span><span class="sxs-lookup"><span data-stu-id="7f721-124">**EnableUserVhd**</span></span>](enableuservhd-win32-tssessiondirectory.md)                                         | <span data-ttu-id="7f721-125">Habilita um VHD de perfil de usuário em um servidor RDSH.</span><span class="sxs-lookup"><span data-stu-id="7f721-125">Enables a user profile VHD on an RDSH server.</span></span><br/>                                                     |
| [<span data-ttu-id="7f721-126">**GetCurrentRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="7f721-126">**GetCurrentRedirectableAddresses**</span></span>](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="7f721-127">Obtém a lista atualmente configurada de endereços DNS qualificados e o tipo de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="7f721-127">Obtains the currently configured list of DNS eligible addresses, and the redirection type.</span></span><br/>        |
| [<span data-ttu-id="7f721-128">**GetRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="7f721-128">**GetRedirectableAddresses**</span></span>](getredirectableaddresses-win32-tssessiondirectory.md)                   | <span data-ttu-id="7f721-129">Obtém a lista completa de endereços do DNS qualificados.</span><span class="sxs-lookup"><span data-stu-id="7f721-129">Obtains the entire list of DNS eligible addresses.</span></span><br/>                                                |
| [<span data-ttu-id="7f721-130">**PingSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="7f721-130">**PingSessionDirectory**</span></span>](pingsessiondirectory-win32-tssessiondirectory.md)                           | <span data-ttu-id="7f721-131">Verifica se o servidor do agente de conexão RD está disponível.</span><span class="sxs-lookup"><span data-stu-id="7f721-131">Checks whether the RD Connection Broker server is available.</span></span><br/>                                      |
| [<span data-ttu-id="7f721-132">**SetCurrentRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="7f721-132">**SetCurrentRedirectableAddresses**</span></span>](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="7f721-133">Define a lista configurada de endereços DNS qualificados e o tipo de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="7f721-133">Sets the configured list of DNS eligible addresses, and the redirection type.</span></span><br/>                     |
| [<span data-ttu-id="7f721-134">**SetLoadBalancingState**</span><span class="sxs-lookup"><span data-stu-id="7f721-134">**SetLoadBalancingState**</span></span>](setloadbalancingstate-win32-tssessiondirectory.md)                         | <span data-ttu-id="7f721-135">Define o valor para indicar se o servidor participará do balanceamento de carga do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="7f721-135">Sets the value to indicate if the server will participate in RD Connection Broker load balancing.</span></span><br/> |
| [<span data-ttu-id="7f721-136">**SetServerWeight**</span><span class="sxs-lookup"><span data-stu-id="7f721-136">**SetServerWeight**</span></span>](setserverweight-win32-tssessiondirectory.md)                                     | <span data-ttu-id="7f721-137">Define o valor de peso do servidor para o balanceamento de carga do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="7f721-137">Sets the server weight value for RD Connection Broker load balancing.</span></span><br/>                             |
| [<span data-ttu-id="7f721-138">**SetSessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="7f721-138">**SetSessionDirectoryActive**</span></span>](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | <span data-ttu-id="7f721-139">Desabilita e habilita o agente de conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="7f721-139">Disables and enables the RD Connection Broker.</span></span><br/>                                                    |
| [<span data-ttu-id="7f721-140">**SetSessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="7f721-140">**SetSessionDirectoryExposeServerIP**</span></span>](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | <span data-ttu-id="7f721-141">Define a propriedade **SessionDirectoryExposeServerIP** .</span><span class="sxs-lookup"><span data-stu-id="7f721-141">Sets the **SessionDirectoryExposeServerIP** property.</span></span><br/>                                             |
| [<span data-ttu-id="7f721-142">**SetSessionDirectoryProperty**</span><span class="sxs-lookup"><span data-stu-id="7f721-142">**SetSessionDirectoryProperty**</span></span>](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | <span data-ttu-id="7f721-143">Define a propriedade **SessionDirectoryLocation** ou a propriedade **SessionDirectoryClusterName** .</span><span class="sxs-lookup"><span data-stu-id="7f721-143">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property.</span></span><br/>   |
| [<span data-ttu-id="7f721-144">**SetTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="7f721-144">**SetTSRedirectorMode**</span></span>](settsredirectormode-win32-tssessiondirectory.md)                             | <span data-ttu-id="7f721-145">Esse método não está disponível.</span><span class="sxs-lookup"><span data-stu-id="7f721-145">This method is not available.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="7f721-146">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7f721-146">Properties</span></span>

<span data-ttu-id="7f721-147">A classe **Win32 \_ TSSessionDirectory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7f721-147">The **Win32\_TSSessionDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f721-148">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="7f721-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7f721-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f721-151">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7f721-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7f721-152">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="7f721-152">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="7f721-153">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f721-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f721-154">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7f721-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7f721-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-157">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="7f721-157">Description of the object.</span></span>

<span data-ttu-id="7f721-158">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f721-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f721-159">**GetLoadBalancingState**</span><span class="sxs-lookup"><span data-stu-id="7f721-159">**GetLoadBalancingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-160">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-162">Indica se o servidor está configurado para participar do balanceamento de carga do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="7f721-162">Indicates if the server is configured to participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="7f721-163">0</span><span class="sxs-lookup"><span data-stu-id="7f721-163">0</span></span>
</dt> <dd>

<span data-ttu-id="7f721-164">O servidor não está configurado para participar do balanceamento de carga do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="7f721-164">The server is not configured to participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="7f721-165">1</span><span class="sxs-lookup"><span data-stu-id="7f721-165">1</span></span>
</dt> <dd>

<span data-ttu-id="7f721-166">O servidor está configurado para participar do balanceamento de carga do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="7f721-166">The server is configured to participate in RD Connection Broker load balancing.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f721-167">**GetServerWeight**</span><span class="sxs-lookup"><span data-stu-id="7f721-167">**GetServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-170">Recupera o valor de peso do servidor que é usado no balanceamento de carga do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="7f721-170">Retrieves the server weight value that is used in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="7f721-171">**GetTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="7f721-171">**GetTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-172">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-174">Indica se o servidor está configurado para atuar como um redirecionador de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="7f721-174">Indicates if the server is configured to act as a Remote Desktop Services redirector.</span></span>

<dt>

<span data-ttu-id="7f721-175">0</span><span class="sxs-lookup"><span data-stu-id="7f721-175">0</span></span>
</dt> <dd>

<span data-ttu-id="7f721-176">O servidor está configurado para atuar como um redirecionador de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="7f721-176">The server is configured to act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="7f721-177">1</span><span class="sxs-lookup"><span data-stu-id="7f721-177">1</span></span>
</dt> <dd>

<span data-ttu-id="7f721-178">O servidor não está configurado para atuar como um redirecionador de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="7f721-178">The server is not configured to act as a Remote Desktop Services redirector.</span></span>

</dd> </dl>

<span data-ttu-id="7f721-179">**Windows Server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="7f721-179">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="7f721-180">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7f721-180">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-181">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7f721-181">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f721-183">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="7f721-183">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="7f721-184">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="7f721-184">The date the object was installed.</span></span> <span data-ttu-id="7f721-185">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="7f721-185">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7f721-186">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f721-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f721-187">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7f721-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7f721-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-190">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="7f721-190">The name of the object.</span></span>

<span data-ttu-id="7f721-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f721-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f721-192">**PolicySourceLoadBalancing**</span><span class="sxs-lookup"><span data-stu-id="7f721-192">**PolicySourceLoadBalancing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-193">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-195">Indica se a propriedade **GetLoadBalancingState** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7f721-195">Indicates if the **GetLoadBalancingState** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="7f721-196">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="7f721-196">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-197">Servidor</span><span class="sxs-lookup"><span data-stu-id="7f721-197">Server</span></span>

</dd> <dt>

<span data-ttu-id="7f721-198">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="7f721-198">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-199">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="7f721-199">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f721-200">**PolicySourceSessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="7f721-200">**PolicySourceSessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-201">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-203">Indica se a propriedade **SessionDirectoryActive** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7f721-203">Indicates if the **SessionDirectoryActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="7f721-204">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="7f721-204">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-205">Servidor</span><span class="sxs-lookup"><span data-stu-id="7f721-205">Server</span></span>

</dd> <dt>

<span data-ttu-id="7f721-206">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="7f721-206">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-207">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="7f721-207">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f721-208">**PolicySourceSessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="7f721-208">**PolicySourceSessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-209">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-211">Indica se a propriedade **SessionDirectoryClusterName** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7f721-211">Indicates if the **SessionDirectoryClusterName** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="7f721-212">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="7f721-212">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-213">Servidor</span><span class="sxs-lookup"><span data-stu-id="7f721-213">Server</span></span>

</dd> <dt>

<span data-ttu-id="7f721-214">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="7f721-214">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-215">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="7f721-215">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f721-216">**PolicySourceSessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="7f721-216">**PolicySourceSessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-217">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-219">Indica se a propriedade **SessionDirectoryExposeServerIP** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7f721-219">Indicates if the **SessionDirectoryExposeServerIP** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="7f721-220">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="7f721-220">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-221">Servidor</span><span class="sxs-lookup"><span data-stu-id="7f721-221">Server</span></span>

</dd> <dt>

<span data-ttu-id="7f721-222">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="7f721-222">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-223">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="7f721-223">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f721-224">**PolicySourceSessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="7f721-224">**PolicySourceSessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-225">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-227">Indica se a propriedade **SessionDirectoryLocation** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7f721-227">Indicates if the **SessionDirectoryLocation** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="7f721-228">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="7f721-228">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-229">Servidor</span><span class="sxs-lookup"><span data-stu-id="7f721-229">Server</span></span>

</dd> <dt>

<span data-ttu-id="7f721-230">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="7f721-230">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-231">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="7f721-231">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f721-232">**PolicySourceTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="7f721-232">**PolicySourceTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-233">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-235">Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="7f721-235">This property is not available.</span></span>

<span data-ttu-id="7f721-236">**Windows Server 2008 R2:** Indica se a propriedade **GetTSRedirectorMode** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7f721-236">**Windows Server 2008 R2:** Indicates if the **GetTSRedirectorMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="7f721-237">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="7f721-237">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-238">Servidor</span><span class="sxs-lookup"><span data-stu-id="7f721-238">Server</span></span>

</dd> <dt>

<span data-ttu-id="7f721-239">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="7f721-239">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="7f721-240">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="7f721-240">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f721-241">**SessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="7f721-241">**SessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-242">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f721-244">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7f721-244">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7f721-245">Especifica se Serviços de Área de Trabalho Remota participa do agente de conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="7f721-245">Specifies if Remote Desktop Services participates in the RD Connection Broker.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="7f721-246"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="7f721-246"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7f721-247">A participação Serviços de Área de Trabalho Remota no agente de conexão de área de trabalho remota está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7f721-247">Remote Desktop Services participation in the RD Connection Broker is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="7f721-248"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="7f721-248"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7f721-249">A participação Serviços de Área de Trabalho Remota no agente de conexão de área de trabalho remota está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7f721-249">Remote Desktop Services participation in the RD Connection Broker is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f721-250">**SessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="7f721-250">**SessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7f721-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-253">O endereço IP virtual do cluster ao qual o servidor de Host da Sessão RD pertence.</span><span class="sxs-lookup"><span data-stu-id="7f721-253">The virtual IP address of the cluster to which the RD Session Host server belongs.</span></span>

</dd> <dt>

<span data-ttu-id="7f721-254">**SessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="7f721-254">**SessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-255">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f721-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-257">Especifica se a recuperação do endereço IP do agente de conexão de área de trabalho remota é permitida.</span><span class="sxs-lookup"><span data-stu-id="7f721-257">Specifies if retrieval of the IP address of the RD Connection Broker is allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="7f721-258"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="7f721-258"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7f721-259">A recuperação foi negada.</span><span class="sxs-lookup"><span data-stu-id="7f721-259">Retrieval is denied.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="7f721-260"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="7f721-260"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7f721-261">A recuperação é permitida.</span><span class="sxs-lookup"><span data-stu-id="7f721-261">Retrieval is allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f721-262">**SessionDirectoryIPAddress**</span><span class="sxs-lookup"><span data-stu-id="7f721-262">**SessionDirectoryIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-263">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7f721-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-264">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7f721-264">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7f721-265">O endereço IP do adaptador de LAN usado pelo diretório de sessão.</span><span class="sxs-lookup"><span data-stu-id="7f721-265">The IP address of the LAN adapter used by the session directory.</span></span>

</dd> <dt>

<span data-ttu-id="7f721-266">**SessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="7f721-266">**SessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7f721-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f721-269">O nome DNS da rede ou o endereço IP do servidor em que o serviço do agente de conexão de área de trabalho remota está em execução.</span><span class="sxs-lookup"><span data-stu-id="7f721-269">The network DNS name or IP address of the server where the RD Connection Broker service is running.</span></span>

</dd> <dt>

<span data-ttu-id="7f721-270">**Status**</span><span class="sxs-lookup"><span data-stu-id="7f721-270">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f721-271">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7f721-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f721-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f721-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f721-273">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="7f721-273">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="7f721-274">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="7f721-274">Current status of the object.</span></span> <span data-ttu-id="7f721-275">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="7f721-275">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7f721-276">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="7f721-276">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7f721-277">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="7f721-277">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7f721-278">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="7f721-278">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7f721-279">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="7f721-279">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7f721-280">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f721-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="7f721-281">("OK")</span><span class="sxs-lookup"><span data-stu-id="7f721-281">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7f721-282">("Erro")</span><span class="sxs-lookup"><span data-stu-id="7f721-282">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7f721-283">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="7f721-283">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7f721-284">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="7f721-284">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7f721-285">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7f721-285">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7f721-286">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="7f721-286">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7f721-287">("Parando")</span><span class="sxs-lookup"><span data-stu-id="7f721-287">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7f721-288">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="7f721-288">("Service")</span></span>


<span data-ttu-id="7f721-289"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7f721-289"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7f721-290">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f721-290">Remarks</span></span>

<span data-ttu-id="7f721-291">Para se conectar ao \\ \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="7f721-291">To connect to the \\\\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="7f721-292">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="7f721-292">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="7f721-293">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de seis.</span><span class="sxs-lookup"><span data-stu-id="7f721-293">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="7f721-294">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="7f721-294">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="7f721-295">No Windows Server 2008, o nome do recurso do diretório de sessões dos serviços de terminal foi alterado para agente de sessão dos serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="7f721-295">In Windows Server 2008, the name of the Terminal Services Session Directory feature was changed to Terminal Services Session Broker.</span></span>

<span data-ttu-id="7f721-296">No Windows Server 2008 R2, o nome do recurso de agente de sessão dos serviços de terminal foi alterado para Conexão de Área de Trabalho Remota Broker.</span><span class="sxs-lookup"><span data-stu-id="7f721-296">In Windows Server 2008 R2, the name of the Terminal Services Session Broker feature was changed to Remote Desktop Connection Broker.</span></span>

<span data-ttu-id="7f721-297">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7f721-297">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7f721-298">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7f721-298">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7f721-299">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="7f721-299">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7f721-300">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7f721-300">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f721-301">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f721-301">Requirements</span></span>



| <span data-ttu-id="7f721-302">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f721-302">Requirement</span></span> | <span data-ttu-id="7f721-303">Valor</span><span class="sxs-lookup"><span data-stu-id="7f721-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f721-304">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f721-304">Minimum supported client</span></span><br/> | <span data-ttu-id="7f721-305">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7f721-305">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7f721-306">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f721-306">Minimum supported server</span></span><br/> | <span data-ttu-id="7f721-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f721-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f721-308">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f721-308">Namespace</span></span><br/>                | <span data-ttu-id="7f721-309">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="7f721-309">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7f721-310">MOF</span><span class="sxs-lookup"><span data-stu-id="7f721-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f721-311"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f721-311"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f721-312">DLL</span><span class="sxs-lookup"><span data-stu-id="7f721-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f721-313"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f721-313"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f721-314">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f721-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f721-315">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="7f721-315">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="7f721-316">**\_TSSessionDirectorySetting Win32**</span><span class="sxs-lookup"><span data-stu-id="7f721-316">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

