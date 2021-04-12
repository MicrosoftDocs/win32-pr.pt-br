---
description: Uma \_ classe de sistema CIM representa uma coleção especial de \_ instâncias do CIM ManagedSystemElement.
ms.assetid: c4fd0598-3cb3-428f-ad39-a14232ef7c17
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystem (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.Caption
- CIM_ComputerSystem.Description
- CIM_ComputerSystem.InstallDate
- CIM_ComputerSystem.Status
- CIM_ComputerSystem.CreationClassName
- CIM_ComputerSystem.Name
- CIM_ComputerSystem.PrimaryOwnerContact
- CIM_ComputerSystem.PrimaryOwnerName
- CIM_ComputerSystem.Roles
- CIM_ComputerSystem.NameFormat
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4645a8d4b2440b0b102658d3eca74d825d774dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457078"
---
# <a name="cim_computersystem-class-cimwin32-wmi-providers"></a><span data-ttu-id="ccb36-103">Classe CIM_ComputerSystem (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ccb36-103">CIM_ComputerSystem class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ccb36-104">Uma classe de **\_ sistema CIM** representa uma coleção especial de instâncias do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="ccb36-104">A **CIM\_ComputerSystem** class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="ccb36-105">Esta coleção fornece recursos do computador e serve como um ponto de agregação para associar um ou mais dos seguintes elementos: sistema de arquivos, sistema operacional, processador e memória (armazenamento volátil e não volátil).</span><span class="sxs-lookup"><span data-stu-id="ccb36-105">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="ccb36-106">Essa classe é derivada do [**\_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-106">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ccb36-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ccb36-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ccb36-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ccb36-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ccb36-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ccb36-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ccb36-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ccb36-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb36-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccb36-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C525-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
  string   NameFormat;
};
```

## <a name="members"></a><span data-ttu-id="ccb36-112">Membros</span><span class="sxs-lookup"><span data-stu-id="ccb36-112">Members</span></span>

<span data-ttu-id="ccb36-113">A classe de **\_ sistema CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ccb36-113">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="ccb36-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ccb36-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ccb36-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ccb36-115">Properties</span></span>

<span data-ttu-id="ccb36-116">A classe de **\_ ComputerSystem de CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ccb36-116">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ccb36-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ccb36-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb36-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccb36-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb36-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ccb36-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ccb36-121">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ccb36-121">A short textual description of the object.</span></span>

<span data-ttu-id="ccb36-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccb36-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ccb36-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb36-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccb36-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb36-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-126">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ccb36-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ccb36-127">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="ccb36-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ccb36-128">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="ccb36-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ccb36-129">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccb36-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ccb36-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb36-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccb36-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb36-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-133">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="ccb36-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ccb36-134">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ccb36-134">A textual description of the object.</span></span>

<span data-ttu-id="ccb36-135">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccb36-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ccb36-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb36-137">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ccb36-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb36-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-139">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="ccb36-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ccb36-140">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="ccb36-140">Indicates when the object was installed.</span></span> <span data-ttu-id="ccb36-141">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="ccb36-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ccb36-142">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccb36-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ccb36-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb36-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccb36-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb36-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-146">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ccb36-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ccb36-147">Define o rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="ccb36-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="ccb36-148">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccb36-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="ccb36-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb36-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccb36-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb36-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-152">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="ccb36-152">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="ccb36-153">Identifica como o nome do sistema de computador é gerado, usando uma heurística.</span><span class="sxs-lookup"><span data-stu-id="ccb36-153">Identifies how the computer system name is generated, using a heuristic.</span></span> <span data-ttu-id="ccb36-154">A heurística é descrita em detalhes na especificação de modelo comum do CIM v2.</span><span class="sxs-lookup"><span data-stu-id="ccb36-154">The heuristic is outlined, in detail, in the CIM V2 Common Model specification.</span></span> <span data-ttu-id="ccb36-155">Ele pressupõe que as regras documentadas são percorridas em ordem, para determinar e atribuir um nome.</span><span class="sxs-lookup"><span data-stu-id="ccb36-155">It assumes that the documented rules are traversed in order, to determine and assign a name.</span></span> <span data-ttu-id="ccb36-156">A lista de valores **NameFormat** define a ordem de precedência para atribuir o nome do sistema do computador.</span><span class="sxs-lookup"><span data-stu-id="ccb36-156">The **NameFormat** values list defines the precedence order for assigning the computer system name.</span></span> <span data-ttu-id="ccb36-157">Várias regras são mapeadas para o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="ccb36-157">Several rules do map to the same Value.</span></span>

<span data-ttu-id="ccb36-158">Observe que o **nome** do objeto é calculado usando o heurístico é o valor de chave do sistema.</span><span class="sxs-lookup"><span data-stu-id="ccb36-158">Note that the object's **Name** is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="ccb36-159">Outros nomes podem ser atribuídos e usados para o objeto que melhor atendam aos negócios, usando aliases.</span><span class="sxs-lookup"><span data-stu-id="ccb36-159">Other names can be assigned and used for the object that better suit the business, using Aliases.</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="ccb36-160">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="ccb36-160">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="ccb36-161">**Discar** ("discar")</span><span class="sxs-lookup"><span data-stu-id="ccb36-161">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="ccb36-162">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="ccb36-162">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="ccb36-163">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="ccb36-163">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="ccb36-164">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="ccb36-164">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="ccb36-165">**X25** ("X25")</span><span class="sxs-lookup"><span data-stu-id="ccb36-165">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="ccb36-166">**ISDN** ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="ccb36-166">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="ccb36-167">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="ccb36-167">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="ccb36-168">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="ccb36-168">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="ccb36-169">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="ccb36-169">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="ccb36-170">**E. 164** ("E. 164")</span><span class="sxs-lookup"><span data-stu-id="ccb36-170">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="ccb36-171">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="ccb36-171">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="ccb36-172">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="ccb36-172">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ccb36-173">**Outro** ("outro")</span><span class="sxs-lookup"><span data-stu-id="ccb36-173">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ccb36-174">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="ccb36-174">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb36-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccb36-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb36-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccb36-177">Como o proprietário do sistema primário pode ser alcançado (por exemplo, número de telefone ou endereço de email).</span><span class="sxs-lookup"><span data-stu-id="ccb36-177">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="ccb36-178">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-178">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccb36-179">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="ccb36-179">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb36-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccb36-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb36-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-182">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ccb36-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ccb36-183">Nome do proprietário do sistema primário.</span><span class="sxs-lookup"><span data-stu-id="ccb36-183">Name of the primary system owner.</span></span>

<span data-ttu-id="ccb36-184">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-184">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccb36-185">**Funções**</span><span class="sxs-lookup"><span data-stu-id="ccb36-185">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb36-186">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccb36-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ccb36-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ccb36-188">As funções que o sistema desempenha no ambiente de tecnologia da informação.</span><span class="sxs-lookup"><span data-stu-id="ccb36-188">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="ccb36-189">As subclasses do sistema podem substituir essa propriedade para definir valores de função explícitos.</span><span class="sxs-lookup"><span data-stu-id="ccb36-189">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="ccb36-190">Como alternativa, um grupo de trabalho pode descrever a heurística, as convenções e as diretrizes para especificar funções.</span><span class="sxs-lookup"><span data-stu-id="ccb36-190">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="ccb36-191">Por exemplo, para uma instância de um sistema de rede, essa propriedade pode conter a cadeia de caracteres "switch" ou "Bridge".</span><span class="sxs-lookup"><span data-stu-id="ccb36-191">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="ccb36-192">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-192">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccb36-193">**Status**</span><span class="sxs-lookup"><span data-stu-id="ccb36-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb36-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccb36-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb36-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccb36-196">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ccb36-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ccb36-197">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ccb36-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="ccb36-198">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="ccb36-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ccb36-199">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="ccb36-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ccb36-200">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="ccb36-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ccb36-201">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="ccb36-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ccb36-202">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="ccb36-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ccb36-203">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="ccb36-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ccb36-204">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ccb36-205">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ccb36-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ccb36-206">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ccb36-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ccb36-207">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="ccb36-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ccb36-208">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="ccb36-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ccb36-209">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="ccb36-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ccb36-210">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ccb36-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ccb36-211">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="ccb36-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ccb36-212">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="ccb36-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ccb36-213">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="ccb36-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ccb36-214">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="ccb36-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ccb36-215">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="ccb36-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ccb36-216">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="ccb36-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ccb36-217">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="ccb36-217">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="ccb36-218"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ccb36-218"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ccb36-219">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccb36-219">Remarks</span></span>

<span data-ttu-id="ccb36-220">A classe de **\_ ComputerSystem do CIM** é derivada do [**\_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-220">The **CIM\_ComputerSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="ccb36-221">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="ccb36-221">WMI does not implement this class.</span></span> <span data-ttu-id="ccb36-222">Para obter mais informações sobre classes derivadas do **CIM \_ ComputerSystem**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ccb36-222">For more information about classes derived from **CIM\_ComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ccb36-223">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="ccb36-223">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ccb36-224">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="ccb36-224">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb36-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccb36-225">Requirements</span></span>



| <span data-ttu-id="ccb36-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb36-226">Requirement</span></span> | <span data-ttu-id="ccb36-227">Valor</span><span class="sxs-lookup"><span data-stu-id="ccb36-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb36-228">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccb36-228">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb36-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccb36-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ccb36-230">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccb36-230">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb36-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccb36-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ccb36-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccb36-232">Namespace</span></span><br/>                | <span data-ttu-id="ccb36-233">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ccb36-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ccb36-234">MOF</span><span class="sxs-lookup"><span data-stu-id="ccb36-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccb36-235"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ccb36-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ccb36-236">DLL</span><span class="sxs-lookup"><span data-stu-id="ccb36-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccb36-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccb36-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccb36-238">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccb36-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb36-239">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="ccb36-239">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

