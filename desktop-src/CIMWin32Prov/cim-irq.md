---
description: A classe de IRQ de CIM \_ representa uma IRQ (linha de solicitação de interrupção) de arquitetura da Intel.
ms.assetid: d72d4914-c57b-496d-a9fe-d8f5b522504c
ms.tgt_platform: multiple
title: Classe CIM_IRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_IRQ
- CIM_IRQ.Caption
- CIM_IRQ.Description
- CIM_IRQ.InstallDate
- CIM_IRQ.Name
- CIM_IRQ.Status
- CIM_IRQ.Availability
- CIM_IRQ.CreationClassName
- CIM_IRQ.CSCreationClassName
- CIM_IRQ.CSName
- CIM_IRQ.IRQNumber
- CIM_IRQ.Shareable
- CIM_IRQ.TriggerLevel
- CIM_IRQ.TriggerType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03a336caa02c766160fe6501f91b28f06a872ecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826453"
---
# <a name="cim_irq-class"></a><span data-ttu-id="46c51-103">Classe de IRQ de CIM \_</span><span class="sxs-lookup"><span data-stu-id="46c51-103">CIM\_IRQ class</span></span>

<span data-ttu-id="46c51-104">A classe de **\_ IRQ de CIM** representa uma IRQ (linha de solicitação de interrupção) de arquitetura da Intel.</span><span class="sxs-lookup"><span data-stu-id="46c51-104">The **CIM\_IRQ** class represents an Intel architecture interrupt request line (IRQ).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46c51-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="46c51-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="46c51-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="46c51-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="46c51-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="46c51-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="46c51-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="46c51-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c51-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46c51-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_IRQ : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint32   IRQNumber;
  boolean  Shareable;
  uint16   TriggerLevel;
  uint16   TriggerType;
};
```

## <a name="members"></a><span data-ttu-id="46c51-110">Membros</span><span class="sxs-lookup"><span data-stu-id="46c51-110">Members</span></span>

<span data-ttu-id="46c51-111">A classe de **\_ IRQ de CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="46c51-111">The **CIM\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="46c51-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="46c51-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46c51-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="46c51-113">Properties</span></span>

<span data-ttu-id="46c51-114">A classe de **\_ IRQ de CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="46c51-114">The **CIM\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46c51-115">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="46c51-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46c51-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-118">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="46c51-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="46c51-119">Disponibilidade do IRQ.</span><span class="sxs-lookup"><span data-stu-id="46c51-119">Availability of the IRQ.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46c51-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="46c51-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46c51-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="46c51-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="46c51-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponível** (3)</span><span class="sxs-lookup"><span data-stu-id="46c51-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="46c51-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**Em uso/não disponível** (4)</span><span class="sxs-lookup"><span data-stu-id="46c51-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="46c51-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**Em uso e disponível/compartilhável** (5)</span><span class="sxs-lookup"><span data-stu-id="46c51-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="46c51-125">Em uso e disponível/compartilhável</span><span class="sxs-lookup"><span data-stu-id="46c51-125">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46c51-126">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="46c51-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46c51-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-129">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="46c51-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="46c51-130">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="46c51-130">A short textual description of the object.</span></span>

<span data-ttu-id="46c51-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46c51-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46c51-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="46c51-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46c51-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-135">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="46c51-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="46c51-136">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="46c51-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="46c51-137">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="46c51-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="46c51-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="46c51-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46c51-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-141">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="46c51-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="46c51-142">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="46c51-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="46c51-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="46c51-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46c51-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-146">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="46c51-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="46c51-147">Nome do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="46c51-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="46c51-148">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="46c51-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46c51-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-151">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="46c51-151">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="46c51-152">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="46c51-152">A textual description of the object.</span></span>

<span data-ttu-id="46c51-153">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46c51-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46c51-154">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="46c51-154">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-155">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="46c51-155">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-157">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="46c51-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="46c51-158">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="46c51-158">Indicates when the object was installed.</span></span> <span data-ttu-id="46c51-159">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="46c51-159">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="46c51-160">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46c51-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46c51-161">**IRQNumber**</span><span class="sxs-lookup"><span data-stu-id="46c51-161">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46c51-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-164">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 1,1 "), [**chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46c51-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46c51-165">Parte do valor de chave do objeto, número de IRQ.</span><span class="sxs-lookup"><span data-stu-id="46c51-165">Part of the object's key value, IRQ number.</span></span>

</dd> <dt>

<span data-ttu-id="46c51-166">**Nome**</span><span class="sxs-lookup"><span data-stu-id="46c51-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46c51-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-169">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="46c51-169">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="46c51-170">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="46c51-170">Label by which the object is known.</span></span> <span data-ttu-id="46c51-171">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="46c51-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="46c51-172">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46c51-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46c51-173">**Compartilhável**</span><span class="sxs-lookup"><span data-stu-id="46c51-173">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-174">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="46c51-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-176">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="46c51-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="46c51-177">Se **for true**, o IRQ poderá ser compartilhado.</span><span class="sxs-lookup"><span data-stu-id="46c51-177">If **TRUE**, the IRQ can be shared.</span></span>

</dd> <dt>

<span data-ttu-id="46c51-178">**Status**</span><span class="sxs-lookup"><span data-stu-id="46c51-178">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="46c51-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-181">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="46c51-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="46c51-182">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="46c51-182">String that indicates the current status of the object.</span></span> <span data-ttu-id="46c51-183">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="46c51-183">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="46c51-184">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="46c51-184">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="46c51-185">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="46c51-185">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="46c51-186">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="46c51-186">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="46c51-187">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="46c51-187">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="46c51-188">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="46c51-188">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="46c51-189">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46c51-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="46c51-190">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="46c51-190">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="46c51-191">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="46c51-191">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="46c51-192">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="46c51-192">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="46c51-193">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="46c51-193">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46c51-194">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="46c51-194">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="46c51-195">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="46c51-195">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="46c51-196">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="46c51-196">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="46c51-197">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="46c51-197">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="46c51-198">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="46c51-198">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="46c51-199">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="46c51-199">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="46c51-200">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="46c51-200">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="46c51-201">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="46c51-201">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="46c51-202">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="46c51-202">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46c51-203">**TriggerLevel**</span><span class="sxs-lookup"><span data-stu-id="46c51-203">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-204">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46c51-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-206">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de IRQ do recurso do sistema DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="46c51-206">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="46c51-207">Indica se a interrupção é disparada pelo sinal de hardware que ficará alto ou baixo.</span><span class="sxs-lookup"><span data-stu-id="46c51-207">Indicates whether the interruption is triggered by the hardware signal going high or low.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46c51-208">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="46c51-208">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46c51-209">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="46c51-209">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="46c51-210">**Ativo baixo** (3)</span><span class="sxs-lookup"><span data-stu-id="46c51-210">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="46c51-211">**Ativo alto** (4)</span><span class="sxs-lookup"><span data-stu-id="46c51-211">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46c51-212">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="46c51-212">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46c51-213">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46c51-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46c51-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c51-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46c51-215">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 1,3 "," MIF. \|Informações de IRQ do recurso do sistema DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="46c51-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="46c51-216">Tipo de interrupção que pode ocorrer.</span><span class="sxs-lookup"><span data-stu-id="46c51-216">Type of interruption that can occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46c51-217">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="46c51-217">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46c51-218">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="46c51-218">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="46c51-219">**Nível** (3)</span><span class="sxs-lookup"><span data-stu-id="46c51-219">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="46c51-220">**Borda** (4)</span><span class="sxs-lookup"><span data-stu-id="46c51-220">**Edge** (4)</span></span>


<span data-ttu-id="46c51-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="46c51-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="46c51-222">Comentários</span><span class="sxs-lookup"><span data-stu-id="46c51-222">Remarks</span></span>

<span data-ttu-id="46c51-223">A classe de **\_ IRQ de CIM** é derivada do [**CIM \_ SystemResource**](cim-systemresource.md). O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="46c51-223">The **CIM\_IRQ** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).WMI does not implement this class.</span></span> <span data-ttu-id="46c51-224">Consulte [classes Win32](win32-provider.md) para classes derivadas do **\_ IRQ de CIM**.</span><span class="sxs-lookup"><span data-stu-id="46c51-224">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_IRQ**.</span></span>

<span data-ttu-id="46c51-225">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="46c51-225">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="46c51-226">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="46c51-226">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="46c51-227">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46c51-227">Requirements</span></span>



| <span data-ttu-id="46c51-228">Requisito</span><span class="sxs-lookup"><span data-stu-id="46c51-228">Requirement</span></span> | <span data-ttu-id="46c51-229">Valor</span><span class="sxs-lookup"><span data-stu-id="46c51-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46c51-230">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46c51-230">Minimum supported client</span></span><br/> | <span data-ttu-id="46c51-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46c51-231">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46c51-232">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46c51-232">Minimum supported server</span></span><br/> | <span data-ttu-id="46c51-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46c51-233">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46c51-234">Namespace</span><span class="sxs-lookup"><span data-stu-id="46c51-234">Namespace</span></span><br/>                | <span data-ttu-id="46c51-235">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="46c51-235">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46c51-236">MOF</span><span class="sxs-lookup"><span data-stu-id="46c51-236">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46c51-237"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46c51-237"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46c51-238">DLL</span><span class="sxs-lookup"><span data-stu-id="46c51-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46c51-239"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46c51-239"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46c51-240">Confira também</span><span class="sxs-lookup"><span data-stu-id="46c51-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c51-241">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="46c51-241">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

