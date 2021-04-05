---
description: A \_ classe CIM ModifySettingAction representa as informações para modificar um arquivo de configuração específico, para uma entrada específica, com um valor específico.
ms.assetid: 6d22bc11-f798-4634-8688-797d4a4a4bee
ms.tgt_platform: multiple
title: Classe CIM_ModifySettingAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ModifySettingAction
- CIM_ModifySettingAction.ActionID
- CIM_ModifySettingAction.Caption
- CIM_ModifySettingAction.Description
- CIM_ModifySettingAction.Direction
- CIM_ModifySettingAction.Name
- CIM_ModifySettingAction.SoftwareElementID
- CIM_ModifySettingAction.SoftwareElementState
- CIM_ModifySettingAction.TargetOperatingSystem
- CIM_ModifySettingAction.Version
- CIM_ModifySettingAction.ActionType
- CIM_ModifySettingAction.EntryName
- CIM_ModifySettingAction.EntryValue
- CIM_ModifySettingAction.FileName
- CIM_ModifySettingAction.SectionKey
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 450e73eaa6f405e47d79cbf3840932e0f106a4b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646447"
---
# <a name="cim_modifysettingaction-class"></a><span data-ttu-id="3a98b-103">\_Classe CIM ModifySettingAction</span><span class="sxs-lookup"><span data-stu-id="3a98b-103">CIM\_ModifySettingAction class</span></span>

<span data-ttu-id="3a98b-104">A classe **CIM \_ ModifySettingAction** representa as informações para modificar um arquivo de configuração específico, para uma entrada específica, com um valor específico.</span><span class="sxs-lookup"><span data-stu-id="3a98b-104">The **CIM\_ModifySettingAction** class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a98b-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3a98b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3a98b-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3a98b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3a98b-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3a98b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3a98b-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="3a98b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a98b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a98b-109">Syntax</span></span>

``` syntax
[UUID("{ECDE0B90-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ModifySettingAction : CIM_Action
{
  string ActionID;
  string Caption;
  string Description;
  uint16 Direction;
  string Name;
  string SoftwareElementID;
  uint16 SoftwareElementState;
  uint16 TargetOperatingSystem;
  string Version;
  uint16 ActionType;
  string EntryName;
  string EntryValue;
  string FileName;
  string SectionKey;
};
```

## <a name="members"></a><span data-ttu-id="3a98b-110">Membros</span><span class="sxs-lookup"><span data-stu-id="3a98b-110">Members</span></span>

<span data-ttu-id="3a98b-111">A classe **CIM \_ ModifySettingAction** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3a98b-111">The **CIM\_ModifySettingAction** class has these types of members:</span></span>

-   [<span data-ttu-id="3a98b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a98b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3a98b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3a98b-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3a98b-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a98b-114">Methods</span></span>

<span data-ttu-id="3a98b-115">A classe **CIM \_ ModifySettingAction** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3a98b-115">The **CIM\_ModifySettingAction** class has these methods.</span></span>



| <span data-ttu-id="3a98b-116">Método</span><span class="sxs-lookup"><span data-stu-id="3a98b-116">Method</span></span>                                                           | <span data-ttu-id="3a98b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a98b-117">Description</span></span>                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="3a98b-118">**Chame**</span><span class="sxs-lookup"><span data-stu-id="3a98b-118">**Invoke**</span></span>](invoke-method-in-class-cim-modifysettingaction.md) | <span data-ttu-id="3a98b-119">Executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="3a98b-119">Takes a specific action.</span></span> <span data-ttu-id="3a98b-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="3a98b-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3a98b-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3a98b-121">Properties</span></span>

<span data-ttu-id="3a98b-122">A classe **CIM \_ ModifySettingAction** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3a98b-122">The **CIM\_ModifySettingAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a98b-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="3a98b-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a98b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-126">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3a98b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-127">Identificador exclusivo atribuído a uma ação específica para um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="3a98b-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="3a98b-128">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="3a98b-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a98b-129">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="3a98b-129">**ActionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a98b-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-132">Tipo de ação a ser executada na entrada de configuração especificada.</span><span class="sxs-lookup"><span data-stu-id="3a98b-132">Type of action to perform on the specified setting entry.</span></span> <span data-ttu-id="3a98b-133">As adições são consideradas diferenciadas entre maiúsculas e minúsculas; no entanto, supõe-se que as remoções não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a98b-133">Additions are assumed to be case sensitive; however, removals are assumed to be case insensitive.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="3a98b-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Criar** (0)</span><span class="sxs-lookup"><span data-stu-id="3a98b-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Create** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-135">Cria a entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="3a98b-135">Creates the specified entry.</span></span>

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="3a98b-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Excluir** (1)</span><span class="sxs-lookup"><span data-stu-id="3a98b-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-137">Exclui a entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="3a98b-137">Deletes the specified entry.</span></span>

