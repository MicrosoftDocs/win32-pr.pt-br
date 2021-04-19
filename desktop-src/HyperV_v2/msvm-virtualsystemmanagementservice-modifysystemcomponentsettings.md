---
description: Modifica as configurações genéricas do componente do sistema.
ms.assetid: e745be32-c26a-4343-99c8-950788243adf
title: Método ModifySystemComponentSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9495256d1b7610bebdac1fb2cc8b70960a63304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778581"
---
# <a name="modifysystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6217b-103">Método ModifySystemComponentSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="6217b-103">ModifySystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6217b-104">Modifica as configurações genéricas do componente do sistema.</span><span class="sxs-lookup"><span data-stu-id="6217b-104">Modifies generic system component settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="6217b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6217b-105">Syntax</span></span>


```mof
uint32 ModifySystemComponentSettings(
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6217b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6217b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6217b-107">*ComponentSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6217b-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6217b-108">Uma matriz de configurações de componente para atualizar.</span><span class="sxs-lookup"><span data-stu-id="6217b-108">An array of component settings to update.</span></span>

</dd> <dt>

<span data-ttu-id="6217b-109">*ResultingComponentSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6217b-109">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6217b-110">Em caso de sucesso, retorna uma matriz de [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) que referencia as configurações de componente resultantes.</span><span class="sxs-lookup"><span data-stu-id="6217b-110">On success, returns an array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="6217b-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="6217b-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6217b-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6217b-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6217b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6217b-113">Return value</span></span>

<span data-ttu-id="6217b-114">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="6217b-114">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6217b-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="6217b-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6217b-116">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="6217b-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6217b-117">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="6217b-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6217b-118">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="6217b-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6217b-119">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="6217b-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6217b-120">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="6217b-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6217b-121">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="6217b-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6217b-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6217b-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6217b-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="6217b-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6217b-124">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6217b-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6217b-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6217b-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6217b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6217b-126">Requirements</span></span>



| <span data-ttu-id="6217b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6217b-127">Requirement</span></span> | <span data-ttu-id="6217b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6217b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6217b-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6217b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6217b-130">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="6217b-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6217b-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6217b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6217b-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6217b-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6217b-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="6217b-133">Namespace</span></span><br/>                | <span data-ttu-id="6217b-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6217b-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6217b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6217b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6217b-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6217b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6217b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6217b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6217b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6217b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6217b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="6217b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6217b-140">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6217b-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

