---
description: Atualiza as configurações de um disco rígido virtual.
ms.assetid: 10f80313-bc78-447e-bdf2-5635d7354e3c
title: Método SetVirtualHardDiskSettingData da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 969e9019d05b49f2f171f2177e1e74f135e212da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297455"
---
# <a name="setvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="8445e-103">Método SetVirtualHardDiskSettingData da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="8445e-103">SetVirtualHardDiskSettingData method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="8445e-104">Atualiza as configurações de um disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="8445e-104">Updates the settings for a virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="8445e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8445e-105">Syntax</span></span>


```mof
uint32 SetVirtualHardDiskSettingData(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8445e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8445e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8445e-107">*VirtualDiskSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8445e-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8445e-108">Uma representação de cadeia de caracteres da classe [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) que especifica o disco rígido virtual a ser atualizado e que contém os novos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="8445e-108">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the virtual hard disk to update and that contains the new setting data.</span></span> <span data-ttu-id="8445e-109">Somente as propriedades **ParentPath**, **PhysicalSectorSize** ou **VirtualDiskId** podem ser atualizadas com esse método.</span><span class="sxs-lookup"><span data-stu-id="8445e-109">Only the **ParentPath**, **PhysicalSectorSize**, or **VirtualDiskId** properties can be updated with this method.</span></span> <span data-ttu-id="8445e-110">Você não pode atualizar essas propriedades com uma chamada de método.</span><span class="sxs-lookup"><span data-stu-id="8445e-110">You can't update these properties with one method call.</span></span> <span data-ttu-id="8445e-111">Você só pode atualizar uma dessas propriedades com uma única chamada de método.</span><span class="sxs-lookup"><span data-stu-id="8445e-111">You can only update one of these properties with a single method call.</span></span>

</dd> <dt>

<span data-ttu-id="8445e-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8445e-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8445e-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8445e-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8445e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8445e-114">Return value</span></span>

<span data-ttu-id="8445e-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8445e-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8445e-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="8445e-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8445e-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="8445e-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="8445e-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="8445e-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="8445e-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="8445e-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="8445e-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="8445e-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="8445e-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="8445e-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="8445e-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="8445e-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="8445e-129">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="8445e-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="8445e-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="8445e-130">Remarks</span></span>

<span data-ttu-id="8445e-131">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="8445e-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8445e-132">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8445e-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8445e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8445e-133">Requirements</span></span>



| <span data-ttu-id="8445e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8445e-134">Requirement</span></span> | <span data-ttu-id="8445e-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8445e-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8445e-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8445e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8445e-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8445e-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8445e-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8445e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8445e-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8445e-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8445e-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="8445e-140">Namespace</span></span><br/>                | <span data-ttu-id="8445e-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8445e-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8445e-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8445e-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8445e-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8445e-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8445e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8445e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8445e-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8445e-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8445e-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="8445e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8445e-147">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="8445e-147">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

