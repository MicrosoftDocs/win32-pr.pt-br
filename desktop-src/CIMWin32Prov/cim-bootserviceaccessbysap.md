---
description: A \_ classe CIM BootServiceAccessBySAP associa um serviço de inicialização e seus pontos de acesso.
ms.assetid: 993469dd-fb9c-4d21-99e0-03c4b19eb7fd
ms.tgt_platform: multiple
title: Classe CIM_BootServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootServiceAccessBySAP
- CIM_BootServiceAccessBySAP.Dependent
- CIM_BootServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90548be52defbcf3419d6c7defc21395da5cfbfe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646429"
---
# <a name="cim_bootserviceaccessbysap-class"></a><span data-ttu-id="d29c0-103">\_Classe CIM BootServiceAccessBySAP</span><span class="sxs-lookup"><span data-stu-id="d29c0-103">CIM\_BootServiceAccessBySAP class</span></span>

<span data-ttu-id="d29c0-104">A classe **CIM \_ BootServiceAccessBySAP** associa um serviço de inicialização e seus pontos de acesso.</span><span class="sxs-lookup"><span data-stu-id="d29c0-104">The **CIM\_BootServiceAccessBySAP** class associates a boot service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d29c0-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d29c0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d29c0-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d29c0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d29c0-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d29c0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d29c0-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d29c0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d29c0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d29c0-109">Syntax</span></span>

``` syntax
[UUID("{6EDF1DD2-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_BootSAP     REF Dependent;
  CIM_BootService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d29c0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d29c0-110">Members</span></span>

<span data-ttu-id="d29c0-111">A classe **CIM \_ BootServiceAccessBySAP** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d29c0-111">The **CIM\_BootServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="d29c0-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d29c0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d29c0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d29c0-113">Properties</span></span>

<span data-ttu-id="d29c0-114">A classe **CIM \_ BootServiceAccessBySAP** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d29c0-114">The **CIM\_BootServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d29c0-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d29c0-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d29c0-116">Tipo de dados: **CIM \_ DS**</span><span class="sxs-lookup"><span data-stu-id="d29c0-116">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="d29c0-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d29c0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d29c0-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d29c0-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d29c0-119">Um [**\_ DS CIM**](cim-bootservice.md) que descreve o serviço de inicialização.</span><span class="sxs-lookup"><span data-stu-id="d29c0-119">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service.</span></span>

</dd> <dt>

<span data-ttu-id="d29c0-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d29c0-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d29c0-121">Tipo de dados: **CIM \_ BootSAP**</span><span class="sxs-lookup"><span data-stu-id="d29c0-121">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="d29c0-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d29c0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d29c0-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="d29c0-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d29c0-124">Um [**\_ BootSAP CIM**](cim-bootsap.md) que descreve um ponto de acesso para o serviço de inicialização.</span><span class="sxs-lookup"><span data-stu-id="d29c0-124">A [**CIM\_BootSAP**](cim-bootsap.md) that describes an access point for the boot service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d29c0-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="d29c0-125">Remarks</span></span>

<span data-ttu-id="d29c0-126">A classe **CIM \_ BootServiceAccessBySAP** é derivada de [**\_ ServiceAccessBySAP CIM**](cim-serviceaccessbysap.md).</span><span class="sxs-lookup"><span data-stu-id="d29c0-126">The **CIM\_BootServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="d29c0-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d29c0-127">WMI does not implement this class.</span></span>

<span data-ttu-id="d29c0-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d29c0-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d29c0-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d29c0-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d29c0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d29c0-130">Requirements</span></span>



| <span data-ttu-id="d29c0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d29c0-131">Requirement</span></span> | <span data-ttu-id="d29c0-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d29c0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d29c0-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d29c0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d29c0-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d29c0-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d29c0-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d29c0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d29c0-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d29c0-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d29c0-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d29c0-137">Namespace</span></span><br/>                | <span data-ttu-id="d29c0-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d29c0-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d29c0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d29c0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d29c0-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d29c0-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d29c0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d29c0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d29c0-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d29c0-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d29c0-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="d29c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d29c0-144">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="d29c0-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

