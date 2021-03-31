---
title: Classe Win32_TSStartMenuApplication
description: Descreve os aplicativos que estão no menu iniciar de um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 88b412b8-139f-4266-b7d8-c34f93940a72
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSStartMenuApplication Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSStartMenuApplication classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSStartMenuApplication
- Win32_TSStartMenuApplication.Caption
- Win32_TSStartMenuApplication.Description
- Win32_TSStartMenuApplication.InstallDate
- Win32_TSStartMenuApplication.Name
- Win32_TSStartMenuApplication.Status
- Win32_TSStartMenuApplication.Path
- Win32_TSStartMenuApplication.VPath
- Win32_TSStartMenuApplication.IconPath
- Win32_TSStartMenuApplication.IconIndex
- Win32_TSStartMenuApplication.CommandLineArguments
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dae7610381745f6ced2a01e76f8545b33d1205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645173"
---
# <a name="win32_tsstartmenuapplication-class"></a><span data-ttu-id="6499e-105">\_Classe Win32 TSStartMenuApplication</span><span class="sxs-lookup"><span data-stu-id="6499e-105">Win32\_TSStartMenuApplication class</span></span>

<span data-ttu-id="6499e-106">Descreve os aplicativos que estão no menu iniciar de um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="6499e-106">Describes the applications that are on the Start menu of a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6499e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6499e-107">Syntax</span></span>

``` syntax
class Win32_TSStartMenuApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Path;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  string   CommandLineArguments;
};
```

## <a name="members"></a><span data-ttu-id="6499e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6499e-108">Members</span></span>

<span data-ttu-id="6499e-109">A classe **Win32 \_ TSStartMenuApplication** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6499e-109">The **Win32\_TSStartMenuApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="6499e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6499e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6499e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6499e-111">Properties</span></span>

<span data-ttu-id="6499e-112">A classe **Win32 \_ TSStartMenuApplication** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6499e-112">The **Win32\_TSStartMenuApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6499e-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6499e-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6499e-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6499e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6499e-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6499e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6499e-116">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6499e-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6499e-117">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="6499e-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="6499e-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6499e-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6499e-119">**CommandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="6499e-119">**CommandLineArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6499e-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6499e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6499e-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6499e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6499e-122">Os argumentos de linha de comando a serem usados.</span><span class="sxs-lookup"><span data-stu-id="6499e-122">The command-line arguments to use.</span></span>

</dd> <dt>

<span data-ttu-id="6499e-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6499e-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6499e-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6499e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6499e-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6499e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6499e-126">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="6499e-126">Description of the object.</span></span>

<span data-ttu-id="6499e-127">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6499e-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6499e-128">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="6499e-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6499e-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6499e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6499e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6499e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6499e-131">O índice ou a ID do ícone.</span><span class="sxs-lookup"><span data-stu-id="6499e-131">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="6499e-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="6499e-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6499e-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6499e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6499e-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6499e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6499e-135">O caminho do ícone do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6499e-135">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="6499e-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6499e-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6499e-137">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6499e-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6499e-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6499e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6499e-139">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="6499e-139">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6499e-140">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="6499e-140">The date the object was installed.</span></span> <span data-ttu-id="6499e-141">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="6499e-141">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6499e-142">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6499e-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6499e-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6499e-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6499e-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6499e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6499e-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6499e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6499e-146">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="6499e-146">The name of the object.</span></span>

<span data-ttu-id="6499e-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6499e-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6499e-148">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="6499e-148">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6499e-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6499e-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6499e-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6499e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6499e-151">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="6499e-151">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6499e-152">O caminho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6499e-152">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="6499e-153">**Status**</span><span class="sxs-lookup"><span data-stu-id="6499e-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6499e-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6499e-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6499e-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6499e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6499e-156">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="6499e-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="6499e-157">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6499e-157">Current status of the object.</span></span> <span data-ttu-id="6499e-158">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="6499e-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6499e-159">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="6499e-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6499e-160">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="6499e-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6499e-161">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="6499e-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6499e-162">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="6499e-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6499e-163">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6499e-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="6499e-164">("OK")</span><span class="sxs-lookup"><span data-stu-id="6499e-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6499e-165">("Erro")</span><span class="sxs-lookup"><span data-stu-id="6499e-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6499e-166">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="6499e-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6499e-167">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6499e-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6499e-168">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6499e-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6499e-169">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="6499e-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6499e-170">("Parando")</span><span class="sxs-lookup"><span data-stu-id="6499e-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6499e-171">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="6499e-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6499e-172">**VPath**</span><span class="sxs-lookup"><span data-stu-id="6499e-172">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6499e-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6499e-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6499e-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6499e-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6499e-175">O caminho virtual do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6499e-175">The virtual path of the application.</span></span> <span data-ttu-id="6499e-176">Isso inclui variáveis de ambiente do sistema, como% windir%.</span><span class="sxs-lookup"><span data-stu-id="6499e-176">This includes system environment variables, such as %windir%.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6499e-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="6499e-177">Remarks</span></span>

<span data-ttu-id="6499e-178">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="6499e-178">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="6499e-179">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="6499e-179">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="6499e-180">Para chamadas C/C++, esse é um nível de autenticação **de \_ \_ privacidade do \_ PCT no \_ nível \_** de autenticado RPC C, que pode ser definido usando a função com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="6499e-180">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="6499e-181">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="6499e-181">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="6499e-182">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="6499e-182">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="6499e-183">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6499e-183">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6499e-184">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6499e-184">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6499e-185">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="6499e-185">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6499e-186">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6499e-186">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6499e-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6499e-187">Requirements</span></span>



| <span data-ttu-id="6499e-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="6499e-188">Requirement</span></span> | <span data-ttu-id="6499e-189">Valor</span><span class="sxs-lookup"><span data-stu-id="6499e-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6499e-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6499e-190">Minimum supported client</span></span><br/> | <span data-ttu-id="6499e-191">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6499e-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6499e-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6499e-192">Minimum supported server</span></span><br/> | <span data-ttu-id="6499e-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6499e-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6499e-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="6499e-194">Namespace</span></span><br/>                | <span data-ttu-id="6499e-195">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6499e-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6499e-196">MOF</span><span class="sxs-lookup"><span data-stu-id="6499e-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6499e-197"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6499e-197"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="6499e-198">DLL</span><span class="sxs-lookup"><span data-stu-id="6499e-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6499e-199"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6499e-199"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

