---
description: Modifica o modo de início de um \_ serviço do SystemDriver Win32.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Método ChangeStartMode da classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500911"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="e2b7a-103">Método ChangeStartMode da \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="e2b7a-103">ChangeStartMode method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="e2b7a-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica o modo de início de um serviço do [**\_ SystemDriver Win32**](win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="e2b7a-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span>

<span data-ttu-id="e2b7a-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e2b7a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e2b7a-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e2b7a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b7a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2b7a-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="e2b7a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2b7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2b7a-109">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e2b7a-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b7a-110">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="e2b7a-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="e2b7a-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial** ("inicialização")</span><span class="sxs-lookup"><span data-stu-id="e2b7a-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="e2b7a-112">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e2b7a-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="e2b7a-113">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="e2b7a-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="e2b7a-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="e2b7a-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="e2b7a-115">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e2b7a-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="e2b7a-116">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="e2b7a-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="e2b7a-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="e2b7a-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="e2b7a-118">Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="e2b7a-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="e2b7a-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda** ("manual")</span><span class="sxs-lookup"><span data-stu-id="e2b7a-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="e2b7a-120">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="e2b7a-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e2b7a-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")</span><span class="sxs-lookup"><span data-stu-id="e2b7a-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="e2b7a-122">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="e2b7a-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2b7a-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2b7a-123">Return value</span></span>

<span data-ttu-id="e2b7a-124">Retorna um valor de 0 (zero) se o serviço tiver sido modificado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="e2b7a-124">Returns a value of 0 (zero) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e2b7a-125">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-125">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-126">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-126">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-127">**Acesso negado** (2)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-127">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-128">**Serviços dependentes em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-128">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-129">**Controle de serviço inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-129">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-130">O **serviço não pode aceitar o controle** (5)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-130">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-131">**Serviço não ativo** (6)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-131">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-132">**Tempo limite da solicitação de serviço** (7)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-132">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-133">**Falha desconhecida** (8)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-133">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-134">**Caminho não encontrado** (9)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-134">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-135">**Serviço já em execução** (10)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-135">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-136">**Banco de dados de serviço bloqueado** (11)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-136">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-137">**Dependência de serviço excluída** (12)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-137">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-138">**Falha de dependência de serviço** (13)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-138">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-139">**Serviço desabilitado** (14)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-139">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-140">**Falha no logon do serviço** (15)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-140">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-141">**Serviço marcado para exclusão** (16)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-141">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-142">**Serviço sem thread** (17)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-142">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-143">**Dependência circular de status** (18)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-143">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-144">**Nome duplicado de status** (19)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-144">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-145">**Nome inválido do status** (20)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-145">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-146">**Parâmetro de status inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-146">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-147">**Conta de serviço inválida de status** (22)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-147">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-148">O **serviço de status existe** (23)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-148">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-149">**Serviço já pausado** (24)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-149">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="e2b7a-150">**Outro** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="e2b7a-150">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e2b7a-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2b7a-151">Requirements</span></span>



| <span data-ttu-id="e2b7a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2b7a-152">Requirement</span></span> | <span data-ttu-id="e2b7a-153">Valor</span><span class="sxs-lookup"><span data-stu-id="e2b7a-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b7a-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2b7a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b7a-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2b7a-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2b7a-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2b7a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b7a-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2b7a-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2b7a-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2b7a-158">Namespace</span></span><br/>                | <span data-ttu-id="e2b7a-159">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e2b7a-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2b7a-160">MOF</span><span class="sxs-lookup"><span data-stu-id="e2b7a-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2b7a-161"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2b7a-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2b7a-162">DLL</span><span class="sxs-lookup"><span data-stu-id="e2b7a-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2b7a-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2b7a-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b7a-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2b7a-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2b7a-165">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e2b7a-165">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e2b7a-166">**Systemdrive do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="e2b7a-166">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

