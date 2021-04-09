---
description: O Win32 \_ IRQResource &\# 160; A classe WMI representa um número de IRQ (linha de solicitação de interrupção) em um sistema de computador executando o Windows.
ms.assetid: bae0c28e-2b66-40ac-9679-b2dfe9269306
ms.tgt_platform: multiple
title: Classe Win32_IRQResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IRQResource
- Win32_IRQResource.Availability
- Win32_IRQResource.Caption
- Win32_IRQResource.CreationClassName
- Win32_IRQResource.CSCreationClassName
- Win32_IRQResource.CSName
- Win32_IRQResource.Description
- Win32_IRQResource.Hardware
- Win32_IRQResource.InstallDate
- Win32_IRQResource.IRQNumber
- Win32_IRQResource.Name
- Win32_IRQResource.Shareable
- Win32_IRQResource.Status
- Win32_IRQResource.TriggerLevel
- Win32_IRQResource.TriggerType
- Win32_IRQResource.Vector
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd02487fe166cd7ce55482eaca1339c8701f2b62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089023"
---
# <a name="win32_irqresource-class"></a><span data-ttu-id="13b8f-103">\_Classe Win32 IRQResource</span><span class="sxs-lookup"><span data-stu-id="13b8f-103">Win32\_IRQResource class</span></span>

<span data-ttu-id="13b8f-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ IRQResource do Win32** representa um número de IRQ (linha de solicitação de interrupção) em um sistema de computador executando o Windows.  </span><span class="sxs-lookup"><span data-stu-id="13b8f-104">The **Win32\_IRQResource**  [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an interrupt request line (IRQ) number on a computer system running Windows.</span></span> <span data-ttu-id="13b8f-105">Uma solicitação de interrupção é um sinal enviado à CPU por um dispositivo ou programa para eventos críticos de tempo.</span><span class="sxs-lookup"><span data-stu-id="13b8f-105">An interrupt request is a signal sent to the CPU by a device or program for time critical events.</span></span> <span data-ttu-id="13b8f-106">O IRQ pode ser baseado em hardware ou em software.</span><span class="sxs-lookup"><span data-stu-id="13b8f-106">IRQ can be hardware-based or software-based.</span></span>

