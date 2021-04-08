---
description: Modifica os dados de configuração para o serviço.
ms.assetid: 76669180-fa95-4d6e-b89a-53e45da664c4
title: Método ModifyServiceSettings da classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c2d6550d8b15264bf9cef126239228494996d080
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829360"
---
# <a name="modifyservicesettings-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="fe19f-103">Método ModifyServiceSettings da \_ classe TerminalService Msvm</span><span class="sxs-lookup"><span data-stu-id="fe19f-103">ModifyServiceSettings method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="fe19f-104">Modifica os dados de configuração para o serviço.</span><span class="sxs-lookup"><span data-stu-id="fe19f-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe19f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe19f-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fe19f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe19f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe19f-107">*ServiceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe19f-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe19f-108">Uma representação de cadeia de caracteres da classe [**Msvm \_ TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) que contém os dados de configuração modificados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="fe19f-108">A string representation of the [**Msvm\_TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="fe19f-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="fe19f-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe19f-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fe19f-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe19f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe19f-111">Return value</span></span>

<span data-ttu-id="fe19f-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe19f-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fe19f-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="fe19f-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="fe19f-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="fe19f-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="fe19f-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="fe19f-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="fe19f-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="fe19f-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="fe19f-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="fe19f-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="fe19f-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="fe19f-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="fe19f-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fe19f-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="fe19f-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fe19f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe19f-126">Requirements</span></span>



| <span data-ttu-id="fe19f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe19f-127">Requirement</span></span> | <span data-ttu-id="fe19f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fe19f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe19f-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe19f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fe19f-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fe19f-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fe19f-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe19f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fe19f-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fe19f-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe19f-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe19f-133">Namespace</span></span><br/>                | <span data-ttu-id="fe19f-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fe19f-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fe19f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fe19f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe19f-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe19f-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe19f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fe19f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe19f-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe19f-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fe19f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe19f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe19f-140">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="fe19f-140">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

