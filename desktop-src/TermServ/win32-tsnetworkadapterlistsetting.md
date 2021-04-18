---
title: Classe Win32_TSNetworkAdapterListSetting
description: Enumera a lista de adaptadores de rede que podem ser configurados para um terminal do Win32 \_ , com base no protocolo de terminal e no método de transporte especificados.
ms.assetid: affe440a-1a7b-49be-a4aa-d792811c59ea
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSNetworkAdapterListSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSNetworkAdapterListSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterListSetting
- Win32_TSNetworkAdapterListSetting.Caption
- Win32_TSNetworkAdapterListSetting.Description
- Win32_TSNetworkAdapterListSetting.InstallDate
- Win32_TSNetworkAdapterListSetting.Name
- Win32_TSNetworkAdapterListSetting.Status
- Win32_TSNetworkAdapterListSetting.TerminalName
- Win32_TSNetworkAdapterListSetting.NetworkAdapterID
- Win32_TSNetworkAdapterListSetting.NetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8c1ac9466d389924d0717748d7da9ec1f5b55f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779265"
---
# <a name="win32_tsnetworkadapterlistsetting-class"></a><span data-ttu-id="ce2c3-105">\_Classe Win32 TSNetworkAdapterListSetting</span><span class="sxs-lookup"><span data-stu-id="ce2c3-105">Win32\_TSNetworkAdapterListSetting class</span></span>

<span data-ttu-id="ce2c3-106">A classe WMI **\_ TSNetworkAdapterListSetting do Win32** enumera a lista de adaptadores de rede que podem ser configurados para um [**\_ terminal do Win32**](win32-terminal.md), com base no protocolo de terminal e no método de transporte especificados.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-106">The **Win32\_TSNetworkAdapterListSetting** WMI class enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

<span data-ttu-id="ce2c3-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce2c3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce2c3-108">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSNETWORKADAPTERLISTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterListSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   NetworkAdapterID;
  string   NetworkAdapterIP;
};
```

## <a name="members"></a><span data-ttu-id="ce2c3-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ce2c3-109">Members</span></span>

<span data-ttu-id="ce2c3-110">A classe **Win32 \_ TSNetworkAdapterListSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ce2c3-110">The **Win32\_TSNetworkAdapterListSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ce2c3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce2c3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce2c3-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce2c3-112">Properties</span></span>

<span data-ttu-id="ce2c3-113">A classe **Win32 \_ TSNetworkAdapterListSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-113">The **Win32\_TSNetworkAdapterListSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce2c3-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2c3-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce2c3-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ce2c3-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ce2c3-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ce2c3-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ce2c3-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce2c3-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2c3-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce2c3-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce2c3-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-123">Description of the object.</span></span>

<span data-ttu-id="ce2c3-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ce2c3-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce2c3-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2c3-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce2c3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-128">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="ce2c3-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ce2c3-129">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-129">The date the object was installed.</span></span> <span data-ttu-id="ce2c3-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ce2c3-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ce2c3-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce2c3-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2c3-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce2c3-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce2c3-135">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-135">The name of the object.</span></span>

<span data-ttu-id="ce2c3-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ce2c3-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce2c3-137">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-137">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2c3-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce2c3-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce2c3-140">O GUID do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-140">The GUID of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ce2c3-141">**NetworkAdapterIP**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-141">**NetworkAdapterIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2c3-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce2c3-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-144">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ce2c3-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ce2c3-145">O endereço IP do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-145">The IP address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ce2c3-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2c3-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce2c3-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-149">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ce2c3-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ce2c3-150">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-150">Current status of the object.</span></span> <span data-ttu-id="ce2c3-151">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ce2c3-152">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="ce2c3-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ce2c3-153">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="ce2c3-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ce2c3-154">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ce2c3-155">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ce2c3-156">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ce2c3-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ce2c3-157">("OK")</span><span class="sxs-lookup"><span data-stu-id="ce2c3-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ce2c3-158">("Erro")</span><span class="sxs-lookup"><span data-stu-id="ce2c3-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ce2c3-159">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="ce2c3-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ce2c3-160">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="ce2c3-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ce2c3-161">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ce2c3-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ce2c3-162">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="ce2c3-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ce2c3-163">("Parando")</span><span class="sxs-lookup"><span data-stu-id="ce2c3-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ce2c3-164">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="ce2c3-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce2c3-165">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-165">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2c3-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2c3-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce2c3-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce2c3-168">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-168">The name of the terminal.</span></span>

<span data-ttu-id="ce2c3-169">Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="ce2c3-169">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce2c3-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce2c3-170">Remarks</span></span>

<span data-ttu-id="ce2c3-171">Para se conectar ao namespace " \\ \\ terminal cimv2" raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-171">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="ce2c3-172">Para chamadas C/C++, isso seria um nível de autenticação de **privacidade do PCT no nível do RPC \_ C \_ Authn \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-172">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="ce2c3-173">Para chamadas de script e de Visual Basic, isso seria um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-173">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="ce2c3-174">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-174">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="ce2c3-175">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ce2c3-175">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ce2c3-176">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-176">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ce2c3-177">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-177">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ce2c3-178">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ce2c3-178">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce2c3-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce2c3-179">Requirements</span></span>



| <span data-ttu-id="ce2c3-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce2c3-180">Requirement</span></span> | <span data-ttu-id="ce2c3-181">Valor</span><span class="sxs-lookup"><span data-stu-id="ce2c3-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2c3-182">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce2c3-182">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2c3-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce2c3-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce2c3-184">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce2c3-184">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2c3-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce2c3-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce2c3-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce2c3-186">Namespace</span></span><br/>                | <span data-ttu-id="ce2c3-187">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="ce2c3-187">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ce2c3-188">MOF</span><span class="sxs-lookup"><span data-stu-id="ce2c3-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce2c3-189"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce2c3-189"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce2c3-190">DLL</span><span class="sxs-lookup"><span data-stu-id="ce2c3-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce2c3-191"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce2c3-191"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce2c3-192">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce2c3-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce2c3-193">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-193">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="ce2c3-194">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="ce2c3-194">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

