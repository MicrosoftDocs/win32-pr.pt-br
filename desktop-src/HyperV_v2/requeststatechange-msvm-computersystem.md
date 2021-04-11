---
description: Solicita que o estado da máquina virtual seja alterado para o valor especificado.
ms.assetid: 87BE4C7D-604B-4F8D-B4DC-89BD563E3999
title: Método RequestStateChange da classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 291d72797b1ee765507a3d23921cd518cf605354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172343"
---
# <a name="requeststatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="43be8-103">Método RequestStateChange da classe de \_ ComputerSystem Msvm</span><span class="sxs-lookup"><span data-stu-id="43be8-103">RequestStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="43be8-104">Solicita que o estado da máquina virtual seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="43be8-104">Requests that the state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="43be8-105">Invocar o método **RequestStateChange** várias vezes pode fazer com que as solicitações anteriores fossem substituídas ou perdidas.</span><span class="sxs-lookup"><span data-stu-id="43be8-105">Invoking the **RequestStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="43be8-106">Esse método só tem suporte para instâncias da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representam uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43be8-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

<span data-ttu-id="43be8-107">Enquanto a alteração de estado está em andamento, a propriedade **requestedstate** é alterada para o valor do parâmetro *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="43be8-107">While the state change is in progress, the **RequestedState** property is changed to the value of the *RequestedState* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="43be8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43be8-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="43be8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43be8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43be8-110">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43be8-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43be8-111">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43be8-111">Type: **uint16**</span></span>

<span data-ttu-id="43be8-112">O novo estado.</span><span class="sxs-lookup"><span data-stu-id="43be8-112">The new state.</span></span> <span data-ttu-id="43be8-113">Valores maiores que 32767 são valores propostos da **DMTF** e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="43be8-113">Values that are greater than 32767 are **DMTF** proposed values and are subject to change.</span></span>

<span data-ttu-id="43be8-114">Estes são os valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="43be8-114">Here are possible values:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43be8-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="43be8-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-116">Corresponde a [**CIM \_ EnabledLogicalElement. enabledstate**](/previous-versions//cc136818(v=vs.85)) = Other.</span><span class="sxs-lookup"><span data-stu-id="43be8-116">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Other.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="43be8-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="43be8-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-118">Corresponde a [**CIM \_ EnabledLogicalElement. enabledstate**](/previous-versions//cc136818(v=vs.85)) = habilitado.</span><span class="sxs-lookup"><span data-stu-id="43be8-118">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="43be8-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="43be8-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-120">Corresponde a [**CIM \_ EnabledLogicalElement. enabledstate**](/previous-versions//cc136818(v=vs.85)) = desabilitado.</span><span class="sxs-lookup"><span data-stu-id="43be8-120">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Disabled.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="43be8-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="43be8-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-122">Válido na versão 1 (v1) do Hyper-V apenas.</span><span class="sxs-lookup"><span data-stu-id="43be8-122">Valid in version 1 (V1) of Hyper-V only.</span></span> <span data-ttu-id="43be8-123">A máquina virtual está sendo desligada por meio do serviço de desligamento.</span><span class="sxs-lookup"><span data-stu-id="43be8-123">The virtual machine is shutting down via the shutdown service.</span></span> <span data-ttu-id="43be8-124">Corresponde a [**CIM \_ EnabledLogicalElement. enabledstate**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown.</span><span class="sxs-lookup"><span data-stu-id="43be8-124">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown.</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="43be8-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="43be8-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-126">Corresponde a [**CIM \_ EnabledLogicalElement. enabledstate**](/previous-versions//cc136818(v=vs.85)) = habilitado, mas offline.</span><span class="sxs-lookup"><span data-stu-id="43be8-126">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled but offline.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="43be8-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="43be8-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="43be8-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="43be8-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="43be8-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="43be8-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-130">Corresponde a [**CIM \_ EnabledLogicalElement. enabledstate**](/previous-versions//cc136818(v=vs.85)) = fechar, habilitado, mas em pausa.</span><span class="sxs-lookup"><span data-stu-id="43be8-130">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Quiesce, Enabled but paused.</span></span>

</dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="43be8-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="43be8-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-132">Transição de estado de **desativado** ou **salvo** para **em execução**.</span><span class="sxs-lookup"><span data-stu-id="43be8-132">State transition from **Off** or **Saved** to **Running**.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="43be8-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="43be8-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-134">Redefina a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43be8-134">Reset the virtual machine.</span></span> <span data-ttu-id="43be8-135">Corresponde a [**CIM \_ EnabledLogicalElement. enabledstate**](/previous-versions//cc136818(v=vs.85)) = redefinir.</span><span class="sxs-lookup"><span data-stu-id="43be8-135">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Reset.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="43be8-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Salvando** (32773)</span><span class="sxs-lookup"><span data-stu-id="43be8-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-137">Na versão 1 (v1) do Hyper-V, corresponde a **EnabledStateSaving**.</span><span class="sxs-lookup"><span data-stu-id="43be8-137">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateSaving**.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="43be8-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausando** (32776)</span><span class="sxs-lookup"><span data-stu-id="43be8-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-139">Na versão 1 (v1) do Hyper-V, corresponde a **EnabledStatePausing**.</span><span class="sxs-lookup"><span data-stu-id="43be8-139">In version 1 (V1) of Hyper-V, corresponds to **EnabledStatePausing**.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="43be8-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Retomando** (32777)</span><span class="sxs-lookup"><span data-stu-id="43be8-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-141">Na versão 1 (v1) do Hyper-V, corresponde a **EnabledStateResuming**.</span><span class="sxs-lookup"><span data-stu-id="43be8-141">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateResuming**.</span></span> <span data-ttu-id="43be8-142">Transição de estado de em **pausa** para **em execução**.</span><span class="sxs-lookup"><span data-stu-id="43be8-142">State transition from **Paused** to **Running**.</span></span>

</dd> <dt>

<span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>

<span data-ttu-id="43be8-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779)</span><span class="sxs-lookup"><span data-stu-id="43be8-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-144">Corresponde a **EnabledStateFastSuspend**.</span><span class="sxs-lookup"><span data-stu-id="43be8-144">Corresponds to **EnabledStateFastSuspend**.</span></span>

</dd> <dt>

<span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>

<span data-ttu-id="43be8-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780)</span><span class="sxs-lookup"><span data-stu-id="43be8-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780)</span></span>


