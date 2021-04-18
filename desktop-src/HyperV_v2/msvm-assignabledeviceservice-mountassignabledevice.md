---
description: Monta o dispositivo PCI especificado para que ele possa ser usado pelo sistema de computador host.
ms.assetid: 2a07174e-c221-4c04-81b8-5968aa67e235
title: Método MountAssignableDevice da classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.MountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: df5f8a337fbf4baf47a4f695322944ed0b97e82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766898"
---
# <a name="mountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="68df3-103">Método MountAssignableDevice da \_ classe AssignableDeviceService Msvm</span><span class="sxs-lookup"><span data-stu-id="68df3-103">MountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="68df3-104">Monta o dispositivo PCI especificado para que ele possa ser usado pelo sistema de computador host.</span><span class="sxs-lookup"><span data-stu-id="68df3-104">Mounts the specified PCI device so that it can be used by the host computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="68df3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68df3-105">Syntax</span></span>


```mof
uint32 MountAssignableDevice(
  [in]  string              DeviceInstancePath,
  [in]  string              DeviceLocationPath,
  [out] string              MountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="68df3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68df3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68df3-107">*DeviceInstancePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68df3-107">*DeviceInstancePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68df3-108">Cadeia de caracteres que contém o caminho da instância do dispositivo para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68df3-108">String containing the device instance path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="68df3-109">*DeviceLocationPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68df3-109">*DeviceLocationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68df3-110">Cadeia de caracteres que contém o caminho do local do dispositivo para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68df3-110">String containing the device location path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="68df3-111">*MountedDeviceInstancePath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="68df3-111">*MountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68df3-112">Cadeia de caracteres que contém o caminho da instância do dispositivo para o dispositivo montado.</span><span class="sxs-lookup"><span data-stu-id="68df3-112">String containing the device instance path to the mounted device.</span></span>

</dd> <dt>

<span data-ttu-id="68df3-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="68df3-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68df3-114">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="68df3-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68df3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68df3-115">Return value</span></span>

<span data-ttu-id="68df3-116">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="68df3-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="68df3-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="68df3-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="68df3-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="68df3-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="68df3-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="68df3-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="68df3-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="68df3-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="68df3-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="68df3-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="68df3-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="68df3-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="68df3-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="68df3-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="68df3-130">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="68df3-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="68df3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68df3-131">Requirements</span></span>



| <span data-ttu-id="68df3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="68df3-132">Requirement</span></span> | <span data-ttu-id="68df3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="68df3-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68df3-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68df3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="68df3-135">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="68df3-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="68df3-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68df3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="68df3-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="68df3-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="68df3-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="68df3-138">Namespace</span></span><br/>                | <span data-ttu-id="68df3-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="68df3-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="68df3-140">MOF</span><span class="sxs-lookup"><span data-stu-id="68df3-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68df3-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68df3-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="68df3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="68df3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68df3-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68df3-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="68df3-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="68df3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68df3-145">**Msvm \_ AssignableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="68df3-145">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