</dd> <dt>

<span id="Append"></span><span id="append"></span><span id="APPEND"></span>

<span data-ttu-id="3a98b-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Acrescentar** (2)</span><span class="sxs-lookup"><span data-stu-id="3a98b-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Append** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-139">Anexa ao final da entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="3a98b-139">Appends to the end of the specified entry.</span></span>

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>

<span data-ttu-id="3a98b-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Remover** (3)</span><span class="sxs-lookup"><span data-stu-id="3a98b-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Remove** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-141">Remove o valor da entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="3a98b-141">Removes the value from the specified entry.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a98b-142">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="3a98b-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a98b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-145">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3a98b-145">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-146">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3a98b-146">Short textual description of the object.</span></span>

<span data-ttu-id="3a98b-147">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="3a98b-147">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a98b-148">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3a98b-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a98b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-151">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="3a98b-151">Description of the object.</span></span>

<span data-ttu-id="3a98b-152">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="3a98b-152">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a98b-153">**Direção**</span><span class="sxs-lookup"><span data-stu-id="3a98b-153">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-154">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a98b-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-156">Indica se um objeto [**de \_ ação CIM**](cim-action.md) específico faz parte de uma sequência de ações para fazer a transição do elemento de software atual para seu próximo estado, como "instalar" ou para remover o elemento de software atual, como "Desinstalar".</span><span class="sxs-lookup"><span data-stu-id="3a98b-156">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="3a98b-157">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="3a98b-157">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="3a98b-158">**Instalar** (0)</span><span class="sxs-lookup"><span data-stu-id="3a98b-158">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="3a98b-159">**Desinstalar** (1)</span><span class="sxs-lookup"><span data-stu-id="3a98b-159">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a98b-160">**Entryname**</span><span class="sxs-lookup"><span data-stu-id="3a98b-160">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a98b-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-163">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3a98b-163">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-164">Nome da entrada a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="3a98b-164">Name of the entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="3a98b-165">**Entryvalue**</span><span class="sxs-lookup"><span data-stu-id="3a98b-165">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a98b-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-168">Valor a adicionar, acrescentar ou substituir a configuração especificada.</span><span class="sxs-lookup"><span data-stu-id="3a98b-168">Value to add, append, or to replace the specified setting.</span></span>

</dd> <dt>

<span data-ttu-id="3a98b-169">**FileName**</span><span class="sxs-lookup"><span data-stu-id="3a98b-169">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a98b-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-172">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="3a98b-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-173">Nome do arquivo da entrada do arquivo de configuração a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="3a98b-173">File name of the setting file entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="3a98b-174">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3a98b-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a98b-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-177">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3a98b-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-178">Identifica o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="3a98b-178">Identifies the software element.</span></span>

<span data-ttu-id="3a98b-179">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="3a98b-179">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a98b-180">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="3a98b-180">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a98b-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-183">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3a98b-183">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-184">Chave da seção da entrada de configuração a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="3a98b-184">Section key of the setting entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="3a98b-185">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="3a98b-185">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a98b-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-188">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3a98b-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-189">Identificador para o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="3a98b-189">Identifier for the software element.</span></span>

<span data-ttu-id="3a98b-190">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="3a98b-190">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a98b-191">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="3a98b-191">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-192">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a98b-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-194">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a98b-194">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-195">Estado de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="3a98b-195">State of a software element.</span></span>

<span data-ttu-id="3a98b-196">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="3a98b-196">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="3a98b-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="3a98b-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-198">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="3a98b-198">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="3a98b-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="3a98b-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-200">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="3a98b-200">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="3a98b-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="3a98b-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-202">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="3a98b-202">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="3a98b-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="3a98b-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-204">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="3a98b-204">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a98b-205">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="3a98b-205">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-206">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a98b-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-208">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="3a98b-208">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-209">Sistema operacional de destino do elemento de software proprietário.</span><span class="sxs-lookup"><span data-stu-id="3a98b-209">Target operating system of the owning software element.</span></span>

