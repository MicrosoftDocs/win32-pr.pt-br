---
description: A \_ classe CIM ServiceServiceDependency representa uma associação entre dois serviços.
ms.assetid: 0fb43fb3-2c05-4762-b339-2dcc090ed38d
ms.tgt_platform: multiple
title: Classe CIM_ServiceServiceDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceServiceDependency
- CIM_ServiceServiceDependency.Dependent
- CIM_ServiceServiceDependency.Antecedent
- CIM_ServiceServiceDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fdc8ea1a3324395e5230ca6d47487b61c8c02ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755846"
---
# <a name="cim_serviceservicedependency-class"></a><span data-ttu-id="703ca-103">\_Classe CIM ServiceServiceDependency</span><span class="sxs-lookup"><span data-stu-id="703ca-103">CIM\_ServiceServiceDependency class</span></span>

<span data-ttu-id="703ca-104">A classe **CIM \_ ServiceServiceDependency** representa uma associação entre dois serviços.</span><span class="sxs-lookup"><span data-stu-id="703ca-104">The **CIM\_ServiceServiceDependency** class represents an association between two services.</span></span> <span data-ttu-id="703ca-105">O serviço associado deve estar presente, deve ter sido concluído ou deve estar ausente para que o outro serviço funcione.</span><span class="sxs-lookup"><span data-stu-id="703ca-105">The associated service must be present, must have completed, or must be absent for the other service to function.</span></span> <span data-ttu-id="703ca-106">Por exemplo, os serviços de inicialização podem ser dependentes de BIOS, disco e serviços de inicialização subjacentes.</span><span class="sxs-lookup"><span data-stu-id="703ca-106">For example, boot services can be dependent on underlying BIOS, disk, and initialization services.</span></span> <span data-ttu-id="703ca-107">Para os serviços de inicialização, o serviço de inicialização depende da conclusão dos serviços de inicialização.</span><span class="sxs-lookup"><span data-stu-id="703ca-107">For initialization services, the boot service is dependent on the initialization services completing.</span></span> <span data-ttu-id="703ca-108">Para serviços de disco, os serviços de inicialização podem realmente usar os SAPs deste serviço.</span><span class="sxs-lookup"><span data-stu-id="703ca-108">For disk services, boot services can actually use the SAPs of this service.</span></span> <span data-ttu-id="703ca-109">Essa dependência de uso é modelada na associação [**\_ ServiceSAPDependency do CIM**](cim-servicesapdependency.md) .</span><span class="sxs-lookup"><span data-stu-id="703ca-109">This usage dependency is modeled on the [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="703ca-110">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="703ca-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="703ca-111">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="703ca-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="703ca-112">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="703ca-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="703ca-113">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="703ca-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="703ca-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="703ca-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ServiceServiceDependency : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_Service REF Antecedent;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="703ca-115">Membros</span><span class="sxs-lookup"><span data-stu-id="703ca-115">Members</span></span>

<span data-ttu-id="703ca-116">A classe **CIM \_ ServiceServiceDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="703ca-116">The **CIM\_ServiceServiceDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="703ca-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="703ca-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="703ca-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="703ca-118">Properties</span></span>

<span data-ttu-id="703ca-119">A classe **CIM \_ ServiceServiceDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="703ca-119">The **CIM\_ServiceServiceDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="703ca-120">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="703ca-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="703ca-121">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="703ca-121">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="703ca-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="703ca-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="703ca-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="703ca-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="703ca-124">Um [**\_ serviço CIM**](cim-service.md) que descreve o serviço necessário.</span><span class="sxs-lookup"><span data-stu-id="703ca-124">A [**CIM\_Service**](cim-service.md) that describes the required service.</span></span>

</dd> <dt>

<span data-ttu-id="703ca-125">**Depende**</span><span class="sxs-lookup"><span data-stu-id="703ca-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="703ca-126">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="703ca-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="703ca-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="703ca-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="703ca-128">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="703ca-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="703ca-129">Um [**\_ serviço CIM**](cim-service.md) que descreve o serviço que é dependente de um serviço subjacente.</span><span class="sxs-lookup"><span data-stu-id="703ca-129">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying service.</span></span>

</dd> <dt>

<span data-ttu-id="703ca-130">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="703ca-130">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="703ca-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="703ca-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="703ca-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="703ca-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="703ca-133">Natureza da dependência entre serviços.</span><span class="sxs-lookup"><span data-stu-id="703ca-133">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="703ca-134">Essa propriedade indica que o serviço associado deve ter sido concluído, deve ser iniciado ou não deve ser iniciado para que o serviço funcione.</span><span class="sxs-lookup"><span data-stu-id="703ca-134">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="703ca-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="703ca-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="703ca-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="703ca-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="703ca-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>O **serviço deve ter sido concluído** (2)</span><span class="sxs-lookup"><span data-stu-id="703ca-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="703ca-138">O serviço deve ter sido concluído.</span><span class="sxs-lookup"><span data-stu-id="703ca-138">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="703ca-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>O **serviço deve ser iniciado** (3)</span><span class="sxs-lookup"><span data-stu-id="703ca-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="703ca-140">O serviço deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="703ca-140">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="703ca-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>O **serviço não deve ser iniciado** (4)</span><span class="sxs-lookup"><span data-stu-id="703ca-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="703ca-142">O serviço não deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="703ca-142">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="703ca-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="703ca-143">Remarks</span></span>

<span data-ttu-id="703ca-144">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="703ca-144">WMI does not implement this class.</span></span> <span data-ttu-id="703ca-145">Para classes WMI derivadas do **CIM \_ ServiceServiceDependency**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="703ca-145">For WMI classes derived from **CIM\_ServiceServiceDependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="703ca-146">A classe **CIM \_ ServiceServiceDependency** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="703ca-146">The **CIM\_ServiceServiceDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="703ca-147">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="703ca-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="703ca-148">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="703ca-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="703ca-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="703ca-149">Requirements</span></span>



| <span data-ttu-id="703ca-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="703ca-150">Requirement</span></span> | <span data-ttu-id="703ca-151">Valor</span><span class="sxs-lookup"><span data-stu-id="703ca-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="703ca-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="703ca-152">Minimum supported client</span></span><br/> | <span data-ttu-id="703ca-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="703ca-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="703ca-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="703ca-154">Minimum supported server</span></span><br/> | <span data-ttu-id="703ca-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="703ca-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="703ca-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="703ca-156">Namespace</span></span><br/>                | <span data-ttu-id="703ca-157">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="703ca-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="703ca-158">MOF</span><span class="sxs-lookup"><span data-stu-id="703ca-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="703ca-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="703ca-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="703ca-160">DLL</span><span class="sxs-lookup"><span data-stu-id="703ca-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="703ca-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="703ca-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="703ca-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="703ca-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="703ca-163">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="703ca-163">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

