---
title: Classe Win32_TSPermissionsSetting
description: Inclui um método para adicionar novas contas ao terminal e um método para restaurar as permissões padrão para um terminal.
ms.assetid: ebc6e96a-668e-44aa-b589-c3e476fb3029
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSPermissionsSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSPermissionsSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting.Caption
- Win32_TSPermissionsSetting.Description
- Win32_TSPermissionsSetting.InstallDate
- Win32_TSPermissionsSetting.Name
- Win32_TSPermissionsSetting.Status
- Win32_TSPermissionsSetting.TerminalName
- Win32_TSPermissionsSetting.DenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.PolicySourceDenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.StringSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877b8373667bf01010ceb63c0ec35e46db48f702
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764731"
---
# <a name="win32_tspermissionssetting-class"></a><span data-ttu-id="1b52f-105">\_Classe Win32 TSPermissionsSetting</span><span class="sxs-lookup"><span data-stu-id="1b52f-105">Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="1b52f-106">A classe WMI **\_ TSPermissionsSetting do Win32** inclui um método para adicionar novas contas ao terminal e um método para restaurar as permissões padrão para um terminal.</span><span class="sxs-lookup"><span data-stu-id="1b52f-106">The **Win32\_TSPermissionsSetting** WMI class includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

<span data-ttu-id="1b52f-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="1b52f-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="1b52f-108">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="1b52f-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b52f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b52f-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSPERMISSIONSSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSPermissionsSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   DenyAdminPermissionForCustomization;
  uint32   PolicySourceDenyAdminPermissionForCustomization;
  string   StringSecurityDescriptor;
};
```

## <a name="members"></a><span data-ttu-id="1b52f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="1b52f-110">Members</span></span>

<span data-ttu-id="1b52f-111">A classe **Win32 \_ TSPermissionsSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1b52f-111">The **Win32\_TSPermissionsSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="1b52f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1b52f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1b52f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b52f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1b52f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="1b52f-114">Methods</span></span>

<span data-ttu-id="1b52f-115">A classe **Win32 \_ TSPermissionsSetting** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1b52f-115">The **Win32\_TSPermissionsSetting** class has these methods.</span></span>



| <span data-ttu-id="1b52f-116">Método</span><span class="sxs-lookup"><span data-stu-id="1b52f-116">Method</span></span>                                                                | <span data-ttu-id="1b52f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b52f-117">Description</span></span>                                                                                                                    |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b52f-118">**Addconta**</span><span class="sxs-lookup"><span data-stu-id="1b52f-118">**AddAccount**</span></span>](win32-tspermissionssetting-addaccount.md)           | <span data-ttu-id="1b52f-119">Adiciona uma conta ao terminal com o conjunto de permissões especificado no valor do parâmetro *PermissionPreSet* .</span><span class="sxs-lookup"><span data-stu-id="1b52f-119">Adds an account to the terminal with the permission set specified in the value of the *PermissionPreSet* parameter.</span></span><br/> |
| [<span data-ttu-id="1b52f-120">**RestoreDefaults**</span><span class="sxs-lookup"><span data-stu-id="1b52f-120">**RestoreDefaults**</span></span>](win32-tspermissionssetting-restoredefaults.md) | <span data-ttu-id="1b52f-121">Restaura os valores padrão do conjunto de permissões para o terminal.</span><span class="sxs-lookup"><span data-stu-id="1b52f-121">Restores the default permission set values for the terminal.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="1b52f-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b52f-122">Properties</span></span>

<span data-ttu-id="1b52f-123">A classe **Win32 \_ TSPermissionsSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1b52f-123">The **Win32\_TSPermissionsSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b52f-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1b52f-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b52f-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b52f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b52f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-127">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1b52f-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1b52f-128">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b52f-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="1b52f-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1b52f-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b52f-130">**DenyAdminPermissionForCustomization**</span><span class="sxs-lookup"><span data-stu-id="1b52f-130">**DenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b52f-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b52f-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b52f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b52f-133">Especifica se o administrador local tem permissão para personalizar.</span><span class="sxs-lookup"><span data-stu-id="1b52f-133">Specifies whether local administrator has permission to customize.</span></span>

</dd> <dt>

<span data-ttu-id="1b52f-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b52f-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b52f-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b52f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b52f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b52f-137">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b52f-137">Description of the object.</span></span>

<span data-ttu-id="1b52f-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1b52f-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b52f-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1b52f-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b52f-140">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1b52f-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b52f-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-142">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="1b52f-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="1b52f-143">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="1b52f-143">The date the object was installed.</span></span> <span data-ttu-id="1b52f-144">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="1b52f-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1b52f-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1b52f-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b52f-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1b52f-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b52f-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b52f-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b52f-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b52f-149">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b52f-149">The name of the object.</span></span>

<span data-ttu-id="1b52f-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1b52f-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b52f-151">**PolicySourceDenyAdminPermissionForCustomization**</span><span class="sxs-lookup"><span data-stu-id="1b52f-151">**PolicySourceDenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b52f-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b52f-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b52f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b52f-154">Indica se a propriedade **MinEncryptionLevel** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="1b52f-154">Indicates whether the **MinEncryptionLevel** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="1b52f-155">0</span><span class="sxs-lookup"><span data-stu-id="1b52f-155">0</span></span>
</dt> <dd>

<span data-ttu-id="1b52f-156">Servidor</span><span class="sxs-lookup"><span data-stu-id="1b52f-156">Server</span></span>

</dd> <dt>

<span data-ttu-id="1b52f-157">1</span><span class="sxs-lookup"><span data-stu-id="1b52f-157">1</span></span>
</dt> <dd>

<span data-ttu-id="1b52f-158">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="1b52f-158">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1b52f-159">**Status**</span><span class="sxs-lookup"><span data-stu-id="1b52f-159">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b52f-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b52f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b52f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-162">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="1b52f-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="1b52f-163">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b52f-163">Current status of the object.</span></span> <span data-ttu-id="1b52f-164">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="1b52f-164">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1b52f-165">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="1b52f-165">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1b52f-166">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="1b52f-166">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1b52f-167">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="1b52f-167">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1b52f-168">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="1b52f-168">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1b52f-169">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1b52f-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="1b52f-170">("OK")</span><span class="sxs-lookup"><span data-stu-id="1b52f-170">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b52f-171">("Erro")</span><span class="sxs-lookup"><span data-stu-id="1b52f-171">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b52f-172">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="1b52f-172">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b52f-173">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="1b52f-173">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b52f-174">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1b52f-174">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b52f-175">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="1b52f-175">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b52f-176">("Parando")</span><span class="sxs-lookup"><span data-stu-id="1b52f-176">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b52f-177">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="1b52f-177">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b52f-178">**StringSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1b52f-178">**StringSecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b52f-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b52f-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-180">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b52f-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1b52f-181">Descritor de segurança associado ao terminal em formato de matriz de bytes binários.</span><span class="sxs-lookup"><span data-stu-id="1b52f-181">Security descriptor associated with the terminal in binary byte array format.</span></span>

</dd> <dt>

<span data-ttu-id="1b52f-182">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="1b52f-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b52f-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b52f-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b52f-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b52f-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b52f-185">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="1b52f-185">The name of the terminal.</span></span>

<span data-ttu-id="1b52f-186">Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="1b52f-186">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b52f-187">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b52f-187">Remarks</span></span>

<span data-ttu-id="1b52f-188">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="1b52f-188">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="1b52f-189">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="1b52f-189">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="1b52f-190">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="1b52f-190">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="1b52f-191">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="1b52f-191">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="1b52f-192">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1b52f-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1b52f-193">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1b52f-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1b52f-194">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="1b52f-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1b52f-195">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1b52f-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b52f-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b52f-196">Requirements</span></span>



| <span data-ttu-id="1b52f-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b52f-197">Requirement</span></span> | <span data-ttu-id="1b52f-198">Valor</span><span class="sxs-lookup"><span data-stu-id="1b52f-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b52f-199">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b52f-199">Minimum supported client</span></span><br/> | <span data-ttu-id="1b52f-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b52f-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b52f-201">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b52f-201">Minimum supported server</span></span><br/> | <span data-ttu-id="1b52f-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b52f-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b52f-203">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b52f-203">Namespace</span></span><br/>                | <span data-ttu-id="1b52f-204">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="1b52f-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1b52f-205">MOF</span><span class="sxs-lookup"><span data-stu-id="1b52f-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b52f-206"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b52f-206"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b52f-207">DLL</span><span class="sxs-lookup"><span data-stu-id="1b52f-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b52f-208"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b52f-208"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b52f-209">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b52f-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b52f-210">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="1b52f-210">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

