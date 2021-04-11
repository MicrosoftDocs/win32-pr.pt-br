---
description: Cria uma nova instância de máquina virtual.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Método DefineSystem da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170675"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f46ee-103">Método DefineSystem da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="f46ee-103">DefineSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f46ee-104">Cria uma nova instância de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f46ee-104">Creates a new virtual machine instance.</span></span> <span data-ttu-id="f46ee-105">As propriedades que não forem especificadas serão preenchidas com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="f46ee-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f46ee-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f46ee-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f46ee-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f46ee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f46ee-108">*SystemSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f46ee-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46ee-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f46ee-109">Type: **string**</span></span>

<span data-ttu-id="f46ee-110">Uma instância inserida da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que é usada para definir os atributos da máquina virtual a ser criada.</span><span class="sxs-lookup"><span data-stu-id="f46ee-110">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is used to define the attributes of the virtual machine to be created.</span></span> <span data-ttu-id="f46ee-111">Este parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="f46ee-111">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="f46ee-112">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f46ee-112">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46ee-113">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f46ee-113">Type: **string\[\]**</span></span>

<span data-ttu-id="f46ee-114">Várias instâncias inseridas da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (ou classes derivadas).</span><span class="sxs-lookup"><span data-stu-id="f46ee-114">A number of embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class (or derived classes thereof).</span></span> <span data-ttu-id="f46ee-115">Juntas, essas instâncias descrevem os recursos virtuais da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f46ee-115">Together these instances describe the virtual resources of the virtual machine.</span></span> <span data-ttu-id="f46ee-116">Um conjunto padrão de dispositivos será criado para a máquina virtual, independentemente de esse parâmetro ser definido.</span><span class="sxs-lookup"><span data-stu-id="f46ee-116">A default set of devices will be created for the virtual machine regardless of whether this parameter is set.</span></span> <span data-ttu-id="f46ee-117">Por exemplo, o processador e a memória são criados e configurados automaticamente com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="f46ee-117">For example, processor and memory are automatically created and configured with default values.</span></span>

</dd> <dt>

<span data-ttu-id="f46ee-118">*ReferenceConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f46ee-118">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46ee-119">Tipo: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="f46ee-119">Type: **CIM\_VirtualSystemSettingData**</span></span>

<span data-ttu-id="f46ee-120">Uma referência a uma instância da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que é o objeto de nível superior de uma configuração de máquina virtual de referência.</span><span class="sxs-lookup"><span data-stu-id="f46ee-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is the top level object of a reference virtual machine configuration.</span></span> <span data-ttu-id="f46ee-121">A configuração de referência será usada para complementar a configuração da nova máquina virtual se os parâmetros *SystemSettings* e *ResourceSettings* não fornecerem as respectivas informações.</span><span class="sxs-lookup"><span data-stu-id="f46ee-121">The reference configuration is used to complement the configuration of the new virtual machine if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="f46ee-122">*ResultingSystem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f46ee-122">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f46ee-123">Tipo: **\_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="f46ee-123">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="f46ee-124">Uma referência a uma instância da classe [**de \_ ComputerSystem do CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual recém-criada.</span><span class="sxs-lookup"><span data-stu-id="f46ee-124">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly created virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="f46ee-125">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f46ee-125">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f46ee-126">Tipo: **CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="f46ee-126">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="f46ee-127">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f46ee-127">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f46ee-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f46ee-128">Return value</span></span>

<span data-ttu-id="f46ee-129">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f46ee-129">Type: **uint32**</span></span>

<span data-ttu-id="f46ee-130">Se esse método for executado de forma síncrona, ele retornará 0 se tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="f46ee-130">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="f46ee-131">Se esse método for executado de forma assíncrona, ele retornará 4096 e o parâmetro de saída do *trabalho* poderá ser usado para acompanhar o progresso da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f46ee-131">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="f46ee-132">Qualquer outro valor de retorno indica um erro.</span><span class="sxs-lookup"><span data-stu-id="f46ee-132">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="f46ee-133">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="f46ee-133">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f46ee-134">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="f46ee-134">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f46ee-135">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="f46ee-135">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f46ee-136">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="f46ee-136">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f46ee-137">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="f46ee-137">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f46ee-138">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f46ee-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f46ee-139">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f46ee-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f46ee-140">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f46ee-140">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f46ee-141">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f46ee-141">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f46ee-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="f46ee-142">Remarks</span></span>

<span data-ttu-id="f46ee-143">O acesso à classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="f46ee-143">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f46ee-144">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f46ee-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f46ee-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f46ee-145">Requirements</span></span>



| <span data-ttu-id="f46ee-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f46ee-146">Requirement</span></span> | <span data-ttu-id="f46ee-147">Valor</span><span class="sxs-lookup"><span data-stu-id="f46ee-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f46ee-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f46ee-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f46ee-149">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f46ee-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f46ee-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f46ee-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f46ee-151">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f46ee-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f46ee-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="f46ee-152">Namespace</span></span><br/>                | <span data-ttu-id="f46ee-153">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f46ee-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f46ee-154">MOF</span><span class="sxs-lookup"><span data-stu-id="f46ee-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f46ee-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f46ee-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f46ee-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f46ee-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f46ee-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f46ee-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f46ee-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="f46ee-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f46ee-159">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="f46ee-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