<span data-ttu-id="13b8f-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="13b8f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="13b8f-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="13b8f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b8f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13b8f-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_IRQResource : CIM_IRQ
{
  uint16   Availability;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  boolean  Hardware;
  datetime InstallDate;
  uint32   IRQNumber;
  string   Name;
  boolean  Shareable;
  string   Status;
  uint16   TriggerLevel;
  uint16   TriggerType;
  uint32   Vector;
};
```

## <a name="members"></a><span data-ttu-id="13b8f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="13b8f-110">Members</span></span>

<span data-ttu-id="13b8f-111">A classe **Win32 \_ IRQResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="13b8f-111">The **Win32\_IRQResource** class has these types of members:</span></span>

-   [<span data-ttu-id="13b8f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="13b8f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13b8f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="13b8f-113">Properties</span></span>

<span data-ttu-id="13b8f-114">A classe **Win32 \_ IRQResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="13b8f-114">The **Win32\_IRQResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13b8f-115">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="13b8f-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13b8f-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-118">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="13b8f-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-119">Disponibilidade do IRQ.</span><span class="sxs-lookup"><span data-stu-id="13b8f-119">Availability of the IRQ.</span></span>

<span data-ttu-id="13b8f-120">Essa propriedade é herdada [**do \_ IRQ de CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-120">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="13b8f-121"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="13b8f-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="13b8f-122">Outro</span><span class="sxs-lookup"><span data-stu-id="13b8f-122">Other</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13b8f-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="13b8f-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="13b8f-124">Unknown</span><span class="sxs-lookup"><span data-stu-id="13b8f-124">Unknown</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13b8f-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="13b8f-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="13b8f-126">Disponível</span><span class="sxs-lookup"><span data-stu-id="13b8f-126">Available</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="13b8f-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponível** (3)</span><span class="sxs-lookup"><span data-stu-id="13b8f-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="13b8f-128">Em uso ou não disponível</span><span class="sxs-lookup"><span data-stu-id="13b8f-128">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="13b8f-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**Em uso/não disponível** (4)</span><span class="sxs-lookup"><span data-stu-id="13b8f-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="13b8f-130">Em uso e disponível ou compartilhável</span><span class="sxs-lookup"><span data-stu-id="13b8f-130">In Use and Available or Sharable</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="13b8f-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**Em uso e disponível/compartilhável** (5)</span><span class="sxs-lookup"><span data-stu-id="13b8f-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="13b8f-132">Em uso e disponível/compartilhável</span><span class="sxs-lookup"><span data-stu-id="13b8f-132">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13b8f-133">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="13b8f-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13b8f-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-136">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="13b8f-136">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-137">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="13b8f-137">Short description of the object a one-line string.</span></span>

<span data-ttu-id="13b8f-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b8f-139">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13b8f-139">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13b8f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-142">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="13b8f-142">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-143">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="13b8f-143">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="13b8f-144">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="13b8f-144">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="13b8f-145">Essa propriedade é herdada [**do \_ IRQ de CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-145">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b8f-146">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13b8f-146">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13b8f-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-149">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="13b8f-149">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-150">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="13b8f-150">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="13b8f-151">Essa propriedade é herdada [**do \_ IRQ de CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-151">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b8f-152">**CSName**</span><span class="sxs-lookup"><span data-stu-id="13b8f-152">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13b8f-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-155">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="13b8f-155">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-156">Nome do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="13b8f-156">Name of the scoping computer system.</span></span>

<span data-ttu-id="13b8f-157">Essa propriedade é herdada [**do \_ IRQ de CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-157">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b8f-158">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="13b8f-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13b8f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-161">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="13b8f-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-162">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="13b8f-162">Textual description of the object.</span></span>

<span data-ttu-id="13b8f-163">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b8f-164">**Hardware**</span><span class="sxs-lookup"><span data-stu-id="13b8f-164">**Hardware**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-165">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="13b8f-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-167">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| descritor de recursos de estruturas do sistema \| \_ \| ")</span><span class="sxs-lookup"><span data-stu-id="13b8f-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|RESOURCE\_DESCRIPTOR\|InterfaceType")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-168">Se for **true**, a interrupção será baseada em hardware ou software.</span><span class="sxs-lookup"><span data-stu-id="13b8f-168">If **TRUE**, the interrupt is hardware or software based.</span></span> <span data-ttu-id="13b8f-169">Um IRQ de hardware é um fio físico do periférico para o chip do controlador de interrupção programável (PIC) por meio do qual a CPU pode ser notificada de eventos de tempo crítico.</span><span class="sxs-lookup"><span data-stu-id="13b8f-169">A hardware IRQ is a physical wire from the peripheral to the programmable interrupt controller (PIC) chip through which the CPU can be notified of time-critical events.</span></span> <span data-ttu-id="13b8f-170">Algumas linhas de IRQ são reservadas para dispositivos Standard, como o teclado, as unidades de disquete e o relógio do sistema.</span><span class="sxs-lookup"><span data-stu-id="13b8f-170">Some IRQ lines are reserved for standard devices, such as the keyboard, floppy disk drives, and the system clock.</span></span> <span data-ttu-id="13b8f-171">Uma interrupção de software permite que os aplicativos obtenham a atenção do processador.</span><span class="sxs-lookup"><span data-stu-id="13b8f-171">A software interrupt allows applications to get the attention of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="13b8f-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="13b8f-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-173">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13b8f-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-175">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="13b8f-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-176">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="13b8f-176">Date and time the object was installed.</span></span> <span data-ttu-id="13b8f-177">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="13b8f-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="13b8f-178">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b8f-179">**IRQNumber**</span><span class="sxs-lookup"><span data-stu-id="13b8f-179">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-180">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13b8f-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-182">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 1,1 "), [**chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13b8f-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-183">Parte do valor de chave do objeto.</span><span class="sxs-lookup"><span data-stu-id="13b8f-183">Part of the object's key value.</span></span>

<span data-ttu-id="13b8f-184">Essa propriedade é herdada [**do \_ IRQ de CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-184">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b8f-185">**Nome**</span><span class="sxs-lookup"><span data-stu-id="13b8f-185">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13b8f-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-188">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="13b8f-188">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-189">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="13b8f-189">Label by which the object is known.</span></span> <span data-ttu-id="13b8f-190">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="13b8f-190">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="13b8f-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b8f-192">**Compartilhável**</span><span class="sxs-lookup"><span data-stu-id="13b8f-192">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-193">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="13b8f-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-195">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="13b8f-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-196">Se **for true**, o IRQ poderá ser compartilhado.</span><span class="sxs-lookup"><span data-stu-id="13b8f-196">If **TRUE**, the IRQ can be shared.</span></span>

<span data-ttu-id="13b8f-197">Essa propriedade é herdada [**do \_ IRQ de CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-197">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b8f-198">**Status**</span><span class="sxs-lookup"><span data-stu-id="13b8f-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13b8f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-201">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="13b8f-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-202">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="13b8f-202">Current status of the object.</span></span> <span data-ttu-id="13b8f-203">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="13b8f-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="13b8f-204">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="13b8f-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="13b8f-205">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="13b8f-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="13b8f-206">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="13b8f-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="13b8f-207">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="13b8f-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="13b8f-208">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="13b8f-209">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="13b8f-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="13b8f-210">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="13b8f-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="13b8f-211">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="13b8f-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="13b8f-212">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="13b8f-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13b8f-213">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="13b8f-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="13b8f-214">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="13b8f-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="13b8f-215">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="13b8f-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="13b8f-216">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="13b8f-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="13b8f-217">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="13b8f-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="13b8f-218">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="13b8f-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="13b8f-219">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="13b8f-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="13b8f-220">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="13b8f-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="13b8f-221">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="13b8f-221">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13b8f-222">**TriggerLevel**</span><span class="sxs-lookup"><span data-stu-id="13b8f-222">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-223">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13b8f-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-225">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de IRQ do recurso do sistema DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="13b8f-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-226">Nível de gatilho de IRQ que indica se a interrupção é disparada pelo sinal de hardware ficando alta (4) ou baixa (3).</span><span class="sxs-lookup"><span data-stu-id="13b8f-226">IRQ trigger level indicating whether the interrupt is triggered by the hardware signal going high (4) or low (3).</span></span>

<span data-ttu-id="13b8f-227">Essa propriedade é herdada [**do \_ IRQ de CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-227">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13b8f-228">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="13b8f-228">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13b8f-229">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="13b8f-229">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="13b8f-230">**Ativo baixo** (3)</span><span class="sxs-lookup"><span data-stu-id="13b8f-230">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="13b8f-231">**Ativo alto** (4)</span><span class="sxs-lookup"><span data-stu-id="13b8f-231">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13b8f-232">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="13b8f-232">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-233">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13b8f-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-235">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| IRQ \| 1,3 "," MIF. \|Informações de IRQ do recurso do sistema DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="13b8f-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-236">Tipo de gatilho de IRQ indicando se ocorrerem interrupções disparadas por borda (4) ou disparadas por nível (3).</span><span class="sxs-lookup"><span data-stu-id="13b8f-236">IRQ trigger type indicating whether edge-triggered (4) or level-triggered (3) interrupts occur.</span></span>

<span data-ttu-id="13b8f-237">Essa propriedade é herdada [**do \_ IRQ de CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-237">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13b8f-238">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="13b8f-238">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13b8f-239">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="13b8f-239">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="13b8f-240">**Nível** (3)</span><span class="sxs-lookup"><span data-stu-id="13b8f-240">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="13b8f-241">**Borda** (4)</span><span class="sxs-lookup"><span data-stu-id="13b8f-241">**Edge** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13b8f-242">**Vetor**</span><span class="sxs-lookup"><span data-stu-id="13b8f-242">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b8f-243">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13b8f-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="13b8f-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b8f-245">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| estruturas do sistema cm/nível de interrupção do \| [**\_ \_ \_ descritor de recursos parciais**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| \| ")</span><span class="sxs-lookup"><span data-stu-id="13b8f-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Interrupt\|Level")</span></span>
</dt> </dl>

<span data-ttu-id="13b8f-246">Vetor do recurso de IRQ do Windows.</span><span class="sxs-lookup"><span data-stu-id="13b8f-246">Vector of the Windows IRQ resource.</span></span> <span data-ttu-id="13b8f-247">Um vetor contém o endereço de memória para a função que será executada quando a solicitação de interrupção for confirmada pela CPU.</span><span class="sxs-lookup"><span data-stu-id="13b8f-247">A vector contains the memory address to the function that will execute once the interrupt request is acknowledged by the CPU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13b8f-248">Comentários</span><span class="sxs-lookup"><span data-stu-id="13b8f-248">Remarks</span></span>

<span data-ttu-id="13b8f-249">A classe **Win32 \_ IRQResource** é derivada de [**\_ IRQ de CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="13b8f-249">The **Win32\_IRQResource** class is derived from [**CIM\_IRQ**](cim-irq.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13b8f-250">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13b8f-250">Requirements</span></span>



| <span data-ttu-id="13b8f-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="13b8f-251">Requirement</span></span> | <span data-ttu-id="13b8f-252">Valor</span><span class="sxs-lookup"><span data-stu-id="13b8f-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13b8f-253">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13b8f-253">Minimum supported client</span></span><br/> | <span data-ttu-id="13b8f-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13b8f-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13b8f-255">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13b8f-255">Minimum supported server</span></span><br/> | <span data-ttu-id="13b8f-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13b8f-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13b8f-257">Namespace</span><span class="sxs-lookup"><span data-stu-id="13b8f-257">Namespace</span></span><br/>                | <span data-ttu-id="13b8f-258">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="13b8f-258">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13b8f-259">MOF</span><span class="sxs-lookup"><span data-stu-id="13b8f-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13b8f-260"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13b8f-260"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13b8f-261">DLL</span><span class="sxs-lookup"><span data-stu-id="13b8f-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13b8f-262"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13b8f-262"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13b8f-263">Confira também</span><span class="sxs-lookup"><span data-stu-id="13b8f-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b8f-264">**IRQ de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="13b8f-264">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dt>

[<span data-ttu-id="13b8f-265">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="13b8f-265">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

