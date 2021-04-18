---
description: Desmonta o dispositivo PCI especificado para que ele possa ser atribuído.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Método DismountAssignableDevice da classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 53036cd09113430d1045c8e9eae7a8d782b35960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810353"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="a1e2a-103">Método DismountAssignableDevice da \_ classe AssignableDeviceService Msvm</span><span class="sxs-lookup"><span data-stu-id="a1e2a-103">DismountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="a1e2a-104">Desmonta o dispositivo PCI especificado para que ele possa ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-104">Dismounts the specified PCI device so that it can be assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1e2a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1e2a-105">Syntax</span></span>


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a1e2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1e2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e2a-107">*DismountSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a1e2a-107">*DismountSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e2a-108">Instância inserida de um objeto de dados de configuração que especifica o dispositivo PCI a ser desmontado.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-108">Embedded instance of a setting data object that specifies the PCI device to dismount.</span></span>

</dd> <dt>

<span data-ttu-id="a1e2a-109">*DismountedDeviceInstancePath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a1e2a-109">*DismountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e2a-110">Cadeia de caracteres que contém o caminho da instância do dispositivo para o dispositivo desmontado.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-110">String containing the device instance path to the dismounted device.</span></span>

</dd> <dt>

<span data-ttu-id="a1e2a-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a1e2a-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e2a-112">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="a1e2a-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e2a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1e2a-113">Return value</span></span>

<span data-ttu-id="a1e2a-114">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-114">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a1e2a-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a1e2a-128">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a1e2a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1e2a-129">Requirements</span></span>



| <span data-ttu-id="a1e2a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1e2a-130">Requirement</span></span> | <span data-ttu-id="a1e2a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a1e2a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e2a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1e2a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e2a-133">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="a1e2a-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a1e2a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1e2a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e2a-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a1e2a-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a1e2a-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1e2a-136">Namespace</span></span><br/>                | <span data-ttu-id="a1e2a-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a1e2a-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a1e2a-138">MOF</span><span class="sxs-lookup"><span data-stu-id="a1e2a-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1e2a-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1e2a-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1e2a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a1e2a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1e2a-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1e2a-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a1e2a-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1e2a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e2a-143">**Msvm \_ AssignableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="a1e2a-143">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