<span data-ttu-id="3a98b-210">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="3a98b-210">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a98b-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a98b-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a98b-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3a98b-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="3a98b-213"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="3a98b-213"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-214">Mac OS</span><span class="sxs-lookup"><span data-stu-id="3a98b-214">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="3a98b-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="3a98b-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="3a98b-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="3a98b-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="3a98b-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="3a98b-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="3a98b-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="3a98b-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="3a98b-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="3a98b-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-220">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="3a98b-220">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="3a98b-221"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="3a98b-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-222">HP-UX</span><span class="sxs-lookup"><span data-stu-id="3a98b-222">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="3a98b-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="3a98b-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="3a98b-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="3a98b-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="3a98b-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="3a98b-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="3a98b-226"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="3a98b-226"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="3a98b-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="3a98b-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-228">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="3a98b-228">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="3a98b-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="3a98b-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="3a98b-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="3a98b-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-231">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="3a98b-231">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="3a98b-232"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="3a98b-232"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-233">Windows 95</span><span class="sxs-lookup"><span data-stu-id="3a98b-233">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="3a98b-234"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="3a98b-234"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-235">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3a98b-235">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="3a98b-236"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="3a98b-236"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-237">Windows NT</span><span class="sxs-lookup"><span data-stu-id="3a98b-237">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="3a98b-238"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="3a98b-238"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-239">Windows CE</span><span class="sxs-lookup"><span data-stu-id="3a98b-239">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="3a98b-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="3a98b-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-241">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="3a98b-241">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="3a98b-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="3a98b-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="3a98b-243"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="3a98b-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="3a98b-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="3a98b-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="3a98b-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="3a98b-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="3a98b-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="3a98b-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="3a98b-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="3a98b-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="3a98b-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="3a98b-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="3a98b-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="3a98b-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="3a98b-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="3a98b-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="3a98b-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="3a98b-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="3a98b-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="3a98b-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="3a98b-253"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="3a98b-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-254">Uma série</span><span class="sxs-lookup"><span data-stu-id="3a98b-254">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="3a98b-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="3a98b-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-256">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="3a98b-256">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="3a98b-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="3a98b-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-258">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="3a98b-258">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="3a98b-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="3a98b-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-260">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="3a98b-260">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="3a98b-261"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="3a98b-261"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="3a98b-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="3a98b-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="3a98b-263"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="3a98b-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="3a98b-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="3a98b-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="3a98b-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="3a98b-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="3a98b-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="3a98b-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-267">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="3a98b-267">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="3a98b-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="3a98b-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="3a98b-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="3a98b-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="3a98b-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="3a98b-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="3a98b-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="3a98b-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-272">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="3a98b-272">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="3a98b-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="3a98b-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="3a98b-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="3a98b-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="3a98b-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="3a98b-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="3a98b-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="3a98b-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="3a98b-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="3a98b-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="3a98b-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="3a98b-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="3a98b-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="3a98b-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="3a98b-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="3a98b-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-281">Ser so</span><span class="sxs-lookup"><span data-stu-id="3a98b-281">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="3a98b-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="3a98b-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="3a98b-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="3a98b-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="3a98b-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="3a98b-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="3a98b-285">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="3a98b-285">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="3a98b-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="3a98b-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="3a98b-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="3a98b-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="3a98b-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="3a98b-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="3a98b-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="3a98b-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="3a98b-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="3a98b-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a98b-291">**Versão**</span><span class="sxs-lookup"><span data-stu-id="3a98b-291">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a98b-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a98b-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a98b-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a98b-294">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="3a98b-294">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="3a98b-295">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="3a98b-295">Version of the operation.</span></span>

<span data-ttu-id="3a98b-296">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="3a98b-296">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="3a98b-297"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="3a98b-297"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="3a98b-298"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="3a98b-298"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="3a98b-299">Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="3a98b-299">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a98b-300">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a98b-300">Remarks</span></span>

<span data-ttu-id="3a98b-301">A classe **CIM \_ ModifySettingAction** é derivada da [**\_ ação CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="3a98b-301">The **CIM\_ModifySettingAction** class is derived from [**CIM\_Action**](cim-action.md).</span></span>

<span data-ttu-id="3a98b-302">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="3a98b-302">WMI does not implement this class.</span></span>

<span data-ttu-id="3a98b-303">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3a98b-303">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3a98b-304">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3a98b-304">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a98b-305">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a98b-305">Requirements</span></span>



| <span data-ttu-id="3a98b-306">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a98b-306">Requirement</span></span> | <span data-ttu-id="3a98b-307">Valor</span><span class="sxs-lookup"><span data-stu-id="3a98b-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a98b-308">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a98b-308">Minimum supported client</span></span><br/> | <span data-ttu-id="3a98b-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a98b-309">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a98b-310">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a98b-310">Minimum supported server</span></span><br/> | <span data-ttu-id="3a98b-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a98b-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a98b-312">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a98b-312">Namespace</span></span><br/>                | <span data-ttu-id="3a98b-313">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3a98b-313">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a98b-314">MOF</span><span class="sxs-lookup"><span data-stu-id="3a98b-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a98b-315"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a98b-315"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a98b-316">DLL</span><span class="sxs-lookup"><span data-stu-id="3a98b-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a98b-317"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a98b-317"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a98b-318">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a98b-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a98b-319">**Ação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3a98b-319">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

