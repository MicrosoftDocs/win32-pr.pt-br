---
description: Modifica os dados de configuração de mesclagem de disco.
ms.assetid: 91775dc5-105a-4e38-a334-fb34dd4e59f8
title: Método ModifyDiskMergeSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyDiskMergeSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe737c084b4c1c76a411ce1d2eba513554b40f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775735"
---
# <a name="modifydiskmergesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="15c3e-103">Método ModifyDiskMergeSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="15c3e-103">ModifyDiskMergeSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="15c3e-104">Modifica os dados de configuração de mesclagem de disco.</span><span class="sxs-lookup"><span data-stu-id="15c3e-104">Modifies the disk merge setting data.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c3e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15c3e-105">Syntax</span></span>


```mof
uint32 ModifyDiskMergeSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="15c3e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15c3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c3e-107">*SettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15c3e-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c3e-108">Uma instância inserida da classe [**Msvm \_ DiskMergeSettingData**](msvm-diskmergesettingdata.md) que contém dados de configuração modificados para a função de mesclagem de disco.</span><span class="sxs-lookup"><span data-stu-id="15c3e-108">An embedded instance of the [**Msvm\_DiskMergeSettingData**](msvm-diskmergesettingdata.md) class that contains modified setting data for the disk merge function.</span></span>

</dd> <dt>

<span data-ttu-id="15c3e-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="15c3e-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15c3e-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15c3e-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15c3e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15c3e-111">Return value</span></span>

<span data-ttu-id="15c3e-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="15c3e-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="15c3e-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="15c3e-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="15c3e-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="15c3e-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="15c3e-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="15c3e-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="15c3e-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="15c3e-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="15c3e-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="15c3e-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="15c3e-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="15c3e-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="15c3e-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="15c3e-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="15c3e-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="15c3e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15c3e-126">Requirements</span></span>



| <span data-ttu-id="15c3e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="15c3e-127">Requirement</span></span> | <span data-ttu-id="15c3e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="15c3e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15c3e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15c3e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="15c3e-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="15c3e-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="15c3e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15c3e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="15c3e-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="15c3e-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15c3e-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="15c3e-133">Namespace</span></span><br/>                | <span data-ttu-id="15c3e-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="15c3e-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="15c3e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="15c3e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15c3e-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15c3e-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15c3e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="15c3e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15c3e-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15c3e-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15c3e-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="15c3e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c3e-140">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="15c3e-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

