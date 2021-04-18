---
title: Método SetVirtualDesktopState da classe Win32_RDMSVirtualDesktop
description: Atualiza o estado da área de trabalho virtual.
ms.assetid: 8f4f3d31-0434-4018-a33a-2ffd62c09669
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetVirtualDesktopState
- Método SetVirtualDesktopState Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota, método SetVirtualDesktopState
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af913e29857a59cacf283bff6a1642e0ea4cef9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787577"
---
# <a name="setvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="17bed-106">Método SetVirtualDesktopState da classe Win32 \_ RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="17bed-106">SetVirtualDesktopState method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="17bed-107">Atualiza o estado da área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="17bed-107">Updates the state of the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="17bed-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17bed-108">Syntax</span></span>


```mof
uint32 SetVirtualDesktopState(
  [in] uint32 VMState
);
```



## <a name="parameters"></a><span data-ttu-id="17bed-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17bed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17bed-110">*VMState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17bed-110">*VMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17bed-111">Um valor que especifica o novo estado da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="17bed-111">A value that specifies the new state of the virtual machine.</span></span>

<span data-ttu-id="17bed-112">Esse parâmetro pode apostar definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="17bed-112">This parameter can bet set to one of the following values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="17bed-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0 (padrão))</span><span class="sxs-lookup"><span data-stu-id="17bed-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0 (Default))</span></span>


</dt> <dd>

<span data-ttu-id="17bed-114">Não foi possível determinar o estado da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="17bed-114">The state of the virtual machine could not be determined.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="17bed-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="17bed-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="17bed-116">A máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="17bed-116">The virtual machine is running.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="17bed-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="17bed-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="17bed-118">A máquina virtual está desligada.</span><span class="sxs-lookup"><span data-stu-id="17bed-118">The virtual machine is turned off.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="17bed-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (32768)</span><span class="sxs-lookup"><span data-stu-id="17bed-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="17bed-120">A máquina virtual está pausada.</span><span class="sxs-lookup"><span data-stu-id="17bed-120">The virtual machine is paused.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="17bed-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspenso** (32769)</span><span class="sxs-lookup"><span data-stu-id="17bed-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="17bed-122">A máquina virtual está em um estado salvo.</span><span class="sxs-lookup"><span data-stu-id="17bed-122">The virtual machine is in a saved state.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="17bed-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (32770)</span><span class="sxs-lookup"><span data-stu-id="17bed-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="17bed-124">A máquina virtual está iniciando.</span><span class="sxs-lookup"><span data-stu-id="17bed-124">The virtual machine is starting.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="17bed-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Salvando** (32773)</span><span class="sxs-lookup"><span data-stu-id="17bed-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="17bed-126">A máquina virtual está salvando seu estado.</span><span class="sxs-lookup"><span data-stu-id="17bed-126">The virtual machine is saving its state.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="17bed-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (32774)</span><span class="sxs-lookup"><span data-stu-id="17bed-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (32774)</span></span>


</dt> <dd>

<span data-ttu-id="17bed-128">A máquina virtual está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="17bed-128">The virtual machine is turning off.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="17bed-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausando** (32776)</span><span class="sxs-lookup"><span data-stu-id="17bed-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="17bed-130">A máquina virtual está sendo pausada.</span><span class="sxs-lookup"><span data-stu-id="17bed-130">The virtual machine is pausing.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="17bed-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Retomando** (32777)</span><span class="sxs-lookup"><span data-stu-id="17bed-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="17bed-132">A máquina virtual está retomando de um estado em pausa.</span><span class="sxs-lookup"><span data-stu-id="17bed-132">The virtual machine is resuming from a paused state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17bed-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17bed-133">Return value</span></span>

<span data-ttu-id="17bed-134">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="17bed-134">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="17bed-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17bed-135">Requirements</span></span>



| <span data-ttu-id="17bed-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="17bed-136">Requirement</span></span> | <span data-ttu-id="17bed-137">Valor</span><span class="sxs-lookup"><span data-stu-id="17bed-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="17bed-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17bed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="17bed-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="17bed-139">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="17bed-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17bed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="17bed-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17bed-141">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="17bed-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="17bed-142">Namespace</span></span><br/>                | <span data-ttu-id="17bed-143">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="17bed-143">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="17bed-144">MOF</span><span class="sxs-lookup"><span data-stu-id="17bed-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17bed-145"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17bed-145"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="17bed-146">DLL</span><span class="sxs-lookup"><span data-stu-id="17bed-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17bed-147"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17bed-147"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="17bed-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="17bed-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17bed-149">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="17bed-149">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





