---
description: Modifica os dados de configuração para o serviço.
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Método ModifyServiceSettings da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b680f5f46d99d46f99094e05db653083fd7ae952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647330"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="90274-103">Método ModifyServiceSettings da \_ classe MetricService Msvm</span><span class="sxs-lookup"><span data-stu-id="90274-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="90274-104">Modifica os dados de configuração para o serviço.</span><span class="sxs-lookup"><span data-stu-id="90274-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="90274-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90274-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="90274-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90274-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90274-107">*SettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90274-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90274-108">Contém uma instância inserida da classe [**Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) que contém os dados de configuração modificados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="90274-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="90274-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="90274-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90274-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="90274-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90274-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90274-111">Return value</span></span>

<span data-ttu-id="90274-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="90274-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="90274-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="90274-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="90274-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="90274-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="90274-115"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="90274-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="90274-116">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="90274-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="90274-117"><dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="90274-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="90274-118">Parâmetros de método marcados, trabalho iniciado.</span><span class="sxs-lookup"><span data-stu-id="90274-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="90274-119"><dt>32768</dt> <dt>**com falha**</dt></span><span class="sxs-lookup"><span data-stu-id="90274-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="90274-120">Falhou.</span><span class="sxs-lookup"><span data-stu-id="90274-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="90274-121"><dt>**Acesso negado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="90274-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="90274-122">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="90274-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="90274-123"><dt>**Sem suporte**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="90274-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="90274-124">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="90274-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="90274-125">O <dt>**status é desconhecido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="90274-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="90274-126">O status é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="90274-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="90274-127"><dt>**Tempo limite**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="90274-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="90274-128">Tempo limite.</span><span class="sxs-lookup"><span data-stu-id="90274-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="90274-129"><dt>**Parâmetro inválido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="90274-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="90274-130">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="90274-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="90274-131">O <dt>**sistema está em uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="90274-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="90274-132">O sistema está em uso.</span><span class="sxs-lookup"><span data-stu-id="90274-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="90274-133"><dt>**Estado inválido para esta operação**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="90274-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="90274-134">Estado inválido para esta operação.</span><span class="sxs-lookup"><span data-stu-id="90274-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="90274-135"><dt>**Tipo de dados incorreto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="90274-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="90274-136">Tipo de dados incorreto.</span><span class="sxs-lookup"><span data-stu-id="90274-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="90274-137">O <dt>**sistema não está disponível**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="90274-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="90274-138">O sistema não está disponível.</span><span class="sxs-lookup"><span data-stu-id="90274-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="90274-139"><dt>**Memória insuficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="90274-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="90274-140">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="90274-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="90274-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90274-141">Requirements</span></span>



| <span data-ttu-id="90274-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="90274-142">Requirement</span></span> | <span data-ttu-id="90274-143">Valor</span><span class="sxs-lookup"><span data-stu-id="90274-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90274-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90274-144">Minimum supported client</span></span><br/> | <span data-ttu-id="90274-145">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="90274-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="90274-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90274-146">Minimum supported server</span></span><br/> | <span data-ttu-id="90274-147">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="90274-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90274-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="90274-148">Namespace</span></span><br/>                | <span data-ttu-id="90274-149">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="90274-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="90274-150">MOF</span><span class="sxs-lookup"><span data-stu-id="90274-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90274-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90274-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90274-152">DLL</span><span class="sxs-lookup"><span data-stu-id="90274-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90274-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90274-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90274-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="90274-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90274-155">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="90274-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

