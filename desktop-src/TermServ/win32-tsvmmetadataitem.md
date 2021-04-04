---
title: Classe Win32_TSVmMetadataItem
description: Representa um item de metadados para uma máquina virtual Área de Trabalho Remota.
ms.assetid: d2678eb0-8634-450c-b73f-611b6f68d556
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSVmMetadataItem Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSVmMetadataItem classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataItem
- Win32_TSVmMetadataItem.Caption
- Win32_TSVmMetadataItem.Description
- Win32_TSVmMetadataItem.InstallDate
- Win32_TSVmMetadataItem.Name
- Win32_TSVmMetadataItem.Status
- Win32_TSVmMetadataItem.VmName
- Win32_TSVmMetadataItem.SectionId
- Win32_TSVmMetadataItem.Value
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872cec5bf3ff0e7b45ab07cb41b6227bcfb8636d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918046"
---
# <a name="win32_tsvmmetadataitem-class"></a><span data-ttu-id="708d1-105">\_Classe Win32 TSVmMetadataItem</span><span class="sxs-lookup"><span data-stu-id="708d1-105">Win32\_TSVmMetadataItem class</span></span>

<span data-ttu-id="708d1-106">Representa um item de metadados para uma máquina virtual Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="708d1-106">Represents a metadata item for a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="708d1-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="708d1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="708d1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="708d1-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  sint32   SectionId;
  string   Value;
};
```

## <a name="members"></a><span data-ttu-id="708d1-109">Membros</span><span class="sxs-lookup"><span data-stu-id="708d1-109">Members</span></span>

<span data-ttu-id="708d1-110">A classe **Win32 \_ TSVmMetadataItem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="708d1-110">The **Win32\_TSVmMetadataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="708d1-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="708d1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="708d1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="708d1-112">Properties</span></span>

<span data-ttu-id="708d1-113">A classe **Win32 \_ TSVmMetadataItem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="708d1-113">The **Win32\_TSVmMetadataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="708d1-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="708d1-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="708d1-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="708d1-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="708d1-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="708d1-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="708d1-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="708d1-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="708d1-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="708d1-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="708d1-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="708d1-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="708d1-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="708d1-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="708d1-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="708d1-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="708d1-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="708d1-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="708d1-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="708d1-123">Description of the object.</span></span>

<span data-ttu-id="708d1-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="708d1-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="708d1-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="708d1-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="708d1-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="708d1-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="708d1-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="708d1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="708d1-128">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="708d1-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="708d1-129">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="708d1-129">The date the object was installed.</span></span> <span data-ttu-id="708d1-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="708d1-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="708d1-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="708d1-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="708d1-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="708d1-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="708d1-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="708d1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="708d1-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="708d1-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="708d1-135">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="708d1-135">The name of the object.</span></span>

<span data-ttu-id="708d1-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="708d1-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="708d1-137">**Seção de seções**</span><span class="sxs-lookup"><span data-stu-id="708d1-137">**SectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="708d1-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="708d1-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="708d1-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="708d1-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="708d1-140">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="708d1-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="708d1-141">Especifica a seção dentro dos metadados onde esse item reside.</span><span class="sxs-lookup"><span data-stu-id="708d1-141">Specifies the section within the metadata where this item resides.</span></span>

<dt>

<span data-ttu-id="708d1-142">0</span><span class="sxs-lookup"><span data-stu-id="708d1-142">0</span></span>
</dt> <dd>

<span data-ttu-id="708d1-143">Seção de configuração.</span><span class="sxs-lookup"><span data-stu-id="708d1-143">Configuration section.</span></span>

</dd> <dt>

<span data-ttu-id="708d1-144">1</span><span class="sxs-lookup"><span data-stu-id="708d1-144">1</span></span>
</dt> <dd>

<span data-ttu-id="708d1-145">Seção de configurações de esclarecimento.</span><span class="sxs-lookup"><span data-stu-id="708d1-145">Enlightenment settings section.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="708d1-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="708d1-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="708d1-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="708d1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="708d1-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="708d1-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="708d1-149">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="708d1-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="708d1-150">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="708d1-150">Current status of the object.</span></span> <span data-ttu-id="708d1-151">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="708d1-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="708d1-152">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="708d1-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="708d1-153">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="708d1-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="708d1-154">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="708d1-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="708d1-155">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="708d1-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="708d1-156">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="708d1-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="708d1-157">("OK")</span><span class="sxs-lookup"><span data-stu-id="708d1-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="708d1-158">("Erro")</span><span class="sxs-lookup"><span data-stu-id="708d1-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="708d1-159">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="708d1-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="708d1-160">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="708d1-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="708d1-161">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="708d1-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="708d1-162">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="708d1-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="708d1-163">("Parando")</span><span class="sxs-lookup"><span data-stu-id="708d1-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="708d1-164">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="708d1-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="708d1-165">**Valor**</span><span class="sxs-lookup"><span data-stu-id="708d1-165">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="708d1-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="708d1-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="708d1-167">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="708d1-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="708d1-168">O valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="708d1-168">The value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="708d1-169">**VmName**</span><span class="sxs-lookup"><span data-stu-id="708d1-169">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="708d1-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="708d1-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="708d1-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="708d1-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="708d1-172">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="708d1-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="708d1-173">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="708d1-173">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="708d1-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="708d1-174">Requirements</span></span>



| <span data-ttu-id="708d1-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="708d1-175">Requirement</span></span> | <span data-ttu-id="708d1-176">Valor</span><span class="sxs-lookup"><span data-stu-id="708d1-176">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="708d1-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="708d1-177">Minimum supported client</span></span><br/> | <span data-ttu-id="708d1-178">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="708d1-178">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="708d1-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="708d1-179">Minimum supported server</span></span><br/> | <span data-ttu-id="708d1-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="708d1-180">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="708d1-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="708d1-181">Namespace</span></span><br/>                | <span data-ttu-id="708d1-182">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="708d1-182">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="708d1-183">MOF</span><span class="sxs-lookup"><span data-stu-id="708d1-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="708d1-184"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="708d1-184"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="708d1-185">DLL</span><span class="sxs-lookup"><span data-stu-id="708d1-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="708d1-186"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="708d1-186"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

