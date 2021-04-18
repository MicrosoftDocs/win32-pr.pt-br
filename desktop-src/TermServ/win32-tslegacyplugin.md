---
title: Classe Win32_TSLegacyPlugin
description: Representa um servidor Área de Trabalho Remota que os plug-ins de Serviço Gerenciamento de Conexão de RemoteApp e Área de Trabalho internos consultarão os programas do RemoteApp.
ms.assetid: 99bec477-ae9d-4bc9-bf9d-11a4e439306b
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLegacyPlugin Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLegacyPlugin classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLegacyPlugin
- Win32_TSLegacyPlugin.Caption
- Win32_TSLegacyPlugin.Description
- Win32_TSLegacyPlugin.InstallDate
- Win32_TSLegacyPlugin.Name
- Win32_TSLegacyPlugin.Status
- Win32_TSLegacyPlugin.Type
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 548eadac272f6f87daf1c43020cb65485e434aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810424"
---
# <a name="win32_tslegacyplugin-class"></a><span data-ttu-id="de12c-105">\_Classe Win32 TSLegacyPlugin</span><span class="sxs-lookup"><span data-stu-id="de12c-105">Win32\_TSLegacyPlugin class</span></span>

<span data-ttu-id="de12c-106">Representa um servidor Área de Trabalho Remota que os plug-ins de Serviço Gerenciamento de Conexão de RemoteApp e Área de Trabalho internos consultarão os programas do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="de12c-106">Represents a Remote Desktop server that the built-in RemoteApp and Desktop Connection Management Service plug-ins will query for RemoteApp programs.</span></span>

<span data-ttu-id="de12c-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="de12c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

<span data-ttu-id="de12c-108">Essa classe foi preterida a partir do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="de12c-108">This class is deprecated beginning with Windows Server 2012.</span></span>

## <a name="syntax"></a><span data-ttu-id="de12c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de12c-109">Syntax</span></span>

``` syntax
[DEPRECATED, dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSLegacyPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="de12c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="de12c-110">Members</span></span>

<span data-ttu-id="de12c-111">A classe **Win32 \_ TSLegacyPlugin** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="de12c-111">The **Win32\_TSLegacyPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="de12c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de12c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de12c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de12c-113">Properties</span></span>

<span data-ttu-id="de12c-114">A classe **Win32 \_ TSLegacyPlugin** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="de12c-114">The **Win32\_TSLegacyPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de12c-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="de12c-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de12c-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de12c-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de12c-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de12c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de12c-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="de12c-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="de12c-119">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="de12c-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="de12c-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de12c-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de12c-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="de12c-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de12c-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de12c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de12c-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de12c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de12c-124">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="de12c-124">Description of the object.</span></span>

<span data-ttu-id="de12c-125">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de12c-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de12c-126">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="de12c-126">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de12c-127">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="de12c-127">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="de12c-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de12c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de12c-129">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="de12c-129">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="de12c-130">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="de12c-130">The date the object was installed.</span></span> <span data-ttu-id="de12c-131">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="de12c-131">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="de12c-132">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de12c-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de12c-133">**Nome**</span><span class="sxs-lookup"><span data-stu-id="de12c-133">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de12c-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de12c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de12c-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de12c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de12c-136">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="de12c-136">The name of the object.</span></span>

<span data-ttu-id="de12c-137">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de12c-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de12c-138">**Status**</span><span class="sxs-lookup"><span data-stu-id="de12c-138">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de12c-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de12c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de12c-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de12c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de12c-141">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="de12c-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="de12c-142">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="de12c-142">Current status of the object.</span></span> <span data-ttu-id="de12c-143">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="de12c-143">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="de12c-144">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="de12c-144">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="de12c-145">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="de12c-145">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="de12c-146">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="de12c-146">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="de12c-147">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="de12c-147">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="de12c-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de12c-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="de12c-149">("OK")</span><span class="sxs-lookup"><span data-stu-id="de12c-149">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de12c-150">("Erro")</span><span class="sxs-lookup"><span data-stu-id="de12c-150">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de12c-151">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="de12c-151">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de12c-152">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="de12c-152">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de12c-153">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="de12c-153">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de12c-154">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="de12c-154">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de12c-155">("Parando")</span><span class="sxs-lookup"><span data-stu-id="de12c-155">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de12c-156">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="de12c-156">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="de12c-157">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="de12c-157">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de12c-158">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de12c-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de12c-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="de12c-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="de12c-160">O tipo do servidor de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="de12c-160">The type of the Remote Desktop Services server.</span></span>

<dt>

<span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>

<span data-ttu-id="de12c-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="de12c-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server(0)** (0)</span></span>


</dt> <dd>

<span data-ttu-id="de12c-162">Área de Trabalho Remota Server.</span><span class="sxs-lookup"><span data-stu-id="de12c-162">Remote Desktop server.</span></span>

</dd> <dt>

<span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>

<span data-ttu-id="de12c-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Terminal Server fictício para o farm de VMs (1)** (1)</span><span class="sxs-lookup"><span data-stu-id="de12c-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Dummy Terminal Server for VM Farm(1)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="de12c-164">Servidor Área de Trabalho Remota artificial para um farm de VMs.</span><span class="sxs-lookup"><span data-stu-id="de12c-164">Artificial Remote Desktop server for a VM farm.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de12c-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de12c-165">Requirements</span></span>



| <span data-ttu-id="de12c-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="de12c-166">Requirement</span></span> | <span data-ttu-id="de12c-167">Valor</span><span class="sxs-lookup"><span data-stu-id="de12c-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de12c-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de12c-168">Minimum supported client</span></span><br/> | <span data-ttu-id="de12c-169">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="de12c-169">None supported</span></span><br/>                                                                |
| <span data-ttu-id="de12c-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de12c-170">Minimum supported server</span></span><br/> | <span data-ttu-id="de12c-171">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de12c-171">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="de12c-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="de12c-172">Namespace</span></span><br/>                | <span data-ttu-id="de12c-173">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="de12c-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="de12c-174">MOF</span><span class="sxs-lookup"><span data-stu-id="de12c-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de12c-175"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de12c-175"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="de12c-176">DLL</span><span class="sxs-lookup"><span data-stu-id="de12c-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de12c-177"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de12c-177"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

