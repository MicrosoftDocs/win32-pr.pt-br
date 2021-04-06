---
description: A \_ classe CIM UnitaryComputerSystem representa um computador desktop, móvel, de rede, servidor ou outro tipo de sistema de computador de nó único.
ms.assetid: c696050d-c921-4056-adc7-e4a2e9f4e119
ms.tgt_platform: multiple
title: Classe CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem
- CIM_UnitaryComputerSystem.Caption
- CIM_UnitaryComputerSystem.CreationClassName
- CIM_UnitaryComputerSystem.Description
- CIM_UnitaryComputerSystem.InitialLoadInfo
- CIM_UnitaryComputerSystem.InstallDate
- CIM_UnitaryComputerSystem.LastLoadInfo
- CIM_UnitaryComputerSystem.Name
- CIM_UnitaryComputerSystem.NameFormat
- CIM_UnitaryComputerSystem.PowerManagementCapabilities
- CIM_UnitaryComputerSystem.PowerManagementSupported
- CIM_UnitaryComputerSystem.PowerState
- CIM_UnitaryComputerSystem.PrimaryOwnerContact
- CIM_UnitaryComputerSystem.PrimaryOwnerName
- CIM_UnitaryComputerSystem.ResetCapability
- CIM_UnitaryComputerSystem.Roles
- CIM_UnitaryComputerSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e14812fda7971ffe045e8e36752c983cf5350402
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920223"
---
# <a name="cim_unitarycomputersystem-class"></a><span data-ttu-id="812cd-103">\_Classe CIM UnitaryComputerSystem</span><span class="sxs-lookup"><span data-stu-id="812cd-103">CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="812cd-104">A classe **CIM \_ UnitaryComputerSystem** representa um computador desktop, móvel, de rede, servidor ou outro tipo de sistema de computador de nó único.</span><span class="sxs-lookup"><span data-stu-id="812cd-104">The **CIM\_UnitaryComputerSystem** class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="812cd-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="812cd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="812cd-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="812cd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="812cd-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="812cd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="812cd-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="812cd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="812cd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="812cd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C526-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UnitaryComputerSystem : CIM_ComputerSystem
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  string   InitialLoadInfo[];
  datetime InstallDate;
  string   LastLoadInfo;
  string   Name;
  string   NameFormat;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  string   Roles[];
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="812cd-110">Membros</span><span class="sxs-lookup"><span data-stu-id="812cd-110">Members</span></span>

<span data-ttu-id="812cd-111">A classe **CIM \_ UnitaryComputerSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="812cd-111">The **CIM\_UnitaryComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="812cd-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="812cd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="812cd-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="812cd-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="812cd-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="812cd-114">Methods</span></span>

<span data-ttu-id="812cd-115">A classe **CIM \_ UnitaryComputerSystem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="812cd-115">The **CIM\_UnitaryComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="812cd-116">Método</span><span class="sxs-lookup"><span data-stu-id="812cd-116">Method</span></span>                                                                           | <span data-ttu-id="812cd-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="812cd-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="812cd-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="812cd-118">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md) | <span data-ttu-id="812cd-119">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="812cd-119">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="812cd-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="812cd-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="812cd-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="812cd-121">Properties</span></span>

<span data-ttu-id="812cd-122">A classe **CIM \_ UnitaryComputerSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="812cd-122">The **CIM\_UnitaryComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="812cd-123">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="812cd-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812cd-126">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="812cd-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="812cd-127">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="812cd-127">Short textual description of the object.</span></span>

<span data-ttu-id="812cd-128">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="812cd-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="812cd-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812cd-132">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="812cd-132">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="812cd-133">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="812cd-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="812cd-134">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="812cd-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="812cd-135">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-135">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="812cd-136">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="812cd-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812cd-139">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="812cd-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="812cd-140">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="812cd-140">Textual description of the object.</span></span>