</dt> <dd>

<span data-ttu-id="43be8-146">Corresponde a **EnabledStateFastSuspending**.</span><span class="sxs-lookup"><span data-stu-id="43be8-146">Corresponds to **EnabledStateFastSuspending**.</span></span> <span data-ttu-id="43be8-147">Transição de estado de **em execução** para **FastSaved**.</span><span class="sxs-lookup"><span data-stu-id="43be8-147">State transition from **Running** to **FastSaved**.</span></span>

</dd> </dl>

<span data-ttu-id="43be8-148">Esses valores representam Estados críticos:</span><span class="sxs-lookup"><span data-stu-id="43be8-148">These values represent critical states:</span></span>

<dt>

<span id="RunningCritical"></span><span id="runningcritical"></span><span id="RUNNINGCRITICAL"></span>

<span data-ttu-id="43be8-149">**RunningCritical** (32781)</span><span class="sxs-lookup"><span data-stu-id="43be8-149">**RunningCritical** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="OffCritical"></span><span id="offcritical"></span><span id="OFFCRITICAL"></span>

<span data-ttu-id="43be8-150">**OffCritical** (32782)</span><span class="sxs-lookup"><span data-stu-id="43be8-150">**OffCritical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="StoppingCritical"></span><span id="stoppingcritical"></span><span id="STOPPINGCRITICAL"></span>

<span data-ttu-id="43be8-151">**StoppingCritical** (32783)</span><span class="sxs-lookup"><span data-stu-id="43be8-151">**StoppingCritical** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="SavedCritical"></span><span id="savedcritical"></span><span id="SAVEDCRITICAL"></span>

<span data-ttu-id="43be8-152">**SavedCritical** (32784)</span><span class="sxs-lookup"><span data-stu-id="43be8-152">**SavedCritical** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="PausedCritical"></span><span id="pausedcritical"></span><span id="PAUSEDCRITICAL"></span>

