---
description: Modifica as configurações para o serviço de réplica do Hyper-V.
ms.assetid: e203f9f5-da4b-4ba7-8637-add7169990d3
title: Método ModifyServiceSettings da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe20f8e6f113dce05961eb11fbafdc7841f39e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647328"
---
# <a name="modifyservicesettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="f71ec-103">Método ModifyServiceSettings da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="f71ec-103">ModifyServiceSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="f71ec-104">Modifica as configurações para o serviço de réplica do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f71ec-104">Modifies the settings for the Hyper-V Replica service.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f71ec-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f71ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f71ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f71ec-107">*SettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f71ec-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f71ec-108">Uma representação de cadeia de caracteres da classe [**Msvm \_ ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) que contém os dados de configuração modificados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="f71ec-108">A string representation of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="f71ec-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f71ec-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f71ec-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f71ec-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f71ec-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f71ec-111">Return value</span></span>

<span data-ttu-id="f71ec-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f71ec-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f71ec-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="f71ec-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f71ec-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="f71ec-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f71ec-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="f71ec-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f71ec-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="f71ec-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f71ec-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f71ec-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="f71ec-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f71ec-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="f71ec-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f71ec-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f71ec-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f71ec-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f71ec-126">Requirements</span></span>



| <span data-ttu-id="f71ec-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f71ec-127">Requirement</span></span> | <span data-ttu-id="f71ec-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f71ec-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71ec-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f71ec-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f71ec-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f71ec-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f71ec-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f71ec-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f71ec-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f71ec-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f71ec-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="f71ec-133">Namespace</span></span><br/>                | <span data-ttu-id="f71ec-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f71ec-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f71ec-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f71ec-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f71ec-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f71ec-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f71ec-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f71ec-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f71ec-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f71ec-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f71ec-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f71ec-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71ec-140">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="f71ec-140">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