<span data-ttu-id="812cd-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="812cd-142">**InitialLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="812cd-142">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-143">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="812cd-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="812cd-145">Dados necessários para localizar o dispositivo de carga inicial (sua chave) ou o serviço de inicialização para solicitar que o sistema operacional seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="812cd-145">Data needed to find either the initial load device (its key) or the boot service to request the operating system to start.</span></span> <span data-ttu-id="812cd-146">Além disso, os parâmetros de carregamento (ou seja, um nome de caminho e parâmetros) também podem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="812cd-146">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="812cd-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="812cd-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-148">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="812cd-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812cd-150">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="812cd-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="812cd-151">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="812cd-151">Date and time the object was installed.</span></span> <span data-ttu-id="812cd-152">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="812cd-152">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="812cd-153">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="812cd-154">**LastLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="812cd-154">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="812cd-157">Dados que identificam o dispositivo de carga inicial (sua chave) ou o serviço de inicialização que solicitou a última carga do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="812cd-157">Data that identifies either the initial load device (its key) or the boot service that requested the last operating system load.</span></span> <span data-ttu-id="812cd-158">Além disso, os parâmetros de carregamento (ou seja, um nome de caminho e parâmetros) também podem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="812cd-158">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="812cd-159">**Nome**</span><span class="sxs-lookup"><span data-stu-id="812cd-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812cd-162">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="812cd-162">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="812cd-163">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="812cd-163">Label by which the object is known.</span></span> <span data-ttu-id="812cd-164">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="812cd-164">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="812cd-165">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="812cd-166">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="812cd-166">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="812cd-169">O objeto de [**\_ sistema**](cim-computersystem.md) de sistemas CIM e seus derivados são objetos de nível superior do CIM que fornecem o escopo para vários componentes e exigem chaves de [**\_ sistema CIM**](cim-system.md) exclusivas.</span><span class="sxs-lookup"><span data-stu-id="812cd-169">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of CIM that provide the scope for numerous components and require unique [**CIM\_System**](cim-system.md) keys.</span></span> <span data-ttu-id="812cd-170">Um heurístico é definido para criar o nome do sistema de **\_ sistema CIM** em uma tentativa de sempre gerar o mesmo nome de System, independentemente do protocolo de descoberta.</span><span class="sxs-lookup"><span data-stu-id="812cd-170">A heuristic is defined to create the **CIM\_ComputerSystem** name in an attempt to always generate the same system name, independent of discovery protocol.</span></span> <span data-ttu-id="812cd-171">Isso impede problemas de inventário e gerenciamento em que o mesmo ativo ou entidade é descoberto várias vezes, mas não pode ser resolvido para um único objeto.</span><span class="sxs-lookup"><span data-stu-id="812cd-171">This prevents inventory and management problems where the same asset or entity is discovered multiple times, but cannot be resolved to a single object.</span></span> <span data-ttu-id="812cd-172">Essa propriedade identifica como o nome do sistema foi gerado usando a heurística de subclasse.</span><span class="sxs-lookup"><span data-stu-id="812cd-172">This property identifies how the system name was generated by using the subclass heuristic.</span></span> <span data-ttu-id="812cd-173">A heurística é descrita na especificação de modelo comum do CIM V2 e pressupõe que as regras documentadas sejam percorridas para determinar e atribuir um nome.</span><span class="sxs-lookup"><span data-stu-id="812cd-173">The heuristic is outlined in the CIM V2 Common Model specification and assumes that the documented rules are traversed to determine and assign a name.</span></span> <span data-ttu-id="812cd-174">A lista de valores de **NameFormat** define a ordem de precedência para atribuir o nome do sistema com várias regras mapeando para o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="812cd-174">The **NameFormat** values list defines the precedence order for assigning the system name with several rules mapping to the same value.</span></span> <span data-ttu-id="812cd-175">Observe que o nome do sistema de sistema **CIM \_** que é calculado usando o heurístico é o valor de chave do System.</span><span class="sxs-lookup"><span data-stu-id="812cd-175">Note that the **CIM\_ComputerSystem** name that is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="812cd-176">Outros nomes podem ser atribuídos e usados para o **\_ sistema** de trabalho CIM que melhor atendam aos negócios, usando aliases.</span><span class="sxs-lookup"><span data-stu-id="812cd-176">Other names can be assigned and used for the **CIM\_ComputerSystem** that better suit the business, using aliases.</span></span>

