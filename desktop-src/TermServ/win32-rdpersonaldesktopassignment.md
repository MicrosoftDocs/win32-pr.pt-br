---
title: Classe Win32_RDPersonalDesktopAssignment
description: A lista de atribuições de área de trabalho pessoal.
ms.assetid: 3abf773d-8dc3-44ae-8887-1a1f38e29fbb
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDPersonalDesktopAssignment Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDPersonalDesktopAssignment classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDPersonalDesktopAssignment
- Win32_RDPersonalDesktopAssignment.Caption
- Win32_RDPersonalDesktopAssignment.Description
- Win32_RDPersonalDesktopAssignment.InstallDate
- Win32_RDPersonalDesktopAssignment.Name
- Win32_RDPersonalDesktopAssignment.Status
- Win32_RDPersonalDesktopAssignment.UserName
- Win32_RDPersonalDesktopAssignment.DomainName
- Win32_RDPersonalDesktopAssignment.FarmAlias
- Win32_RDPersonalDesktopAssignment.VMName
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088e7be5da0a62a0f5b7ed72f8a439661cc41c80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784058"
---
# <a name="win32_rdpersonaldesktopassignment-class"></a><span data-ttu-id="81e97-105">\_Classe Win32 RDPersonalDesktopAssignment</span><span class="sxs-lookup"><span data-stu-id="81e97-105">Win32\_RDPersonalDesktopAssignment class</span></span>

<span data-ttu-id="81e97-106">A lista de atribuições de área de trabalho pessoal.</span><span class="sxs-lookup"><span data-stu-id="81e97-106">The list of personal desktop assignments.</span></span>

<span data-ttu-id="81e97-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="81e97-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e97-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81e97-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDPersonalDesktopAssignment : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   UserName;
  string   DomainName;
  string   FarmAlias;
  string   VMName;
};
```

## <a name="members"></a><span data-ttu-id="81e97-109">Membros</span><span class="sxs-lookup"><span data-stu-id="81e97-109">Members</span></span>

<span data-ttu-id="81e97-110">A classe **Win32 \_ RDPersonalDesktopAssignment** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="81e97-110">The **Win32\_RDPersonalDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="81e97-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81e97-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81e97-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81e97-112">Properties</span></span>

<span data-ttu-id="81e97-113">A classe **Win32 \_ RDPersonalDesktopAssignment** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="81e97-113">The **Win32\_RDPersonalDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81e97-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="81e97-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81e97-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81e97-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81e97-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81e97-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81e97-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="81e97-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="81e97-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="81e97-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="81e97-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81e97-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81e97-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="81e97-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81e97-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81e97-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81e97-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81e97-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81e97-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="81e97-123">Description of the object.</span></span>

<span data-ttu-id="81e97-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81e97-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81e97-125">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="81e97-125">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81e97-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81e97-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81e97-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81e97-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="81e97-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="81e97-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="81e97-129">Nome de domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="81e97-129">Domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="81e97-130">**FarmAlias**</span><span class="sxs-lookup"><span data-stu-id="81e97-130">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81e97-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81e97-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81e97-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81e97-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="81e97-133">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="81e97-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="81e97-134">Farm no qual a área de trabalho pessoal foi atribuída.</span><span class="sxs-lookup"><span data-stu-id="81e97-134">Farm in which personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="81e97-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="81e97-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81e97-136">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="81e97-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81e97-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81e97-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81e97-138">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="81e97-138">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="81e97-139">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="81e97-139">The date the object was installed.</span></span> <span data-ttu-id="81e97-140">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="81e97-140">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="81e97-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81e97-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81e97-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="81e97-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81e97-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81e97-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81e97-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81e97-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81e97-145">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="81e97-145">The name of the object.</span></span>

<span data-ttu-id="81e97-146">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81e97-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81e97-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="81e97-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81e97-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81e97-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81e97-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81e97-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81e97-150">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="81e97-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="81e97-151">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="81e97-151">Current status of the object.</span></span> <span data-ttu-id="81e97-152">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="81e97-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="81e97-153">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="81e97-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="81e97-154">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="81e97-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="81e97-155">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="81e97-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="81e97-156">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="81e97-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="81e97-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81e97-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="81e97-158">("OK")</span><span class="sxs-lookup"><span data-stu-id="81e97-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="81e97-159">("Erro")</span><span class="sxs-lookup"><span data-stu-id="81e97-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="81e97-160">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="81e97-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="81e97-161">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="81e97-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="81e97-162">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="81e97-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="81e97-163">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="81e97-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="81e97-164">("Parando")</span><span class="sxs-lookup"><span data-stu-id="81e97-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="81e97-165">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="81e97-165">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81e97-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="81e97-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81e97-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81e97-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81e97-168">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81e97-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="81e97-169">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="81e97-169">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="81e97-170">Nome de usuário ao qual a área de trabalho pessoal foi atribuída.</span><span class="sxs-lookup"><span data-stu-id="81e97-170">User name to whom personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="81e97-171">**VMName**</span><span class="sxs-lookup"><span data-stu-id="81e97-171">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81e97-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81e97-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81e97-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81e97-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="81e97-174">Nome da VM atribuído.</span><span class="sxs-lookup"><span data-stu-id="81e97-174">Assigned VM name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81e97-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81e97-175">Requirements</span></span>



| <span data-ttu-id="81e97-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="81e97-176">Requirement</span></span> | <span data-ttu-id="81e97-177">Valor</span><span class="sxs-lookup"><span data-stu-id="81e97-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e97-178">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81e97-178">Minimum supported client</span></span><br/> | <span data-ttu-id="81e97-179">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="81e97-179">None supported</span></span><br/>                                                                |
| <span data-ttu-id="81e97-180">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81e97-180">Minimum supported server</span></span><br/> | <span data-ttu-id="81e97-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81e97-181">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="81e97-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="81e97-182">Namespace</span></span><br/>                | <span data-ttu-id="81e97-183">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="81e97-183">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="81e97-184">MOF</span><span class="sxs-lookup"><span data-stu-id="81e97-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81e97-185"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81e97-185"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="81e97-186">DLL</span><span class="sxs-lookup"><span data-stu-id="81e97-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81e97-187"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81e97-187"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

