---
title: Classe Win32_TSDiscoveredLicenseServer
description: Fornece detalhes sobre o servidor de licença Área de Trabalho Remota descoberto.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSDiscoveredLicenseServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSDiscoveredLicenseServer classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455849"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a><span data-ttu-id="08bab-105">\_Classe Win32 TSDiscoveredLicenseServer</span><span class="sxs-lookup"><span data-stu-id="08bab-105">Win32\_TSDiscoveredLicenseServer class</span></span>

<span data-ttu-id="08bab-106">Fornece detalhes sobre o servidor de licença Área de Trabalho Remota descoberto.</span><span class="sxs-lookup"><span data-stu-id="08bab-106">Provides details about the discovered Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="08bab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08bab-107">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a><span data-ttu-id="08bab-108">Membros</span><span class="sxs-lookup"><span data-stu-id="08bab-108">Members</span></span>

<span data-ttu-id="08bab-109">A classe **Win32 \_ TSDiscoveredLicenseServer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08bab-109">The **Win32\_TSDiscoveredLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="08bab-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08bab-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08bab-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08bab-111">Properties</span></span>

<span data-ttu-id="08bab-112">A classe **Win32 \_ TSDiscoveredLicenseServer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="08bab-112">The **Win32\_TSDiscoveredLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08bab-113">**HowDiscovered**</span><span class="sxs-lookup"><span data-stu-id="08bab-113">**HowDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bab-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08bab-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bab-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08bab-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bab-116">Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="08bab-116">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="08bab-117">Esta propriedade não é mais suportada.</span><span class="sxs-lookup"><span data-stu-id="08bab-117">This property is no longer supported.</span></span>

