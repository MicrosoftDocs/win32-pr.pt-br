---
description: Cria um arquivo de disco rígido virtual.
ms.assetid: 6c136000-1df2-4456-833c-094671408338
title: Método CreateVirtualHardDisk da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b80a309274eb51ad7aff768898a9c3bd211f37cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759247"
---
# <a name="createvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="ef2a8-103">Método CreateVirtualHardDisk da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="ef2a8-103">CreateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="ef2a8-104">Cria um arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="ef2a8-104">Creates a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef2a8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef2a8-105">Syntax</span></span>


```mof
uint32 CreateVirtualHardDisk(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ef2a8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef2a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef2a8-107">*VirtualDiskSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef2a8-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef2a8-108">Cadeia de caracteres que contém uma instância inserida da classe [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) que é usada para definir os atributos do disco rígido virtual a ser criado.</span><span class="sxs-lookup"><span data-stu-id="ef2a8-108">String that contains an embedded instance of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that is used to define attributes of the virtual hard disk to be created.</span></span>

</dd> <dt>

<span data-ttu-id="ef2a8-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="ef2a8-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef2a8-110">Uma referência ao trabalho (pode ser **NULL** se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="ef2a8-110">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef2a8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef2a8-111">Return value</span></span>

<span data-ttu-id="ef2a8-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ef2a8-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ef2a8-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ef2a8-126">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="ef2a8-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ef2a8-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef2a8-127">Remarks</span></span>

<span data-ttu-id="ef2a8-128">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="ef2a8-128">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ef2a8-129">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ef2a8-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef2a8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef2a8-130">Requirements</span></span>



| <span data-ttu-id="ef2a8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef2a8-131">Requirement</span></span> | <span data-ttu-id="ef2a8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ef2a8-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2a8-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef2a8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ef2a8-134">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ef2a8-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef2a8-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef2a8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ef2a8-136">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ef2a8-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef2a8-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef2a8-137">Namespace</span></span><br/>                | <span data-ttu-id="ef2a8-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ef2a8-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef2a8-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ef2a8-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef2a8-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef2a8-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef2a8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ef2a8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef2a8-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef2a8-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef2a8-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef2a8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef2a8-144">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="ef2a8-144">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

