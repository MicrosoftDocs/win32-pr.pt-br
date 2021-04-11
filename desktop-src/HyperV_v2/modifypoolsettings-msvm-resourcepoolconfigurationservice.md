---
description: Altera as configurações de um pool filho que não estão relacionados à alocação.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Método ModifyPoolSettings da classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: edc5f48dabfb84554954cc80d9c4e8a20678d34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170673"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="17bf8-103">Método ModifyPoolSettings da \_ classe ResourcePoolConfigurationService Msvm</span><span class="sxs-lookup"><span data-stu-id="17bf8-103">ModifyPoolSettings method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="17bf8-104">Altera as configurações de um pool filho que não estão relacionados à alocação.</span><span class="sxs-lookup"><span data-stu-id="17bf8-104">Changes the settings of a child pool that are not allocation related.</span></span>

## <a name="syntax"></a><span data-ttu-id="17bf8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17bf8-105">Syntax</span></span>


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="17bf8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17bf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17bf8-107">*ChildPool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17bf8-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17bf8-108">Uma referência a uma instância da classe [**CIM \_ ResourcePool**](cim-resourcepool.md) que representa o pool filho a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="17bf8-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="17bf8-109">*PoolSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17bf8-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17bf8-110">Uma instância inserida da classe [**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) que é usada para especificar as novas configurações para o pool.</span><span class="sxs-lookup"><span data-stu-id="17bf8-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the new settings for the pool.</span></span>

</dd> <dt>

<span data-ttu-id="17bf8-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="17bf8-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17bf8-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17bf8-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17bf8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17bf8-113">Return value</span></span>

<span data-ttu-id="17bf8-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="17bf8-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="17bf8-115">**Trabalho concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="17bf8-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-116">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="17bf8-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="17bf8-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-118">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="17bf8-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="17bf8-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="17bf8-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="17bf8-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-122">**Desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="17bf8-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="17bf8-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="17bf8-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-125">**Em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="17bf8-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-126">**Estado inválido** (32775)</span><span class="sxs-lookup"><span data-stu-id="17bf8-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-127">**Tipo de recurso incorreto para o pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="17bf8-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-128">**Não disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="17bf8-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="17bf8-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-130">**Fornecedor reservado** (32779)</span><span class="sxs-lookup"><span data-stu-id="17bf8-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-131">**Recursos insuficientes** (32780)</span><span class="sxs-lookup"><span data-stu-id="17bf8-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-132">**Objeto não encontrado** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="17bf8-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-133">O **objeto existe** (32788)</span><span class="sxs-lookup"><span data-stu-id="17bf8-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="17bf8-134">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="17bf8-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="17bf8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17bf8-135">Requirements</span></span>



| <span data-ttu-id="17bf8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="17bf8-136">Requirement</span></span> | <span data-ttu-id="17bf8-137">Valor</span><span class="sxs-lookup"><span data-stu-id="17bf8-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17bf8-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17bf8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="17bf8-139">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="17bf8-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="17bf8-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17bf8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="17bf8-141">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="17bf8-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17bf8-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="17bf8-142">Namespace</span></span><br/>                | <span data-ttu-id="17bf8-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="17bf8-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="17bf8-144">MOF</span><span class="sxs-lookup"><span data-stu-id="17bf8-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17bf8-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17bf8-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17bf8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="17bf8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17bf8-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17bf8-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="17bf8-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="17bf8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17bf8-149">**Msvm \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="17bf8-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

