---
description: Método ModifyServiceSettings da classe Msvm_TerminalService – modifica os dados de configuração para o serviço.
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
ms.openlocfilehash: 930b29c5c07c755b493a0aabad88ae776c0803e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119324"
---
# <a name="modifyservicesettings-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="be0cd-103">Método ModifyServiceSettings da \_ classe TerminalService Msvm</span><span class="sxs-lookup"><span data-stu-id="be0cd-103">ModifyServiceSettings method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="be0cd-104">Modifica os dados de configuração para o serviço.</span><span class="sxs-lookup"><span data-stu-id="be0cd-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="be0cd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be0cd-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="be0cd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be0cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be0cd-107">*ServiceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be0cd-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be0cd-108">Uma representação de cadeia de caracteres da classe [**Msvm \_ TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) que contém os dados de configuração modificados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="be0cd-108">A string representation of the [**Msvm\_TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="be0cd-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="be0cd-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be0cd-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be0cd-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be0cd-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="be0cd-111">Return value</span></span>

<span data-ttu-id="be0cd-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="be0cd-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="be0cd-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="be0cd-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="be0cd-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="be0cd-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="be0cd-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="be0cd-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="be0cd-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="be0cd-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="be0cd-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="be0cd-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="be0cd-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="be0cd-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="be0cd-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="be0cd-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="be0cd-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="be0cd-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be0cd-126">Requirements</span></span>



| <span data-ttu-id="be0cd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="be0cd-127">Requirement</span></span> | <span data-ttu-id="be0cd-128">Valor</span><span class="sxs-lookup"><span data-stu-id="be0cd-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be0cd-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be0cd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="be0cd-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="be0cd-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="be0cd-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be0cd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="be0cd-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="be0cd-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="be0cd-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="be0cd-133">Namespace</span></span><br/>                | <span data-ttu-id="be0cd-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="be0cd-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="be0cd-135">MOF</span><span class="sxs-lookup"><span data-stu-id="be0cd-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be0cd-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be0cd-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="be0cd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="be0cd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be0cd-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="be0cd-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="be0cd-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="be0cd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0cd-140">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="be0cd-140">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

