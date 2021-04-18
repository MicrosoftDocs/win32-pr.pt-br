---
description: Uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado.
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Classe Msvm_DeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9551d4409edfdfca18b66e3a3b86d6adcb28b19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757147"
---
# <a name="msvm_devicesapimplementation-class"></a><span data-ttu-id="3ebee-103">\_Classe Msvm DeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="3ebee-103">Msvm\_DeviceSAPImplementation class</span></span>

<span data-ttu-id="3ebee-104">Uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado.</span><span class="sxs-lookup"><span data-stu-id="3ebee-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="3ebee-105">A cardinalidade dessa associação é muitos-para-muitos.</span><span class="sxs-lookup"><span data-stu-id="3ebee-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="3ebee-106">Um SAP pode ser fornecido por mais de um dispositivo lógico, operando em conjunto.</span><span class="sxs-lookup"><span data-stu-id="3ebee-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="3ebee-107">Qualquer dispositivo pode fornecer mais de um SAP.</span><span class="sxs-lookup"><span data-stu-id="3ebee-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="3ebee-108">Quando muitos dispositivos lógicos são associados a um único SAP, supõe-se que esses elementos operam em conjunto para fornecer o ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="3ebee-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="3ebee-109">Se diferentes implementações de um SAP existirem, cada uma dessas implementações resultaria em instanciações individuais do objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="3ebee-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="3ebee-110">Essas instanciações individuais teriam associações para as implementações exclusivas.</span><span class="sxs-lookup"><span data-stu-id="3ebee-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="3ebee-111">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3ebee-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ebee-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ebee-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3ebee-113">Membros</span><span class="sxs-lookup"><span data-stu-id="3ebee-113">Members</span></span>

<span data-ttu-id="3ebee-114">A classe **Msvm \_ DeviceSAPImplementation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3ebee-114">The **Msvm\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="3ebee-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ebee-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ebee-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ebee-116">Properties</span></span>

<span data-ttu-id="3ebee-117">A classe **Msvm \_ DeviceSAPImplementation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3ebee-117">The **Msvm\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ebee-118">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="3ebee-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebee-119">Tipo de dados: **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="3ebee-119">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="3ebee-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ebee-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ebee-121">O dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3ebee-121">The logical device.</span></span> <span data-ttu-id="3ebee-122">Essa propriedade é herdada do [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="3ebee-122">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> <dt>

<span data-ttu-id="3ebee-123">**Depende**</span><span class="sxs-lookup"><span data-stu-id="3ebee-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebee-124">Tipo de dados: **[ **CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span><span class="sxs-lookup"><span data-stu-id="3ebee-124">Data type: **[**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span></span>
</dt> <dt>

<span data-ttu-id="3ebee-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ebee-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ebee-126">O ponto de acesso ao serviço implementado usando o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3ebee-126">The service access point implemented using the logical device.</span></span> <span data-ttu-id="3ebee-127">Essa propriedade é herdada do [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="3ebee-127">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ebee-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ebee-128">Remarks</span></span>

<span data-ttu-id="3ebee-129">O acesso à classe **Msvm \_ DeviceSAPImplementation** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="3ebee-129">Access to the **Msvm\_DeviceSAPImplementation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3ebee-130">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3ebee-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="3ebee-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ebee-131">Examples</span></span>

<span data-ttu-id="3ebee-132">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3ebee-132">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ebee-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ebee-133">Requirements</span></span>



| <span data-ttu-id="3ebee-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ebee-134">Requirement</span></span> | <span data-ttu-id="3ebee-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3ebee-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ebee-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ebee-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3ebee-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3ebee-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3ebee-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ebee-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3ebee-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3ebee-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ebee-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ebee-140">Namespace</span></span><br/>                | <span data-ttu-id="3ebee-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3ebee-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3ebee-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3ebee-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ebee-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ebee-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ebee-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3ebee-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ebee-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ebee-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ebee-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ebee-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ebee-147">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3ebee-147">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dt>

[<span data-ttu-id="3ebee-148">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3ebee-148">**CIM\_DeviceSAPImplementation**</span></span>](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

