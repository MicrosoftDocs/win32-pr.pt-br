---
description: A \_ associação CIM SystemDevice representa uma relação explícita na qual os dispositivos lógicos podem ser agregados por um sistema.
ms.assetid: df624a9f-0c10-44a3-8075-908e5e481e3c
ms.tgt_platform: multiple
title: Classe CIM_SystemDevice (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.PartComponent
- CIM_SystemDevice.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbff9a0ead8790de9ab323509c8b2f1392e6ed6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748266"
---
# <a name="cim_systemdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="dac6f-103">Classe CIM_SystemDevice (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="dac6f-103">CIM_SystemDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="dac6f-104">A associação **CIM \_ SystemDevice** representa uma relação explícita na qual os dispositivos lógicos podem ser agregados por um sistema.</span><span class="sxs-lookup"><span data-stu-id="dac6f-104">The **CIM\_SystemDevice** association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dac6f-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="dac6f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dac6f-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dac6f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dac6f-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="dac6f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dac6f-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="dac6f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac6f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dac6f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4B2C30D7-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_LogicalDevice REF PartComponent;
  CIM_System        REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="dac6f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="dac6f-110">Members</span></span>

<span data-ttu-id="dac6f-111">A classe **CIM \_ SystemDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dac6f-111">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="dac6f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dac6f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dac6f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dac6f-113">Properties</span></span>

<span data-ttu-id="dac6f-114">A classe **CIM \_ SystemDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dac6f-114">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dac6f-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="dac6f-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac6f-116">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="dac6f-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="dac6f-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dac6f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dac6f-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="dac6f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="dac6f-119">Um [**\_ sistema CIM**](cim-system.md) que descreve o sistema pai na associação.</span><span class="sxs-lookup"><span data-stu-id="dac6f-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="dac6f-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="dac6f-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dac6f-121">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="dac6f-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="dac6f-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dac6f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dac6f-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dac6f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dac6f-124">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico que é um componente de um sistema.</span><span class="sxs-lookup"><span data-stu-id="dac6f-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dac6f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="dac6f-125">Remarks</span></span>

<span data-ttu-id="dac6f-126">A classe **CIM \_ SystemDevice** é derivada de [**\_ Systemcomponent CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="dac6f-126">The **CIM\_SystemDevice** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="dac6f-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="dac6f-127">WMI does not implement this class.</span></span> <span data-ttu-id="dac6f-128">Para classes WMI derivadas do **CIM \_ SystemDevice**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="dac6f-128">For WMI classes derived from **CIM\_SystemDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="dac6f-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="dac6f-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dac6f-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="dac6f-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac6f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dac6f-131">Requirements</span></span>



| <span data-ttu-id="dac6f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac6f-132">Requirement</span></span> | <span data-ttu-id="dac6f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="dac6f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dac6f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dac6f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dac6f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dac6f-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dac6f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dac6f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dac6f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dac6f-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dac6f-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="dac6f-138">Namespace</span></span><br/>                | <span data-ttu-id="dac6f-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dac6f-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dac6f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="dac6f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dac6f-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dac6f-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dac6f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="dac6f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dac6f-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dac6f-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dac6f-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="dac6f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac6f-145">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="dac6f-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