<span data-ttu-id="43be8-153">**PausedCritical** (32785)</span><span class="sxs-lookup"><span data-stu-id="43be8-153">**PausedCritical** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="StartingCritical"></span><span id="startingcritical"></span><span id="STARTINGCRITICAL"></span>

<span data-ttu-id="43be8-154">**StartingCritical** (32786)</span><span class="sxs-lookup"><span data-stu-id="43be8-154">**StartingCritical** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="ResetCritical"></span><span id="resetcritical"></span><span id="RESETCRITICAL"></span>

<span data-ttu-id="43be8-155">**ResetCritical** (32787)</span><span class="sxs-lookup"><span data-stu-id="43be8-155">**ResetCritical** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="SavingCritical"></span><span id="savingcritical"></span><span id="SAVINGCRITICAL"></span>

<span data-ttu-id="43be8-156">**SavingCritical** (32788)</span><span class="sxs-lookup"><span data-stu-id="43be8-156">**SavingCritical** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="PausingCritical"></span><span id="pausingcritical"></span><span id="PAUSINGCRITICAL"></span>

<span data-ttu-id="43be8-157">**PausingCritical** (32789)</span><span class="sxs-lookup"><span data-stu-id="43be8-157">**PausingCritical** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="ResumingCritical"></span><span id="resumingcritical"></span><span id="RESUMINGCRITICAL"></span>

<span data-ttu-id="43be8-158">**ResumingCritical** (32790)</span><span class="sxs-lookup"><span data-stu-id="43be8-158">**ResumingCritical** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavedCritical"></span><span id="fastsavedcritical"></span><span id="FASTSAVEDCRITICAL"></span>

<span data-ttu-id="43be8-159">**FastSavedCritical** (32791)</span><span class="sxs-lookup"><span data-stu-id="43be8-159">**FastSavedCritical** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavingCritical"></span><span id="fastsavingcritical"></span><span id="FASTSAVINGCRITICAL"></span>

<span data-ttu-id="43be8-160">**FastSavingCritical** (32792)</span><span class="sxs-lookup"><span data-stu-id="43be8-160">**FastSavingCritical** (32792)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="43be8-161">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="43be8-161">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43be8-162">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="43be8-162">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="43be8-163">Uma referência opcional a um objeto [**Msvm \_ ConcreteJob**](msvm-concretejob.md) que é retornado se a operação é executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="43be8-163">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="43be8-164">Se estiver presente, a referência retornada poderá ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="43be8-164">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="43be8-165">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43be8-165">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43be8-166">Tipo: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="43be8-166">Type: **datetime**</span></span>

<span data-ttu-id="43be8-167">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="43be8-167">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43be8-168">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43be8-168">Return value</span></span>

<span data-ttu-id="43be8-169">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43be8-169">Type: **uint32**</span></span>

<span data-ttu-id="43be8-170">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="43be8-170">This method returns one of the following values.</span></span>



| <span data-ttu-id="43be8-171">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="43be8-171">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="43be8-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="43be8-172">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43be8-173"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-173"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="43be8-174">Êxito.</span><span class="sxs-lookup"><span data-stu-id="43be8-174">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="43be8-175"><dt>**Parâmetros de método verificados-transição iniciada**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-175"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="43be8-176">A transição é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="43be8-176">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="43be8-177"><dt>**Acesso negado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-177"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="43be8-178">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="43be8-178">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="43be8-179"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-179"><dt></dt> <dt>32768</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="43be8-180"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-180"><dt></dt> <dt>32770</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="43be8-181"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-181"><dt></dt> <dt>32771</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="43be8-182"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-182"><dt></dt> <dt>32772</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="43be8-183"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-183"><dt></dt> <dt>32773</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="43be8-184"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-184"><dt></dt> <dt>32774</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="43be8-185"><dt>**Estado inválido para esta operação**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-185"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="43be8-186">Não há suporte para o valor especificado no parâmetro *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="43be8-186">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="43be8-187"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-187"><dt></dt> <dt>32776</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="43be8-188"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-188"><dt></dt> <dt>32777</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="43be8-189"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-189"><dt></dt> <dt>32778</dt></span></span> </dl>                                                  |                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="43be8-190">Comentários</span><span class="sxs-lookup"><span data-stu-id="43be8-190">Remarks</span></span>