<span data-ttu-id="812cd-177">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-177">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="812cd-178">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="812cd-178">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="812cd-179">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="812cd-179">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="812cd-180">**Discar** ("discar")</span><span class="sxs-lookup"><span data-stu-id="812cd-180">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="812cd-181">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="812cd-181">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="812cd-182">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="812cd-182">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="812cd-183">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="812cd-183">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="812cd-184">**X25** ("X25")</span><span class="sxs-lookup"><span data-stu-id="812cd-184">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="812cd-185">**ISDN** ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="812cd-185">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="812cd-186">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="812cd-186">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="812cd-187">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="812cd-187">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="812cd-188">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="812cd-188">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="812cd-189">**E. 164** ("E. 164")</span><span class="sxs-lookup"><span data-stu-id="812cd-189">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="812cd-190">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="812cd-190">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="812cd-191">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="812cd-191">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="812cd-192">**Outro** ("outro")</span><span class="sxs-lookup"><span data-stu-id="812cd-192">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="812cd-193">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="812cd-193">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-194">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="812cd-194">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="812cd-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812cd-196">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controles de energia do sistema DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="812cd-196">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="812cd-197">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="812cd-197">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="812cd-198">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="812cd-198">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="812cd-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="812cd-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="812cd-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="812cd-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="812cd-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="812cd-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="812cd-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="812cd-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-203">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="812cd-203">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="812cd-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="812cd-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-205">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="812cd-205">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="812cd-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="812cd-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-207">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="812cd-207">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="812cd-208">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="812cd-208">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="812cd-209">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="812cd-209">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="812cd-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="812cd-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-211">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="812cd-211">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="812cd-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="812cd-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-213">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="812cd-213">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="812cd-214">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="812cd-214">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-215">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="812cd-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="812cd-217">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="812cd-217">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="812cd-218">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="812cd-218">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="812cd-219">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="812cd-219">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="812cd-220">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="812cd-220">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="812cd-221">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="812cd-221">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-222">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="812cd-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="812cd-224">Estado de energia atual do sistema de computador e seu sistema operacional associado.</span><span class="sxs-lookup"><span data-stu-id="812cd-224">Current power state of the computer system and its associated operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="812cd-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="812cd-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-226">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="812cd-226">Unknown.</span></span>

</dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="812cd-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Energia completa** (1)</span><span class="sxs-lookup"><span data-stu-id="812cd-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-228">Potência total.</span><span class="sxs-lookup"><span data-stu-id="812cd-228">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="812cd-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (2)</span><span class="sxs-lookup"><span data-stu-id="812cd-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-230">O sistema está em um estado de economia de energia e ainda está funcionando, mas pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="812cd-230">System is in a power-save state and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="812cd-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (3)</span><span class="sxs-lookup"><span data-stu-id="812cd-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-232">O sistema não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="812cd-232">System is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="812cd-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (4)</span><span class="sxs-lookup"><span data-stu-id="812cd-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-234">O sistema é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="812cd-234">System is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="812cd-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (5)</span><span class="sxs-lookup"><span data-stu-id="812cd-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-236">Ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="812cd-236">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="812cd-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (6** )</span><span class="sxs-lookup"><span data-stu-id="812cd-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-238">Desligar.</span><span class="sxs-lookup"><span data-stu-id="812cd-238">Power off.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="812cd-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (7)</span><span class="sxs-lookup"><span data-stu-id="812cd-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-240">O sistema está em um estado de aviso e também em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="812cd-240">System is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="812cd-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save-hibernar** (8)</span><span class="sxs-lookup"><span data-stu-id="812cd-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-242">Power Save Hibernate.</span><span class="sxs-lookup"><span data-stu-id="812cd-242">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="812cd-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Economia **de energia – soft off** (9)</span><span class="sxs-lookup"><span data-stu-id="812cd-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="812cd-244">Power Save soft off.</span><span class="sxs-lookup"><span data-stu-id="812cd-244">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="812cd-245">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="812cd-245">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="812cd-248">Cadeia de caracteres que fornece informações sobre como alcançar o proprietário do sistema primário (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="812cd-248">String that provides information on how to reach the primary system owner (for example, phone number, email address, and so on).</span></span>

<span data-ttu-id="812cd-249">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-249">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="812cd-250">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="812cd-250">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812cd-253">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="812cd-253">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="812cd-254">Nome do proprietário do sistema primário.</span><span class="sxs-lookup"><span data-stu-id="812cd-254">Name of the primary system owner.</span></span>

<span data-ttu-id="812cd-255">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-255">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="812cd-256">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="812cd-256">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-257">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="812cd-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812cd-259">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Segurança de hardware do sistema DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="812cd-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="812cd-260">Se habilitado, o sistema de computador unitário pode ser redefinido com hardware (por exemplo, com os botões potência e redefinição).</span><span class="sxs-lookup"><span data-stu-id="812cd-260">If enabled, the unitary computer system can be reset with hardware (for example, with the power and reset buttons).</span></span> <span data-ttu-id="812cd-261">Se desabilitado, a redefinição de hardware não é permitida.</span><span class="sxs-lookup"><span data-stu-id="812cd-261">If disabled, hardware reset is not allowed.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="812cd-262">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="812cd-262">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="812cd-263">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="812cd-263">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="812cd-264">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="812cd-264">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="812cd-265">**Habilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="812cd-265">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="812cd-266">**Não implementado** (5)</span><span class="sxs-lookup"><span data-stu-id="812cd-266">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="812cd-267">**Funções**</span><span class="sxs-lookup"><span data-stu-id="812cd-267">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-268">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="812cd-269">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="812cd-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="812cd-270">As funções que o sistema desempenha no ambiente de tecnologia da informação.</span><span class="sxs-lookup"><span data-stu-id="812cd-270">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="812cd-271">As subclasses do sistema podem substituir essa propriedade para definir valores de função explícitos.</span><span class="sxs-lookup"><span data-stu-id="812cd-271">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="812cd-272">Como alternativa, um grupo de trabalho pode descrever a heurística, as convenções e as diretrizes para especificar funções.</span><span class="sxs-lookup"><span data-stu-id="812cd-272">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="812cd-273">Por exemplo, para uma instância de um sistema de rede, essa propriedade pode conter a cadeia de caracteres "switch" ou "Bridge".</span><span class="sxs-lookup"><span data-stu-id="812cd-273">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="812cd-274">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-274">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="812cd-275">**Status**</span><span class="sxs-lookup"><span data-stu-id="812cd-275">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812cd-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="812cd-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812cd-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="812cd-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812cd-278">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="812cd-278">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="812cd-279">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="812cd-279">Current status of the object.</span></span> <span data-ttu-id="812cd-280">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="812cd-281">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="812cd-281">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="812cd-282">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="812cd-282">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="812cd-283">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="812cd-283">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="812cd-284">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="812cd-284">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="812cd-285">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="812cd-285">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="812cd-286">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="812cd-286">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="812cd-287">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="812cd-287">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="812cd-288">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="812cd-288">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="812cd-289">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="812cd-289">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="812cd-290">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="812cd-290">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="812cd-291">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="812cd-291">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="812cd-292">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="812cd-292">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="812cd-293">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="812cd-293">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="812cd-294"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="812cd-294"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="812cd-295">Comentários</span><span class="sxs-lookup"><span data-stu-id="812cd-295">Remarks</span></span>

<span data-ttu-id="812cd-296">A classe **CIM \_ UnitaryComputerSystem** é derivada do [**CIM \_ ComputerSystem**](cim-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-296">The **CIM\_UnitaryComputerSystem** class is derived from [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="812cd-297">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="812cd-297">WMI does not implement this class.</span></span> <span data-ttu-id="812cd-298">Para classes WMI derivadas do **CIM \_ UnitaryComputerSystem**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="812cd-298">For WMI classes derived from **CIM\_UnitaryComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="812cd-299">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="812cd-299">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="812cd-300">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="812cd-300">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="812cd-301">Requisitos</span><span class="sxs-lookup"><span data-stu-id="812cd-301">Requirements</span></span>



| <span data-ttu-id="812cd-302">Requisito</span><span class="sxs-lookup"><span data-stu-id="812cd-302">Requirement</span></span> | <span data-ttu-id="812cd-303">Valor</span><span class="sxs-lookup"><span data-stu-id="812cd-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="812cd-304">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="812cd-304">Minimum supported client</span></span><br/> | <span data-ttu-id="812cd-305">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="812cd-305">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="812cd-306">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="812cd-306">Minimum supported server</span></span><br/> | <span data-ttu-id="812cd-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="812cd-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="812cd-308">Namespace</span><span class="sxs-lookup"><span data-stu-id="812cd-308">Namespace</span></span><br/>                | <span data-ttu-id="812cd-309">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="812cd-309">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="812cd-310">MOF</span><span class="sxs-lookup"><span data-stu-id="812cd-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="812cd-311"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="812cd-311"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="812cd-312">DLL</span><span class="sxs-lookup"><span data-stu-id="812cd-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="812cd-313"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="812cd-313"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="812cd-314">Confira também</span><span class="sxs-lookup"><span data-stu-id="812cd-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="812cd-315">**\_Sistema de COMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="812cd-315">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

