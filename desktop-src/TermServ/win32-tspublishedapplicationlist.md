---
title: Classe Win32_TSPublishedApplicationList
description: Representa a lista de programas que estão na lista de programas do RemoteApp em um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 3dbefe54-8c31-439f-a87a-5148214a07d5
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSPublishedApplicationList Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSPublishedApplicationList classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplicationList
- Win32_TSPublishedApplicationList.Caption
- Win32_TSPublishedApplicationList.Description
- Win32_TSPublishedApplicationList.InstallDate
- Win32_TSPublishedApplicationList.Name
- Win32_TSPublishedApplicationList.Status
- Win32_TSPublishedApplicationList.Disabled
- Win32_TSPublishedApplicationList.PolicySourceDisabled
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f87a87dc6f95bcdb33c7dbd1364ad6b3114ddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009235"
---
# <a name="win32_tspublishedapplicationlist-class"></a><span data-ttu-id="88825-105">\_Classe Win32 TSPublishedApplicationList</span><span class="sxs-lookup"><span data-stu-id="88825-105">Win32\_TSPublishedApplicationList class</span></span>

<span data-ttu-id="88825-106">Representa a lista de programas que estão na lista de programas do RemoteApp em um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="88825-106">Represents the list of programs that are in the RemoteApp Programs list on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="88825-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88825-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplicationList : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  Disabled;
  uint32   PolicySourceDisabled;
};
```

## <a name="members"></a><span data-ttu-id="88825-108">Membros</span><span class="sxs-lookup"><span data-stu-id="88825-108">Members</span></span>

<span data-ttu-id="88825-109">A classe **Win32 \_ TSPublishedApplicationList** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="88825-109">The **Win32\_TSPublishedApplicationList** class has these types of members:</span></span>

-   [<span data-ttu-id="88825-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="88825-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88825-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="88825-111">Properties</span></span>

<span data-ttu-id="88825-112">A classe **Win32 \_ TSPublishedApplicationList** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="88825-112">The **Win32\_TSPublishedApplicationList** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88825-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="88825-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88825-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="88825-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88825-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88825-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88825-116">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="88825-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88825-117">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="88825-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="88825-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88825-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88825-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="88825-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88825-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="88825-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88825-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88825-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88825-122">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="88825-122">Description of the object.</span></span>

<span data-ttu-id="88825-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88825-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88825-124">**Desabilitado**</span><span class="sxs-lookup"><span data-stu-id="88825-124">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88825-125">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="88825-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88825-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="88825-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="88825-127">Indica se o servidor de Host da Sessão RD restringe os programas que um usuário pode iniciar na conexão inicial com os programas que estão na lista de programas do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="88825-127">Indicates whether the RD Session Host server restricts the programs that a user can start on initial connection to the programs that are in the RemoteApp Programs list.</span></span>

</dd> <dt>

<span data-ttu-id="88825-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88825-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88825-129">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88825-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88825-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88825-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88825-131">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="88825-131">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="88825-132">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="88825-132">The date the object was installed.</span></span> <span data-ttu-id="88825-133">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="88825-133">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="88825-134">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88825-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88825-135">**Nome**</span><span class="sxs-lookup"><span data-stu-id="88825-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88825-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="88825-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88825-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88825-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88825-138">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="88825-138">The name of the object.</span></span>

<span data-ttu-id="88825-139">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88825-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88825-140">**PolicySourceDisabled**</span><span class="sxs-lookup"><span data-stu-id="88825-140">**PolicySourceDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88825-141">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88825-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88825-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88825-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88825-143">Indica onde a propriedade **desabilitada** está configurada.</span><span class="sxs-lookup"><span data-stu-id="88825-143">Indicates where the **Disabled** property is configured.</span></span> <span data-ttu-id="88825-144">Os valores possíveis incluem:</span><span class="sxs-lookup"><span data-stu-id="88825-144">Possible values include:</span></span>

<dt>

<span data-ttu-id="88825-145">0</span><span class="sxs-lookup"><span data-stu-id="88825-145">0</span></span>
</dt> <dd>

<span data-ttu-id="88825-146">A configuração é configurada no servidor por meio de Gerenciador RemoteApp ou do provedor WMI do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="88825-146">The setting is configured on the server through RemoteApp Manager or the RemoteApp WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="88825-147">1</span><span class="sxs-lookup"><span data-stu-id="88825-147">1</span></span>
</dt> <dd>

<span data-ttu-id="88825-148">A configuração é definida por meio da diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="88825-148">The setting is configured through group policy.</span></span>

</dd> <dt>

<span data-ttu-id="88825-149">2</span><span class="sxs-lookup"><span data-stu-id="88825-149">2</span></span>
</dt> <dd>

<span data-ttu-id="88825-150">A configuração não está configurada.</span><span class="sxs-lookup"><span data-stu-id="88825-150">The setting is not configured.</span></span> <span data-ttu-id="88825-151">O valor padrão **false** é usado para a propriedade **Disabled** .</span><span class="sxs-lookup"><span data-stu-id="88825-151">The default value of **FALSE** is used for the **Disabled** property.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="88825-152">**Status**</span><span class="sxs-lookup"><span data-stu-id="88825-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88825-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="88825-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88825-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88825-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88825-155">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="88825-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="88825-156">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="88825-156">Current status of the object.</span></span> <span data-ttu-id="88825-157">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="88825-157">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="88825-158">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="88825-158">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="88825-159">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="88825-159">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="88825-160">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="88825-160">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="88825-161">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="88825-161">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="88825-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88825-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="88825-163">("OK")</span><span class="sxs-lookup"><span data-stu-id="88825-163">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88825-164">("Erro")</span><span class="sxs-lookup"><span data-stu-id="88825-164">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88825-165">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="88825-165">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88825-166">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="88825-166">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88825-167">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="88825-167">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88825-168">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="88825-168">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88825-169">("Parando")</span><span class="sxs-lookup"><span data-stu-id="88825-169">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88825-170">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="88825-170">("Service")</span></span>


<span data-ttu-id="88825-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="88825-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="88825-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="88825-172">Remarks</span></span>

<span data-ttu-id="88825-173">Você deve ser um membro do grupo Administradores para definir propriedades usando essa classe.</span><span class="sxs-lookup"><span data-stu-id="88825-173">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="88825-174">A propriedade **Disabled** não impede que os usuários iniciem programas não listados remotamente depois de se conectarem ao servidor de host da Sessão RD usando um programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="88825-174">The **Disabled** property does not prevent users from starting unlisted programs remotely after they connect to the RD Session Host server by using a RemoteApp program.</span></span>

<span data-ttu-id="88825-175">A propriedade **Disabled** será definida como um valor de 2 somente se a seguinte entrada do registro estiver ausente:</span><span class="sxs-lookup"><span data-stu-id="88825-175">The **Disabled** property will be set to a value of 2 only if the following registry entry is missing:</span></span>

<span data-ttu-id="88825-176">**HKEY \_ SOFTWARE de \_ máquina local** \\  \\ **Microsoft** \\  \\  \\ **TerminalServer** CurrentVersion \\ **TSAppAllowList** \\ **fDisabledAllowList**</span><span class="sxs-lookup"><span data-stu-id="88825-176">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WindowsNT**\\**CurrentVersion**\\**TerminalServer**\\**TSAppAllowList**\\**fDisabledAllowList**</span></span>

<span data-ttu-id="88825-177">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="88825-177">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="88825-178">Para chamadas C/C++, esse é um nível de autenticação **de \_ \_ privacidade do \_ PCT no \_ nível \_** de autenticado RPC C, que pode ser definido usando a função com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="88825-178">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="88825-179">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="88825-179">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="88825-180">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="88825-180">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="88825-181">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="88825-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="88825-182">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="88825-182">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="88825-183">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="88825-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="88825-184">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="88825-184">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="88825-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88825-185">Requirements</span></span>



| <span data-ttu-id="88825-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="88825-186">Requirement</span></span> | <span data-ttu-id="88825-187">Valor</span><span class="sxs-lookup"><span data-stu-id="88825-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88825-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88825-188">Minimum supported client</span></span><br/> | <span data-ttu-id="88825-189">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="88825-189">None supported</span></span><br/>                                                               |
| <span data-ttu-id="88825-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88825-190">Minimum supported server</span></span><br/> | <span data-ttu-id="88825-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88825-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88825-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="88825-192">Namespace</span></span><br/>                | <span data-ttu-id="88825-193">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="88825-193">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="88825-194">MOF</span><span class="sxs-lookup"><span data-stu-id="88825-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88825-195"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88825-195"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="88825-196">DLL</span><span class="sxs-lookup"><span data-stu-id="88825-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88825-197"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88825-197"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

