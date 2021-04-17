---
description: Usado no método GetSummaryInformation na \_ classe VirtualSystemManagementService Msvm para recuperar rapidamente informações comuns relacionadas a um instantâneo ou um sistema virtual.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Classe Msvm_SummaryInformationBase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748176"
---
# <a name="msvm_summaryinformationbase-class"></a><span data-ttu-id="7e1bf-103">\_Classe Msvm SummaryInformationBase</span><span class="sxs-lookup"><span data-stu-id="7e1bf-103">Msvm\_SummaryInformationBase class</span></span>

<span data-ttu-id="7e1bf-104">Usado no método [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) na classe [**\_ VirtualSystemManagementService Msvm**](msvm-virtualsystemmanagementservice.md) para recuperar rapidamente informações comuns relacionadas a um instantâneo ou um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) method in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual system or snapshot.</span></span>

<span data-ttu-id="7e1bf-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e1bf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e1bf-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="7e1bf-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7e1bf-107">Members</span></span>

<span data-ttu-id="7e1bf-108">A classe **Msvm \_ SummaryInformationBase** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7e1bf-108">The **Msvm\_SummaryInformationBase** class has these types of members:</span></span>

-   [<span data-ttu-id="7e1bf-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7e1bf-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e1bf-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7e1bf-110">Properties</span></span>

<span data-ttu-id="7e1bf-111">A classe **Msvm \_ SummaryInformationBase** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-111">The **Msvm\_SummaryInformationBase** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e1bf-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-113">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-113">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-115">A hora em que o sistema virtual ou o instantâneo foi criado.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-115">The time at which the virtual system or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-116">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-116">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-119">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managedelement. ElementName")</span><span class="sxs-lookup"><span data-stu-id="7e1bf-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-120">O nome amigável para o instantâneo ou o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-120">The friendly name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-121">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-121">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-122">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-124">O estado atual do instantâneo ou do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-124">The current state of the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-125">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-125">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-128">Indica se as conexões de modo avançado são permitidas ou não pelo host e se são permitidas, se elas estão disponíveis para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-128">Indicates whether or not enhanced mode connections are allowed by the host and if allowed, whether or not they are available to the virtual machine.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="7e1bf-129">**Permitido e disponível** (2)</span><span class="sxs-lookup"><span data-stu-id="7e1bf-129">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="7e1bf-130">**Não permitido** (3)</span><span class="sxs-lookup"><span data-stu-id="7e1bf-130">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="7e1bf-131">**Permitido, mas não disponível** (6)</span><span class="sxs-lookup"><span data-stu-id="7e1bf-131">**Allowed but not available** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e1bf-132">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-132">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-135">O estado de integridade atual do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-135">The current health state for the virtual system.</span></span> <span data-ttu-id="7e1bf-136">Esta propriedade não é válida para instâncias de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) representando um instantâneo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-136">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-137">**HostComputerSystemName**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-137">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-140">O nome do computador que hospeda esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-140">The name of the computer hosting this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-144">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managedelement. InstanceId"), [**chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7e1bf-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-145">InstanceID é uma propriedade opcional que pode ser usada para identificar de forma opaca e exclusiva uma instância dessa classe dentro do escopo do namespace de instanciação.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-145">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="7e1bf-146">Várias subclasses dessa classe podem substituir essa propriedade para torná-la necessária ou uma chave.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-146">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="7e1bf-147">Essas subclasses também podem modificar os algoritmos preferenciais para garantir a exclusividade definida abaixo.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-147">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="7e1bf-148">Para garantir a exclusividade no NameSpace, o valor de InstanceID deve ser construído usando o seguinte algoritmo "preferencial":</span><span class="sxs-lookup"><span data-stu-id="7e1bf-148">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="7e1bf-149"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="7e1bf-149"><OrgID>:<LocalID></span></span>

<span data-ttu-id="7e1bf-150">Onde <OrgID> e <LocalID> são separados por dois-pontos (:), e onde <OrgID> devem incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que está criando ou definindo a InstanceId ou que é uma ID registrada atribuída à entidade de negócios por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-150">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="7e1bf-151">(Esse requisito é semelhante ao <Schema Name> \_ <Class Name> estrutura de nomes de classe de esquema.) Além disso, para garantir a exclusividade, <OrgID> não deve conter dois-pontos (:).</span><span class="sxs-lookup"><span data-stu-id="7e1bf-151">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="7e1bf-152">Ao usar esse algoritmo, os primeiros dois-pontos a serem exibidos em InstanceID devem aparecer entre <OrgID> e <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="7e1bf-152">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="7e1bf-153"><LocalID> é escolhido pela entidade de negócios e não deve ser reutilizado para identificar elementos subjacentes (reais) diferentes.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-153"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="7e1bf-154">Se não for nulo e o algoritmo "preferencial" acima não for usado, a entidade de definição deverá garantir que a InstanceID resultante não seja reutilizada em quaisquer InstanceIDs produzidas por este ou outros provedores para o NameSpace dessa instância.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-154">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="7e1bf-155">Se não estiver definido como nulo para instâncias definidas por DMTF, o algoritmo "preferencial" deverá ser usado com o <OrgID> conjunto como CIM.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-155">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-156">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-159">O nome exclusivo para o sistema virtual ou instantâneo.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-159">The unique name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-160">**Observações**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-163">As notas associadas ao sistema virtual ou instantâneo.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-163">The notes associated with the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-164">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-164">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-165">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-167">O número total de processadores virtuais alocados para o sistema virtual ou instantâneo.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-167">The total number of virtual processors allocated to the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-168">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-168">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-169">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-171">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="7e1bf-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-172">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-172">The current status of the element.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-173">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-173">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-176">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="7e1bf-176">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="7e1bf-177">Essa propriedade deve ser definida como NULL quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-177">This property must be set to null when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-178">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-178">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-179">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-181">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="7e1bf-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-182">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="7e1bf-182">Strings that describe the various **OperationalStatus** array values.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-183">**Atividade**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-183">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-184">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-186">A quantidade de tempo desde a última inicialização do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-186">The amount of time since the virtual system was last booted.</span></span> <span data-ttu-id="7e1bf-187">Esta propriedade não é válida para instâncias de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) representando um instantâneo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-187">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-188">**Versão**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-188">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-191">A versão do sistema virtual em um formato de "Major. Minor"; por exemplo, "2,0".</span><span class="sxs-lookup"><span data-stu-id="7e1bf-191">The version of the virtual system in a format of "major.minor"; for example, "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-192">**VirtualSwitchNames**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-192">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-193">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-193">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-195">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="7e1bf-195">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-196">Cadeias de caracteres que listam os nomes amigáveis dos comutadores virtuais aos quais a VM está conectada.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-196">Strings that list the friendly names of the virtual switches the VM is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="7e1bf-197">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-197">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e1bf-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e1bf-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7e1bf-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e1bf-200">O subtipo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7e1bf-200">The subtype of the virtual system.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="7e1bf-201">**Microsoft: Hyper-v: subtipo: 1** ("Microsoft: Hyper-v: subtipo: 1")</span><span class="sxs-lookup"><span data-stu-id="7e1bf-201">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="7e1bf-202">**Microsoft: Hyper-v: subtipo: 2** ("Microsoft: Hyper-v: subtipo: 2")</span><span class="sxs-lookup"><span data-stu-id="7e1bf-202">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


<span data-ttu-id="7e1bf-203"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7e1bf-203"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7e1bf-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e1bf-204">Requirements</span></span>



| <span data-ttu-id="7e1bf-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e1bf-205">Requirement</span></span> | <span data-ttu-id="7e1bf-206">Valor</span><span class="sxs-lookup"><span data-stu-id="7e1bf-206">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e1bf-207">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e1bf-207">Minimum supported client</span></span><br/> | <span data-ttu-id="7e1bf-208">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="7e1bf-208">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7e1bf-209">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e1bf-209">Minimum supported server</span></span><br/> | <span data-ttu-id="7e1bf-210">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7e1bf-210">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7e1bf-211">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e1bf-211">Namespace</span></span><br/>                | <span data-ttu-id="7e1bf-212">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7e1bf-212">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e1bf-213">MOF</span><span class="sxs-lookup"><span data-stu-id="7e1bf-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e1bf-214"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e1bf-214"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e1bf-215">DLL</span><span class="sxs-lookup"><span data-stu-id="7e1bf-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e1bf-216"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e1bf-216"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e1bf-217">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e1bf-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e1bf-218">**Exibição de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="7e1bf-218">**CIM\_View**</span></span>](cim-view.md)
</dt> </dl>

 

