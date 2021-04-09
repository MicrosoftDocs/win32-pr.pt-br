---
description: A \_ classe CIM HostedBootService associa um sistema de hospedagem e um serviço de inicialização. Como essa relação é subclasse de CIM \_ HostedService, ela herda o esquema de escopo/nomenclatura definido para o serviço, em que um serviço é adiado para seu sistema de hospedagem.
ms.assetid: 91621288-a231-4423-94df-7601bdf2ebe1
ms.tgt_platform: multiple
title: Classe CIM_HostedBootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootService
- CIM_HostedBootService.Antecedent
- CIM_HostedBootService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12baa364653feda1400ad15d658e6739859b2521
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089281"
---
# <a name="cim_hostedbootservice-class"></a><span data-ttu-id="6492a-104">\_Classe CIM HostedBootService</span><span class="sxs-lookup"><span data-stu-id="6492a-104">CIM\_HostedBootService class</span></span>

<span data-ttu-id="6492a-105">A classe **CIM \_ HostedBootService** associa um sistema de hospedagem e um serviço de inicialização.</span><span class="sxs-lookup"><span data-stu-id="6492a-105">The **CIM\_HostedBootService** class associates a hosting system and a boot service.</span></span> <span data-ttu-id="6492a-106">Como essa relação é subclasse de [**CIM \_ HostedService**](cim-hostedservice.md), ela herda o esquema de escopo/nomenclatura definido para o serviço, em que um serviço é adiado para seu sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="6492a-106">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6492a-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6492a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6492a-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6492a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6492a-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6492a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6492a-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6492a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6492a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6492a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6DAE7092-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootService : CIM_HostedService
{
  CIM_System      REF Antecedent;
  CIM_BootService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6492a-112">Membros</span><span class="sxs-lookup"><span data-stu-id="6492a-112">Members</span></span>

<span data-ttu-id="6492a-113">A classe **CIM \_ HostedBootService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6492a-113">The **CIM\_HostedBootService** class has these types of members:</span></span>

-   [<span data-ttu-id="6492a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6492a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6492a-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6492a-115">Properties</span></span>

<span data-ttu-id="6492a-116">A classe **CIM \_ HostedBootService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6492a-116">The **CIM\_HostedBootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6492a-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="6492a-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6492a-118">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="6492a-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="6492a-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6492a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6492a-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)</span><span class="sxs-lookup"><span data-stu-id="6492a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="6492a-121">Um [**\_ sistema CIM**](cim-system.md) que descreve o sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="6492a-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="6492a-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="6492a-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6492a-123">Tipo de dados: **CIM \_ DS**</span><span class="sxs-lookup"><span data-stu-id="6492a-123">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="6492a-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6492a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6492a-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="6492a-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6492a-126">Um [**\_ DS CIM**](cim-bootservice.md) que descreve o serviço de inicialização hospedado no sistema.</span><span class="sxs-lookup"><span data-stu-id="6492a-126">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6492a-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="6492a-127">Remarks</span></span>

<span data-ttu-id="6492a-128">A classe **CIM \_ HostedBootService** é derivada de [**CIM \_ HostedService**](cim-hostedservice.md).</span><span class="sxs-lookup"><span data-stu-id="6492a-128">The **CIM\_HostedBootService** class is derived from [**CIM\_HostedService**](cim-hostedservice.md).</span></span>

<span data-ttu-id="6492a-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="6492a-129">WMI does not implement this class.</span></span>

<span data-ttu-id="6492a-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6492a-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6492a-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6492a-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6492a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6492a-132">Requirements</span></span>



| <span data-ttu-id="6492a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6492a-133">Requirement</span></span> | <span data-ttu-id="6492a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="6492a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6492a-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6492a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6492a-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6492a-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6492a-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6492a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6492a-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6492a-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6492a-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="6492a-139">Namespace</span></span><br/>                | <span data-ttu-id="6492a-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6492a-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6492a-141">MOF</span><span class="sxs-lookup"><span data-stu-id="6492a-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6492a-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6492a-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6492a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6492a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6492a-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6492a-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6492a-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="6492a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6492a-146">**HostedService do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="6492a-146">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> </dl>

 

