---
title: Classe Win32_TSVm
description: Representa um Área de Trabalho Remota máquina virtual.
ms.assetid: 9e076963-1c02-4419-b4d5-9863a2bbb23b
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSVm Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSVm classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSVm
- Win32_TSVm.Caption
- Win32_TSVm.Description
- Win32_TSVm.InstallDate
- Win32_TSVm.Name
- Win32_TSVm.Status
- Win32_TSVm.VmName
- Win32_TSVm.EnlightmentSettings
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f419a888adef946d2a7b281919a9a9293eeca5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787570"
---
# <a name="win32_tsvm-class"></a><span data-ttu-id="d35e7-105">\_Classe Win32 TSVm</span><span class="sxs-lookup"><span data-stu-id="d35e7-105">Win32\_TSVm class</span></span>

<span data-ttu-id="d35e7-106">Representa um Área de Trabalho Remota máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d35e7-106">Represents a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="d35e7-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d35e7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d35e7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d35e7-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  string   EnlightmentSettings;
};
```

## <a name="members"></a><span data-ttu-id="d35e7-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d35e7-109">Members</span></span>

<span data-ttu-id="d35e7-110">A classe **Win32 \_ TSVm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d35e7-110">The **Win32\_TSVm** class has these types of members:</span></span>

-   [<span data-ttu-id="d35e7-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d35e7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d35e7-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d35e7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d35e7-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d35e7-113">Methods</span></span>

<span data-ttu-id="d35e7-114">A classe **Win32 \_ TSVm** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d35e7-114">The **Win32\_TSVm** class has these methods.</span></span>



| <span data-ttu-id="d35e7-115">Método</span><span class="sxs-lookup"><span data-stu-id="d35e7-115">Method</span></span>                                                                | <span data-ttu-id="d35e7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d35e7-116">Description</span></span>                                              |
|:----------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="d35e7-117">**DumpVmInfo**</span><span class="sxs-lookup"><span data-stu-id="d35e7-117">**DumpVmInfo**</span></span>](dumpvminfo-win32-tsvm.md)                           | <span data-ttu-id="d35e7-118">Somente para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="d35e7-118">For test purposes only.</span></span><br/>                       |
| [<span data-ttu-id="d35e7-119">**Exportação**</span><span class="sxs-lookup"><span data-stu-id="d35e7-119">**Export**</span></span>](export-win32-tsvm.md)                                   | <span data-ttu-id="d35e7-120">Obter informações de monitoramento da sessão da VM</span><span class="sxs-lookup"><span data-stu-id="d35e7-120">Gets Session Monitoring Information of the VM</span></span><br/> |
| [<span data-ttu-id="d35e7-121">**QueryOfflineInformation**</span><span class="sxs-lookup"><span data-stu-id="d35e7-121">**QueryOfflineInformation**</span></span>](queryofflineinformation-win32-tsvm.md) | <span data-ttu-id="d35e7-122">Consulta propriedades somente quando está offline.</span><span class="sxs-lookup"><span data-stu-id="d35e7-122">Queries properties only when it is offline.</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="d35e7-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d35e7-123">Properties</span></span>

<span data-ttu-id="d35e7-124">A classe **Win32 \_ TSVm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d35e7-124">The **Win32\_TSVm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d35e7-125">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d35e7-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d35e7-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d35e7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d35e7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-128">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d35e7-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d35e7-129">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="d35e7-129">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d35e7-130">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d35e7-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d35e7-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d35e7-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d35e7-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d35e7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d35e7-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d35e7-134">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d35e7-134">Description of the object.</span></span>

<span data-ttu-id="d35e7-135">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d35e7-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d35e7-136">**EnlightmentSettings**</span><span class="sxs-lookup"><span data-stu-id="d35e7-136">**EnlightmentSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d35e7-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d35e7-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d35e7-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-139">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d35e7-139">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d35e7-140">Um BLOB XML que contém as configurações de esclarecimento para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d35e7-140">An XML BLOB that contains the enlightenment settings for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d35e7-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d35e7-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d35e7-142">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d35e7-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d35e7-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-144">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="d35e7-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d35e7-145">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d35e7-145">The date the object was installed.</span></span> <span data-ttu-id="d35e7-146">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="d35e7-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d35e7-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d35e7-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d35e7-148">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d35e7-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d35e7-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d35e7-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d35e7-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d35e7-151">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="d35e7-151">The name of the object.</span></span>

<span data-ttu-id="d35e7-152">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d35e7-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d35e7-153">**Status**</span><span class="sxs-lookup"><span data-stu-id="d35e7-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d35e7-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d35e7-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d35e7-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-156">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="d35e7-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d35e7-157">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d35e7-157">Current status of the object.</span></span> <span data-ttu-id="d35e7-158">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="d35e7-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d35e7-159">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d35e7-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d35e7-160">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="d35e7-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d35e7-161">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="d35e7-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d35e7-162">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="d35e7-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d35e7-163">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d35e7-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d35e7-164">("OK")</span><span class="sxs-lookup"><span data-stu-id="d35e7-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d35e7-165">("Erro")</span><span class="sxs-lookup"><span data-stu-id="d35e7-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d35e7-166">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="d35e7-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d35e7-167">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="d35e7-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d35e7-168">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d35e7-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d35e7-169">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="d35e7-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d35e7-170">("Parando")</span><span class="sxs-lookup"><span data-stu-id="d35e7-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d35e7-171">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="d35e7-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d35e7-172">**VmName**</span><span class="sxs-lookup"><span data-stu-id="d35e7-172">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d35e7-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d35e7-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d35e7-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d35e7-175">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d35e7-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d35e7-176">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d35e7-176">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d35e7-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d35e7-177">Requirements</span></span>



| <span data-ttu-id="d35e7-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="d35e7-178">Requirement</span></span> | <span data-ttu-id="d35e7-179">Valor</span><span class="sxs-lookup"><span data-stu-id="d35e7-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d35e7-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d35e7-180">Minimum supported client</span></span><br/> | <span data-ttu-id="d35e7-181">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d35e7-181">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="d35e7-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d35e7-182">Minimum supported server</span></span><br/> | <span data-ttu-id="d35e7-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d35e7-183">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="d35e7-184">Namespace</span><span class="sxs-lookup"><span data-stu-id="d35e7-184">Namespace</span></span><br/>                | <span data-ttu-id="d35e7-185">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="d35e7-185">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="d35e7-186">MOF</span><span class="sxs-lookup"><span data-stu-id="d35e7-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d35e7-187"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d35e7-187"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="d35e7-188">DLL</span><span class="sxs-lookup"><span data-stu-id="d35e7-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d35e7-189"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d35e7-189"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

