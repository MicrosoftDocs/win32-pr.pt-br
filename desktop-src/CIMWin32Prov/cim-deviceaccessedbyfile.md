---
description: A \_ classe de associação CIM DeviceAccessedByFile especifica o dispositivo lógico acessado usando a classe de dispositivo CIM referenciada \_ .
ms.assetid: 8ba44f40-8b84-4f5c-b719-aded10877654
ms.tgt_platform: multiple
title: Classe CIM_DeviceAccessedByFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceAccessedByFile
- CIM_DeviceAccessedByFile.Dependent
- CIM_DeviceAccessedByFile.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cf84d2e7943dfe6da88f81ef6963190553f028e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826464"
---
# <a name="cim_deviceaccessedbyfile-class"></a><span data-ttu-id="08895-103">\_Classe CIM DeviceAccessedByFile</span><span class="sxs-lookup"><span data-stu-id="08895-103">CIM\_DeviceAccessedByFile class</span></span>

<span data-ttu-id="08895-104">A classe de associação **CIM \_ DeviceAccessedByFile** especifica o dispositivo lógico acessado usando a classe de [**\_ dispositivo CIM**](cim-devicefile.md) referenciada.</span><span class="sxs-lookup"><span data-stu-id="08895-104">The **CIM\_DeviceAccessedByFile** association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08895-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="08895-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="08895-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="08895-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="08895-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="08895-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="08895-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="08895-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="08895-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08895-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{05D1FFF2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceAccessedByFile : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_DeviceFile    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="08895-110">Membros</span><span class="sxs-lookup"><span data-stu-id="08895-110">Members</span></span>

<span data-ttu-id="08895-111">A classe **CIM \_ DeviceAccessedByFile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08895-111">The **CIM\_DeviceAccessedByFile** class has these types of members:</span></span>

-   [<span data-ttu-id="08895-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08895-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08895-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08895-113">Properties</span></span>

<span data-ttu-id="08895-114">A classe **CIM \_ DeviceAccessedByFile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="08895-114">The **CIM\_DeviceAccessedByFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08895-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="08895-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08895-116">Tipo de dados **: \_ dispositivo CIM**</span><span class="sxs-lookup"><span data-stu-id="08895-116">Data type: **CIM\_DeviceFile**</span></span>
</dt> <dt>

<span data-ttu-id="08895-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08895-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08895-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="08895-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="08895-119">Um [**\_ dispositivo CIM**](cim-devicefile.md) que descreve o arquivo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08895-119">A [**CIM\_DeviceFile**](cim-devicefile.md) that describes the device file.</span></span>

</dd> <dt>

<span data-ttu-id="08895-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="08895-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08895-121">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="08895-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="08895-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08895-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08895-123">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="08895-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="08895-124">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo que é acessado usando o arquivo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08895-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device that is accessed using the device file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08895-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="08895-125">Remarks</span></span>

<span data-ttu-id="08895-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="08895-126">WMI does not implement this class.</span></span>

<span data-ttu-id="08895-127">A classe **CIM \_ DeviceAccessedByFile** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="08895-127">The **CIM\_DeviceAccessedByFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="08895-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="08895-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="08895-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="08895-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="08895-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08895-130">Requirements</span></span>



| <span data-ttu-id="08895-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="08895-131">Requirement</span></span> | <span data-ttu-id="08895-132">Valor</span><span class="sxs-lookup"><span data-stu-id="08895-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08895-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08895-133">Minimum supported client</span></span><br/> | <span data-ttu-id="08895-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08895-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08895-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08895-135">Minimum supported server</span></span><br/> | <span data-ttu-id="08895-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08895-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08895-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="08895-137">Namespace</span></span><br/>                | <span data-ttu-id="08895-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="08895-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08895-139">MOF</span><span class="sxs-lookup"><span data-stu-id="08895-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08895-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08895-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08895-141">DLL</span><span class="sxs-lookup"><span data-stu-id="08895-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08895-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08895-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08895-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="08895-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08895-144">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="08895-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

