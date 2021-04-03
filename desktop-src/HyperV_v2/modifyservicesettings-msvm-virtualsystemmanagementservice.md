---
description: Modifica os dados de configuração para o serviço.
ms.assetid: 1CA49922-894D-4AA1-B741-6A0DC9F5654E
title: Método ModifyServiceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e93d86c454de4f214c72a6ed95a414d184419c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829359"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="2f9aa-103">Método ModifyServiceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="2f9aa-103">ModifyServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="2f9aa-104">Modifica os dados de configuração para o serviço.</span><span class="sxs-lookup"><span data-stu-id="2f9aa-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f9aa-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2f9aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f9aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f9aa-107">*SettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f9aa-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f9aa-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2f9aa-108">Type: **string**</span></span>

<span data-ttu-id="2f9aa-109">Uma instância inserida da classe [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) que contém os aspectos modificados do serviço existente.</span><span class="sxs-lookup"><span data-stu-id="2f9aa-109">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the modified aspects of the existing service.</span></span>

</dd> <dt>

<span data-ttu-id="2f9aa-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="2f9aa-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f9aa-111">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="2f9aa-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="2f9aa-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2f9aa-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f9aa-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f9aa-113">Return value</span></span>

<span data-ttu-id="2f9aa-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f9aa-114">Type: **uint32**</span></span>

<span data-ttu-id="2f9aa-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f9aa-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2f9aa-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2f9aa-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2f9aa-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2f9aa-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f9aa-129">Remarks</span></span>

<span data-ttu-id="2f9aa-130">O acesso à classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="2f9aa-130">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2f9aa-131">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2f9aa-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f9aa-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f9aa-132">Requirements</span></span>



| <span data-ttu-id="2f9aa-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f9aa-133">Requirement</span></span> | <span data-ttu-id="2f9aa-134">Valor</span><span class="sxs-lookup"><span data-stu-id="2f9aa-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f9aa-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f9aa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2f9aa-136">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2f9aa-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2f9aa-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f9aa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2f9aa-138">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2f9aa-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f9aa-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f9aa-139">Namespace</span></span><br/>                | <span data-ttu-id="2f9aa-140">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2f9aa-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2f9aa-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2f9aa-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f9aa-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f9aa-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f9aa-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2f9aa-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f9aa-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f9aa-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f9aa-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f9aa-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f9aa-146">**ModifyServiceSettings (v1)**</span><span class="sxs-lookup"><span data-stu-id="2f9aa-146">**ModifyServiceSettings (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyservicesettings-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="2f9aa-147">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="2f9aa-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="2f9aa-148">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f9aa-148">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> </dl>

 

