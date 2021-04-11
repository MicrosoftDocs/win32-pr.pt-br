---
description: A \_ classe WMI de associação DependentService do Win32 relaciona dois serviços base interdependentes.
ms.assetid: ba21fce3-f8f9-4886-b09d-a9e830376364
ms.tgt_platform: multiple
title: Classe Win32_DependentService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DependentService
- Win32_DependentService.TypeOfDependency
- Win32_DependentService.Antecedent
- Win32_DependentService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 047ec3411186f09f3d0e76da27158aa8ee91d4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089658"
---
# <a name="win32_dependentservice-class"></a><span data-ttu-id="64212-103">\_Classe Win32 DependentService</span><span class="sxs-lookup"><span data-stu-id="64212-103">Win32\_DependentService class</span></span>

<span data-ttu-id="64212-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ DependentService do Win32** relaciona dois serviços base interdependentes.</span><span class="sxs-lookup"><span data-stu-id="64212-104">The **Win32\_DependentService** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two interdependent base services.</span></span>

<span data-ttu-id="64212-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="64212-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="64212-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="64212-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="64212-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64212-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DependentService : CIM_ServiceServiceDependency
{
  uint16                TypeOfDependency;
  Win32_BaseService REF Antecedent;
  Win32_BaseService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="64212-108">Membros</span><span class="sxs-lookup"><span data-stu-id="64212-108">Members</span></span>

<span data-ttu-id="64212-109">A classe **Win32 \_ DependentService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="64212-109">The **Win32\_DependentService** class has these types of members:</span></span>

-   [<span data-ttu-id="64212-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="64212-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64212-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="64212-111">Properties</span></span>

<span data-ttu-id="64212-112">A classe **Win32 \_ DependentService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="64212-112">The **Win32\_DependentService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64212-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="64212-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64212-114">Tipo de dados: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="64212-114">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="64212-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64212-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64212-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="64212-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="64212-117">Um [**\_ BaseService Win32**](win32-baseservice.md) que representa o serviço base de acordo com a propriedade **dependent** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="64212-117">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service relied upon by the **Dependent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="64212-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="64212-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64212-119">Tipo de dados: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="64212-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="64212-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64212-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64212-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="64212-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="64212-122">Um [**\_ BaseService Win32**](win32-baseservice.md) que representa o serviço base que é dependente da propriedade **Antecedent** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="64212-122">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service that is dependent on the **Antecedent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="64212-123">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="64212-123">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64212-124">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="64212-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64212-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64212-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64212-126">Natureza da dependência entre serviços.</span><span class="sxs-lookup"><span data-stu-id="64212-126">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="64212-127">Essa propriedade indica que o serviço associado deve ter sido concluído, deve ser iniciado ou não deve ser iniciado para que o serviço funcione.</span><span class="sxs-lookup"><span data-stu-id="64212-127">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<span data-ttu-id="64212-128">Essa propriedade é herdada do [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md).</span><span class="sxs-lookup"><span data-stu-id="64212-128">This property is inherited from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="64212-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="64212-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="64212-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="64212-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="64212-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>O **serviço deve ter sido concluído** (2)</span><span class="sxs-lookup"><span data-stu-id="64212-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="64212-132">O serviço deve ter sido concluído.</span><span class="sxs-lookup"><span data-stu-id="64212-132">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="64212-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>O **serviço deve ser iniciado** (3)</span><span class="sxs-lookup"><span data-stu-id="64212-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="64212-134">O serviço deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="64212-134">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="64212-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>O **serviço não deve ser iniciado** (4)</span><span class="sxs-lookup"><span data-stu-id="64212-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="64212-136">O serviço não deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="64212-136">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64212-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="64212-137">Remarks</span></span>

<span data-ttu-id="64212-138">A classe **Win32 \_ DependentService** é derivada de [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md).</span><span class="sxs-lookup"><span data-stu-id="64212-138">The **Win32\_DependentService** class is derived from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64212-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64212-139">Requirements</span></span>



| <span data-ttu-id="64212-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="64212-140">Requirement</span></span> | <span data-ttu-id="64212-141">Valor</span><span class="sxs-lookup"><span data-stu-id="64212-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64212-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64212-142">Minimum supported client</span></span><br/> | <span data-ttu-id="64212-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64212-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64212-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64212-144">Minimum supported server</span></span><br/> | <span data-ttu-id="64212-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64212-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64212-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="64212-146">Namespace</span></span><br/>                | <span data-ttu-id="64212-147">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="64212-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64212-148">MOF</span><span class="sxs-lookup"><span data-stu-id="64212-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64212-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64212-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64212-150">DLL</span><span class="sxs-lookup"><span data-stu-id="64212-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64212-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64212-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64212-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="64212-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64212-153">**\_SERVICESERVICEDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="64212-153">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dt>

<span data-ttu-id="64212-154">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64212-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

