---
title: Classe Win32_Workspace
description: Especifica Serviços de Área de Trabalho Remota informações de configuração do espaço de trabalho.
ms.assetid: 27192dca-cbb4-4620-ae52-c27aba4b4dff
ms.tgt_platform: multiple
keywords:
- Classe de Win32_Workspace Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_Workspace classe, descrita
topic_type:
- apiref
api_name:
- Win32_Workspace
- Win32_Workspace.Caption
- Win32_Workspace.Description
- Win32_Workspace.InstallDate
- Win32_Workspace.Name
- Win32_Workspace.Status
- Win32_Workspace.IsDefaultName
- Win32_Workspace.ID
- Win32_Workspace.Redirector
- Win32_Workspace.RedirectorAlternateAddress
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1153a4eb8a260e539845a9458a5c8cee4581d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757183"
---
# <a name="win32_workspace-class"></a><span data-ttu-id="c2011-105">\_Classe de espaço de trabalho Win32</span><span class="sxs-lookup"><span data-stu-id="c2011-105">Win32\_Workspace class</span></span>

<span data-ttu-id="c2011-106">Especifica Serviços de Área de Trabalho Remota informações de configuração do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2011-106">Specifies Remote Desktop Services workspace configuration information.</span></span>

<span data-ttu-id="c2011-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c2011-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2011-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2011-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov"), singleton]
class Win32_Workspace : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  IsDefaultName;
  string   ID;
  string   Redirector;
  string   RedirectorAlternateAddress;
};
```

## <a name="members"></a><span data-ttu-id="c2011-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c2011-109">Members</span></span>

<span data-ttu-id="c2011-110">A classe de **\_ espaço de trabalho do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c2011-110">The **Win32\_Workspace** class has these types of members:</span></span>

-   [<span data-ttu-id="c2011-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c2011-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2011-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c2011-112">Properties</span></span>

<span data-ttu-id="c2011-113">A classe de **\_ espaço de trabalho do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c2011-113">The **Win32\_Workspace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2011-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c2011-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2011-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2011-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2011-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2011-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2011-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c2011-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c2011-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="c2011-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c2011-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2011-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2011-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c2011-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2011-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2011-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2011-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2011-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2011-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c2011-123">Description of the object.</span></span>

<span data-ttu-id="c2011-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2011-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2011-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="c2011-125">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2011-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2011-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2011-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c2011-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c2011-128">O identificador do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2011-128">The identifier of the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="c2011-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c2011-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2011-130">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c2011-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c2011-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2011-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2011-132">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="c2011-132">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c2011-133">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c2011-133">The date the object was installed.</span></span> <span data-ttu-id="c2011-134">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="c2011-134">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c2011-135">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2011-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2011-136">**Isdefaultname**</span><span class="sxs-lookup"><span data-stu-id="c2011-136">**IsDefaultName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2011-137">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2011-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2011-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2011-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2011-139">Especifica se o nome do espaço de trabalho é o nome padrão.</span><span class="sxs-lookup"><span data-stu-id="c2011-139">Specifies if the workspace name is the default name.</span></span> <span data-ttu-id="c2011-140">Contém zero se o nome for um nome padrão ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c2011-140">Contains nonzero if the name is a default name or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="c2011-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c2011-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2011-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2011-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2011-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2011-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2011-144">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="c2011-144">The name of the object.</span></span>

<span data-ttu-id="c2011-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2011-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2011-146">**Redirecionador**</span><span class="sxs-lookup"><span data-stu-id="c2011-146">**Redirector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2011-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2011-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2011-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c2011-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c2011-149">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c2011-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c2011-150">O nome do computador do redirecionador para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2011-150">The machine name of the redirector for the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="c2011-151">**RedirectorAlternateAddress**</span><span class="sxs-lookup"><span data-stu-id="c2011-151">**RedirectorAlternateAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2011-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2011-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2011-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c2011-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c2011-154">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c2011-154">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c2011-155">O endereço alternativo para o redirecionador.</span><span class="sxs-lookup"><span data-stu-id="c2011-155">The alternate address for the redirector.</span></span>

</dd> <dt>

<span data-ttu-id="c2011-156">**Status**</span><span class="sxs-lookup"><span data-stu-id="c2011-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2011-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2011-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2011-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2011-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2011-159">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c2011-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c2011-160">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c2011-160">Current status of the object.</span></span> <span data-ttu-id="c2011-161">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c2011-161">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c2011-162">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="c2011-162">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c2011-163">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="c2011-163">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c2011-164">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="c2011-164">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c2011-165">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="c2011-165">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c2011-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2011-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c2011-167">("OK")</span><span class="sxs-lookup"><span data-stu-id="c2011-167">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2011-168">("Erro")</span><span class="sxs-lookup"><span data-stu-id="c2011-168">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2011-169">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="c2011-169">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2011-170">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c2011-170">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2011-171">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c2011-171">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2011-172">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c2011-172">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2011-173">("Parando")</span><span class="sxs-lookup"><span data-stu-id="c2011-173">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c2011-174">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="c2011-174">("Service")</span></span>


<span data-ttu-id="c2011-175"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c2011-175"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c2011-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2011-176">Requirements</span></span>



| <span data-ttu-id="c2011-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2011-177">Requirement</span></span> | <span data-ttu-id="c2011-178">Valor</span><span class="sxs-lookup"><span data-stu-id="c2011-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2011-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2011-179">Minimum supported client</span></span><br/> | <span data-ttu-id="c2011-180">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c2011-180">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c2011-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2011-181">Minimum supported server</span></span><br/> | <span data-ttu-id="c2011-182">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2011-182">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c2011-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2011-183">Namespace</span></span><br/>                | <span data-ttu-id="c2011-184">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="c2011-184">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c2011-185">MOF</span><span class="sxs-lookup"><span data-stu-id="c2011-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2011-186"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2011-186"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="c2011-187">DLL</span><span class="sxs-lookup"><span data-stu-id="c2011-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2011-188"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2011-188"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

