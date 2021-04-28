---
description: Método ModifyServiceSettings da classe Msvm_MetricService – modifica os dados de configuração para o serviço.
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
ms.openlocfilehash: 088aec001dd63de7344256fd9e114b6ff73e4425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112174"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="59f41-103">Método ModifyServiceSettings da \_ classe MetricService Msvm</span><span class="sxs-lookup"><span data-stu-id="59f41-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="59f41-104">Modifica os dados de configuração para o serviço.</span><span class="sxs-lookup"><span data-stu-id="59f41-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59f41-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="59f41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59f41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59f41-107">*SettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59f41-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59f41-108">Contém uma instância inserida da classe [**Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) que contém os dados de configuração modificados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="59f41-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="59f41-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="59f41-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59f41-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59f41-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59f41-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="59f41-111">Return value</span></span>

<span data-ttu-id="59f41-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="59f41-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="59f41-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="59f41-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="59f41-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="59f41-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="59f41-115"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="59f41-116">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="59f41-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="59f41-117"><dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="59f41-118">Parâmetros de método marcados, trabalho iniciado.</span><span class="sxs-lookup"><span data-stu-id="59f41-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="59f41-119"><dt>32768</dt> <dt>**com falha**</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="59f41-120">Falhou.</span><span class="sxs-lookup"><span data-stu-id="59f41-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="59f41-121"><dt>**Acesso negado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="59f41-122">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="59f41-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="59f41-123"><dt>**Sem suporte**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="59f41-124">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="59f41-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="59f41-125">O <dt>**status é desconhecido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="59f41-126">O status é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="59f41-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="59f41-127"><dt>**Tempo limite**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="59f41-128">Tempo limite.</span><span class="sxs-lookup"><span data-stu-id="59f41-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="59f41-129"><dt>**Parâmetro inválido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="59f41-130">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="59f41-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="59f41-131">O <dt>**sistema está em uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="59f41-132">O sistema está em uso.</span><span class="sxs-lookup"><span data-stu-id="59f41-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="59f41-133"><dt>**Estado inválido para esta operação**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="59f41-134">Estado inválido para esta operação.</span><span class="sxs-lookup"><span data-stu-id="59f41-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="59f41-135"><dt>**Tipo de dados incorreto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="59f41-136">Tipo de dados incorreto.</span><span class="sxs-lookup"><span data-stu-id="59f41-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="59f41-137">O <dt>**sistema não está disponível**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="59f41-138">O sistema não está disponível.</span><span class="sxs-lookup"><span data-stu-id="59f41-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="59f41-139"><dt>**Memória insuficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="59f41-140">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="59f41-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="59f41-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59f41-141">Requirements</span></span>



| <span data-ttu-id="59f41-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="59f41-142">Requirement</span></span> | <span data-ttu-id="59f41-143">Valor</span><span class="sxs-lookup"><span data-stu-id="59f41-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59f41-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59f41-144">Minimum supported client</span></span><br/> | <span data-ttu-id="59f41-145">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="59f41-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="59f41-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59f41-146">Minimum supported server</span></span><br/> | <span data-ttu-id="59f41-147">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="59f41-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59f41-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="59f41-148">Namespace</span></span><br/>                | <span data-ttu-id="59f41-149">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="59f41-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="59f41-150">MOF</span><span class="sxs-lookup"><span data-stu-id="59f41-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59f41-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="59f41-152">DLL</span><span class="sxs-lookup"><span data-stu-id="59f41-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59f41-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="59f41-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="59f41-154">Consulte também</span><span class="sxs-lookup"><span data-stu-id="59f41-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f41-155">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="59f41-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