<span data-ttu-id="08bab-118">**Windows Server 2008:** O método de descoberta do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="08bab-118">**Windows Server 2008:** The Remote Desktop license server discovery method.</span></span>

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span data-ttu-id="08bab-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span><span class="sxs-lookup"><span data-stu-id="08bab-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-120">O servidor de licença foi descoberto usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="08bab-120">The license server was discovered by using group policy.</span></span>

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span data-ttu-id="08bab-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span><span class="sxs-lookup"><span data-stu-id="08bab-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-122">O servidor de licença foi descoberto usando uma configuração de registro.</span><span class="sxs-lookup"><span data-stu-id="08bab-122">The license server was discovered by using a registry setting.</span></span>

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span data-ttu-id="08bab-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span><span class="sxs-lookup"><span data-stu-id="08bab-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-124">O servidor de licença foi descoberto usando o escopo de descoberta de grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="08bab-124">The license server was discovered by using the workgroup discovery scope.</span></span>

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span data-ttu-id="08bab-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span><span class="sxs-lookup"><span data-stu-id="08bab-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-126">O servidor de licença foi descoberto usando o escopo de descoberta de domínio.</span><span class="sxs-lookup"><span data-stu-id="08bab-126">The license server was discovered by using the domain discovery scope.</span></span>

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span data-ttu-id="08bab-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span><span class="sxs-lookup"><span data-stu-id="08bab-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-128">O servidor de licença foi descoberto usando o escopo de descoberta de floresta.</span><span class="sxs-lookup"><span data-stu-id="08bab-128">The license server was discovered by using the forest discovery scope.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08bab-129">**IsAdminOnLS**</span><span class="sxs-lookup"><span data-stu-id="08bab-129">**IsAdminOnLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bab-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08bab-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bab-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08bab-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08bab-132">Indica se a conta que está sendo usada para executar o script ou o arquivo. exe que está usando a classe **Win32 \_ TSDiscoveredLicenseServer** tem acesso de administrador ao servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="08bab-132">Indicates whether the account that is being used to run the script or .exe file that is using the **Win32\_TSDiscoveredLicenseServer** class has administrator access to the license server.</span></span>

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span data-ttu-id="08bab-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**Não** (0)</span><span class="sxs-lookup"><span data-stu-id="08bab-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-134">A conta que está sendo usada não tem acesso de administrador ao servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="08bab-134">The account that is being used does not have administrator access to the license server.</span></span>

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span data-ttu-id="08bab-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Sim** (1)</span><span class="sxs-lookup"><span data-stu-id="08bab-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Yes** (1)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-136">A conta que está sendo usada tem acesso de administrador ao servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="08bab-136">The account that is being used has administrator access to the license server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="08bab-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Não **sei** (2)</span><span class="sxs-lookup"><span data-stu-id="08bab-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-138">Não é possível determinar se a conta que está sendo usada tem acesso de administrador ao servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="08bab-138">It cannot be determined whether the account that is being used has administrator access to the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08bab-139">**IsLSAvailable**</span><span class="sxs-lookup"><span data-stu-id="08bab-139">**IsLSAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bab-140">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08bab-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bab-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08bab-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08bab-142">Indica se o servidor de licença está disponível (se uma conexão RPC de chamada de procedimento remoto \[ \] pode ser feita no servidor).</span><span class="sxs-lookup"><span data-stu-id="08bab-142">Indicates whether the license server is available (whether a remote procedure call \[RPC\] connection can be made to the server).</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="08bab-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="08bab-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-144">O servidor de licença não está disponível.</span><span class="sxs-lookup"><span data-stu-id="08bab-144">The license server is not available.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="08bab-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="08bab-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-146">O servidor de licença está disponível.</span><span class="sxs-lookup"><span data-stu-id="08bab-146">The license server is available.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08bab-147">**IssuingCALs**</span><span class="sxs-lookup"><span data-stu-id="08bab-147">**IssuingCALs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bab-148">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08bab-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08bab-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08bab-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08bab-150">Indica se o servidor de licença pode emitir Serviços de Área de Trabalho Remota licenças de acesso para cliente (RDS CALs) para o servidor Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="08bab-150">Indicates whether the license server is allowed to issue Remote Desktop Services client access licenses (RDS CALs) to the RD Session Host server.</span></span>

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="08bab-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Não permitido** (0)</span><span class="sxs-lookup"><span data-stu-id="08bab-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not Allowed** (0)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-152">O servidor de licença não tem permissão para emitir CALs RDS para o servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="08bab-152">The license server is not allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span data-ttu-id="08bab-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Permitido** (1)</span><span class="sxs-lookup"><span data-stu-id="08bab-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Allowed** (1)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-154">O servidor de licença pode emitir RDS CALs para o servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="08bab-154">The license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="08bab-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Não **sei** (2)</span><span class="sxs-lookup"><span data-stu-id="08bab-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="08bab-156">Não é possível determinar se o servidor de licença tem permissão para emitir RDS CALs para o servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="08bab-156">It cannot be determined whether the license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08bab-157">**LicenseServer**</span><span class="sxs-lookup"><span data-stu-id="08bab-157">**LicenseServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08bab-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08bab-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08bab-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08bab-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08bab-160">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08bab-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="08bab-161">Nome do servidor de licença de Área de Trabalho Remota descoberto.</span><span class="sxs-lookup"><span data-stu-id="08bab-161">Name of the discovered Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08bab-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="08bab-162">Remarks</span></span>

<span data-ttu-id="08bab-163">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="08bab-163">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="08bab-164">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="08bab-164">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="08bab-165">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="08bab-165">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="08bab-166">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="08bab-166">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="08bab-167">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="08bab-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="08bab-168">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="08bab-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="08bab-169">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="08bab-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="08bab-170">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="08bab-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="08bab-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08bab-171">Requirements</span></span>



| <span data-ttu-id="08bab-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="08bab-172">Requirement</span></span> | <span data-ttu-id="08bab-173">Valor</span><span class="sxs-lookup"><span data-stu-id="08bab-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08bab-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08bab-174">Minimum supported client</span></span><br/> | <span data-ttu-id="08bab-175">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="08bab-175">None supported</span></span><br/>                                                               |
| <span data-ttu-id="08bab-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08bab-176">Minimum supported server</span></span><br/> | <span data-ttu-id="08bab-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08bab-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08bab-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="08bab-178">Namespace</span></span><br/>                | <span data-ttu-id="08bab-179">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="08bab-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="08bab-180">MOF</span><span class="sxs-lookup"><span data-stu-id="08bab-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08bab-181"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08bab-181"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="08bab-182">DLL</span><span class="sxs-lookup"><span data-stu-id="08bab-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08bab-183"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08bab-183"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

