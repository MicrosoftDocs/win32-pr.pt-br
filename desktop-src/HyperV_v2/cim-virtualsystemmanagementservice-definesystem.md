---
description: Define um sistema virtual.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Método DefineSystem da classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785459"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="05ead-103">Método DefineSystem da \_ classe VIRTUALSYSTEMMANAGEMENTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="05ead-103">DefineSystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="05ead-104">Define um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="05ead-104">Defines a virtual system.</span></span>

<span data-ttu-id="05ead-105">A entrada que não está completamente especificada pode ser preenchida com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="05ead-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="05ead-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05ead-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="05ead-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05ead-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05ead-108">*SystemSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="05ead-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05ead-109">Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que é usada para definir os atributos do sistema virtual a ser criado.</span><span class="sxs-lookup"><span data-stu-id="05ead-109">String containing an embedded instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to define attributes of the virtual system to be created.</span></span>

</dd> <dt>

<span data-ttu-id="05ead-110">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="05ead-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05ead-111">Matriz de cadeias de caracteres que contém uma instância incorporada da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que descreve os aspectos virtuais de um recurso virtual a ser criado no escopo do novo sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="05ead-111">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be created in the scope of the new virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="05ead-112">*ReferenceConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="05ead-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05ead-113">Referência a uma instância de objeto [**CIM \_ VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) que é o objeto de nível superior de uma configuração de sistema virtual de referência.</span><span class="sxs-lookup"><span data-stu-id="05ead-113">Reference to a [**CIM\_VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) object instance that is the top level object of a reference virtual system configuration.</span></span> <span data-ttu-id="05ead-114">A configuração de referência será usada para complementar a configuração do novo sistema virtual se os parâmetros *SystemSettings* e *ResourceSettings* não fornecerem as respectivas informações.</span><span class="sxs-lookup"><span data-stu-id="05ead-114">The reference configuration is used to complement the configuration of the new virtual system if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="05ead-115">*ResultingSystem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="05ead-115">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05ead-116">Se um sistema de computador virtual for definido com êxito, uma referência a uma instância da classe [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa o sistema de computador virtual recém-definido é retornado.</span><span class="sxs-lookup"><span data-stu-id="05ead-116">If a virtual computer system is successfully defined, a reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the newly defined virtual computer system is returned.</span></span>

</dd> <dt>

<span data-ttu-id="05ead-117">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="05ead-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05ead-118">Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="05ead-118">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="05ead-119">Nesse caso, a instância da classe [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa o novo sistema virtual é apresentada por meio [**de \_ AffectedJobElement de CIM**](cim-affectedjobelement.md) de associação com a propriedade **afetoed** fazendo referência à nova instância da classe **CIM \_ ComputerSystem** e da propriedade **ElementEffects** definida como 5 (Create).</span><span class="sxs-lookup"><span data-stu-id="05ead-119">In this case, the instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the new virtual system is presented via association [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) with the property **AffectedElement** referring to the new instance of class **CIM\_ComputerSystem** and property **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05ead-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05ead-120">Return value</span></span>

<span data-ttu-id="05ead-121">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="05ead-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="05ead-122">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="05ead-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="05ead-123">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="05ead-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="05ead-124">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="05ead-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="05ead-125">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="05ead-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="05ead-126">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="05ead-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="05ead-127">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="05ead-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="05ead-128">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="05ead-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="05ead-129">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="05ead-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="05ead-130">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="05ead-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="05ead-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05ead-131">Requirements</span></span>



| <span data-ttu-id="05ead-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="05ead-132">Requirement</span></span> | <span data-ttu-id="05ead-133">Valor</span><span class="sxs-lookup"><span data-stu-id="05ead-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05ead-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05ead-134">Minimum supported client</span></span><br/> | <span data-ttu-id="05ead-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="05ead-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="05ead-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05ead-136">Minimum supported server</span></span><br/> | <span data-ttu-id="05ead-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="05ead-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="05ead-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="05ead-138">Namespace</span></span><br/>                | <span data-ttu-id="05ead-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="05ead-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="05ead-140">MOF</span><span class="sxs-lookup"><span data-stu-id="05ead-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05ead-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05ead-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05ead-142">DLL</span><span class="sxs-lookup"><span data-stu-id="05ead-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05ead-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05ead-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="05ead-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="05ead-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ead-145">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="05ead-145">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