<span data-ttu-id="43be8-191">O acesso à classe de [**\_ ComputerSystem Msvm**](msvm-computersystem.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="43be8-191">Access to the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="43be8-192">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="43be8-192">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="43be8-193">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43be8-193">Examples</span></span>

<span data-ttu-id="43be8-194">O exemplo C# a seguir inicia ou desabilita uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43be8-194">The following C# example starts or disables a virtual machine.</span></span> <span data-ttu-id="43be8-195">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="43be8-195">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43be8-196">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="43be8-196">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    public class RequestStateChangeClass
    {
        public static void RequestStateChange(string vmName, string action)
        {
            ManagementScope scope = new ManagementScope(@"\\.\root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);

            if (null == vm)
            {
                throw new ArgumentException(
                    string.Format(
                    "The virtual machine '{0}' could not be found.", 
                    vmName));
            }

            ManagementBaseObject inParams = vm.GetMethodParameters("RequestStateChange");

            const int Enabled = 2;
            const int Disabled = 3;

            if (action.ToLower() == "start")
            {
                inParams["RequestedState"] = Enabled;
            }
            else if (action.ToLower() == "stop")
            {
                inParams["RequestedState"] = Disabled;
            }
            else
            {
                throw new Exception("Wrong action is specified");
            }

            ManagementBaseObject outParams = vm.InvokeMethod(
                "RequestStateChange", 
                inParams, 
                null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine(
                        "{0} state was changed successfully.", 
                        vmName);
                }
                else
                {
                    Console.WriteLine("Failed to change virtual system state");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine(
                    "{0} state was changed successfully.", 
                    vmName);
            }
            else
            {
                Console.WriteLine(
                    "Change virtual system state failed with error {0}", 
                    outParams["ReturnValue"]);
            }

        }

        public static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: <application> vmName action");
                Console.WriteLine("action: start|stop");
                return;
            }

            RequestStateChange(args[0], args[1]);
        }

    }
}
```



<span data-ttu-id="43be8-197">O exemplo a seguir Visual Basic Scripting Edition (VBScript) inicia ou desabilita uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43be8-197">The following Visual Basic Scripting Edition (VBScript) example starts or disables a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43be8-198">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="43be8-198">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```VB
dim objWMIService
dim fileSystem

const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const Enabled = 2
const Disabled = 3



Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    strComputer = "."
    set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       action = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript StartVM.vbs vmName start|stop"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)

    if RequestStateChange(computerSystem, action) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "RequestStateChange failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Turn on a virtual machine
'-----------------------------------------------------------------
Function RequestStateChange(computerSystem, action)
    WriteLog Format2("RequestStateChange({0}, {1})", computerSystem.ElementName, action)

    RequestStateChange = false
    set objInParam = computerSystem.Methods_("RequestStateChange").InParameters.SpawnInstance_()
    
    if action = "start" then
        objInParam.RequestedState = Enabled
    else
        objInParam.RequestedState = Disabled
    end if

    set objOutParams = computerSystem.ExecMethod_("RequestStateChange", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VM {0} was started successfully", computerSystem.ElementName)
            RequestStateChange = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)

    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        end if

    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    dim WMIJob

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting

        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState

    wend


    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\StartVM.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="43be8-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43be8-199">Requirements</span></span>



| <span data-ttu-id="43be8-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="43be8-200">Requirement</span></span> | <span data-ttu-id="43be8-201">Valor</span><span class="sxs-lookup"><span data-stu-id="43be8-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43be8-202">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43be8-202">Minimum supported client</span></span><br/> | <span data-ttu-id="43be8-203">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="43be8-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="43be8-204">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43be8-204">Minimum supported server</span></span><br/> | <span data-ttu-id="43be8-205">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="43be8-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43be8-206">Namespace</span><span class="sxs-lookup"><span data-stu-id="43be8-206">Namespace</span></span><br/>                | <span data-ttu-id="43be8-207">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="43be8-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="43be8-208">MOF</span><span class="sxs-lookup"><span data-stu-id="43be8-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43be8-209"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="43be8-210">DLL</span><span class="sxs-lookup"><span data-stu-id="43be8-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43be8-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="43be8-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="43be8-212">Confira também</span><span class="sxs-lookup"><span data-stu-id="43be8-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43be8-213">**Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="43be8-213">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

